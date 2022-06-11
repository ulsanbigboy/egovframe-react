# 전자정부 FrontEnd

※ 본 프로젝트는 기존 JSP 뷰 방식에서 벗어나 BackEnd와 FrontEnd를 분리하기 위한 예시 파일로 참고만 하시길 바랍니다.

## 환경 설정

프로젝트에서 사용된 환경 프로그램 정보는 다음과 같다.

| 프로그램 명 | 버전 명 |
| :------ | :------ |
| Node.js |  v14.16 |
| NPM     | v7.20.0 |



## BackEnd 구동

[심플 홈페이지 Backend](https://github.com/eGovFramework/egovframe-template-simple-backend.git) 소스를 받아 구동한다.



## FrontEnd 구동

아래 1 ~ 3의 과정을 따라서 진행한다.



### 1. 프로젝트의 생성

Git에서 복제하여 설치 시 1-1. 을 참고한다.

표준프레임워크 개발환경에서 설치 시 1-2. 를 참고한다. (2022년 2월 현재)


#### 1-1. Git에서 프로젝트 복제 및 모듈 설치

Git에서 clone 한다.

```bash
# 프로젝트 저장소를 로컬로 복제
git clone https://github.com/eGovFramework/egovframe-template-simple-react.git

# 복제된 프로젝트 디렉토리로 이동
cd egovframe-template-simple-react

# node modules를 설치해 준다.
npm install 
```

#### 1-2. 표준프레임워크 개발환경에서 설치

egovframe-template-simple-backend 설치 이후
egovframe-template-simple-react 디렉터리를 egovframe-template-simple-backend 디렉터리 밖으로 이동한다.

```bash
# 이동한 프로젝트 디렉토리로 이동
cd egovframe-template-simple-react

# node modules를 설치해 준다.
npm install 
```



### 2. 백엔드 프로젝트 설정

구동된 BackEnd 서버의 URL을 본 어플리케이션의 .env.development 파일의  REACT_APP_EGOV_CONTEXT_URL에 설정해 준다.
(단, 개발환경에서는 사용하는 환경변수 정보는 .env.development, build 시 사용하는 환경변수는 .env.production 에 기입해 준다.)

```bash
# .env.development 예시
REACT_APP_EGOV_CONTEXT_URL=localhost:8080
```



### 3. 프로젝트 실행 및 기타 명령어

```bash
# 테스트용 리액트 서버를 실행할 때 아래 명령어를 사용한다.
npm start
```

---



### 참조

보다 상세한 설명은 아래의 문서를 확인한다.

1. [Available scripts in CRA](./Docs/create-react-app-script.md)
2. [개발환경 초기 설정](./Docs/development-env-setting.md)


### 참조

1. cd D:\Front
2. git clone https://github.com/eGovFramework/egovframe-template-simple-react.git
3. cd D:\Front\egovframe-template-simple-react
4. npm install
5. npm start


## Quick start

- [깃허브 다운로드](https://github.com/ulsanbigboy/egovframe-react/archive/master.zip) or 레파지토리 클론 : `git clone https://github.com/ulsanbigboy/egovframe-react.git`
- Make sure your NodeJS and npm versions are up to date for `React 17`
- 초기설정: `npm install`
- 서버실행: `npm start`
- 배포실행: `npm run build`
- 사이트보기: `localhost:3000`

## File Structure

Within the download you'll find the following directories and files:

```
egovframe-react

┌── .env.development (개발환경)
├── .env.production (실행환경)
├── .gitignore
├── jsconfig.json
├── package.json
├── package-lock.json
├── README.md (개발문서)
├── build (디플로이 결과 디렉토리)
├── doc (참고문서)
├── public
│   ├── index.html
│   └── assets
└── src
    ├── App.js
    ├── index.js
    ├── reportWebVitals.js
    ├── context
    │   ├── code.js
    │   ├── config.js
    │   ├── egovFetch.js
    │   └── url.js
    ├── css
    │   ├── base.css
    │   ├── component.css
    │   ├── layout.css
    │   ├── page.css
    │   ├── response.css
    │   └── images
    │       └── bg_btn_calendar.png
    ├── egov
    │   ├── about (Home > 사이트 소개)
    │   │   ├── EgovAboutHistory.jsx (연혁)
    │   │   ├── EgovAboutLocation.jsx (찾아오시는길)
    │   │   ├── EgovAboutOrganization.jsx (조직소개)
    │   │   └── EgovAboutSite.jsx (소개)
    │   │
    │   ├── admin
    │   │   ├── board
    │   │   │   ├── EgovAdminBoardEdit.jsx
    │   │   │   └── EgovAdminBoardList.jsx
    │   │   ├── gallery
    │   │   │   ├── EgovAdminGalleryDetail.jsx
    │   │   │   ├── EgovAdminGalleryEdit.jsx
    │   │   │   └── EgovAdminGalleryList.jsx
    │   │   ├── notice
    │   │   │   ├── EgovAdminNoticeDetail.jsx
    │   │   │   ├── EgovAdminNoticeEdit.jsx
    │   │   │   └── EgovAdminNoticeList.jsx
    │   │   ├── schedule
    │   │   │   ├── EgovAdminScheduleDetail.jsx
    │   │   │   ├── EgovAdminScheduleEdit.jsx
    │   │   │   └── EgovAdminScheduleList.jsx
    │   │   ├── template
    │   │   │   ├── EgovAdminTemplateEdit.jsx
    │   │   │   └── EgovAdminTemplateList.jsx
    │   │   └── usage
    │   │       ├── EgovAdminUsageEdit.jsx
    │   │       └── EgovAdminUsageList.jsx
    │   ├── common
    │   │   ├── EgovAttachFile.jsx
    │   │   ├── EgovCondition.jsx
    │   │   ├── EgovContainer.jsx
    │   │   ├── EgovError.jsx
    │   │   ├── EgovFooter.jsx
    │   │   ├── EgovHeader.jsx
    │   │   ├── EgovImageGallery.jsx
    │   │   ├── EgovInfoPopup.jsx
    │   │   ├── EgovLeftNav.jsx
    │   │   ├── EgovPaging.jsx
    │   │   ├── EgovRadioButton.jsx
    │   │   ├── EgovRadioButtonGroup.jsx
    │   │   ├── EgovSelect.jsx
    │   │   ├── EgovViewTemplate.jsx
    │   │   └── leftmenu
    │   │       ├── EgovLeftNavAbout.jsx
    │   │       ├── EgovLeftNavAdmin.jsx
    │   │       ├── EgovLeftNavInform.jsx
    │   │       ├── EgovLeftNavIntro.jsx
    │   │       └── EgovLeftNavSupport.jsx
    │   ├── inform
    │   │   ├── daily
    │   │   │   ├── EgovDailyDetail.jsx
    │   │   │   └── EgovDailyList.jsx
    │   │   ├── gallery
    │   │   │   ├── EgovGalleryDetail.jsx
    │   │   │   ├── EgovGalleryEdit.jsx
    │   │   │   └── EgovGalleryList.jsx
    │   │   ├── notice
    │   │   │   ├── EgovNoticeDetail.jsx
    │   │   │   ├── EgovNoticeEdit.jsx
    │   │   │   └── EgovNoticeList.jsx
    │   │   └── weekly
    │   │       └── EgovWeeklyList.jsx
    │   ├── intro
    │   │   ├── EgovIntroService.jsx
    │   │   └── EgovIntroWork.jsx
    │   ├── login
    │   │   ├── EgovLogin.jsx
    │   │   └── EgovLoginContent.jsx
    │   ├── main
    │   │   └── EgovMain.jsx
    │   └── support
    │       ├── apply
    │       │   └── EgovSupportApply.jsx
    │       ├── download
    │       │   ├── EgovDownloadCreate.jsx
    │       │   ├── EgovDownloadDetail.jsx
    │       │   └── EgovDownloadList.jsx
    │       └── qna
    │           ├── EgovQnaDetail.jsx
    │           └── EgovQnaList.jsx
    └── js
        ├── jquery-1.11.2.min.js
        └── ui.js

```
