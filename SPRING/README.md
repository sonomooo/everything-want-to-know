Spring

- 스프링의 구동원리 

크게 컴파일 시점과 런타임 시점으로 구분할 수 있다. 이는 자바에서 스프링으로 넘어가는 흐름으로 이해하면 편하다.
우선 컴파일 시점에서 우리가 작성한 코드는 바이트 코드로 변환된다. 이때부터 OS와는 독립적인 코드로 움직인다.

변환된 바이트 코드는 JVM에서 ClassLoader를 통해서 JVM 메모리에 로드된다. 이 시점부터 JVM은 환경설정 등 본격적인 구동을 위해서 설정을 시작한다.
환경이 구축된다면 JVM은 구동을 시작한다.
JVM이 구동이 시작된다면 main() 메서드가 실행되는데 이는 SpringApplication.run()을 구동한다.

SpringApplication.run()이 실행되면 스프링은 컨테이너를 통해서 빈들을 등록하고, 의존성을 연결시킨다.
빈들을 등록하고 연결시키는 컨테이너의 일종으로는 SpringContext가 존재한다.

후에 컨텍스트가 완성이되면, 서버를 실행한다.

<img width="478" height="764" alt="image" src="https://github.com/user-attachments/assets/3efa358e-ee21-4359-a336-158c9db2fade" />
