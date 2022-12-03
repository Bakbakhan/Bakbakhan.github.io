# Bakbakhan.github.io<br/>
<br/>
# ElasticSearch Twitter logging<br/>
<br/>

## 하나

![1번](https://user-images.githubusercontent.com/102347088/205426804-a434186a-16ab-4ff9-a1da-aab8d0517182.png)
Elastic 폴더의 bin 폴더를 클릭후
elasticsearch.bat 파일을 실행

![2번](https://user-images.githubusercontent.com/102347088/205426904-86e4af68-37aa-4dc1-b9a7-fdf24770480e.png)
실행화면<br/>
![3번](https://user-images.githubusercontent.com/102347088/205426945-784f9ca9-976a-4e68-9483-2dbf0a9b4141.png)
localhost:9200 으로 실행을 확인 가능
<br/>


## 둘
![4qjs](https://user-images.githubusercontent.com/102347088/205426988-3b42da11-9252-46f3-954a-815358f4aa4e.png)
Kibana 폴더의 bin 파일을 눌러 Kibana.bat를 실행시킴<br/>


![5](https://user-images.githubusercontent.com/102347088/205427005-1b20fa32-26e3-4e1e-be80-a3fad99c0950.png)
Kibana.bat 파일을 실행시킨 후 화면<br/>


![6](https://user-images.githubusercontent.com/102347088/205427024-5ea60cfd-b971-4e9a-8e7d-6eefebc1ed3a.png)

localhost:5601 로 실행이 완료 된걸 확인할 수 있음<br/>

## 셋
![7](https://user-images.githubusercontent.com/102347088/205427053-a62e1816-44a7-45cb-a93e-26ce66862e70.png)
kibana.bat을 실행 후 logstash파일에 들어가서 실행이 아닌 경로부분에 cmd를 입력하여 커맨드 창을 실행<br/>


![8](https://user-images.githubusercontent.com/102347088/205427063-b9a42eb6-2c41-43eb-bb88-ac196aece424.png)
cmd창을 실행 후 bin\logstash.bat –f config\logstash-twitter.conf 를 입력<br/>


![9](https://user-images.githubusercontent.com/102347088/205427122-02f36851-c7a8-466b-869b-3f5f3e6b00b2.png)
실행 완료된 화면<br/>


![12](https://user-images.githubusercontent.com/102347088/205427168-909857b7-eb66-4d1a-b039-0f6276334542.png)
cmd창 실행 후 Scripts\activate 명령어를 입력하여 가상화 모드에 진입<br/>


![13](https://user-images.githubusercontent.com/102347088/205427192-cda7d0a5-fa89-4303-90f9-eea76a3e5e84.png)
진입 후 화면<br/>


![10](https://user-images.githubusercontent.com/102347088/205427270-6bf0db6b-2f6a-408e-9387-797b35e801b6.png)
tweeetlog폴더에 들어간 후 tweepy2.py파일을 실행<br/>


![11](https://user-images.githubusercontent.com/102347088/205427287-ed5f91c0-22d6-487d-a4fb-4c5d6692622d.png)<br/>
BEARER_TOKEN 은 가려줌 // 개인정보는 가려줌

![14](https://user-images.githubusercontent.com/102347088/205427343-1bdb502d-af65-4c62-990b-d7ccc82d7a3e.png)
bin\logstash.bat -f config\logstash-twitter.conf 명령어를 실행했던 화면에서 트위터 로깅되는 것을 확인<br/>



## 넷
![15](https://user-images.githubusercontent.com/102347088/205427399-7184021f-717b-4a66-b018-56f8ddde0c38.png)
Managemet의 Stack Management를 누름</br>

![16](https://user-images.githubusercontent.com/102347088/205427417-3986f1be-6bac-4846-9c74-7706d920f896.png)
Index Management를 누름</br>

![17](https://user-images.githubusercontent.com/102347088/205427445-e5e41fbd-6bfe-475d-a6f2-3c3640151a38.png)
Index Patterns을 누른 후  Create index pattern 에 py 파일에서 설정한 이름을 넣어줌 next step 으로 넘어감</br>

## 다섯
![18](https://user-images.githubusercontent.com/102347088/205427465-cf2913ef-a7a8-4ad1-83c2-809252ac6eba.png)
Kibana 창의 Discover을 누름</br>

![19](https://user-images.githubusercontent.com/102347088/205427483-dd4164a2-c6df-4d24-89e8-049f6d81e8b6.png)
INDEX PATTERN을 twitter_ko로 변경</br>

![20](https://user-images.githubusercontent.com/102347088/205427497-bf2680ce-b89e-4304-84b3-41dad110e9fe.png)
트위터의 로그가 수집된 내역과 수집된 로그양을 보여줌//날짜, 시간 변경 가능</br>
