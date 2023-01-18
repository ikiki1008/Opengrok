# About Opengrok 

![image](https://user-images.githubusercontent.com/80104121/213070832-b7f1a4b5-60e9-443e-9c98-5175865fc295.png)


### What Is Opengrok<br>

1) 웹 기반으로 소스를 탐색할 수 있는 툴
2) Java 등을 이용하여 구성 
3) 다양한 언어와 형상관리 툴들의 정보를 확인, 참조  
4) 코드를 써치하거나 참조를 하는데 도움이 되며 monotone, sccs, rcs, cvs, git 등 다양한 프로그램
파일 형식과 버전 제어 기록도 확인 가능
<br><br><hr><br><br>

### How does work

<br>
![image](https://user-images.githubusercontent.com/80104121/213072302-58b537b4-0692-4d86-ba68-6b0d06ff6a5f.png)

* <strong>src_root</strong><br>
인덱싱할 소스코드가 있는 곳입니다. 인덱싱할 소스코드 파일은 어디에 있던지 상관없고
색인할 때 위치를 지정 할 수 있습니다.

* <strong>opengrok jar</strong><br>
그림에서 보듯이 src_root 를 data_root 로 만들어 주는 jar 파일입니다.
opengrok 코드를 받아서 index 명령어를 실행하면 opengrok.jar 파일이 실행되는 구조입니다.

* <strong>data_root</strong><br>
데이타 루트는 인덱싱된 정보들이 들어있는 폴더의 위치입니다.
즉 인덱싱을 해야 생성이 되는 부분입니다.
src_root와 마찬가지로 위치를 지정할 수 있습니다.

* <strong>configuration.xml</strong><br>
색인 데이터에 관련된 기본 정보를 가지고 있습니다.
어떤 프로젝트를 넣어서 인덱싱 하기 전에 이 configuration xml 파일에서 해당 파일에 대한 정보만
수정해줍니다.

* <strong>source.war</strong><br>
web application 입니다. jsp와 서블릿으로 구성이 되있고
deploy 명령을 통해서 tomcat webapp 폴더 아래에 복사됩니다.
실제 사용자가 브라우저를 통해서 접근하면 톰캣에서 구동되어 동작하는 방식입니다.
<br><br><hr><br><br>


### How to Set up<br>
1) 자바 openjdk 11 이상
2) GlassFish 혹은 Tomcat 10 버전 이상
3) Universal Ctags
<br><br>

![image](https://user-images.githubusercontent.com/80104121/213072535-c15ac09b-3b9e-4b79-b707-3185a02fb207.png)
![image](https://user-images.githubusercontent.com/80104121/213072558-b179129d-7037-403f-8a30-c5acbe9152a9.png)
![image](https://user-images.githubusercontent.com/80104121/213072611-71a63a3f-6064-43bb-bb86-86672ea4b28c.png)
![image](https://user-images.githubusercontent.com/80104121/213072635-ed8d62ad-a243-41e7-8bd0-062fa591c379.png)
<br>
필자의 환경 구성 : 우분투 22.04 & Universal Ctags 5.9.0 & Openjdk 11.0.7 & Tomcat 10.0.6
<br><br><br>


![image](https://user-images.githubusercontent.com/80104121/213073159-1825d6ab-77e0-440f-899e-a115544aa9fd.png)
![image](https://user-images.githubusercontent.com/80104121/213073399-ded92c9c-8567-4f4a-991e-5bdb5a9aef2d.png)

<br><br><hr><br><br>
### Succeed set up and ready to use

<br><br> 
인덱싱이 끝나면 http://localhost:8080/source 로 들어가서 확인하기<br>
당연히 톰캣 켜서 들어가는 것 잊지말기
![image](https://user-images.githubusercontent.com/80104121/213073844-4a8e1508-8ea8-4641-88c1-e3d02fc17308.png)


