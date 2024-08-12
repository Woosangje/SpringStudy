★★★ 일주일전에 spring서버 닫음 마켓에서 설치 불가 (알아두기만 하고 ex01파일을 사용할것) ★★★<br>


● Mv 10-5 실행 "I move it " 클릭<br>
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

com.wsj.www(자기이니셜) 입력 ><br>
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

★ 프로젝트 생성안되면 .m2 밑의 repository폴더의 내용물 삭제하고 이클립스 재시작 할것

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

★★ hom.xml 주석 확실히 공부할것<br>

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
(7.spring) 파일 >  <br>
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

오라클 tord에서 수정시 commit꼭 실행해줄것

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
.xml 코드는 어지간하면 복붙하기<br>
불안정하니 jdk 11버전으로 낮춰라<br>

★★★ pom.xml의 첫줄에 오류발생한는거 <br>
			<plugin><br>
				<!-- https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-war-plugin --><br>
				<groupId>org.apache.maven.plugins</groupId><br>
				<artifactId>maven-war-plugin</artifactId><br>
				<version>3.3.2</version><br>
			</plugin><br>
<plugins></plugins>안에다 추가하면 해결된다.<br>

★★ autowrite? 오류 뜨면 lombok 설치안되있는것<br>


★ 0227<br>
60p 이해할것<br>
★@Log4j 를 Log4j2로 수정할 것<br>
히카리 hikaricp<br>
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
<url-pattern>/</url-pattern> 은 localHost의 /<br>
Request/Response 사용안함<br>
이제 <% value %> 사용안함<br>
★★★123p 여러번 읽어보기 Model에서 데이터를 땡겨온다.<br>
<context:component-scan base-package="org.zerock.controller" /> 의 경로에있어야 <br>
파란색 s마크가 생긴다.<br>
크롬에서 http://localhost/sample/ 입장<br>
void 라서 반환이없으면 똑같은 이름의 jsp를 찾는다. <br>
Get방식은 보안에 안좋다.<br>
★ 131p aaa 실행 안될시 톰켓 /controller 수정되어있는지확인
★ 데이터의 크기가 형식보다(int) 보다크면 자동으로 안된다.<br>
● SampleDTOList<br>
SampleController.java > ex02Bean()<br>
TodoDTO.java > TodoDTO 의 Date는 java.util<br>
● new SimpleDateFormat("yyyy-MM-dd");  입력되는 타입이 같아야 값이 입력된다.<br>

★ http://localhost/sample/ex03?title=test&dueDate=2024-02-27 가 실행안되면<br>
void initBinder() 주석처리하고 실행하면 된다.
138p까지 복습하기

★135p [] 설명<br
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

★<beans:property name="defaultEncoding" value="utf-8"></beans:property> 는 웹에서 등록시 한글깨짐 방지<br>
★ value="file:/C:/upload/tmp"></beans:property> 파일 경로 주의<br>
★★★ 주석 선언할때마다 성실하게 입력해넣기<br>
@GetMapping("/exUpload") 의 exUpload는 .jsp<br>
154p<br>
유튜브에 "구멍가게 코딩단 입력" 코드로 배우는 스프링 2024다보기<br>

★★★C:\oraclexe\app\oracle\product\11.2.0\server\bin 집노트북에 복붙하기<br>
C:\Program Files\Common Files\Oracle\Java\javapath<br>

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

● board가 책의 ex02 170p<br>
★ test경로의 폴더는 export할때 안들어감 sql넣기 좋음<br>
●org.zerock.persistence 패키지에 있는 dataSourceTest.java,JDBCTests.java 복붙 하기<br>
junit으로 실행<br>
★ 엑셀에서 (i) 는 인터페이스란뜻<br>
★ unread 나오는건 나중에 확인
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

