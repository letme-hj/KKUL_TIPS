# 구글 드라이브 파일 wget 다운로드

리눅스 터미널에서 `wget {다운로드 링크}`를 통해 휘리릭 서버로 해당 파일을 다운받을 수 있는데,<br>
종종 구글 드라이브에 공유되어있는 파일을 다운 받고 싶을 때는 어찌해야할지 고민됨.

특히 사이즈가 꽤 큰 경우, 개인 로컬로 다운 받았다가 서버에 업로드하긴 너무 부담스럽고 시간이 오래 걸리기 때문에 직접 서버로 다운받고 싶기 마련이다!

**이 때 구글 드라이브 파일을 리눅스 터미널에서 wget으로 바로 다운**받을 수 있는 방법은?!

`wget --load-cookies ~/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies ~/cookies.txt \
--keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id={FILEID}' -O- | sed -rn 's/.confirm=([0-9A-Za-z_]+)./\1\n/p')&id={FILEID}" \
-O {FILENAME} && rm -rf ~/cookies.txt` <br>
(이걸 복붙하고, {} 안의 값들만 생각해서 넣어주면 완료)

- `{FILEID}` : **file id**는 어디서 구하냐,
              **구글 드라이브에서 해당 파일 우클릭 > 공유 (share) > 링크 복사** 하면 요상하고 기다란 링크가 복사되는데,
               그걸 어딘가(메모장 등)에 기록해뒀다가 **`d`와 `view` 사이의 파일 id**를 사용하면 됨
- `{FILE_NAME}` : 파일 저장은 당사자가 원하는 이름으로 설정하면 되는 듯
