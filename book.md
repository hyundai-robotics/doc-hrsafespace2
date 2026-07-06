
[__SOURCE](README.md)
# Hi7 로봇제어기 기능설명서 - HRSafeSpace2


[__SOURCE](0-about-this-manual/README.md)
# 이 설명서에 대하여

[__SOURCE](0-about-this-manual/precautions.md)
# 사전 주의사항

{% include file="ko/precautions.md" %}

[__SOURCE](0-about-this-manual/safety-notice.md)
# 안전 주의 사항

{% include file="ko/safety-notice.md" %}

[__SOURCE](1-preface/README.md)
# 1. 개요

이 문서는 HD현대로보틱스 Hi7 제어기 SafeSpace2.0 기능의 PC용 설정 유틸리티인 HRSafeSpace2 애플리케이션의 사용법을 설명합니다.

[__SOURCE](1-preface/1-intro.md)
# 1.1 소개

HD현대로보틱스의 Hi7 제어기는 IEC 61508 Functional safety 표준을 준수하는 안전 기능 SafeSpace v2.0이 탑재되어 있습니다.
로봇 시스템의 오조작, 오동작, 고장 시, 사람의 신체를 보호하는 것이 이 기능의 목적입니다.

Hi7 제어기의 SafeSpace2.0 기능의 설정은 아래의 3가지 방법 중 하나로 수행할 수 있습니다.

  * TP630 티치펜던트 (산업용TP)
  * TP640 티치펜던트 (태블릿TP)
  * HRSafeSpace2 애플리케이션 (윈도우 데스크탑 PC용 애플리케이션)

SafeSpace v2.0의 각 설정화면은 위 3가지 디바이스에 동일하게 탑재되어 있습니다. 

본 설명서는 설명화면들에 대해서는 설명하지 않으며, 아래 내용들만을 설명합니다.

  * HRSafeSpace2 애플리케이션의 설치 방법
  * HRSafeSpace2의 화면 구성과 기본적인 조작 방법
  * HRSafeSpace2를 HRSpace4와 연동하여 3D 가상 워크스페이스에서 Safety 레이아웃을 비주얼하게 편집할 수 있는 기능

각각의 설정화면들에 대한 내용은 [SafeSpace2.0 안전 기능 설명서](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/korean/README)를 참고하십시오.

[__SOURCE](1-preface/2-prerequisite.md)
# 1.2 사전 지식 (prerequisite)


본 설명서는 아래 내용을 숙지하고 있는 사용자들을 위한 대상으로 합니다.

  * [Hi6/Hi7 제어기 조작 설명서](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/README)

  * [SafeSpace2.0 안전 기능 설명서](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/korean/README) ; 본 설명서를 먼저 학습해도 됩니다.

  * HRSpace4 기능 설명서 (HRSpace4 도움말) ; HRSpace4 연동 시에만 필요합니다.
  
[__SOURCE](2-install/README.md)
# 2. 설치

- 필수 실행 환경
  * 윈도우10 64bit 및 이후 버전
  * 유선 이더넷 장치

