# SpringStudy
★★★★★★★★★★★★★ 안의 pdf 참조 ★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★

0226<br>
7.Spring<br>
스프링은 끝물이라 스프링 부트로 간다. 스프링은 걸쳐가는 단계<br>


★★★ 일주일전에 spring서버 닫음 마켓에서 설치 불가 (알아두기만 하고 ex01파일을 사용할것) ★★★<br>


● 10-5 실행 "I move it " 클릭<br>
192.168.111.105 기억하기<br>
컴퓨터 이름 10-4로 기억하기<br>
찾기 > cmd > sqlplus > 이클립스 실행<br>
★ 이클립스는 2022-06버전이 제일 안정적임<br>

Open perspective에 스프링 들어 있음<br>
회사 들어가면 spring있는 걸로 줄거임<br>
왼쪽 server 들어가면 톰켓 깔려있음<br>
하단 server localHost 더블클릭<br>
포트번호 8000, 80 인지 확인<br>
80번으로 접속하는건 http이다라고 알아먹음 이제 포트번호 안나옴<br>

● perspective > web > utf-8인지 확인<br>
● file > new > spring legacy project ( spring MVC project, 프로젝트 이름 ex01 )<br>
> com.wsj.www(자기이니셜) 입력 ><br>
package Explorer > 자바프로젝트와 다르게 src/test/java, src/test/sources가 있음<br>
★ 주의할점 앞으로는 테스트 돌려야 한다.<br>
resources에는 jar같은 자원들이 들어간다.<br>
spring과 java 넣는 곳이 분리되어 있다.<br>
★ 항상 인터넷에 연결되어 있어야 한다.(연결끊기면 오류발생할수도 있음)<br>
Package Explorer에서 파란색 s자 붙은 파일들은 spring이 적용되는 파일<br>

● ex01우클릭 > export >Archive File > resolve and export linked resources 도 on 체크하고 확인<br>
> 바탕화면에 ex01.zip이 생기면 본체 바탕화면에 옮긴다음에 10-1에다 붙여서 돌린다.<br>

● 압축풀어서 실행하기(위의 방법은 전부 오류발생한다, 집또는 본체에서 실행하는 방법임)<br>
프로젝트 경로 sts-eclipse로 하고 실행<br>
package Explorer > import projects... > Select All(click) > into folder > Overwrite existing resources without warning는 on 설정 <br>

● 코드로 배우는 스프링 완성 .pdf<br>
★ 부트스트랩 그리드예시같은거 홈페이지가서 보기<br>
java Configuration은 스킵할거임<br>
Lombok 라이브러리가 DTO를 알아서 만듬<br>
집에가서 정독 면접가서 물어본다.<br>
● 10-5 > C:\Users\mit 안에 .m2 가 중요함 안에 스프링에서 사용하는 jar파일들이 있음<br>
설명하는 이유는 네트워크가 끊어지면 안됨 끊어지면 가끔씩 깨지는 파일들이 있음<br>
repository 삭제하고 이클립스 키면 오른쪽 아래 초록색 바에서 자동으로 다시 받는게 보인다.<br>
다시 경로를 보면 repository 가 다시 보인다 알수없는 오류가 있으면 repository삭제하고 다시 받을것<br>
또는 ex01오른쪽 클릭 Maven > update project... > ok 를 하면 repository 다시받는다.<br>

★ pom.xml은 자동화를 담당한다. , <br>
spring은 프레임워크<br>
테스트 돌리고 선생님에게 드려야 한다.<br>
servlet-context.xml은 프론트단<br>
views는 jsp쪽<br>
web.xml은 톰켓 환경설정<br>
pom.xml은 Maven에서 반자동으로 끌어온다.<br>

★★ hom.xml 주석 확실이 공부할것<br>
					★window pro는 어둠의경로로<br>
@Controller에서 뿌려준다.<br>
Model model 이 굉장히 중요함<br>
return "home"일 경우 home.jsp를 찾는다. ex) views폴더에 home.jsp있음<br>
console의 검은색 텍스트가 메모리 영역 만드는거<br>

38p럼북 라이브러리 설치 (이미 설치되어있음)<br>
자동으로 자바 빈즈 만들어준다.<br>
100줄일거 50줄로 짧아진다.<br>
데이터는 model을 통해서 전달, 받는건 EL로 받는다.<br>

