# jQuery 사용법

### `$` 사용 이유
- jQuery로 변수를 만들어 사용할 때에는 앞에 $ 표시하는 경우 많음</br>
  
-> 뒤에 연결되는 메서드 체이닝이 jQuery로 가능하다는 것을 명시하기 위해</br>

`let $value = $('#one')`
---
### jQuery 적용하기
`body`태그 끝나기 전 `script`태그 사용해서 src코드에 `jQuery 링크 추가`

---

# Ajax
### jQuery에서 비동기 통신을 할 수 있는 메서드

- $.ajax() : 비동기 HTTP 요청</br>
- $.get() : GET 방식의 HTTP 요청</br>
- $.post() : POST 방식의 HTTP 요청</br>
- $.getScript(), $.getJSON() : GET 방식의 HTTP 요청 후 정해진 양식으로 소스코드 전달받음</br>
- .load() : HTML 코드를 읽어옴


- responseTxt : 요청 결과</br>
- statusTxt : 요청의 상태</br>
- xhr : 요청한 오브젝트</br>
- xhr.status : 파일의 응답상태