★ 메서드 별로 어디서어디로 갔다 엑셀에 정리하기<br>
★ @RequestMapping("/board/*") ("/~" ) 빼먹지 말기<br>
★ 문제시 Mudule 에 /인지 /controller인지 확인<br>
★ log.info를 파일로 만든다<br>
(ctx).build(); 는 build패턴<br>
★ BoardControllerTests는 servlect-context.xml도 필요하다<br>
@ContextConfiguration({"file:src/main/webapp/WEB-INF/spring/root-context.xml",<br>
file:src/main/webapp/WEB-INF/spring/appServlet/servlet-context.xml"}) //참고할 파일
로 수정할것<br>

●MockMvc.txt, JDBCTests, DataSourceTests 깃에서 복사해서 붙여넣기<br>
String register() 값이 두개있는 경우는 성공시/실패시<br>
★★★★ unread 오류 해결 정보<br>
테이블 조회할 때 콘솔창에서 unread 되는거 해결방법인데 , property에 BoardVO 변수명이랑 맞춰주면 될 것 같아요! column은 테이블 컬럼명이에욤<br>
★ nvarchar을 n붙여너 unread생긴것<br>
★ return "redirect:/board/list"; // 처리후 돌아갈 페이지     같은거 엑셀에저장<br>
★★ BoardMapper.txt 붙여넣기<br>

## MockMvc로 Register 테스트하면 WARNING: An illegal reflective access operation has occurred 오류 발생하는데 신경안써도 DB에 등록은된다



0304<br>
get매핑할때 / 사용할것<br>
controller에서 jsp로 간다.<br>
백을 완성시켜 놓고 프론트에 붙인다.<br>

★ mybatis , 히카리cp 사용안하는 회사도 있다.<br>
프론트 있는 상태에서 개발하는 것을 추천<br>

● 10-5 바탕화면의 spring폴더 > bootstrap > 게시판 만들었던것에 붙일것음<br>
webapp > resources에 css,js 넣기<br>


list에 부트스트랩 table 코드 복붙, 톰켓실행하고 크롬에서 실행하면 경로 때문에 깨져보임<br>
ctrl + shifg + / 주석처리<br>
크롬 google jquery cdn 검색<br>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script><br>

list.jsp파일에 jsp헤더list.txt파일 복붙하기<br>
자바에서 mapper일경우 mapper.xml을 꼭 가보기<br>
★ 오타나면 null point Exception 오류 발생한다.<br>
jsp 상단에 <%@~%> 넣기<br>
● fmt 작성할경우 상단에<br>
<%@ taglib uri=" http://java.sun.com/jsp/jstl/core" prefix="c"%>   
 <%@ taglib uri=" http://java.sun.com/jsp/jstl/fmt" prefix="fmt"%> 선언 안하면 출력안됨<br>
★오타 게시판 mybatis문제 생길경우 jsp에서 content를 context로 적었는지  철자 확인<br>
● 한글처리 web.xml<br>

249<br>
이제 등록 할때 href대신  <form id='operForm'>이랑 Js 사용할것<br>
★★★ jsp에서 java코드들 주석처리하면 웹에서 F12누를경우 주석이 다보인다.<br>
http://localhost/board/register<br>
엑셀파일 마무리<br>
sts.exe Database 설치 방법:  help > update > https://download.eclipse.org/releases/2021-03  로 검색(안될수도 있음)<br>

268p<br>
● id="dataTables-example" 넣으면 페이징과 search가 보인다<br>
● order by의 문제 268p  order by 대신 인덱스를 사용하자<br>
● [CDATA]안에는 주석처리 안하는게 좋음<br>
BoardServiceImpl빨간줄 생기면<br>
● 14페이징 화면 처리 302P<br>
PageDTO 공식 써먹으면된다.<br>
페이지네이션 https://getbootstrap.com/docs/4.3/components/pagination/<br>

★ BoardMapper.xml 에서 resultType을 resultMap으로 입력해도 오류발생하여 웹에서 출력안된다.<br>

※0306<br>
board(페이징,다중검색) 파일 안의 src board안에 복붙<br>
BoardMapper.xml db의 crud를 쿼리 처리<br>

● 웹에서 실행시 이상하면 톰켓다시설정할것 <br>

jsp 2000년도 유행<br>
spring 2010년<br>
화면은 고정된상태에서 모달마냥 crud가 변경되는것 ajax<br>
rest방식<br>
● 안드로이드 프로그래밍책 한번읽어보기<br>
주소에 ?가 없으면 rest 방식<br>
rest 방식은 객체가 아님<br>

353p Rest 프로젝트 생성<br>

★Rest프로젝트와 board프로젝트의 xml은 다르다 복붙주의<br>
https://mvnrepository.com/<br>
jackson 검색 > jackson Databind 클릭<br>
빨간색경고는 보안에 취약함 2.9.6버전 , 실무에서는 다른버전<br>
jackson xml 검색 > Jackson Dataformat XML » 2.9.6<br>
gson 검색 > Gson 2.8.2버전 <br>

★★★ value = "/getText" = localhost/rest/getText<br>
도메인은 객체들<br>
● SampleControllerTests 위에 <br>
@RunWith(SpringJUnit4ClassRunner.class)<br>

//Test for Controller<br>
@WebAppConfiguration<br>

@ContextConfiguration({ "file:src/main/webapp/WEB-INF/spring/root-context.xml",<br>
		"file:src/main/webapp/WEB-INF/spring/appServlet/servlet-context.xml" })<br>
@Log4j2<br>


@Setter(onMethod_ = { @Autowired })<br>
	private WebApplicationContext ctx;<br>

	private MockMvc mockMvc;<br>

	@Before<br>
	public void setup() {<br>
		this.mockMvc = MockMvcBuilders.webAppContextSetup(ctx).build();<br>
	}<br>

붙여넣기<br>

★★★ SampleControllerTests.java의 testConvert() 작성시<br>
import static org.springframework.test.web.servlet.request.MockMvcRequestBuilders.post;<br>
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.status;<br>
붙여넣기<br>

testConvert() 웹에서 실행방법(오류pdf참조)<br>
웹 설정의 확장프로그램에서 chrome 웹스토어 >  rest검색 > Yet Another REST Client > 웹페이지 주소창 오른쪽 <br>
http://localhost/rest/ticket<br>
{"tno":123, "owner":"kkw","grade":"vvip"}<br>

● 17 Ajax 댓글처리 375p<br>
board 프로젝트로 이동<br>
5.3.21 를 5.0.7.RELEASE 로 버전을 낮춘다.<br>
.xml에 json코드도 추가해야한다.<br>

● 오류있을 경우 "board(댓글시작)"파일 붙여넣기<br>


★ 386p delete메소드의 targetRno는 int가 아니라 long이다.<br>
★ 이클립스설치하고 visualstudio 깔면 꼬인다.<br>
★ 댓글관련된페이지 실행안되면 톰켓 초기화하기, 포트번호 1,1 클릭해도 수정안되면 톰켓실행해보고 수정하기 

#0307
5.0.7 RELEASE 로 수정
board(댓글,tx.app)보고 버전 수정 할것
★★★ 384p Long bno 가 아니라 rno
●aop-tx 프로젝트생성

메이븐 레파지토리 > aspectjrt<br>

이거 0307board알집의 pom.xml에 붙여넣기<br>
			<!-- https://mvnrepository.com/artifact/org.aspectj/aspectjweaver -->
		<dependency>
			<groupId>org.aspectj</groupId>
			<artifactId>aspectjweaver</artifactId>
			<version>${org.aspectj-version}</version>
		</dependency> <!-- AOP 관련 설정 추가(객체용)-->

★ 나이같은건 db에 넣지 말것
DB를 두개 넣고싶을때 Transational 사용한다.
● board(댓글,tx,aop) 보고 마무리하기

★★★ 421p 문제있다  board(댓글,tx,aop) 보고 CloseBtn'을 register로 수정하기
★ js에서 } 하나 더있어서 팝업 안생긴것 정렬 잘하기

댓글완료)444p까지
연봉높일려면 form이 아니라 rest사용해야한다.

