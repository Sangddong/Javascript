# AES

### 1. AES 개요
- AES란
- 개발 배경 및 필요성 (DES → AES로의 전환)
- 주요 특징

### 2. AES 알고리즘 구조
- 블록 암호(Block Cipher) 개념
- 블록 크기와 키 길이 (128, 192, 256비트)
- 라운드 수와 키 크기의 관계

### 3. 암호화 과정(Encryption Process)
- SubBytes 단계
- ShiftRows 단계
- MixColumns 단계
- AddRoundKey 단계

### 4. 복호화 과정(Decryption Process)
- Inverse SubBytes
- Inverse ShiftRows
- Inverse MixColumns
- AddRoundKey

## 5. 키 스케줄링(Key Expansion)
- 라운드 키 생성 원리
- S-box와 Rcon의 역할
   * 
   * 

### 6. AES의 보안성
- 알려진 공격 기법과 AES의 대응
- 안전성이 검증된 이유
- 양자 컴퓨팅과 AES

7. AES의 활용 분야
- SSL/TLS
- VPN, IPsec
- 파일 및 데이터베이스 암호화
   * 
   * 
   * 
   * 

8. AES 구현

   * 하드웨어 구현 vs 소프트웨어 구현
   * 성능 최적화 기법
   * 라이브러리/프레임워크 예시

9. AES와 다른 암호 알고리즘 비교

   * DES, 3DES와의 비교
   * 대칭키 암호 vs 비대칭키 암호
   * 실제 서비스에서의 적용 사례

10. 정리 및 향후 전망

    * AES의 현재 표준 지위
    * 향후 대체 가능성 (Post-Quantum Cryptography와의 연계)