● cmd로 이동 > d: > java -jar lombok.jar
Can't find IDE 뜨지만 상관없음 > 닫기
D:\study\eclipse > eclipse.ini에 lombok있는지 확인

● 파랑색 s 자 붙은 파일은 spring이 관리하는것<br>
48p 의존성 주입, 주의할점 읽어보기<br>
spring은 2010년도 거 지금은 api가 너무 무겁다. 2020년 부터 Spring Boot 유행 가벼움<br>
6버전은 boot Spring<br>
★POJO, 의존성 AOP 알기<br>
DTO를 lombok이 만든다.<br>
● 10-5열기<br>
pom.xml > 35줄<br>
https://mvnrepository.com/ 에서 lombok 검색 > 1.18.24 > Maven 안에있는 코드복사 붙여넣기<br>
		<!--  lombok 실행 코드 주입 -->	<br>
● spring-test 검색 너무 많으니 그냥 타이핑 	ex)톰켓 실행중이면 타이핑오류 보일수도 있음 <br>
		<!-- spring-test 코드 주입 --><br>
package Explorer에서 Maven Dependencies 에서<br>
lombok~.jar , spring-test ~ RELEASE.jar 있는지 확인<br>

하단 Problems 탭에서 오류있는지 확인할수 있고 오류 클릭하면 삭제할수 있음<br>

조장이 pom.xml을 뿌려서 통일시킨다.<br>

● 
7.spring 파일 >  <br>
<!-- log4j2 활성화 : resources log4j2.xml 변경 https://logging.apache.org/log4j/2.x/maven-artifacts.html --><br>
내용 복사해서 48p에 붙여넣기<br>
src/test/resources, src/main/resources 에 있던 log4.j2.xml 2개 다 삭제하고<br>
7.spring 파일에 있는 log4.j2.xml 파일을 2번 붙여넣기 한다.<br>

pom.xml > <!-- Test -->는 메소드 마다 테스트<br>
4.12로 버전 바꾸어야 한다. 			<version>4.12</version><br>

● @Com ctrl + enter시 오류 팝업 뜬다 > 팝업의 content assist 클릭 ><br>
아래쪽 목록중 java proprosal 체크 해제할것<br>

★ @선언된건 자동으로 입력되게 해야 오류가 적다.<br>

● root-context.xml >중간의 Namespaces 탭 > "context - ~ " on체크 ><br>
<context:component-scan base-package="org.zerock.sample"></context:component-scan> 추가<br>
추가하고 나면 org.zerock.sample 패키지의 java 파일들에게 s 파란색이 생긴다.<br>
Beans Graph 탭 눌러보기 > 노란색 콩들이보인다 (method)<br>
● src/test/java에서 org.zerock.sample 패키지로 SampleTests.java 생성<br>
★★★ SampleTests 계속 복사해서 써먹는다. 중요<br>
@Log4j2는 보안에 취약<br>
Sysout.console 은 이제 log.info()로 대체된다.<br>
testExist더블클릭 마우스 오른쪽 클릭 > Run as > 2.JUnit Test<br>
하단탭에 JUnit탭 발생하고, 콘솔에 <br>
 INFO  org.zerock.sample.SampleTests(testExist27) - Restaurant(chef=Chef())<br>
 INFO  org.zerock.sample.SampleTests(testExist28) - -------------------------<br>
 INFO  org.zerock.sample.SampleTests(testExist29) - Chef()<br>
가 있어야 한다 없으면 오류, 경로글자 오타일수 있음<br>
● 선생님 이 뿌린 pom.xml 참조 <br>
복습 많이 해야한다.<br>
@Log4j 는 로그찍음 Sysout 대신 log.info<br>
단일 생성자의 묵시적 자동 주입
● src/test/java > SampleTests.java를 SampleTest.java를 복사해서 이름만 바꿔서 생성.<br>
testExist() 더블클릭 > 오른쪽클릭 > Run as > 2.JUnit <br>
SampleHotel.java와 HotelTest.java와 비교해볼것<br>
● SampleHotel > <br>
public SampleHotel(Chef chef) {this.chef = chef; }<br>
주석처리하고 <br>
@AllArgsConstructor //생성자 자동 주입<br>