ex01프로젝트를 복사하여 filedata이름으로 생성
\\192.168.0.200
http://localhost/uploadFormAction 파일넣으면 404에러가 정상
jsp 만들어야한다.

458p<br>
트랜잭션 사용하려면 pom.xml에다 spring-jdbc, spring-tx, mybatis, mybatis-spring, hikari를 추가해야한다.<br>

aop 테스트 실행시 WARNING: An illegal reflective access operation has occurred 경고가 발생하는데 mybatis문제 해결안해도 실행은 된다.<br>
스프링 프레임워크 버전 5.1이상으로 올리면 된다는데 공부시에는 보류할것<br>

480p<br>
480p까지 aop, 트랜잭션 읽기<br>
댓글 수 처리하기, DB에서 실행할것<br>
reply 칼럼<br>
alter table tbl_board add (replycnt number default 0);<br>
기존 댓글이 존재할 경우 실행<br>
update tbl_board set replycnt = (select count(rno) from tbl_reply where tbl_reply.bno = tbl_board.bno);<br>

● 트랜잭션 사용하는 과정에서 오류생길수 있으니 파일별도로 저장하기
● 댓글수 만들려면 트랜잭션 필요<br>

● 498p uploadForm.jsp 경로 board/ 아님

488p 604p까지
서버에 무리가없는데 이상하게 안되면 크롬에서 쿠키삭제할것 또는 vm재부팅할것
● 515p 이미지 업로드시 책과 달리 input에 multiple선언해도 2개, 3개 이런식으로 안뜬다 신경쓰지말것<br>

