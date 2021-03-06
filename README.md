# ML_project
machine learning / CNN / openCV


>### 목표
기존 자신의 앨범에서의 그림과 작품(명화 혹은 자신이 원하는 이미지)을 합성해주는 것이
다. 단순히 사진끼리 합성하는 것이 아니라, 전체를 합성하거나 원하는 부분을 합성하거나를
선택할 수 있다. 또한, 사진을 편집할 수가 있어서 명도와 채도를 원하는 수치를 입력하여
변경할 수 있다.
따라서, 사진을 합성, 편집을 통해 사용자가 원하는 예술작품 형태의 기호를 맞추어 준다.

>### 제공
1. 명화와 이미지의 합성
2. 이미지의 객체를 추출해서 객체를 제외한 이미지 합성
3. 이미지의 RGB를 분석해서 가장 많이 사용되는 RGB제공(상위 5개/비율 포함)
4. 이미지의 명도 / 채도 변환(-100 ~ 100)

>###  CODE
1. index.html
- 사용자가 이미지 선택후 서버에 이미지 업로드 : upload_image.js , upload_image.php
- 사용자가 이미지의 RGB의 평균을 알고 싶을 때 : RGB.py
- 이미지 선택 후 합성(다음 단계) : process_create.py

2. process_create.py
- 사용자 이미지에서 객체 추출하기(create object 버튼 클릭)
- 객체 추출한 것 화면에 띄우기 : makeobject.js -> show_ob.py
- 객체 추출 안함 (건너뛰기) : enter_number2.py
- 추출하고 싶은 객체 입력 : enter_number.py

2-1. show_ob.py
- 객체 추출, 추출한 객체마다 이미지를 다르게 하고 배경을 검은색으로 한 후 ret0 ~ ret(객체수-1) 의 이름으로 jpg생성

3-1. enter_number.py
- 선택된 객체를 제외한 이미지와 명화 합성

3-2. enter_number2.py
- 객체 선택없이 이미지와 명화 합성


4. enter_number2.py / enter_number2.py 
- 명도와 채도 변경 : ChromaBrightTest.py
- 명도 채도 변경없이 건너뛰기 : ChromaBrightSkip.py


5. ChromaBrightTest.py / ChromaBrightSkip.py
- 명도 채도 작업 후 최종이미지, 저장




