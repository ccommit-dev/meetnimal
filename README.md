![meetnimal](https://github.com/ccommit-dev/meetnimal/assets/77635521/ed1947f9-ce22-4cb8-b594-71b2419866e6)
# meetnimal
애견 커뮤니티 프로젝트

- 동물을 사랑하는 사람들끼리의 만남을 위한 최소한의 준비 / 극대화된 즐거움
- 밋니멀에 대한 단어 의미 및 현재 모임 및 커뮤니티 만남을 위한 간소화 비교
- 애완동물이 있는 사람들과의 가벼운 만남/소통(나이/정보 등을 구분할 수 없음, 이성 여부는 고민 필요)이므로 가족과 같은 애완동물과 동행 및 이를 이해해줄 수 있는 사람들끼리 만남을 즉각 선별 가능
- 국내외를 구분하지 않고 만날 수 있어 다양한 동물/사람들과의 소통을 통해 즐거움을 선사
- 가벼운 소통 > 실제 만남 > 지속적인 커뮤니케이션이 지속 가능할 수 있도록 NFT 보상 지급/순환 구조 마련
-  실제 만남/소통을 통해 겪게된 재미있는(또는 신기한) 경험들을 컨텐츠로 소화(만화,쇼츠 등)
- 만남 이외에 애완동물과의 추억(사진/영상/산책코스)을 기억할 수 있는 기능들을 추가하여 밋니멀 앱 하나로 모든걸 다 해결할 수 있는 구조의 생태계로 확장
<details>
<summary>기획</summary>
<div markdown="1">
- 로딩 화면(진입 시 배경 화면)
</div>
<div>
- 메인 화면(구체적인 UI 구성에 대한 논의 필요) 
</div>
<div>
- 채팅/영상 통화 기능(사진/동영상 공유 기능)
</div>
<div>
- 프로필 기능
</div>
<div>
- AI를 이용한 애완동물 유형별 퀘스트 생성/NFT 지급
</div>
</details>

 
# 개발 스텍
- 실시간 통신: WebRTC
- 실시간 메시징: MQTT
- 보안 및 인증: JSON Web Tokens (JWT)
- 프로그래밍 언어: Java
- AI 모델 서빙: TensorFlow Serving
- 블록체인: Ethereum
- 비즈니스 로직 서버: Spring Boot (Java)
- 데이터베이스: Mysql
- 메시지 브로커: RabbitMQ

# 서버 구조도
-  WebSocket 서버 (Spring Boot - Java): 실시간 채팅 및 영상 통화 기능 제공.
	-  WebSocketConfig를 통해 WebSocket 통신 설정.
	-  ChatController를 통해 채팅 및 영상 통화 기능 구현.

-  API 서버 (Spring Boot - Java): 메인 화면 및 기타 비즈니스 로직을 담당.
	-  RESTful API를 통해 클라이언트와 통신.
	-  서비스 간 통신을 위한 마이크로서비스 아키텍처 도입.

-  AI 서버 (Spring Boot - Java): 애완동물 퀘스트 생성을 위한 AI 모델 서빙.
	-  AIModelService를 통해 퀘스트 설명을 생성.

-  블록체인 서버 (Spring Boot - Java): NFT 발행 및 관리를 위한 블록체인 서비스.
	-  NFTService를 통해 NFT 생성 및 사용자에게 지급.

-  데이터베이스 (Mysql):
	-  메인 화면에서 사용할 데이터 저장.
	-  유저 정보, 애완동물 정보, NFT 정보 등을 저장.

-  미디어 서버 (FFmpeg): 채팅/영상 통화에서 사용할 미디어 서버.
	-  사진 및 동영상 공유 기능 제공.

-  메시지 브로커 (RabbitMQ):
	-  비동기 통신을 위한 메시지 브로커.
	-  애완동물 퀘스트 생성과 NFT 지급 관련 이벤트 처리에 사용.