$(document).ready(function() 안에 바닐라 function을 선언하면 웹에서 "showImage is not defined" 같은 에러발생할수 있다
바닐라 function()은 밖에다가 선언할것

탭의search로 변수 입력해서 찾아보자
ajax rest사용해야 연봉이 오른다.

● 531p
파일 업로드 Resource선언 import org.springframework.core.io.FileSystemResource;로할것<br>
● 541p
str += "<li><a href=\"javascript:showImage(\'"+originPath+"\')\"><img src='/display?fileName="+fileCallPath+"'></a><li>";
)">랑 <img src~ 사이에 enter 하지말것 토큰에러 발생한다.
					



Security<br>
Spring = 반자동화<br>
605~738p까지 진행해보기<br>
Intellij<br>
● Project Exploerer탭 에서01ex 복사해서  Security프로젝트 생성<br>
pom.xml을 board프로젝트의 pom.xml으로 마추기<br>

Maven에 spring security 검색<br>
Spring Security Core <br>
5.0.6 복사해서 4번 붙여 넣고<br>
3번 <artifactId>spring-security-core</artifactId> 를 책처럼 수정한다.<br>

security-context.xml 오류있으니<br>
xsi:schemaLocation=  ~<br>
http://www.springframework.org/schema/security/spring-security-5.0.xsd<br>
의 -5.0를 제거할것<br>
● 서버 add & Move 설정하고 Modules / 설정할것<br>
org.zerock.controller로 이름수정하고 servlet-context에 <filter-name>springSecurityFilterChain</filter-name><br>
있는지 확인<br>

서버 실행해보면 SEVERE: 필터 [springSecurityFilterChain]을(를) 시작하는 중 오류 발생<br>
나온다.<br>

안되면 수업자료<br>

● @RequestMapping("/sample/*") 는 폴더경로 smaple폴더<br>
615p
Ldap = 라이트 디렉토리 서비스, 이거하면 좋은점이 학교에서 공부하던거 집에서 똑같이 상용할 수 있음<br>
access=의 "permitAll" , ROLE_MEMBER 이미 만들어져 있는 예약어<br>
●/login.jsp는 테스트용이라 우리가 안만들었다.<br>
★ {noop}실무에서 사용하지 말기<br>

F12 > 탭 Application > 좌측 Cookies > delete<br>

625p 로그인창에서 새로고침하기전에 쿠키세션 삭제하고 새로고침하기<br>
멤버로그인상태에서 admin주소로 이동할시 잘못된 경로라고 알려주는게 필요<br>

Class CustomAccessDeniedHandler 빨간줄뜨면 add ~ 선택 또는 코드입력<br>
● 630p 실행안되면 <bean 입력됐는지 확인 ,그래도 오류뜨면 context0311.txt 복붙하기<br>
//"{noop}member"  주석처리하면 안된다.
_csrf 해킹공격에 대응하는 코드<br>
★ 게시판 10번 만들어보기<br>
● 630p bean id="customLoginSuccess"~ 입력 빼먹지 않기
● 640p <security:logout logout-url="/customLogout" invalidate-session="true"/> 은 <security:http> 안에다 선언한다.
605~643p까지완성된파일<br>
완성본 옮기기605~738p 7. sec(end)파일<br>


xhr은 csrf, security용<br>
646p 로그인하면 500오류가 정상, INFO 책내용대로 나오고 에러도 책대로 나온다.<br>
<security:user-service> {noop} ~ 주석처리해야 한다.<br>

		<!-- 653p--><br>
		<dependency><br>
			<groupId>org.springframework</groupId><br>
			<artifactId>spring-test</artifactId><br>
			<version>${org.springframework-version}</version><br>
		</dependency>   <br>

pom.xml 히카리 mybatis주석달아보기<br>


※ 0312
(교재판매),(도서대여) 637<br>
673 null 뜨는거 선생님의 pom.xml비교해볼것<br>
선생님이 https://github.com/lonen8188/Spring 에다 올림<br>
깃브런치 master로 바꾸면 어제거 보임 customLogin.jsp <br>
LogAdvice 참조<br>

sample/admin 673p 잘안되면 넘어가기<br>
board에다 붙여서 해보기<br>
★ 656p 오류발생시 i를 1로 입력했는지 확인<br>