추가<br>
@AllArgsConstructor 는 모든 필드값에 반응해라라는 뜻<br>
@RequiredArgsConstructor //생성  		책보고 공부<br>
●●● 03 스프링과 Oracle Database연동 71p<br>
D:\Desktop\Spring\OracleXE112_Win64\DISK1 setup.ext실행<br>
id,패스워드는 oracle<br>
오라클 설치<br>
Open perspective > Data base ><br>
Database Connections > new > 이번엔 ojdbc8.jar사용 > DB생성<br>
스프링으로 이동 > src/main/resources/에 sql생성<br>

● TEST쪽에 package org.zerock.persistence; 로 JDBCTests.java 생성<br>
★★★★ void testConnection()의 try 중괄호가 아닌 소괄호로 try()<br>
try (Connection con = DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe","book_ex","book_ex")){<br>
				log.info(con);}<br>

org.zerock.controller 로새스프링 프로젝트생성<br>
10-1 에서는 이제 이클립스 사용안한다. sts.exe실행 시작시 경고 팝업뜨면 톰켓 없어서 그렇다<br>
server탭에서 톰켓연결할것<br>
★★ Package Explorer에서 파일 정보 안보이면 Package Explorer 닫았다가 window탭에서 다시 Package Explorer열어보기<br>
이제부터  복붙으로 프로젝트 생성한다.<br>
10-1 불안정하니 jdk 11버전으로 낮춰라<br>

★★★ pom.xml의 첫줄에 오류발생한는거 <br>
			<plugin><br>
				<!-- https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-war-plugin --><br>
				<groupId>org.apache.maven.plugins</groupId><br>
				<artifactId>maven-war-plugin</artifactId><br>
				<version>3.3.2</version><br>
			</plugin><br>
<plugins></plugins>안에다 추가하면 해결된다.<br>

★★ autowrit? 오류 뜨면 lombok 설치안되있는것<br>


★ 0227
60p 이해할것<br>
★@Log4j 를 Log4j2로 수정할 것<br>
83 히카리 hikaricp<br>
https://mvnrepository.com/search?q=hikaricp<br>
2.7.4 버전 클릭<br>

root-context.xml > 84p 코드 입력 오타나면 안되니 복붙할것<br>
중간  beans 탭 눌러보기 hikariConfig, dataSource있는지 확인하기 있으면 객체화 시켰다는 것<br>

● DataSourceTests.java , hotelTest.java같은 코드는 <br>

@RunWith(SpringJUnit4ClassRunner.class)	// junit으로 테스트 코드<br>
@ContextConfiguration("file:src/main/webapp/WEB-INF/spring/root-context.xml") //참고할 파일<br>
@Log4j2 // Log4j2를 이용해서 로그 출력(콘솔에 찍히는 로그)<br>

붙이기
●testConnection Junit 실행해보기<br>
★@코드네임은 자동완성할것 자동완성 안하면 코드오류 발생할 수 있음<br>
● MyBatis, spring에서 자주 사용함<br>
web.xml에서 히카리 밑에다가 mybatis 선언<br>
철자 틀리면 안되니 "mybatis복붙용 삭제금지".text에서 복붙하기<br>
★ 콘솔의 빨간색은 톰켓 로그 애러아님<br>
● 스프링과의 연동 처리<br>
Mapper는 매핑하는 것 쿼리와 자바를 매핑 , <br>
~를 호출했을때 ~쿼리를 호출하는것<br>
● interface TimeMapper.java<br>
★★★ 주의사항 sql문 뒤에 ; 사용하면 오류<br>
★ Beans Graph탭이나, Namespaces 에 mybatis-spring 안보이면 이클립스 종료재시작 해보기<br>


(testGetTime26)은 spring이 자동으로 만든 구현 클래스<br>

● 98p
TimeMapper.java와 동일한 이름인 TimeMapper.xml 파일을 만든다, 대소문자 일치시키기<br>
★ 오타있으면 안되니  TimeMapper.xml 은 TimeMapper.text 복붙할것<br>
★ 다른곳에서 사용할 때 프로젝트명 :   <mapper namespace="org.zerock.mapper.TimeMapper"> 만 바꾸면 된다.<br>
● testGetTime2() 실행<br>
● 4.3 log4dbc-log4j2 설정 101p<br>
https://mvnrepository.com/search?q=log4jdbc <br>
log4jdbc 검색<br>

● 105p 출력안되면 서블릿과 mybatis 버전때문이다.  <br>
mybatis <version>3.5.15</version>로 변경하기<br>
pom.xml의 <!-- 구버전 주석처리함 --> 참조<br>
105p문제해결.txt 에서 복붙하고 name만 수정하여 사용<br>
<name>ex01</name><br>
● 107p mvc.txt받은거 참고할것<br>
Controller 는 url로 오는걸 view로 뿌려줄지 model로 뿌려줄지 판단함<br>
WebApplication Context = 톰켓<br>

