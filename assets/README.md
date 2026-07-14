# 스크린샷 넣는 곳

`index.html`의 각 프로젝트 카드에는 지금 이런 플레이스홀더가 들어 있습니다.

```html
<div class="shot">
  <!-- 스크린샷 교체: <img src="assets/rtxx.png" alt="RTXX 전투 화면"> -->
  <div class="placeholder"><b>▦</b>스크린샷 자리<br>assets/rtxx.png</div>
</div>
```

이미지를 이 폴더에 넣고, 위 블록을 아래처럼 바꾸면 됩니다.

```html
<div class="shot">
  <img src="assets/rtxx.png" alt="RTXX 전투 화면">
</div>
```

## 필요한 파일

| 파일명 | 프로젝트 |
|---|---|
| `rtxx.png` | RTXX |
| `asciirog.png` | ASCIIROG |
| `mx4.png` | MX4 |
| `sandland.png` | Sandland |
| `scppj.png` | SCPPJ |
| `0mojeon.png` | 0MOJEON |

## 권장 사항

- **비율은 16:9**로 맞춰 주세요 (카드가 `aspect-ratio: 16/9`로 잡혀 있습니다). 1920×1080 또는 1280×720이면 충분합니다.
- **GIF가 정지 이미지보다 훨씬 낫습니다.** 특히 RTXX의 대형 재배치, ASCIIROG의 화재 전파, MX4의 얼룩 지우기는 *움직여야* 무엇이 대단한지 전달됩니다. `<img>` 태그는 GIF도 그대로 받습니다.
- GIF는 용량이 커지기 쉬우니 5~8초, 10MB 이하를 권합니다. 더 길게 담고 싶으면 mp4로 만들어 `<video autoplay muted loop playsinline>`으로 바꾸는 것도 방법입니다.
- 게임 화면이 어두운 편이라면, 카드 배경과 구분되도록 밝은 장면을 고르는 게 좋습니다.