xml에서 mybatis 사용하려면 <!DOCTYPE mapper ~ mybatis> 있어야한다. 붙여넣기<br>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd"><br>

● 662p MemberMapper.xml경로 org, zerock, mapper일일이 클릭해서 들어간다음 생성한다.<br>
○ id="authMap" 를 autoMap으로 오타<br>



※ 0313

회원2명 게시판 2명
팀원끼리 DB 타입 문자길이 일치시켜야한다.
주석달기
667p WARN adim90 에러 있어도 정상
ERROR org.springframework.security.web.authentication.UsernamePasswordAuthenticationFilte
★ 로그인페이지에 새로고침하고나서 쿠키를 삭제해야 admin90에 로그인할수 있다.

★ xml에 <dependency> 같은곳에 이유없이 빨간줄오류 뜨면 코드 지웠다 복붙해보기

○185p설명 파일 복붙후에 실행오류 나는 이유는 BoardMapper.xml에 <select id="getList"~>있어서 그렇다.

● xerd 열기: 7. SpringProject(교재판매) >  boardshop01 > webapp > WEB-INF > erd > <br>
상단 탭 > erd ><br>
erd를 만든다음 테이블에 밀어 넣는다.<br>
jdbc 드라이버 파일선택 > ojdbc8.jar 넣으면됨<br>
★ 쇼핑몰 예제할때 exerd설치하지말고 선생님걸로 설치할것<br>

○mockMvc 은 console.log 같은것<br>



● jsp상단에 붙이기
<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%><br>
<%@ taglib uri="http://java.sun.com/jsp/jstl/fmt" prefix="fmt"%><br>

★ 빛좋은 개살구 BookTopia제대로 만들려면 3달은 있어야함 어디까지할수있나 해보는것<br>
BookTopia 세팅다되어있어서 MVware통째로 가져가야함 <br>

테이블 추가시 한글깨지면 242p참조<br>

※ 0314<br>

10.프로젝트v1.03 3개pdf , 프로젝트_파일목록.ex 4개가 세트<br>

화면 정의서:  고객이 사용하는 메뉴얼<br>
세무 회계 물류 부전공 필요함<br>
조별프로젝트의 핵심요소는 불편함 해소 로직화<br>
boot에서 카카오api연결 spring에서는 나중에<br>
구멍가게 코딩단<br>

○뒤로가기 문제 해결 256p<br>

★ 10이상 20미만을 sql에서 출력하는 방법<br>
select bno, title, content from(<br>
	select /*+INDEX_DESC(tbl_board pk_board) */<br>
	rownum rn, bno, title, content from tbl_board where rownum <=20)<br>
	where rn > 10;<br>

★ postman.com 깔아서 하는게 좋음<br>

317p까지 복습 8시간 67페이지 진행<br>


※ 0315<br>
자료 깃 공부 header master branch 공부하기<br>

BoardMapper BoardController BoardService, BoardSeviceImpl<br>
335p까지<br>
와차피디아<br>
게시글 삭제,공지사항,관리자페이지 , 영화<br>
○ 관리자페이지 > 웹페이지 선택 "와차최상단에 광고 넣는 탭 만들어보자<br>
1.좌측탭 최상단 배너관리 만들어보자<br>


부트스트랩 버전 5로<br>
cdn<br>

● 집에서 <br>
부트스트랩 사이트에서 그리드, 콘테이너, 네비게이션,오픈캔버스 보기,<br>

클래스보기<br>
프론트에 힘쓰지 않기<br>

★ .jsp 실행하려면 Controller에서 GetMapping()메소드 만들어야한다.<br>
adminSample.jsp 만들려고함<br>
와차adminSample 왼쪽탭 아이콘 만들어서 넣어보기<br>

완성된 예제에다가 주석달아놓기




#0318<br>
10-6mv 인텔리제이 프로젝트 파일<br>
★ xml의 <mapper namespace="org.zerock.mapper.BoardMapper">는 BoardMapper.java경로<br>

bannerList 테이블 출력하기

#0319<br>
관리자 페이지 목록,생성 페이지pdf 제작<br>

#0320<br>
관리자 페이지<br>
목록,생성 초벌 프론트 제작<br>

★ aws c언어 가져가기<br>

ex00으로 응용 톰켓연동하고 붙여넣기<br>
체크박스 값 어떻게 보낼지 생각해보기<br>
관리자페이지 디자인신경쓰지 않기<br>

