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


★★프로젝트 생성시 처음 해야 할 것★★<br>
0. 이클립스 utf-8 인코딩변경 -> 폰트 설치(d2 Coding 폰트)설치하면 좋음 텍스트 파일오른쪽클릭 > 설치<br>
1. mvc 프로젝트 생성<br>
2. web.xml을 찾아서 톰켓 web.xml과 버전 일치<br>
3. pom.xml을 찾아서 버전 관리<br>
  - 스프링 버전 5버전 이후로 설정 12행<br>
  - jdk 버전 11버전 이후로 설정 (11, 141, 142행)<br>
4. 톰켓에 add -> 프로젝트 연결 -> 톰켓 더블클릭 -> Modules 탭에 / 컨텍스트패스(path, www) 확인<br>
5. 톰켓 start -> 크롬 -> http://ip주소:포트/컨텍스트루트명(www)<br>
 ->http://192.168.111.105/www (초기화면 나옴)<br>
6. 오라클 설치 -> 포트번호 1521 -> system/oracle<br>
-> cmd -> sqlplus system/oracle<br>
-> 사용할 계정 생성, 권한 부여 (이클립스에 있는 dataSource exp를 활용)<br>
7. 프로젝트에 ojdbc8.jar 연결<br>
 -> 프로젝트 우클릭 -> Build Path -> Libaries -> Classpath : add <br>
 -> Web DeploymentAssembly 확인 (DeploymentAssembly > add > java Build Path Entries클릭해서 진입하면 jdbc8있음 선택하고 close
Project Explorer 에서 ojdbc8.jar있는지 확인<br>



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
