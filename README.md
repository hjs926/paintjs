# paintjs - Painting Board made with VanillaJS

## 1.1 Styles part One

![image](https://user-images.githubusercontent.com/48309309/160432775-e6343ece-0502-4fb9-a147-763af6cc67e9.png)

![image](https://user-images.githubusercontent.com/48309309/160432788-eaa20231-4db6-4dd0-9a64-709e183c9978.png)

![image](https://user-images.githubusercontent.com/48309309/160432869-c6c55d53-b07e-43bd-9835-1aecd55ebec6.png)

## 1.2 Styles part Two

- div.controls\_\_btns>button#jsMode+button#jsSave
- <button id="jsMode">Fill</button> <button id="jsSave">Save</button> (위와 동일)

- .controls**colors .controls**color 랑
- .controls**colors , .controls**color 중간에 , 붙인 거 차이점
- 띄어쓰기는 .controls\_\_colors 안에 있는 .controls_color란 뜻이고
- 콤마는 .controls**colors와 controls**color 두개를 의미한다.

![image](https://user-images.githubusercontent.com/48309309/160432957-5f10cba2-eeac-4f72-9500-975f10f89135.png)

![image](https://user-images.githubusercontent.com/48309309/160432968-aa09f463-8770-4857-a498-d25b48beb9b5.png)

![image](https://user-images.githubusercontent.com/48309309/160432979-a6ce0cad-59d9-4740-b7ab-f91a0e4057be.png)

## 2.0 Canvas Events

![image](https://user-images.githubusercontent.com/48309309/160433038-d4b7f054-6f18-4509-b7b1-37fe7290e7a4.png)

- EventTarget.addEventListener() : 지정한 유형의 이벤트를 대상이 수신할 때마다 호출할 함수를 설정한다.
- mousemove 로 canvas 위에 커서가 움직일 때마다 이벤트가 발생한다. 여기서 얻어야 할 것은 x, y가 어딨느냐인데 client 와 offset 중 canvas 내의 마우스 좌표가 필요하니 offset을 사용한다.

## 2.1 2D Context ~ 2.2 Recap

![image](https://user-images.githubusercontent.com/48309309/160433100-6a5770eb-ce98-4a57-baca-1cfb33973e75.png)

- canvas element는 css 사이즈랑 pixel manipulating 사이즈
- canvas.getContext는 픽셀들을 컨트롤 하는 것
- ctx.strokeStyle 은 그릴 선들이 모두 이 색을 갖는다고 말해준다
- ctx.lineWidth는 그 선의 너비가 2.5px 이라는 것

- 클릭하지 않고 마우스를 움직였을 때에는 path로 시작한다.
- path을 만들면 마우스의 x y 좌표로 path를 옮긴다.
- ctx.linTo(x,y)는 path의 이전 위치에서 지금 위치까지 선을 만든다.
- ctx.stroke는 현재의 sub-path를 현재의 stroke style로 획을 그은다.
- 마우스를 클릭하지 않고 움직일때는 painting = false; 이다

## 2.3 Changing Color

- document.getElementsByClassName("jsColor"); 는 모든 컬러 div를 선택하는 선택자
- querySelector는 수 많은 컬러 div중 오직 맨 처음 하나의 div만 선택한다.
- 결과 적으로 컬러는 변하지 않습니다.
- 이때 사용이 가능한건 querySelectorAll이다. All이 뒤로 붙으며 하나가 아닌 모든 div를
  선택할 수 있어 getElementsByClassName과 같은 효과를 볼 수 있다.

## 2.4 Brush Size ~ #2.5 Filling Mode ~ #2.6 Saving the Image

-- 버튼 클릭시 Reset --

- HTML
  < button id="jsReset" >Reset< /button >

- JS
  const reset = document.getElementById("jsReset");
  function resetBtn(event) {
  window.location.reload();
  }
  if (reset) {
  reset.addEventListener("click", resetBtn);
  }

## END

![1](https://user-images.githubusercontent.com/48309309/160433248-fb85bf1b-fbd6-4981-8e3e-a374a1a3c27c.PNG)
