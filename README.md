# emperors.cc v18 Multi-Page - 150페이지 분산

## 파일 구조
- index.html (허브 6.9KB) - 양력/음력/윤달/출생지 입력 + 목차
- chapter-0.html (왜 8글자 부족? 25p)
- chapter-1.html (연주 OS 20p)
- chapter-2.html (월주 일하는 방식 22p)
- chapter-3.html (일주 본캐 30p) - 핵심
- chapter-4.html (시주+분주 30p)
- chapter-5.html (명궁 20p)
- chapter-6.html (종합 35p)
총 150페이지 이상

## 배포 명령어

### GitHub Pages 배포
```bash
# 1. emperors-cc 폴더로 이동
cd emperors-cc

# 2. 파일 확인 (8개 있어야 함)
ls -lh index.html chapter-*.html

# 3. git 초기화 (처음이면)
# git init
# git remote add origin https://github.com/너의아이디/emperors-cc.git

# 4. 파일 추가 (중요! 챕터 전체 포함)
git add index.html chapter-0.html chapter-1.html chapter-2.html chapter-3.html chapter-4.html chapter-5.html chapter-6.html

# 또는 간단히
git add .

# 5. 커밋
git commit -m "v18 multi-page: 150p 분산, 양력음력윤달출생지, 허브+7챕터"

# 6. 푸시
git push origin main
# main 아니면: git push origin master

# 7. 1-2분 후 확인
# https://너의아이디.github.io/emperors-cc/
# https://너의아이디.github.io/emperors-cc/chapter-0.html
# https://너의아이디.github.io/emperors-cc/chapter-3.html
```

### 로컬 테스트
```bash
# Python 간단 서버
python -m http.server 8000
# 브라우저에서 http://localhost:8000 접속
```

### Vercel/Netlify 배포
- 폴더 그대로 드래그 앤 드롭
- 또는 GitHub 연결하면 자동 배포

## 이전 버그 수정
- v16: 15줄 요약만 저장 (1페이지 버그)
- v18: 15,000자+ 전체 저장 + 멀티 페이지로 소스 분량 해결
