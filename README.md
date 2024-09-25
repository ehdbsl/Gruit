# Gruit
### AI로 보는 식자재

## Intro
일반 소비자의 경우 좋은 품질의 식자재를 판별하기에 어려움이 있다. 
이 서비스는 일반 소비자들도 손쉽게 더 맛있고 품질 좋은 식자재를 찾을 수 있는 앱을 만들고자 기획하게 되었다.

## Sample

1. 식자재 분류 선택
<table>
  <tr>
    <td><img src='./images/1.Category.png' width="300"></td>
    <td><img src='./images/2.SubCategory.png' width="300"></td>
  </tr>
</table>

2. 이미지 업로드
<table>
  <tr>
    <td><img src='./images/3.ImageUploader.png' width="300"></td>
    <td><img src='./images/4.ImageUploder2.png' width="300"></td>
  </tr>
</table>

3. 결과화면
<table>
  <tr>
    <td><img src='./images/5.Result.png' width="300"></td>
    <td><img src='./images/6.DetailResult.png' width="300"></td>
  </tr>
</table>

## train DataSet
* [Kaggle: apple-single-object-detection](https://www.kaggle.com/datasets/aeeeeeep/apple-single-object-detection)

* [roboflow: fruit-classification-vgg Computer Vision Project](https://universe.roboflow.com/brac-university-v9w2y/fruit-classification-vgg) 

* [AiHub: 농산물 품질(QC) 이미지](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=&topMenu=&aihubDataSe=data&dataSetSn=149)  

더 자세한 정보는 ai 디렉토리별 각 README 참조

## Model
Yolov8n, Yolov8m-cls

## Run
해당 Repository를 clone 하여 다운로드
  ```cli
  git clone https://github.com/DEVholder/Gruit.git
  ```
  ```cli
  cd Grult
  ```  

#### FrontEnd App의 경우
* NodeJS, 안드로이드 스튜디오 SDK 필요
  ```cli
  cd ./app/react_native_app
  ```
* nodeJS 패키지 설치
  ```cli
  npm install
  ```
  혹은
  ```
  yarn install
  ```
* .env 파일 생성  
  Server 주소, Fatsecret 유저 키 & 시크릿 키  
  ```.env
  REACT_APP_SERVER_API=http://10.0.2.2:8000
  REACT_APP_FATSECRET_OAUTH_KEY='유저키'
  REACT_APP_FATSECRET_SECRET_KEY='시크릿 키'
  ```
* expo 애뮬레이터 실행
  ```cli
  npx expo start
  ```

#### BackEnd Server의 경우
* Python 필요
  ```cli
  cd ./app/backend
  ```
* Python 가상환경 설치 및 활성화
  ```cli
  python -m venv .venv
  ```
  윈도우의 경우
  ```cli
  .\.venv\Scripts\activate
  ```
  리눅스/맥의 경우
  ```cli
  source ./.venv/bin/activate
  ```

* Python 패키지 설치
  ```cli
  pip install -r requirements.txt
  ```
* FastAPI 서버 실행
  ```cli
  python main.py
  ```