멤버관리자 페이지는 나중에 만들기<br>
영화 리스트 DB연결완료<br>

#0321<br>
★ security 참고하기 부트용이라 위쪽만좀 틀리다.<br>
https://velog.io/@wooryung/Spring-Boot-Spring-Security%EB%A5%BC-%EC%A0%81%EC%9A%A9%ED%95%98%EC%97%AC-%EB%A1%9C%EA%B7%B8%EC%9D%B8-%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85-%EA%B5%AC%ED%98%84%ED%95%98%EA%B8%B0<br>

★<mapper namespace="com.firstgroup.movies.mapper.MoviesMapper"> 는 MoviesMapper(i).java이다<br>
selectKey keyProperty="movBno" 는 MovieVO의 변수 moveBno<br>
★ https://all-record.tistory.com/112<br>
util.Date는 오라클 날짜타입과 연동불가 /그런데 희진씨 sql.date 사용했는데 안됨 <br>

● MovieMapper > MovieServiceImpl.java > MovieServiceTests.java<br>

관리자 Controller만들기<br>
○ 인터페이스는 같이 사용<br>
○ Service는 DB끼리 섞어서 사용할떄 사용<br>
● MovieMapper(i) 의 getList() 매개변수 MovesVO로 변경<br>
●MovieServiceTests.java, AdminController 생성<br>

spring boot 할때 jsp사용안함 ajax사용안함 부트스트랩 안씀 바닐라 js사용안함<br>

내일214p작성하기<br>


#0322<br>
● 원격데스크톱 앱에서 사용하는방법<br>
찾기 > wf.msc > 인바운드 규칙 > 새규칙& tcp > 80 >이름 : 웹프로젝트포트 > 새로고침<br>
한번더  새규칙 > 3389 > 이름: 3389원격데스크톱<br>
암호를 잘걸어야한다.<br>
●찾기 > 컴퓨터관리 > 로컬사용자및 그룹 > 사용자 > mit 우클릭 > 암호설정 (진짜암호로)a650x<br>
우클릭 > 시스템 > 오른쪽에 원격 데스크톱 켬 ><br>
가상 머신(ex10-5) > 오른쪽클릭 setting > Network Adapter > Bridged : Connected<br>
하단 탭 네트워크클릭 > 오른쪽 어댑터 옵션 변경 >속성 >  (TCP/IPv4) ><br>
IP주소와 기본 게이트웨이의 111를 아니라<br>
IP주소는 		0.223 <br>
기본게이트 웨이는  0.1<br>
주소 수정하면 mv종료하기<br>
setting > Nestwork Adapter > Advanced... > a하단 MAC Address 의 Generator 몇번눌러주는 변경됨<br>
(MAC Address가 중복되면 해킹당할수도 있다.)<br>
>ok<br>
● 찾기 > 원격 데스크톱 연결 > ez304.iptime.org:3445<br>
아이디: mit  패스워드: a650x<br>

핸드폰 스토어에서 rdp 검색 Remote Desktop 설치<br>
pc name : ex304.iptime.org:전화번호4<br>
User Account : mit/pw<br>




★MoviesControllerTests.java안의 mockMvc.perform(MockMvcRequestBuilders.get("/board/list"))<br>
는 boardController.java @RequestMapping("/board/*")와 일치시켜야 한다.<br>
"/board/"는 매핑용 클래스 이름 "list"는 메소드 이름<br>

댓글은 restController로 ajax사용하려고만듬<br>

★ postman.com , Postman Interceptor깔아서 하는게 좋음 (선생님이 다시설명)<br>
크롬 추가 뿐만 아니라 exe다운로드도 해주어야한다.<br>
★.param("movBno", "2")의 movBno는 변수명 대소문자 구별해야한다.<br>

● MovieMapper(i) 의 getList() 매개변수 MovesVO로 변경<br>
●MovieServiceTests.java, AdminController 생성<br>

공지사항 페이지 만들기 백부터<br>
멤버 2개 섞어서<br>
192.168.0.224<br>

●다른사람들이 만든것 <br>
로그인 회원가입, 메일로 비밀번호 보내기, 파일업로드, 지도.api, 결제<br>
문의 게시판 문의종류 만들기<br>
★ 깃에 src와 pom.xml파일만 올리기<br>


