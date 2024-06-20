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

## position
- 절대좌표: absolute, fixed
- 상대좌표: static, relative
- top-bottom-left-right

## %, em, rem
[CSS 단위 적용 기준]
1. 부모요소에 따라서 사이즈가 변경되어야 하는경우: %,em
    그렇지 않을 경우: 부포트, rem
2. 요소의 너비 또는 높이에 따라서 사이즈가 변경되어야 하는 경우: %, 뷰포트
    폰트에 따라서 크기가 변경될 경우에는 em,rem

### em VS rem
- rem은 루트 요소에 있는 폰트 사이즈에 따라서 크기가 결정된다.
- em은 부모 요소의 폰트 사이즈에 따라서 크기가 결정된다.

- 고전적인 방법의 layout은 Position, float, table
- flex, grid
## Animation

```css
animation-name: move;
```

- 애니메이션 이름(키프레임명)
- 시간값, 회수값, 방향값, 정지값을 적용하는 객체에 넣어야 함
```css
animation-duration: 1s;
```

- 애니매이션 시간값
```css
animation-iteration-count: 4;
animation-iteration-count: 반복횟수;
```

- 애니메이션 반복횟수 값
- infinite계속반복
```css
animation-direction: alternate;
normal:form~to
alternate:form~to~form
```

- reversnormal:normal과 반대,거꾸로to~form
- alternate-reverse:alternate와 반대 to~from~to 주로 alternate로 작업
```css
animation-delay: 1s;
```

- 애니매이션 지연시간
```css
animation-timing-function: ease-in;
```

- 애니메이션 가속도 형태
```css
animation-fill-mode: forwards;
```

- 마지막 애니메이션에서 정지

키프레임 기본틀

```css
@keyframes 애니매이션 이름{
				
				form{
					시작위치
				}
				50%{
					중간 위치
				}
				to{
					도착 위치
				}
			}
```
> animation : 실행하는 애니메이션 속성을 지정하는 단계 @keyframes 애니메이션의 스타일을 구체적으로 제어

    ```html
    <!doctype html>
    
    <html>
    	<head>
    		<title>Page Title</title>
    		<meta charset="UTF-8">
    		<meta name="viewport" content="initial-scale=1.0">
    		
    		<style>
    			*{padding: 0; margin: 0;}
    			#box{
    				width: 300px;
    				height: 300px;
    				background-color: cornflowerblue;
    				animation-name: move;
    				animation-duration: 1s;
    				animation-iteration-count: 4;
    				animation-direction: alternate;
    				animation-timing-function: ease-in;
    				animation-fill-mode: forwards;
    			}
    			@keyframes move{
    				from{
    					transform: translate(0,0);
    				}
    				to{
    					transform: translate(500px,0);
    				}
    			}
    		</style>
    	</head>
    	<body>
    		<div id="box"></div>
    	</body>
    </html>
    ```

## 3D

transform의 3d와 관련한 스타일
3d가 적용되는 객체의 "부모"에게 지정함

```css
transform-style: preserve-3d;
```

- 3D 형태로 변형

```css
perspective: 1000px;
```

- 원근감 적용
    - 단위가 높을수록 멀리, 작게 보임
    - 단위가 클수록 가까이, 크게 보임

# 만들어본 HTML 활용 

![상단바](https://github.com/GangGnagGnag/basic-HTML/assets/159672857/bb130541-5da6-4fcf-b246-27fbe4a9dac9)

![테두리라인](https://github.com/GangGnagGnag/basic-HTML/assets/159672857/24fc4c26-76f5-4b7e-bfb3-8a27b622b6d6)

![지그제그](https://github.com/GangGnagGnag/basic-HTML/assets/159672857/da0e6e98-d7ab-4bcb-90c2-b84283a03a0b)

![주사위](https://github.com/GangGnagGnag/basic-HTML/assets/159672857/68adabbb-ba3e-43c2-baf8-6ab1e789dceb)

![사진안박스](https://github.com/GangGnagGnag/basic-HTML/assets/159672857/fbf4d920-c498-4f6f-99b0-97111c276208)

![아더에러사이트](https://github.com/GangGnagGnag/basic-HTML/assets/159672857/286a1d74-f9b8-407a-8d7a-105105b1ffcc)
