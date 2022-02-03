# BasicSession
기초세션 과제 repo
------------
## 이승주 피드백
### 승주님 코드
``` python
  for i in range(len(df)):
    if df['요일'][i]==0:
        df['요일'][i] = 'Monday'
```        
      
✏for 문으로 작성한것도 너무너무 좋지만 모범답안 기준으로 loc를 사용하는 방법도 추가로 알려드립니다.
``` python
df.loc[df["요일"] == 0, "요일(humanized)"] = "Monday"
```
------------
pointplot이 힌트라고 준 이유는, lineplot에 데이터값마다 포인트가 있는 plot이 workingday냐 아니냐, 요일별로 비교를 하기 쉬워서 라고 생각합니다! 따라서
### 승주님 코드
```python
sns.barplot(data = df, x = '시간', y = 'count',hue = 'workingday')
```
✏barplot 대신에,
```python
sns.pointplot(data = df, x = '시간', y = 'count',hue = 'workingday')
```
으로 바꾸면 좋을 것 같습니다!

요일도 마찬가지로 pointplot으로 바꾸면 훨씬 비교하기 편할 것 입니다.
승주님 과제하느라 수고하셨습니다! 마지막과제까지 GOOD!

------------
------------
------------
## 권수현 피드백
pointplot이 힌트라고 준 이유는, lineplot에 데이터값마다 포인트가 있는 plot이 workingday냐 아니냐, 요일별로 비교를 하기 쉬워서 라고 생각합니다! 따라서
### 수현님 코드
```python
sns.barplot(data = train, x = 'hour', y = 'count',
            hue = 'holiday', palette = colors)
```
✏barplot 대신에,
```python
sns.pointplot(data =train, x = 'hour', y = 'count',hue = 'workingday')
```
으로 바꾸면 좋을 것 같습니다!
pointplot으로 바꾸면 훨씬 비교하기 편할 것 입니다.
수현님 과제하느라 수고하셨습니다! 마지막과제까지 GOOD!

------------
------------
------------
## 김한빈 피드백
### 한빈님 코드
워드클라우드 오류는 font_path를 두번 지정했기 때문입니다. 코드 확인해보시고, 중복된 부분을 지워주시면 됩니다.

```python
plt.plot(train_dayName_hour_df2['hour'], train_dayName_hour_df2['count'], marker='s', color='slategray') 
```
✏plot에서
```python
plt.plot(train_dayName_hour_df2['hour'], train_dayName_hour_df2['count'], marker='s', hue='workingday')
```
이렇게 바꿔줌으로써, workingday에 따라 색이 구분이 될 것 같습니다.
또는 과제에서 pointplot을 사용하라고 힌트를 주었기 때문에
```python
sns.pointplot(data =train_dayName_hour_df2, x = 'hour', y = 'count',hue = 'workingday')
```
이렇게 작성하는 것이 모범답안입니다.
한빈님 역시 과제하시느라 수고하셨습니다. 마지막까지 GOOD!