4월5일까지<br>
공지사항페이지 만들기 ppt를 올려놓고 어떻게 만들었다를 올려놓는것까지 이사이트의 목표 ,erd<br>
취업담당자가 볼수있게 팀원, 자소서 작품등, 회원가입은 막기 회원가입에대한 내용은 ppt에 넣기<br>
딱2개만 넣기 일반계정의 패스워드를 게시 create는 이상한 댓글 사용못하게 막아놓고 적어놓기<br>

구멍가게 코딩단 security쪽 공부하기 옛버전이라 문제있어서 그렇다.<br>

★ 오라클 11g 에서 sequence 실행시 2번부터 생성될경우 sql에서 start with 0;를 붙이면 1부터 생성된다.<br>


#0325<br>
☆ BoardMapperTests클래스는 BoardMapper인터페이스의 구현체를 주입받아서 동작<br>
☆ mapper xml에서 select 태그의 id 속성값은 메서드의 이름과 일치하게 작성 <br>
 ☆ BoardService 인터페이스를 구현하는 구현체는 BoardServiceImpl이라는 클래스로 작성<br>
☆ @Service는 계층 구조상 주로 비즈니스 영역을 담당하는 객체임을 표시하기 위해사 용<br>
☆ BoardController는 BoardService 타입의 객체와 같이 연동해야 하므로 의존성에 대한 처리도 같이 진행한다.<br>
☆ControllerTests에서 security-context.xml가 아니라 servlet-context.xml 이어야한다 복붙할때 주의하기<br>
 @ContextConfiguration({
	  "file:src/main/webapp/WEB-INF/spring/root-context.xml",<br>
	  "file:src/main/webapp/WEB-INF/spring/servlet-context.xml" })<br>




카카오톡에 선생님이 올리신 주석 참고하기 꼼꼼하게 모르는 사람이 보더라도 알수있게<br>
한줄한줄 왜했는지 파라미터는 어떻게 받았는지 매개값은 무엇이고 어떤 컨트롤러로 가는지<br>

깃에 올리기 본인거에다가 계속 올려보기<br>

강사님 깃허브 security 토큰필요 spring> 브런치에 board Security > webapp > <br>
webinf > spring > securityContext.xml<br>
★Security는 jsp에 전부 연결해야해서 보통 jsp, java에다가 맨 나중에넣는다<br>
https://github.com/lonen8188/Spring/blob/Board%2BSecurity(%EC%A3%BC%EC%84%9D)/8.%20board(security)/src/main/webapp/WEB-INF/spring/security-context.xml<br>

https://wehagothelp.zendesk.com/hc/ko/articles/360000299861--%EA%B2%8C%EC%8B%9C%ED%8C%90-%ED%9A%8C%EC%82%AC%EA%B3%B5%EC%A7%80%EC%82%AC%ED%95%AD-%EB%93%B1%EB%A1%9D

#0326<br>
register.jsp실행시 405 Get 오류 발생할경우<br>
파일 업로드할때 에이젝스보내는 형식으로 하면된다. <br>

#0327<br>
notice/modify.jsp에서 notice/list.jsp로 되돌아가기 완료<br>

#0328<br>
01:07<br>
get.jsp rest방식으로 출력완료<br>
register rest방식으로 출력하게 작성중<br>
04:00 강사님에게 공지페이지 ajax로 작성하지말라고 조언받음, PostMapping문제가 도저히 해결 안되서 일단 팀프로젝트에서 분리하여 공지페이지 작성시작,<br>


★ 나중에 회원가입시 카카오톡 인증하는거해보기 <br>

쳇gpt 페이지에 코드 복여넣어보기 (회사에서는 사용하지 말것)<br>
☆ $ is not defined 오류 발생할 경우 jquery 코드 추가하기<br>
★ get.jsp에서 값을 화면에 출력할때 input을 사용하여 출력하는이유는 input재활용하기위해<br>


#0329<br>
☆ mappertest에서 되는데 controllerTest에서 오류 발생하면 Controller.java에 @Controller, @AllArgsConstructor 있는지 확인하기<br>
☆ get.jsp는 <form>태그 필요없음<br>
회사에서 spring사용 무조건사용하는거 회원가입, 게시판<br>
부트배우고나서 개인적으로 할사람 하고<br>
부트는 혼자해도 나온다.<br>

엑셀에 파라미터 발생하는거 다 써놓기<br>
붙일때 문제생기는 이유는 security문제 Controller의 메소드에 @PreAuthorize(~)박아버리기<br>
308p list페이지이동해결하기<br>


#0401
323p부터 파일목록문서화하기<br>

