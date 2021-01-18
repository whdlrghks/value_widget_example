# widget_value

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.


#### Image Widget

- 이미지를 꽉채워야한다 
    - 이미지를 자른다 : cover
    - 이미지를 늘린다 : fill
- 주위에 공백이 있어도 상관없다.
    - 너비를 살린다 : fitWidth
    - 높이를 살린다 : fitHeight
    - 먼저 맞는 쪽에 맞춘다 : contain

```dart
Image.asset('assets/images/woman.jpg', fit : BoxtFit.contain);
```

#### Input Widget

- __Text Field__
    - onChanged : 키 입력이 끝날떄마다 불리는 이벤트 헨들러 _ex) Textfield(onChanged : (String __val__) => _searchTerm = __val__,)_
    - TextEditingController : TextField에 초깃값을 제공하는 컨트롤러 _ex) TextEditingController _controller = TextEditingController(text: __"Initial Value here"__);_
    -{ decoration : InputDecoration} : TextField 꾸미기
        - labelText : Textinput 위에 나타나서 목적을 알리는 역할
        - hintText : TextField 안에 흐릿하게 나타나는 텍스트로 사용자가 입력하면 사라짐
        - errorText : 말그대로 에러 메시지
        - prefixText : 사용자가 입력하는 텍스트의 왼쪽에 붙는 텍스트
        - suffixText : prefixText와 같음. 오른쪽
        - icon : 전체 TextField 왼쪽에 그려지는 아이콘
        - prefixicon : TextField안에서 왼쪽에 그려지는 아이콘
        - suffixicon : prefixicon와같음
        - obscureText : decoration 밖에서 사용되어야함. __true__일시 점으로 바뀜.
    - KeyboardType : 사용자가 입력시 나타나는 키보드
        - TextInputType.number : 숫자 입력
        - TextInputType.datetime : 숫자판 + : / 
        - TextInputType.email : 기본 qwert 자판 + @
        - TextInputType.phone : 핸드폰 자판
    - inputFormatters : 입력할 수 있는 텍스트의 형식을 제한
        - BlacklistingTextInputFormatter : 특정 문자의 입력을 방지. 사용자가 화면에 입력해도 나타나지 않음.
        - WhitelistingTextInputFormatter : 지정한 문자만 입력 가능
        - LengthLimitingTextInputFormatter : 정해진 문자수 초과 입력 X

- __Check Box__
    - onChanged : 값이 변할때마다 불리는 이벤트 핸들러

- __Radio Button__
    - groupValue : groupValue에 묶인 버튼들은 하나로 묶임. _ex) SearchType _searchType / A와 B가 묶임. A를 선택 그렇다면 B는 자동으로 선택X_

- __Silder__
    - 사용자가 버튼을 움직여 정도 / value를 나타내는 방식
```dart
Silder(
    label : _value.toString(),  # -> 슬라이더에 표시되는 글씨
    min : 0 , max : 100 , # -> 최소, 최대값
    divisions: 100,
    value : _value , 
    onChanged : (double val) => _value = val, # -> 변할때마다의 val을 _value에 저장한다.
)
```

- __DropDown__




