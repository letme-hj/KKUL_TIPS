# screen 간단 사용법
[방법]<br>
1. 터미널에 `screen` 입력
2. 원하는 거 실행
3. `ctrl+a, d` 로 detach (`d` 입력하는 순간 알아서 빠져나와져야 함)
4. 다시 세션에 진입하고 싶으면 `screen -r`

(screen 하나 돌리고 detach 해서 나왔을 때의 화면)<br>
<img width="395" alt="Screen Shot 2022-02-23 at 10 43 25 AM" src="https://user-images.githubusercontent.com/63252804/155248863-e05e8d27-f6a3-4fb8-b3f2-e7ba0a7b5be7.png">

---
### 2개 이상의 세션 돌리기
하나만 할 때는 그냥 편히 하면 되는데, 2개 이상을 하려면 screen 세션에 이름을 지정해주어야 한다.

이름을 지정한 screen session을 실행시키려면
1. `screen -S [이름]`
2. 원하는 세션으로 진입하고 싶으면 `screen -r [이름]`

(detach하는 방식은 똑같음)

### session 현황 확인하기
`screen -ls`로 확인하면 됨! 내가 지정한 session 이름 까먹었을 때 꿀팁 ㅎㅎ
<img width="743" alt="Screen Shot 2022-02-27 at 3 55 39 PM" src="https://user-images.githubusercontent.com/63252804/155871862-e9bed2c6-4781-47e2-95bd-dcb10af3be66.png">


[참고링크](http://www.incodom.kr/Linux/%EA%B8%B0%EB%B3%B8%EB%AA%85%EB%A0%B9%EC%96%B4/screen)
