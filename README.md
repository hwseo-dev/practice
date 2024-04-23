# Git Convention

## 1. Branch

종류

 - main: 제품 출시 브랜치
   - develop: 출시를 위해 개발하는 브랜치
   - feat/{기능명}: 새로운 기능 개발하는 브랜치
 - refactor/{기능명}: 개발된 기능을 리팩터링하는 브랜치
 - hotfix: 출시 버전에서 발생한 버그를 수정하는 브랜치

예시
 - devevlop/feat/login
 - develop/feat/register


## 2. 커밋 메시지 구조
```
type(issue #no) : subject

body

footer
```

<table style="border: 2px;">
  <tr>
    <td> type </td>
    <td> subject </td>
    <td> body(선택 사항) </td>
    <td> footer(선택 사항) </td>
  </tr>
  <tr>
    <td> feat: 새로운 기능 추가 </td>
    <td rowspan="2"> 제목은 최대 50글자를 넘기지 않는다. </td>
    <td> 본문은 한 줄당 72자 내로 작성한다. </td>
    <td> 이슈 트래커 ID를 작성한다. </td>
  </tr>
  <tr>
    <td> fix: 버그 수정 </td>
    <td> 양에 구애받지 않고 최대한 상세히 작성한다. </td>
    <td> "유형: #이슈 번호" 형식으로 작성한다. </td>
  </tr>
  <tr>
    <td> docs: 문서 수정 </td>
    <td rowspan="3"> 마침표 및 특수기호는 사용하지 않는다. </td>
    <td rowspan="8"> 어떻게 변경했는지 보다 무엇을 변경했는지 또는 왜 변경했는지를 설명한다. </td>
    <td> 여러 개의 이슈 번호를 적을 때는 쉼표(,)로 구분한다. </td>
  </tr>
  <tr>
    <td> style: 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우 </td>
    <td> Fixes: 이슈 수정 중 (아직 해결되지 않은 경우) </td>
  </tr>
  <tr>
    <td> refactor: 코드 리팩토링 </td>
    <td> Resolves: 이슈를 해결한 경우 </td>
  </tr>
  <tr>
    <td> test: 테스트 코드, 리팩토링 테스트 코드 추가 </td>
    <td rowspan="5"> 영문으로 표기하는 경우 동사 원형을 가장 앞에 두고 첫 글자는 대문자로 표기한다.(과거 시제 사용 금지) </td>
    <td> Ref: 참고할 이슈가 있을 경우 </td>
  </tr>
  <tr>
    <td> chore: 빌드 업무 수정, 패키지 매니저 수정, production code와 무관한 부분들 (.gitignore, build.gradle 같은) </td>
    <td rowspan="2"> Related to: 해당 커밋에 관련된 이슈 번호(아직 해결되지 않은 경우) </td>
  </tr>
  <tr>
    <td> comment: 주석 추가 및 변경 </td>
  </tr>
  <tr>
    <td> remove: 파일, 폴더 삭제 </td>
    <td rowspan="2"> ex) Fixes: #45 Related to: #34, #23 </td>
  </tr>
  <tr>
    <td> rename: 파일, 폴더명 수정 </td>
  </tr>
</table>

예시
```
feat(#1): 로그인 기능 구현

로그인 시 JWT 발급

Resolves: #111
Ref: #122
related to: #30, #50
```
