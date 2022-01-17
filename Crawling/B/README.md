### 과제 풀이
```
divs = soup.findAll('div', attrs = {'class' : 'list_item'})

div.find('div', attrs = {'class' : 'col company_nm'})
div.find('div', attrs = {'class' : 'col notification_info'})
```
위 코드를 활용하시면 되겠습니다!

### 피드백
- 예진님: 수고하셨습니다!:)
- 용호님: 수고하셨습니다!:)
- 종민님: 바로 a에서 회사명과 제목을 찾아서 순서대로 나눈 것도 좋은 방법이네요!:) div에서 'col company_nm', 'col notification_info'로 각각 찾아내는 방식도 참고하세용! 수고하셨습니다!
- 유리님: 수고하셨습니다! div에서 'col company_nm', 'col notification_info'로 회사명과 공고를 구분해서 찾는 방법도 참고하세요!!
