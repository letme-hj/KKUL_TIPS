# `argparse` 리스트로 받기
**[방법(예시)]**
```
parser = argparse.ArgumentParser()
parser.add_argument("--target-domain", default=None, nargs='+', type=str)
```
`.add_argument`의 인자로 **`nargs='+', type=원하는타입(dtype)`** 를 추가. <br>
n개의 argument를 받겠다는 의미로 직관적으로 받아들이면 될 듯.

---
`nargs`로 들어갈 수 있는 게 `'*', '?'` 도 있는 것 같았다. 아마 정규표현식의 느낌으로 쓰이는 듯!