1. [HD현대로보틱스 다운로드 페이지](https://www.hd-hyundairobotics.com/download-center/list)에 접속하여 제품명에서 HRSafeSpace2를 검색하여 다운로드 받으십시오.
(다운로드를 위해서는 회원가입과 로그인이 필요합니다.)


2. 다운로드한 zip 파일을 임의의 폴더에 풀어놓고 setup.exe를 실행하십시오.


3. `Next >` 버튼을 클릭하면서 진행하십시오.
   
	![](../_assets/ch01_10_install.PNG)


4. Complete 화면이 나오면 `Close` 버튼으로 설치를 종료하십시오. 
   
	![](../_assets/ch01_14_install.PNG)

[__SOURCE](3-operation/README.md)
# 3. 조작 방법

HRSafeSpace2는 단독 (Stand-alone) 애플리케이션으로, 혹은 HRSpace에 내장된 플러그인 (Plug-in) 형태로 실행 가능합니다.

3장과 4장에서는 단독 애플리케이션의 실행 예로서 설명합니다. 이 내용은 플러그인 실행에서도 비슷하게 적용됩니다.

우선 3장에서는 HRSafeSpace2의 실행과 화면 구성, 설정 및 파일 저장과 불러오기에 대해 설명하겠습니다.

[__SOURCE](3-operation/1-start.md)
# 3.1 실행 방법

1. 윈도우 바탕화면, 혹은 시작버튼에서 HRSafeSpace2 아이콘을 클릭하십시오. _ko는 한글버전, _en은 영문버전입니다.

   ![](../_assets/ch03_10_start.PNG)

2. HRSafeSpace2가 실행됩니다.

   ![](../_assets/ch03_20_hrsafespace2.PNG)


{% hint style="info" %}

혹시 실행에 실패한다면, 아래 파일을 설치한 후 다시 시도해 보십시오.

```cmd
C:/Program Files/HHI Robotics/HRSafeSpace2/vc_redist.x64.exe
```

{% endhint %}
[__SOURCE](3-operation/2-screen-layout.md)
# 3.2 화면 구성

![](../_assets/ch03_20_hrsafespace2.PNG)

* 상단에는 제목막대와 풀다운 메뉴, 툴 바가 있습니다.

* 좌측에는 SafeSpace2의 각 설정 항목을 보여주는 트리창이 있습니다.

* 트리창에서 특정한 설정 항목을 선택하면, 해당하는 설정 화면에 우측에 나타납니다.

* 하단에는 각종 에러나 메시지가 기록되는 로그창이 있습니다. 로그창 우측의 `로그 클리어` 버튼을 클릭하면 로그창이 비워집니다.

[__SOURCE](3-operation/3-setting.md)
# 3.3 SafeSpace2 설정

- 트리창에서 설정할 항목을 선택한 후, 우측 화면에 값을 설정하십시오.

  ![](../_assets/ch03_30_setting.PNG)

- 트리창의 다른 항목을 선택하여 다른 화면으로 이동하더라도 입력한 값은 메모리에 보존됩니다. (즉, 다른 화면으로 이동하기 전에 저장할 필요 없습니다.)

- 허용한 범위 밖의 값을 입력한 경우, 다른 화면으로 이동을 시도할 경우 이동 실패하며, 하단의 로그 창에 잘못 입력한 값과 적법한 범위가 표시됩니다. 적법한 값으로 정정한 후, 이동하십시오.

  ![](../_assets/ch03_40_range.PNG)

[__SOURCE](3-operation/4-open-save.md)
# 3.4 저장과 불러오기

- 설정 내용을 저장하려면, `파일(F) - 저장(S)` 혹은 `파일(F) - 다른 이름으로 저장(A)...` 메뉴를 선택하십시오.

  ![](../_assets/ch03_60_open_save.PNG)
  
  혹은 툴 바에서 ![](../_assets/toolbar_save.PNG) 버튼을 클릭하십시오.  
  

- 저장 대화상자에서 원하는 폴더로 이동 후, 파일명을 입력하십시오. 설정 파일은 .json 포맷으로 저장됩니다.

  ![](../_assets/ch03_63_save.PNG)

- HRSafeSpace2를 다시 실행했을 때, 저장된 파일을 불러오기하려면, `파일(F) - 열기(O)`  메뉴를 선택하십시오. 혹은 툴 바에서 ![](../_assets/toolbar_open.PNG) 버튼을 클릭하십시오.

- 저장했던 파일을 선택하면, 설정 내용이 화면에 로드됩니다.

- SafeSpace2의 설정을 디폴트 값으로 다시 시작하려면, `파일(F) - 새 파일(N)` 메뉴를 선택하면 됩니다. 혹은 툴 바에서 ![](../_assets/toolbar_new.PNG) 버튼을 클릭하십시오.

  
[__SOURCE](4-comm/README.md)
# 4. 통신

이번 장에서는 HRSafeSpace2를 Hi7 제어기와 연결하고, 암호를 설정하고, 설정한 내용을 다운로드하거나 업로드하는 방법에 대해 설명하겠습니다.

[__SOURCE](4-comm/1-network-setting.md)
# 4.1 네트워크 설정

1. HRSafeSpace2를 실행한 PC와 Hi7 제어기의 범용 이더넷 포트를 이더넷 케이블로 연결하십시오.

2. PC측 네트워크 아답터의 IP주소는 Hi7 제어기와 같은 서브넷이어야 합니다.

   ![](../_assets/ch04_05_network_adapter.PNG)


3. `도구(T) - IP 주소 설정(A)` 메뉴를 선택하여, IP 주소 설정 대화상자를 여십시오.

   ![](../_assets/ch04_00_tool_menu.PNG)

   혹은 툴 바에서 ![](../_assets/toolbar_ipaddr.PNG) 버튼을 클릭하십시오. 


4. PC측과 로봇 제어기(Hi7) 측의 IP 주소를 각각 입력하고 `확인` 버튼을 클릭하십시오.

   ![](../_assets/ch04_10_ipaddr.PNG)

[__SOURCE](4-comm/2-password.md)
# 4.2 패스워드

SafeSpace2 설정을 권한이 없는 사람이 함부로 수정할 수 없도록, Hi7 제어기에 반드시 SafeSpace2 패스워드를 설정해야 합니다.

## 아직 설정하지 않은 경우, 패스워드 설정 방법

1. `도구(T) - 패스워드 변경(P)` 메뉴를 선택합니다.

   ![](../_assets/ch04_00_tool_menu.PNG)

   혹은 툴 바에서 ![](../_assets/toolbar-password.PNG) 버튼을 클릭하십시오.


2. 아래와 같은 대화상자가 나타나면, `새 패스워드`에 새로 설정할 암호를 입력하고 `패스워드 확인`에도 동일한 암호를 입력한 후, `변경(C)`을 클릭하십시오.

   ![](../_assets/ch04_20_ch_password.PNG)


3. `완료` 메시지박스가 표시되면 성공한 것입니다.

   ![](../_assets/msgbox_complete.PNG)


4. `타임아웃 에러` 메시지박스가 표시되면 IP주소 설정이나 이더넷 케이블 연결, 혹은 Hi7 제어기가 정상적인 상황인지 등을 확인하십시오.

   ![](../_assets/ch04_30_timeout.PNG)


## 설정되어 있는 상태에서, 패스워드 변경 방법

1. `도구(T) - 패스워드 변경(P)` 메뉴를 선택합니다.

   ![](../_assets/ch04_00_tool_menu.PNG)

   혹은 툴 바에서 ![](../_assets/toolbar-password.PNG) 버튼을 클릭하십시오.


2. 아래와 같은 대화상자가 나타나면, `이전 패스워드`에 이전의 패스워드, `새 패스워드`에 새로 설정할 암호를 입력하고, `패스워드 확인`에도 새 패스워드와 동일한 암호를 입력한 후, `변경(C)`을 클릭하십시오.

   ![](../_assets/ch04_40_ch_password2.PNG)


3. `완료` 메시지박스가 표시되면 성공한 것입니다.

   ![](../_assets/msgbox_complete.PNG)
   

[__SOURCE](4-comm/3-download.md)
# 4.3 다운로드

1. `도구(T) - 다운로드(D)` 메뉴를 선택합니다.

   ![](../_assets/ch04_00_tool_menu.PNG)

   혹은 툴 바에서 ![](../_assets/toolbar_download.PNG) 버튼을 클릭하십시오.


2. 아래와 같은 대화상자가 나타나면, `패스워드`에 암호를 입력하고, `다운로드`를 클릭하십시오.

   ![](../_assets/ch04_50_download.PNG)


3. `완료` 메시지박스가 표시되면 성공한 것입니다.

   ![](../_assets/ch04_60_download_ok.PNG)

[__SOURCE](4-comm/4-upload.md)
# 4.4 업로드

1. `도구(T) - 업로드(U)` 메뉴를 선택합니다.

   ![](../_assets/ch04_00_tool_menu.PNG)

   혹은 툴 바에서 ![](../_assets/toolbar_upload.PNG) 버튼을 클릭하십시오.


2. `완료` 메시지박스가 표시되면 성공한 것입니다.

   ![](../_assets/msgbox_complete.PNG)

[__SOURCE](5-hrspace/README.md)
# 5. HRSpace4 연동

이번 장에서는 HRSpace4 프로젝트에 HRSafeSpace2를 플러그인 (Plug-in) 형태로 로드하여, 3D 가상 워크스페이스에서 Safety 레이아웃을 비주얼하게 편집하는 방법을 설명합니다.

{% hint style="info" %}

HRSpace4가 설치되어 있지 않다면, [HD현대로보틱스 다운로드 페이지](https://www.hd-hyundairobotics.com/download-center/list)에 접속하여 제품명에서 HRSpace를 검색하여 최신 버전을 다운로드 받아 설치하십시오.

{% endhint %}

{% hint style="warning" %}
HRSpace v4.3.2.0 이상이 필요합니다.
{% endhint %}


HRSpace4에서 아래와 같은 로봇 스폿 용접 셀의 레이아웃을 설계했다고 가정합시다.

   ![](../_assets/ch05_00_hrspace4.PNG)

HDR220-26 매니퓰레이터 한 대가 셀 안에 설치되어 있습니다. 로봇 플랜지에는 C-타입 스폿 용접건(c_gun_m)이 장착되어 있으며, 로봇은 높이 800mm의 보고대(riser) 위에 설치되어 있습니다. 각 작업 사이클의 시작 시, 작업자가 로봇 전면의 포지셔너(positioner)에 용접 작업물을 장착합니다. 로봇은 작업물에 대해 스폿 용접을 수행하며, 간헐적으로 팁 드레서(tip_dresser)로 드레싱을 수행합니다.

전체 셀은 5면 펜스(fence)로 둘러싸여 있습니다. 또한, 천장 구조물과의 충돌을 막기 위해 로봇 툴의 Z축 범위는 셀 바닥을 기준으로 0~3400mm 영역으로 제한되며, 펜스 내부에는 기둥이 하나 존재한다고 가정합니다.

우리는 HRSpace4 비주얼 편집 연동 기능의 도움을 받아 SafeSpace2 설정 파라미터를 작성한 뒤, 생성된 safety_parameter.json 파일을 실제 Hi7 로봇 컨트롤러에 다운로드하게 될 것입니다.

[__SOURCE](5-hrspace/1-install-plugin.md)
# 5.1 SafeSpace2 플러그인의 설치


1. HRSafeSpace2가 설치된 폴더에서 아래 5개의 파일을 클립보드로 복사합니다.

   * favicon.ico
   * SafeSpace2.en.dll
   * SafeSpace2.ko.dll
   * SafeSpace2_en.hrsj
   * SafeSpace2_ko.hrsj

   ![](../_assets/ch05_10_plugin_install.PNG)


2. HRSpace4가 설치된 폴더에서 Library/Etc/에 SafeSpace2/ 폴더를 생성한 후, 그 안에 파일들을 붙여넣기 합니다.

   ![](../_assets/ch05_15_plugin_install2.PNG)


{% hint style="info" %}

플러그인 설치 후 HRSpace4를 처음 실행할 때, 혹시 아래와 같은 대화상자가 나타난다면 구성이 완료될 때까지 잠시 기다려 주십시오.

   ![](../_assets/ch05_18_plugin_install3.PNG)

{% endhint %}

[__SOURCE](5-hrspace/2-load-plugin.md)
# 5.2 SafeSpace2 플러그인의 로드


1. HRSpace4의 작업공간의 robot 모델에 대해, 팝업 메뉴를 열고 `모델 불러오기...` 를 선택합니다.

   ![](../_assets/ch05_20_plugin_load.PNG)

2. `범주 - 기타` 항목에 체크한 후, 목록에서 `SafeSpace2_ko`를 선택하고, `확인` 버튼을 클릭합니다.

   ![](../_assets/ch05_25_plugin_load2.PNG)

3. robot 모델의 서브 모델로 생성된 SafeSpace2 모델에 팝업 메뉴를 열고 `확장 속성...` 를 선택합니다.

   ![](../_assets/ch05_30_ex_prop.PNG)

4. SafeSpace2 모델의 확장 속성 대화상자로서, HRSafeSpace2 대화상자가 열렸습니다.

   ![](../_assets/ch05_35_ex_prop2.PNG)

[__SOURCE](5-hrspace/3-open-save-in-plugin.md)
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

[__SOURCE](5-hrspace/4-space-working.md)
# 5.4 작업 공간의 설정


로봇 툴의 동작 범위를 허용된 작업 공간 내로 제한하기 위해 space를 정의해 보겠습니다. XY 평면은 5각형의 펜스 안으로 제한하고, Z축 범위는 0~3400mm 로 제한합시다.

1. 작업 편의를 위해 뷰를 위에서 내려다보는 방향으로 바꿉니다. HRSpace4의 `보기(V)` 리본메뉴에서 `위에서 보기`를 선택합니다. (클릭할 때마다 90도씩 회전합니다.)

   ![](../_assets/ch05_40_view_up.PNG)


2. 영역 선택에 방해가 되는 기둥(pillar) 모델은 잠시 `스타일 - 보이기`의 체크를 꺼서 감춥니다.

   ![](../_assets/ch05_43_pillar.PNG)
   ![](../_assets/ch05_46_show.PNG)


3. 확장 속성에서 `layout/spaces/space 0`을 선택합니다. `일반` 탭에서 활성화 항목을 `항상 on`으로 설정합니다. 아래 그림과 같이 설정되어 있어야 합니다.

   ![](../_assets/ch05_50_space_gen.PNG)


4. `영역` 탭에서 우측의 `입력 시작` 버튼을 클릭합니다. (버튼은 `입력 완료`으로 바뀝니다.) 이제 마우스 좌버튼으로 3D 뷰에서 펜스 5개의 모서리의 약간 안쪽 바닥을 차례로 클릭합니다. 작업 공간을 의미하는 연두색 다각형 평면이 표시됩니다.
(Z max, Z min은 자동으로 20, -20으로 설정됩니다.)

   ![](../_assets/ch05_53_space_area.PNG)


5. 5개의 포인트를 모두 클릭했다면, `입력 완료` 버튼을 클릭합니다. (버튼은 다시 `입력 시작`으로 바뀝니다.) 만일 영역을 다시 선택하고 싶다면, `입력 시작` 버튼을 눌러 이전 정점들을 모두 클리어하고 다시 시작할 수 있습니다.

   ![](../_assets/ch05_54_space_area2.PNG)


6. 수치를 정밀하게 조정해야 한다면, 테이블 위젯에 직접 수치를 타이핑하면 됩니다. HRSafeSpace의 저장(![](../_assets/toolbar_save.PNG)) 버튼을 눌러야 3D 뷰에 반영됩니다.

   ![](../_assets/ch05_56_space_area_adjust.PNG)


7. 이제 뷰를 회전시켜서 옆에서 확인해 봅시다. 현재 Z 범위가 -20~20 mm이기 때문에, 옆에서 보면 작업 공간은 로봇 바닥 높이로 납작하게 형성되어 있습니다.

   ![](../_assets/ch05_58_z.PNG)


8. 로봇 좌표계의 높이가 800mm이고, Z축 범위는 월드 좌표계 기준 0~3400mm이어야 하므로, 로봇 좌표계 기준으로 Zmin~Zmax는 -800~2600mm 범위로 설정해야 합니다. 값 입력 후, HRSafeSpace의 저장(![](../_assets/toolbar_save.PNG)) 버튼을 클릭하면, 아래와 같이 설정이 완료됩니다.

   ![](../_assets/ch05_60_z2.PNG)


9. `홈(H) - 기즈모`를 열고, 위치 조정 혹은 크기 조정 모드로 Z축을 드래그하여, Zmax, Zmin을 조정할 수도 있습니다. (X축이나 Y축은 조정할 수 없습니다.)

   ![](../_assets/ch05_61_z3.PNG)


10. 설정된 작업 공간 형상이 셀을 채우고 있어서, 다른 설정에 방해가 됩니다. `일반` 탭에서 활성화 항목을 `항상 off`로 설정하면, 작업 공간 형상이 일단 감춰집니다. 다른 설정을 모두 완료한 후 다시 `항상 on`으로 바꾸도록 합시다.

[__SOURCE](5-hrspace/5-space-protective.md)
# 5.5 보호 공간의 설정


인간 작업자가 서 있을 수 있는 장소를 보호 공간으로 지정합시다.

1. 작업 편의를 위해 뷰를 위에서 내려다보는 방향으로 바꿉니다. HRSpace4의 `보기(V)` 리본메뉴에서 `위에서 보기`를 선택합니다.

   ![](../_assets/ch05_40_view_up.PNG)


2. 확장 속성에서 `layout/spaces/space 1`을 선택합니다. `일반` 탭에서 활성화 항목을 `항상 on`으로 설정하고, 타입은 `보호 공간`으로 설정합니다. 아래 그림과 같이 설정되어 있어야 합니다.

   ![](../_assets/ch05_62_ps01.PNG)


3. `영역` 탭에서 우측의 `입력 시작` 버튼을 클릭합니다. (버튼은 `입력 완료`로 바뀝니다.) 이제 마우스 좌버튼으로 3D 뷰에서 인간 작업자 주변의 바닥 4개의 지점을 차례로 클릭합니다. 보호 공간을 의미하는 빨간색 다각형 평면이 표시됩니다. (Z max, Z min은 자동으로 20, -20으로 설정됩니다.)

   ![](../_assets/ch05_62_ps05.PNG)


4. 4개의 포인트를 모두 클릭했다면, `입력 완료` 버튼을 클릭합니다. (버튼은 다시 `입력 시작`으로 바뀝니다.) 만일 영역을 다시 선택하고 싶다면, `입력 시작` 버튼을 눌러 이전 정점들을 모두 클리어하고 다시 시작할 수 있습니다.


5. 수치를 정밀하게 조정해야 한다면, 테이블 위젯에 직접 수치를 타이핑하면 됩니다. 저장 버튼을 눌러야 3D 뷰에 반영됩니다.

   ![](../_assets/ch05_62_ps10.PNG)


7. 이제 뷰를 회전시켜서 옆에서 확인해 봅시다. 현재 Z 범위가 -20~20 mm이기 때문에, 옆에서 보면 보호 공간은 로봇 바닥 높이로 납작하게 형성되어 있습니다.

   ![](../_assets/ch05_62_ps15.PNG)


8. 로봇 바닥 높이가 800mm 이므로, 보호 공간의 높이를 3000mm로 한다면 Zmin~Zmax를 -800~2200mm 범위로 설정하면 됩니다. 값 입력 후, 확장 속성(HRSafeSpace)의 ![](../_assets/toolbar_save.PNG) 버튼을 클릭하면, 아래와 같이 설정이 완료됩니다.

   ![](../_assets/ch05_62_ps20.PNG)

[__SOURCE](5-hrspace/6-robot-link.md)
# 5.6 로봇 링크의 설정

로봇의 upper_frame과 arm_frame에 캡슐 영역을 씌워서, 충돌을 예방할 수 있습니다. 

1. 확장 속성에서 `layout/robot`을 선택합니다. 링크 3, 링크 2에 대해 각기 아래와 같이 변경하고 ![](../_assets/toolbar_save.PNG) 버튼을 클릭하면, 두 링크의 위치에 각기 캡슐 영역이 나타납니다.

   - 링크 3 (V)
     * 반지름: 300mm 
     * 실린더 높이: 600mm
     * RY : 90 deg

   - 링크 2 (H)
     * 반지름: 300mm 
     * 실린더 높이: 600mm     

   ![](../_assets/ch05_64_link.PNG)


2. `홈(H) - 기즈모`를 열고, 링크 3의 캡슐을 선택합니다. 기즈모를 크기 모드와 위치 모드로 전환해 가면서 캡슐의 크기와 위치를 링크 3를 포함하도록 적당히 조정합니다.

   ![](../_assets/ch05_64_link_gizmo.PNG)

   ![](../_assets/ch05_66_link_gizmo2.PNG)

3. 링크 2의 캡슐을 선택하여, 같은 방법으로 캡슐의 크기와 위치를 링크 2를 포함하도록 적당히 조정합니다. 기즈모로 조작한 결과는 확장 속성 대화상자에 즉각적으로 반영됩니다.

   ![](../_assets/ch05_68_link_gizmo3.PNG)


[__SOURCE](5-hrspace/7-tool.md)
# 5.7 툴의 설정

로봇의 툴에 다양한 형상의 영역을 씌워서, 충돌을 예방할 수 있습니다. 

1. 확장 속성에서 `layout/tools/tool0`을 선택합니다. 각 툴 번호의 형상은 최대 10개의 모델을 조합하여 구성할 수 있습니다. 우선 Model 0의 형상을 아래와 같이 설정하고 ![](../_assets/toolbar_save.PNG) 버튼을 클릭하면 로봇 프렌지 좌표계에 형상이 나타납니다.

   * 형상: `둥근판`
   * 반지름: 200mm
   * 높이: 500mm
   * 너비: 300mm
   * 나머지 항목은 0

   ![](../_assets/ch05_70_tool_tool.PNG)


2. 형상이 툴 전체를 포함하도록, 기즈모를 사용하여 Model 0을 이동, 회전, 크기 조정하십시오. 기즈모로 조작한 결과는 확장 속성 대화상자에 즉각적으로 반영됩니다.

   ![](../_assets/ch05_72_tool_tool2.PNG)


3. 크기나 위치의 정밀하게 조정해야 한다면, Model 0의 모델 속성을 열여 직접 수치를 타이핑해 수정해도 됩니다.

   ![](../_assets/ch05_73_tool_tool_model_prop.PNG)


4. Model 0 형상 바깥으로 튀어나온 부분이 있으므로, Model을 하나 더 추가하겠습니다. Model 1에 아래와 같이 캡슐을 생성한 후, 마찬가지로 기즈모를 사용하여 튀어나온 부분을 덮어주십시오.

   * 형상: `캡슐`
   * 반지름: 200mm
   * 높이: 500mm
   * 나머지 항목은 0

   ![](../_assets/ch05_74_tool_tool3.PNG)

[__SOURCE](5-hrspace/8-tool-orient.md)
# 5.8 툴 방향의 설정

로봇의 툴이 가리키는 방향을 특정한 각도 범위로 제한하고 싶다면, 툴 방향 (tool_orients) 설정 항목을 사용할 수 있습니다.

(시험 및 설명의 편의를 위해, 이전 절에 실습한 tool 형상은 삭제했으며, 스폿 용접 건 툴은 스타일 - 투명도를 60%로 조정했습니다.)


1. 확장 속성에서 `layout/tool_orients`를 선택합니다. 각도 편차를 60 deg로 입력한 후 ![](../_assets/toolbar_save.PNG) 버튼을 클릭하면 로봇 프렌지 좌표계에 원뿔 모양의 툴 방향 범위가 표시됩니다.

   ![](../_assets/ch05_76_tool_orient.PNG)


2. Org.Rx, Ry, Rz가 (0, 0, 0)deg 일 때, 원뿔은 로봇좌표계 기준으로 하늘로 향하는 +Z방향으로 퍼져 나가는 형상이 됩니다. 이 원뿔 범위 60 deg는 TCP의 +Z축을 제한합니다.
   아래 그림은 TCP의 Z축이 허용 범위 내에 있는 상황과, 범위를 벗어난 상황의 예를 보여주고 있습니다.

<table>
   <tr>
      <td>
         <img src="../_assets/ch05_78_tool_orient2.PNG"/>
      </td>
      <td>
         <img src="../_assets/ch05_79_tool_orient3.PNG"/>
      </td>
   </tr>
   <tr>
      <td align='center'>
         범위 내에 있음.
      </td>
      <td align='center'>
         범위를 벗어남.
      </td>
   </tr>
</table>   


3. 툴 방향의 범위 크기나 방향의 수치를 수정한 후 다시 ![](../_assets/toolbar_save.PNG) 버튼을 클릭하면, 3D 뷰에도 반영됩니다.

[__SOURCE](appendices/README.md)
# 별첨

  



[__SOURCE](appendices/rules-occupational-safety.md)
# 산업안전보건기준에 관한 규칙 및 안전검사 고시

당해 산업용 로봇은 산업안전보건기준에 관한 규칙 및 안전검사 고시(검사 대상일 경우)의 검사 기준을 고려하여 설치하여야 한다.

"[산업안전보건기준에 관한 규칙](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/korean/README)"

[__SOURCE](quality-assurance.md)
# 품질보증

"[품질보증](https://hrbook-hrc.web.app/#/view/quality-assurance/ko/README)"
