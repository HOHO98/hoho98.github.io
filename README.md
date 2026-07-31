# 오키나와 여행 가이드

2026년 8월 1~5일 오키나와 여행용 단일 페이지 가이드입니다.

---

## 🚀 GitHub Pages 에 올리기

### 1. 저장소 만들기

1. [github.com](https://github.com) 로그인 → 오른쪽 위 **`+`** → **New repository**
2. **Repository name** 에 이름을 입력합니다 (예: `okinawa`)
   → 나중에 주소가 `https://아이디.github.io/okinawa/` 가 됩니다
3. **Public** 을 선택합니다
   ⚠️ Private 으로 만들면 무료 계정에서는 Pages 가 동작하지 않습니다
4. 아래 체크박스(`Add a README file` 등)는 **전부 해제**한 채로 **Create repository**

### 2. 파일 올리기

만들어진 빈 저장소 화면에서 **`uploading an existing file`** 링크를 누릅니다.
(안 보이면 **Add file → Upload files**)

이때 **`site` 폴더 자체가 아니라, 폴더를 열고 그 안의 내용물을 올려야 합니다.**

```
올릴 것 ○            올리면 안 되는 것 ✗
├── index.html       └── site 폴더 통째로
├── images/  (폴더째 끌어다 놓기)
└── README.md
```

- 파인더/탐색기에서 `site` 폴더를 **열고**, 안에 있는 `index.html` · `images` · `README.md` 를
  브라우저 창으로 **끌어다 놓으세요.**
- 사진이 210장이라 올라가는 데 1~3분 걸립니다. 진행 표시가 끝날 때까지 기다리세요.
- 다 올라오면 아래 **Commit changes** 를 누릅니다.

> `.nojekyll` 이라는 파일도 들어 있는데, 점으로 시작해서 안 보일 수 있습니다.
> 없어도 이 페이지는 정상 동작하니 신경 쓰지 않아도 됩니다.

### 3. Pages 켜기

1. 저장소 위쪽 **Settings** → 왼쪽 메뉴 **Pages**
2. **Source** 를 `Deploy from a branch`
3. **Branch** 를 `main` / 폴더는 `/ (root)` 로 두고 **Save**
4. 1~2분 뒤 새로고침하면 위쪽에 주소가 나옵니다
   → `https://아이디.github.io/저장소이름/`

### 4. 확인

주소를 휴대폰으로 열어보세요. 처음 열면 **사용법 안내가 자동으로 뜹니다.**

- 화면이 안 나오고 파일 목록만 보이면 → `index.html` 이 저장소 **최상단**에 있는지 확인하세요.
  (`site/index.html` 처럼 한 단계 안에 들어가 있으면 안 됩니다)
- 사진이 안 보이면 → `images` 폴더가 `index.html` 과 **같은 위치**에 있는지 확인하세요.

---

## ⚠️ 올린 뒤에 꼭 할 것

### 구글맵 API 키 제한하기

지금은 키가 아무 사이트에서나 쓸 수 있는 상태입니다. 남이 가져다 쓰면 요금이 청구될 수 있습니다.

1. [Google Cloud Console → 사용자 인증 정보](https://console.cloud.google.com/apis/credentials)
2. 사용 중인 키 클릭 → **애플리케이션 제한사항** → **HTTP 리퍼러**
3. 항목 추가: `https://아이디.github.io/*`
4. 저장

### https 로 열기

위치 정보, 유튜브 재생, 구글맵은 파일을 직접 여는(`file://`) 방식에서는 동작하지 않습니다.
GitHub Pages 는 자동으로 https 라서 올리고 나면 전부 살아납니다.

---

## 📝 내용 고치기

`index.html` 을 메모장이나 VS Code 로 열면 위쪽에 `const DATA = { ... }` 가 있습니다.
**그 안이 전부 내용이고, 아래쪽은 화면을 그리는 코드**입니다.

| 고치고 싶은 것 | 찾을 위치 |
|---|---|
| 숙소가 바뀌었다 | `memoLinks.hotelQuery` |
| 렌터카 예약처 링크 | `memoLinks.rentalUrl` |
| 장소 추가·수정 | `spots` 배열 (`lat`/`lng` 를 넣으면 지도와 근처 추천에 자동 반영) |
| 회화 표현 추가 | `talkBlocks` 안의 `phrases` |
| 파란 상자 요약 항목 | `hero` / `driveHero` / `talkHero` 의 `stats` |

고친 뒤에는 GitHub 저장소에서 `index.html` → 연필 아이콘 → 수정 → **Commit changes** 하면
1분 안에 반영됩니다.

---

## 💾 저장되는 것

별표·메모·단어장·퀴즈 기록은 **브라우저에만** 저장됩니다.
서버로 보내지 않으니 안전하지만, **기기를 바꾸거나 브라우저 데이터를 지우면 사라집니다.**

여행 전에 한 번 **설정(⚙︎) → 백업 · 옮기기 → 복사하기** 를 눌러 두세요.
새 기기에서 **붙여넣기** 하면 그대로 돌아옵니다.

---

## 📷 사진 저작권

`images/p/` 에는 웹에서 수집한 사진이 섞여 있습니다.
공개 저장소로 올릴 계획이라면 각 시설 공식 이미지나 무료 소스(Unsplash, Pixabay)로
교체하는 편이 안전합니다.

---

<div align="center">

**HOHO**
*One Man Can Make A Difference.*

</div>