책과 버전 다름<br>
mvc.txt받은거 참고할것<br>
크롬에서 http://localhost/controller/ 검색<br>
112p<br>
<url-pattern>/</url-pattern> 은 localHost의 /<br>
Request/Response 사용안함<br>
이제 <% value %> 사용안함<br>
★★★123p 여러번 읽어보기  ★★Model★★ Model에서 데이터를 땡겨온다.<br>
<context:component-scan base-package="org.zerock.controller" /> 의 경로에있어야 <br>
파란색 s마크가 생긴다.<br>
크롬에서 http://localhost/sample/ 입장<br>
void 라서 반환이없으면 똑같은 이름의 jsp를 찾는다. <br>
Get방식은 보안에 안좋다.<br>
● 131p<br>
★ 데이터의 크기가 형식보다(int) 보다크면 자동으로 안된다.<br>
● SampleDTOList<br>
SampleController.java > ex02Bean()<br>
TodoDTO.java > TodoDTO 의 Date는 java.util<br>
● new SimpleDateFormat("yyyy-MM-dd");  입력되는 타입이 같아야 값이 입력된다.<br>

★ http://localhost/sample/ex03?title=test&dueDate=2024-02-27 가 실행안되면<br>
void initBinder() 주석처리하고 실행하면 된다.
138p까지 복습하기

0228<br>
★135p [] 설명<br>
return "/sample/ex04" ;			/sample 반드시 붙이기<br>
★★★ 웹화면에 hello.jsp 보일경우 하단 톰켓에서 add/remove 설정해보자.<br>

● jackson-databind<br>
https://mvnrepository.com/artifact/com.fasterxml.jackson.core/jackson-databind<br>
2.9.4 버전<br>
F12 > Network > ctrl + r <br>
★ HttpHeaders 는 import org.springframework.http.HttpHeaders; 로 자동완성할것<br>

149p<br>
https://mvnrepository.com/ > commons-fileupload 검색 > Apache Commons FileUpload로 입장 ><br>
1.3.3 버전 코드 복붙<br>
c 드라이브 > 파일이름upload로 생성 > 파일 tmp 생성<br>
servlet-context.xml > <!--  파일 업로드용 5가지 처리 -->이하 코드 추가<br>
오타나면 안되니 받은 텍스트 붙여넣기<br>
★<beans:property name="defaultEncoding" value="utf-8"></beans:property> 는 한글깨짐 방지<br>
★ value="file:/C:/upload/tmp"></beans:property> 파일 경로 주의<br>
★★★ 주석 선언할때마다 성실하게 입력해넣기<br>
@GetMapping("/exUpload") 의 exUpload는 .jsp<br>
154p<br>
유튜브에 "구멍가게 코딩단 입력" 코드로 배우는 스프링 2024다보기<br>

★★★C:\oraclexe\app\oracle\product\11.2.0\server\bin 집노트북에 복붙하기<br>
C:\Program Files\Common Files\Oracle\Java\javapath<br>

error_page.jsp 실행하고나서 주소 age=에 aaa를 넣고 실행해본다.<br>
http://localhost/sample/ex04?name=kkw&age=aaa&page=3<br>

★★web.xml 철자틀리면 톰켓에서 오류 생김<br>
<init-param> <!-- 예외처리를 톰켓이 아닌 spring에서 처리할 것 --><br>
	<param-name>throwExceptionIfNoHandlerFound</param-name><br>
	<param-value>true</param-value><br>
</init-param><br>

● 163p <br>
이제 pstmt 사용안함<br>
paging api사용<br>
DAO 대신 Mapper사용<br>
패키지 나누는 이유 관심사의 분리<br>
엑셀실행 엑셀은 자료관리용 <br>
"파일목록문서화"<br>
보기 > 경로  > 틀고정<br>
우클릭 > 하이퍼링크 제거<br>

● 프로젝트 새로만듬 board<br>
★<web-app > 빨간줄 생기는건 버전이 낮아서 servers > web.xml에서 붙여넣기<br>
★pom 0228완전판 board web.xml에 복붙하기<br>
★56줄 <!-- root-context.xml 에 삽입 " 을 복사해서 root-context.xml에 붙여넣기<br>

