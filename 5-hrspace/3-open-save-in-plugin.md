# 5.3 SafeSpace2 플러그인에서의 파일 열기와 저장하기


HRSpace의 플러그인으로 동작할 때는 별도로 지정하지 않아도, 디폴트로 아래의 파일을 불러오고, 저장합니다.

```
{HRSpace 프로젝트 폴더}/{로봇의 가상제어기 폴더}/project/safety/safety_parameter.json
```

예를 들어, spot_LH2/ 라는 폴더에 spot.LH2.hrsj 파일을 저장했고, 로봇 모델의 이름이 `robot_0` 인 경우라면, 파일 구조는 아래와 같습니다.

```
spot_LH2/
  robot_0/
    project/
      jobs/
      logs/
      safety/
        safety_parameter.json   <--- 이 파일을 자동으로 불러오고 저장함.
      vars/
      hi6_proj.json
  spot.LH2.hrsj
```

디폴트가 아닌 다른 파일을 불러오고 저장하고 싶다면, `파일(F) - 저장(S)` 혹은 `파일(F) - 다른 이름으로 저장(A)...` 메뉴를 사용해도 되며, 3D 뷰와의 연동은 동일하게 적용됩니다.
