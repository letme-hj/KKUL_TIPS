# gradient가 nan 나오는 경우 잡기

**[방법]**
gradient가 계산되는 부분 앞 쪽에 `torch.autograd.set_detect_anomaly(True)`를 붙이면 됨!

**[결과]**
<img width="705" alt="image" src="https://user-images.githubusercontent.com/63252804/172040909-dfd78c1b-b233-4b58-9351-9f00eb4adf86.png">

---
신기하게도 이거 붙이기 전에는 그냥 조용히 nan값 내뱉으며 엉망으로 돌아갔으면서,

요걸 붙였더니 에러를 내뱉어준다. ㅎㅎ

출력해보지 않고서는 몰랐을텐데 한 줄 붙여주면 nan 값 내뱉는 부분에서 바로 잡아낼 수 있으니 유용하게 쓸 수 있을 듯!!
