# JADE NARE · 옥조각 창작소 종합 계산기 (PWA)

설치형 웹앱(PWA) 번들입니다. 브라우저에서 열면 "홈 화면에 추가"로 앱처럼 설치됩니다.

## 파일
- `index.html` — 앱 본체 (모든 CSS/JS 내장)
- `manifest.json` — 앱 이름·아이콘·테마 설정
- `sw.js` — 오프라인 캐시(서비스워커)
- `icons/` — 192/512/마스커블/애플터치 아이콘

## 배포 (HTTPS 필요)
서비스워커는 `https://` 또는 `localhost`에서만 동작합니다. `file://`로 열면 앱은 되지만 설치·오프라인은 안 됩니다.

1. **Netlify Drop** — https://app.netlify.com/drop 에 이 폴더를 통째로 끌어다 놓으면 끝. 발급된 주소를 휴대폰에서 엽니다.
2. **GitHub Pages** — 저장소에 폴더를 올리고 Settings → Pages → Branch(main / root) 지정.
3. **로컬 테스트** — 이 폴더에서 `python3 -m http.server 8080` 실행 후 `http://localhost:8080`.

## 설치
- **Android(Chrome)**: 우측 상단 ⋮ → "앱 설치" 또는 "홈 화면에 추가"
- **iOS(Safari)**: 하단 공유 → "홈 화면에 추가" (iOS는 Safari만 지원)
- 앱 안의 「앱으로 설치」 버튼도 같은 동작을 안내합니다.

## 참고
- 오프라인에서도 계산은 모두 동작합니다.
- 기본 단가 환율은 최초 1회 온라인 조회 후 캐시되며, 오프라인에서는 기본값(192)으로 계산됩니다.
- PNG 저장(html2canvas)은 최초 1회 사용 후 캐시되어 오프라인에서도 동작합니다.
- 내용 수정 시 `sw.js`의 `VER` 값을 바꾸면 기기에 새 버전이 반영됩니다.