선택주문<br>
휴대폰케이구매<br>
주문정보<br>

회원가입<br>
로그인<br>
마이페이지<br>
비밀번호변경(유효성검사)<br>
배송지 관리(신규배송지관리)<br>

상품목록페이지 (비밀글)<br>

동영상으로 포폴넣을수 있으면 넣기<br>

서비스이용약관<br>
주소는 주소 api<br>
간편로그인 네이버,카카오<br>

공지페이지에 글이나 댓글작성하면 관리자가 알수있게작성<br>

delete누를경우 실제로 삭제하면 안된다.  필드에다가 false로 활성화 <br>
업데이트하여 게시물을 안보이게끔 부모키 있으면 삭제안된다.<br>

파일 업로드 만들고 레스트 방식으로 수정한 다음에 <br>
CommonRestController로 만든다<br>

★tml action경로 2개로 선언못한다.<br>
☆ Ajax방식 업로드할경우 jQuery이용하기<br>
★ 502page "FileList"는 F12 Console에서 볼수있다.<br>



★ 페이지 실행시<br>
Request method 'GET' not supported<br>
요청 행에 포함된 해당 메소드는, origin 서버에 의해 인지되었으나, 대상 리소스에 의해 지원되지 않습니다.)<br>
발생할경우 _csrf 붙이기 form안에 한줄만 붙이면 된다.<br>
"<input type="hidden" name="${_csrf.parameterName}" value = "${_csrf.token}"/><br>"

PageDTO.java대신 PageVO로 사용하기 <br>
☆DB용 이미지는 images폴더, 고정사용이미지는 img폴더<br>


#0402<br>
modify에서 수정하고 list로 돌아가서 목록 클릭하면 404에러뜨는거 모달 js코드 주석처리하던지<br>
보이게 수정하면 된다.<br>

교실바꾸는 이야기 5월1일 이동<br>
내일 오후 3시까지 댓글 완성하기<br>
일일 진행현황도 원래 해야한다.<br>


#0403 aws에다 오라클깔고 localhost해가지고 연동해보기<br>
★ 팀프로젝트 할때 jquery 버전 주의하기<br>
★ 웹get.jsp 에서 댓글 등록할때 405오류 발생하면 토큰있어야해서 그렇다.(security문제)
https://github.com/lonen8188/Spring/blob/master/8.%20board(security)/src/main/webapp/WEB-INF/views/board/get.jsp
에서 부족한거 채워넣기<br>
★modal 출력안되는건 보통 js에서 철자틀려서 그렇다.<br>
★ js에서  띄어씌기 남용하지 않기<br>


#0404<br>
부트가 좀더 안정적, 부트 수업7주일도 안함<br>

ppt, 파일정의서, aws게시<br>
ppt(일정관리, 조원소개 및 담당, UI설명, 기능설명)<br>
:프로젝트 하면서 느낀점, 향후 개선 점<br>
프로젝트하면서 느낀점은 로그인과 sequrity공부를 했었어야 했다.<br>

이력서 만들기<br>
aws에 올리는게 최종목적<br>

#0405<br>
프로젝트 마감<br>
1. 각자 코드에 주석 달고, 통합 마무리<br>
2. aws개인 서버에 프로젝트 등록, 게시해 볼것<br>
3. aws에 올린 내용 ppt에 추가할 것<br>
4. 주석 단 코드 git에 올리고 ppt에 링크 추가<br>
5. 프로젝트(ppt, xlsx, 소스파일)압축해서 조장이 lonen@n.com으로 보냄<br>

★get.jsp Security 문제있으면 선생님git참고하기<br>
★★ Cannot read properties of undefined (reading 'on') 오류 발생하면<br>
js의 메소드,객체 순서 정돈해보기<br>

순정js팝업버튼.txt 참조하기<br>
★aws에서 css깨질경우 resources/ 경로 확인해 볼것<br>


#학원졸업 0524 책에있는 에러설명위로로 작업
※ Tomcat으로 실행할 때 invalid loc header (bad signature) 메시지가 보이면서 정상적으로 실행되지 않는 경우 - 대부분 라이브러리문제, 다만 이 문제는 Tomcat쪽에 라이브러리가 제대로 처리되지 않아서 생기는 문제 .m에서 파일 삭제하면 대부분 해결됨
또는 Maven을 강제로 업데이트 해보자 프로젝트를 선택한 후 Maven 메뉴를 이용해서 Update Project를 선택

