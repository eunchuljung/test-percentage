# Vercel 배포 가이드

## 📋 현재 파일 구조
```
프로젝트/
├── index.html              # 메인 페이지 (테스트 목록)
├── love-test.html          # 연애 호구력 테스트
├── work-test.html          # 직장 욕먹을 확률 테스트
├── relationship-test.html  # 인간관계 밀림 테스트
├── spending-test.html      # 충동소비 지수 테스트
├── sns-test.html          # SNS 중독 위험도 테스트
└── vercel.json            # Vercel 설정 파일
```

## ✅ Vercel 배포 준비 완료

### 왜 Vercel이 적합한가?
1. **무료 플랜으로 충분**
   - 정적 파일 호스팅
   - 무제한 대역폭
   - 자동 HTTPS
   - CDN 자동 적용

2. **배포가 쉬움**
   - GitHub 연동 시 자동 배포
   - CLI로 간단 배포 가능
   - 미리보기 URL 자동 생성

3. **성능 최적화**
   - 전 세계 CDN
   - 자동 이미지 최적화 (필요시)
   - 빠른 로딩 속도

## 🚀 배포 방법 (3가지)

### 방법 1: Vercel CLI (가장 빠름)
```bash
# 1. Vercel CLI 설치
npm install -g vercel

# 2. 프로젝트 폴더로 이동
cd /경로/to/프로젝트

# 3. 배포 (처음 실행 시 로그인 필요)
vercel

# 4. 프로덕션 배포
vercel --prod
```

### 방법 2: GitHub 연동 (추천)
1. GitHub에 레포지토리 생성
2. 프로젝트 파일 업로드
3. Vercel 웹사이트(vercel.com) 접속
4. "Import Project" 클릭
5. GitHub 레포지토리 선택
6. "Deploy" 클릭
   - Framework Preset: Other
   - Root Directory: ./
   - Build Command: (비워둠)
   - Output Directory: (비워둠)

### 방법 3: Vercel 웹 UI (드래그앤드롭)
1. vercel.com 접속 및 로그인
2. "Add New" → "Project" 클릭
3. 파일 전체를 드래그앤드롭
4. "Deploy" 클릭

## 📝 배포 후 체크리스트

### 필수 확인 사항
- [ ] 모든 페이지 정상 작동
- [ ] 테스트 간 이동 링크 작동
- [ ] 이미지 저장 기능 작동
- [ ] 모바일 반응형 확인

### 선택 확인 사항
- [ ] Google Analytics 추가 (향후)
- [ ] 카카오 개발자 등록 후 공유 기능 연동
- [ ] Google AdSense 계정 생성 후 광고 추가
- [ ] 커스텀 도메인 연결 (향후)

## 🔧 배포 후 수정 방법

### GitHub 연동한 경우
1. 로컬에서 파일 수정
2. Git commit & push
3. 자동으로 재배포됨 (1-2분 소요)

### CLI 사용한 경우
1. 파일 수정
2. `vercel --prod` 재실행

## 💡 다음 단계 제안

### 1단계: MVP 테스트
- 배포 후 지인들에게 공유
- 실제 사용자 피드백 수집
- 버그 확인 및 수정

### 2단계: 수익화 준비
- Google AdSense 신청
  - 사이트에 최소 10개 페이지 필요
  - 최소 1-2주 정도 운영 후 신청 권장
- 광고 배너 영역에 AdSense 코드 추가

### 3단계: 확장
- 테스트 추가 생성 (5개 → 10개 → 20개)
- 공유 횟수 추적
- A/B 테스트 (질문/결과 개선)

## 🐛 자주 발생하는 문제

### 문제 1: 404 에러
- 해결: vercel.json 파일이 제대로 업로드되었는지 확인

### 문제 2: 페이지 이동 안 됨
- 해결: 파일명이 정확한지 확인 (대소문자 구분)

### 문제 3: 이미지 저장 안 됨
- 해결: html2canvas 라이브러리 로딩 확인 (CDN 정상 작동 확인)

## 📞 도움이 필요하면
- Vercel 공식 문서: https://vercel.com/docs
- Vercel Discord 커뮤니티
- 또는 나에게 다시 물어보기!
