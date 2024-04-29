## HTML
HTML 공부

- 기본적인 틀
```html
<html>
    <head>
        <title></title>
    </head>
    <body>
    </body>
</html>
```

### 타입 종류
- type 속성은 입력양식의 종류를 지정한다.
- type="text" : 텍스트 입력
- type="password" : 비밀번호 입력
- type="radio" : 라디오 버튼
- type="checkbox" : 체크박스
- type="submit" : 전송 버튼
- type="reset" : 초기화 버튼
- type="button" : 버튼
- type="file" : 파일 업로드
- type="hidden" : 숨겨진 입력
- type="image" : 이미지 버튼
- type="color" : 색상 선택
- type="date" : 날짜 선택
- type="email" : 이메일 입력
- type="number" : 숫자 입력
- type="range" : 범위 선택
- type="search" : 검색어 입력

### 시맨틱
![시맨틱](https://github.com/GangGnagGnag/HTML/blob/main/image/시맨틱.jpg)

#### 태그 성질에 따른분류
1. 블록요소 태그
    - html, body, div, p, ul, ol, li, dl, dt, dd...
    - 기본 가로 공간의 크기가 부모태그와 동일하게 인식
    - 공간값이 적용(w,h)
2. 인라인 요소 태그
    - a, span, strong, i, em ...
    - 기본 가로 공간의 크기가 안쪽에 포함된 내용만큼 인식(컨텐츠)
    - 연속해서 작성하면 가로 배열
    - 공간값이 적용 안됨
3. 인라인 블록요소 태그
    - img, input, button
    - 기본 가로 공간의 크기가 안쪽에 포함된 내용만큼 인식
    - 연속해서 작성하면 가로배열
    - 공간값이 적용된다.

## css선택자
- 전체 선택자: *
- 태그 선택자: 태그
- ID 선택자: #id
- 클래스 선택자: . 클래스이름
- 속성 선택지: 선택자[속성 = 값]
- 자식선택자: > 표시로 자식관계를 나타낸다
- 반응 선택자: 사용자의 반응으로 hove와 active 상태가 만들어진다
- 상태 선택자: 입력 양식의 상태를 선택할 때
    :checked - 체크 상태인 input 태그 선택
    :focus - 포커스를 맞춘 input 태그 선택
    :enabled - 사용 가능한 input 태그 선택
    :disabled - 사용 불가능한 input 태그 선택
- 구조선택자: 특정 위치에 있는 태그를 선택할 때 사용
    :nth-child(수열) 형제관계에서 앞에서 수열번째 해당하는 태그선택
    :first-child - 형제관계에서 첫번째로 등장하는 태그 선택
    :last-child - 형제관계에서 마지막으로 등장하는 태그 선택

    list-style은 블릿마커를 제어한다.
    - 원형블릿마커(disc), 숫자순서(decimal), 비어있는 원형블릿마커(circle)
    사각 블릿마커(square)
    border-radius 요소의 테두리를 만든다.
    (좌상, 우상, 우하, 좌하), (좌상우하, 우상좌하), (좌상, 후상좌하,우하)

## CSS 적용 우선 순위
1. 속성값 뒤에 !important
2. style 을 직접 지정한 속성(인라인 속성)
3. #id 로 지정한 속성
4. 태그로 지정한 속성
5. 상위 객체에 의해 상속된 속성