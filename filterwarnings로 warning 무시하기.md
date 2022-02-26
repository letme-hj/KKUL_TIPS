# filterwarnings로 warning 무시하기
**[방법]**<br>
1. import : `import warnings`
2. 코드 추가 : `warnings.filterwarnings('ignore')` (혹은 `(action='ignore')`)

---

버전에 관해서나 어떤 여러가지 이유에서 파이썬 코드를 돌리다보면 Warning: 어쩌구저쩌구~~ 가 자주 뜬다.

이렇게 코드를 돌리면서 진행상황에 대한 로그만 확인하고 싶은데 수많은 warning으로 고통받는 경우가 있는데, warning 무시하는 코드 한 줄로 고통에서 벗어날 수 있음!

매번 필요한데도 또 오랜만에 코드 돌리다보면 까먹음,,
