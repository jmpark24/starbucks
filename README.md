# Starbucks

# 스타벅스 커피 코리아의 메인페이지 및 로그인 페이지

이 프로젝트는 스타벅스 커피 코리아의 메인페이지 및 로그인 페이지를 클론 코딩하였습니다.

배포 된 사이트로 이동하기 : https://radiant-dragon-3e6221.netlify.app

### 프론트엔드 기술

- **HTML5**: 웹 페이지의 구조를 정의합니다.
- **CSS3**: 페이지의 스타일을 지정합니다. (사용된 CSS 파일: `common.css`, `signin.css`)
- **JavaScript**: 페이지의 동작과 상호작용을 구현합니다.

### 사용된 라이브러리

- **GSAP (GreenSock Animation Platform)**: 강력한 애니메이션 라이브러리로, 페이지 요소의 애니메이션을 구현합니다.

  - **기능**: 배지와 상단 이동 버튼의 애니메이션, 페이드 인 효과 등.
  - **예제**:
    ```javascript
    gsap.to(badgeEl, 0.6, { opacity: 0, display: 'none' });
    gsap.to(window, 0.7, { scrollTo: 0 });
    ```

- **Lodash**: 유틸리티 함수 라이브러리로, 이벤트 스로틀링에 사용됩니다.

  - **기능**: 스크롤 이벤트의 호출 빈도를 조절합니다.
  - **예제**:
    ```javascript
    window.addEventListener(
      'scroll',
      _.throttle(function () {
        /*...*/
      }, 300)
    );
    ```

- **Swiper**: 슬라이더 라이브러리로, 다양한 슬라이드 기능을 제공합니다.

  - **기능**: 공지사항, 프로모션, 어워드 섹션의 슬라이더를 설정합니다.
  - **예제**:
    ```javascript
    new Swiper('.promotion .swiper', {
      slidesPerView: 3,
      spaceBetween: 10,
      centeredSlides: true,
      loop: true,
      autoplay: { delay: 5000 },
      pagination: { el: '.promotion .swiper-pagination', clickable: true },
      navigation: { prevEl: '.promotion .swiper-prev', nextEl: '.promotion .swiper-next' },
    });
    ```

- **ScrollMagic**: 스크롤 기반 애니메이션을 제어하는 라이브러리입니다.

  - **기능**: 스크롤 위치에 따라 특정 요소에 클래스를 토글하여 애니메이션을 적용합니다.
  - **예제**:
    ```javascript
    new ScrollMagic.Scene({ triggerElement: spyEl, triggerHook: 0.8 })
      .setClassToggle(spyEl, 'show')
      .addTo(new ScrollMagic.Controller());
    ```

- **YouTube IFrame Player API**: YouTube 비디오를 웹 페이지에 통합하고 제어할 수 있는 API입니다.
  - **기능**: 웹 페이지에 YouTube 비디오를 삽입하고 자동 재생 및 음소거 설정을 합니다.
  - **예제**:
    ```javascript
    var tag = document.createElement('script');
    tag.src = 'https://www.youtube.com/iframe_api';
    var firstScriptTag = document.getElementsByTagName('script')[0];
    firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);
    ```

## 구현된 기능

- **로그인 페이지**: 사용자 로그인 및 인증을 위한 페이지입니다.
- **애니메이션 효과**: 배지, 스크롤 위치, 슬라이더 및 기타 요소에 애니메이션 적용.
- **슬라이더**: 공지사항, 프로모션, 어워드 등의 슬라이드 쇼 구현.
- **YouTube 비디오 플레이어**: 페이지에 삽입된 YouTube 비디오 자동 재생 및 음소거.
- **검색 기능**: 검색창 클릭 시 포커스 및 검색어 입력 시 힌트 표시.

## 설치 방법

1. **프로젝트 클론하기**

   ```bash
   git clone https://github.com/jmpark24/starbucks.git starbucks-signin-page
   ```

2. **디렉토리로 이동**

   ```bash
   cd starbucks-signin-page
   ```

3. **파일 열기**

   - index.html 파일을 웹 브라우저에서 열어 페이지를 확인할 수 있습니다.

## 사용 방법

1. 웹 브라우저에서 signin.html 파일을 열어 로그인 페이지를 확인합니다.
2. 페이지 상단의 메뉴를 통해 다양한 스타벅스 관련 정보를 탐색할 수 있습니다.
3. 로그인 폼을 사용하여 로그인 정보를 입력하고 로그인 버튼을 클릭하여 인증을 시도할 수 있습니다.
4. 로그인 폼 아래의 링크를 사용하여 회원 가입, 아이디 찾기, 비밀번호 찾기 등의 기능을 이용할 수 있습니다.

## 파일 구조

- index.html - 메인 페이지 HTML 파일
- signin/ - 로그인 페이지 디렉토리
  - index.html - 로그인 페이지 HTML 파일
- css/ - CSS 스타일 시트 디렉토리
  - common.css - 공통 스타일
  - main.css - 메일 페이지 전용 스타일
  - signin.css - 로그인 페이지 전용 스타일
- images/ - 이미지 파일 디렉토리
- js/ - JavaScript 파일 디렉토리
  - common.js - 공통 JavaScript 코드
  - main.js - 메인 페이지 JavaScript 코드
  - youtube.js - youtube 라이브러리 JavaScript 코드

## 연락처

프로젝트에 대한 문의 사항이 있으시면 다음 연락처로 문의해 주세요:

이메일: stylack@gmail.com
Blog: https://dry-curry.tistory.com/

```
이 Markdown 문서는 명확하게 각 섹션을 나누어 작성하였으며, 코드 블록과 링크를 포함하고 있습니다. 이를 통해 GitHub 리포지토리의 `README.md` 파일에 쉽게 사용할 수 있습니다.
```
