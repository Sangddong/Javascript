# PM2 정리

### PM2란?
- PM2는 Node.js 애플리케이션을 관리하기 위한 **프로세스 매니저(Process Manager)** 
- 서버 환경에서 애플리케이션을 안정적으로 실행하고 관리할 수 있도록 함
### 주요 기능
- **무중단 실행 (Zero-Downtime)**  
  애플리케이션이 크래시되어도 자동 재시작
- **클러스터 모드 지원**  
  멀티코어 활용 가능 (`-i max`)
- **로그 관리**  
  `pm2 logs` 명령어로 stdout/stderr 로그 확인
- **모니터링**  
  CPU, 메모리 사용량 모니터링 가능 (`pm2 monit`)
- **배포 관리**  
  `pm2 deploy` 기능 제공
### 설치 방법
```bash
npm install pm2 -g

📌 주요 명령어
명령어	설명
pm2 start app.js	앱 실행
pm2 start app.js -i max	멀티코어 클러스터 모드 실행
pm2 list	실행 중인 프로세스 목록 보기
pm2 show <id>	특정 앱 상세 정보
pm2 logs	로그 확인
pm2 stop <id>	앱 중지
pm2 restart <id>	앱 재시작 (다운타임 발생)
pm2 reload <id>	무중단 재시작 (Zero-Downtime)
pm2 delete <id>	앱 삭제
pm2 save	현재 실행 상태 저장
pm2 startup	서버 재부팅 시 자동 실행 설정
📌 reload vs restart
명령어	특징
restart	앱을 중지 후 재실행 → 순간적인 다운타임 발생
reload	프로세스를 순차 교체 → 무중단 재시작

⚠️ 참고: reload는 클러스터 모드(-i)에서만 진정한 무중단 효과가 있습니다.

📌 예시
# 기본 실행
pm2 start app.js

# 앱 이름 지정
pm2 start app.js --name my-server

# 클러스터 모드 (CPU 코어 수만큼 실행)
pm2 start app.js -i max

# 무중단 재시작
pm2 reload all

# 로그 확인
pm2 logs my-server

📌 모니터링
pm2 monit


→ CPU, 메모리 사용량 실시간 확인 가능
