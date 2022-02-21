# Leaking Caffe2 thread-pool after fork. 안 뜨게 하기

github에서 clone 받은 모델을 내 환경에서 돌려보다보면, 이런 warning이 꽤!! 자주 뜬다.

### `[W pthreadpool-cpp.cc:88] Warning: Leaking Caffe2 thread-pool after fork. (function pthreadpool)`
[해결] Dataloader의 `pin_memory` 옵션을 `False`로 바꿔주기 (아마 `True`로 되어있을 것)

---

이 warning은 `warnings.filterwarnings('ignore')`가 통하는 애가 아니다.

자세히 어디서 왜 발생하는 건지는 모르겠지만, 유저 입장에서 크게 신경쓸 만한 warning은 아니라고 하는 것 같고, 일단 냅다 Dataloader 찾아가서 `pin_memory`를 `False`로 바꿔주면 대체로 해결됐음!

pin_memory도 정확히 뭘 위해 어떻게 작동되는 애인지는 모르지만,, 지금까진 저걸 `False`로 바꾼 이유로 문제가 된 경우는 없었다.

이 문제 관련해서 추가로 이해하는 내용이 있다면 업데이트 하겠음!

[참고링크 - pytorch issues](https://github.com/pytorch/pytorch/issues/57273)