★102줄 <!-- root-context.xml 코드 변경  "을 복붙하면 org.zerock.mapper없어서 오류날수 있음<br>
★root-context. "<mybatis-spring:scan" 빨간줄나면 ex01번에 있는거 복붙하고 그래도 <br>
빨간줄 나는건 Namespaces 탭에서 mybatis on하면된다.<br>
★ <context:component-scan base-package="org.zerock.sample"></context:component-scan>
는 지워도 된다.<br>
시작용 board백업폴더<br>
★프론트는 결론 sql자격증 좋음<br>
board가 책의 ex02<br>
★ test경로의 폴더는 export할때 안들어감 sql넣기 좋음<br>
●org.zerock.persistence 패키지에 있는 dataSourceTest.java,JDBCTests.java 복붙 하기<br>
junit으로 실행<br>
★ 에겔에서 (i) 는 인터페이스란뜻<br>
★ unread 나오는건 나중에 확인ㅍ
★ onMethod_ 빨간줄 뜨는건 lombok설치안되서 그렇다 lombok.jar더블클릭해서 설치하지 말고 cmd에서
설치할것<br>


★ 0229<br>
●★ 수업자료에서 "spring-tool-suit-3.9.18.zip " 가져오기 > 압축풀지말고 더블클릭해서 sts-3.9.18.RELEASE<br>
폴더 드래그해서 D: 드라이브에 넣기<br>
>인터넷에서 lombok 검색후 설치 > cmd에서 d: > java -jar lombok.jar<br>
★ sts.exe실행 안되면 STS.ini에서 -javaagent:D:\sts-3.9.18.RELEASE\lombok.jar 경로 수정<br>
★ File > open Projects from File System > 적용안되면 sts의 severs에 톰켓 연결<br>
★ Spring MVC Project 이제 지원안해서 복붙해서 사용하는중<br>
7장 자바 설정은 할필요없음<br>
xml과 interface가 한세트 <br>
제일먼저 DB부터 만든다 DB를 보고 테이블을 구현 콘솔까지만 구현하면된다.<br>
jsp에서 쓰던 ? 대신 #{속성}을 사용한다.<br>
인터페이스 안의 메서드는 조장이 짜준다.<br>

<insert id="insert">의  insert는 메서드 명과 일치<br>
<insert>안에서도 ; 사용하지 말것<br>
lownum사용해서 seq_num 중복만 없으면 상관없음<br>
unread신경쓰지 말고 날짜만 확인하기<br>
198p DB믹스는 Service 계층에서 한다. ex) 틀리면 선생님에게혼남<br>
느슨한 (select *  사용하란 뜻)<br>
mapper는 대부분 DB용어<br>
context는 메모리영역<br>
문제생기면 이클립스 종료재실행 해보기<br>
boot도 10년쓴다.<br>

★ 메서드 별로 어디서어디로 갔다 엑셀에 정리하기<br>
★ @RequestMapping("/board/*") ("/~" ) 빼먹지 말기<br>
★ 문제시 Mudule 에 /인지 /controller인지 확인<br>
★ log.info를 파일로 만든다<br>
★★ 톰켓을 안쓰고 사용하는 방법 class BoardControllerTests 는 가짜 mvc<br>
@Before,  junit걸로 import<br>
(ctx).build(); 는 build패턴<br>
★ BoardControllerTests는 servlect-context.xml도 필요하다<br>
@ContextConfiguration({"file:src/main/webapp/WEB-INF/spring/root-context.xml",<br>
file:src/main/webapp/WEB-INF/spring/appServlet/servlet-context.xml"}) //참고할 파일
로 수정할것<br>
@WebAppConfiguration<br>
●MockMvc.txt복사해서 붙여넣기<br>
String register() 값이 두개있는 경우는 성공시/실패시<br>
★★★★ unread 오류 해결 정보<br>
테이블 조회할 때 콘솔창에서 unread 되는거 해결방법인데 , property에 BoardVO 변수명이랑 맞춰주면 될 것 같아요! column은 테이블 컬럼명이에욤<br>
★ nvarchar을 n붙여너 unread생긴것<br>
★ rog.zerock.controller 철자틀려서 오류생겼었음 com<br>
★ return "redirect:/board/list"; // 처리후 돌아갈 페이지     같은거 엑셀에저장<br>
★★ BoardMapper.txt 붙여넣기<br>

다음주 jsp연결<br>


