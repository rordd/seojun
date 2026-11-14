# 서준이 영상

좋아하는 유튜브 영상의 **원하는 구간만** 모아서 차례로(반복) 틀어주는 웹 앱.
윈도우(크롬/엣지)와 아이패드(Safari)에서 같은 주소로 쓰고, 목록은 자동으로 동기화된다.

- 영상은 다운로드하지 않고 유튜브 공식 플레이어로 재생한다.
- 목록은 이 저장소의 `clips.json` 파일에 저장된다. 모든 기기가 이 파일을 읽는다.
- 목록을 바꾸는 기기에만 GitHub 토큰(동기화 키)이 필요하다. 보기만 하는 기기는 필요 없다.

## 처음 설정 (한 번만)

### 1. GitHub Pages 켜기
저장소 **Settings → Pages → Build and deployment**
- Source: `Deploy from a branch`
- Branch: `main` / `/ (root)` → **Save**

1~2분 뒤 주소: `https://rordd.github.io/seojun/`

### 2. 동기화 키 만들기 (목록을 편집할 기기용)
GitHub 오른쪽 위 프로필 → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**
- Token name: `seojun`
- Expiration: 원하는 기간 (만료되면 새로 만들어 다시 넣으면 된다)
- Repository access: **Only select repositories → `rordd/seojun`**
- Permissions → Repository permissions → **Contents: Read and write**
- **Generate token** → `github_pat_...` 복사

앱의 **목록 편집 → 자동 동기화 → 동기화 키**에 붙여넣고 저장.

### 3. 아이패드
Safari로 주소를 열고 **공유 → 홈 화면에 추가**.

## 사용법
1. **목록 편집** → 유튜브 링크 붙여넣기 → **불러오기**
2. 위 화면에서 영상을 보다가 **지금 → 시작**, **지금 → 끝** (또는 `12:10` 처럼 직접 입력)
3. **목록에 추가** → 1분 안에 다른 기기에도 반영된다 (앱을 다시 열면 바로)
4. **재생 목록** 탭에서 ▶ 재생.

### 반복
- 반복 버튼을 누를 때마다 바뀐다: **🔁 전체 반복**(목록 끝나면 처음부터) → **🔂 한 개 반복**(지금 구간만 계속) → **➡ 한 번만**(목록 끝에서 멈춤)
- 구간마다 **반복 횟수**(1~20)를 정할 수 있다. 예: 3이면 그 구간을 3번 연달아 틀고 다음으로.

## 참고
- 아이패드는 처음 한 번은 ▶를 직접 눌러야 재생된다(애플 자동재생 제한).
- 유튜브 광고는 일반 유튜브처럼 나올 수 있다.
- 저장소가 공개라서 `clips.json`(영상 목록)은 누구나 볼 수 있다. 토큰은 각 기기 브라우저에만 저장된다.
