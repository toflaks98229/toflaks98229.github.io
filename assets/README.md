# 스크린샷 넣는 곳

## 현재 상태

영상이 있는 프로젝트는 **유튜브 썸네일이 자동으로 표시**되므로 이 폴더에 파일을 넣을 필요가 없습니다.
(썸네일은 `i.ytimg.com`에서 직접 불러오고, 클릭하면 그 자리에서 영상이 재생됩니다.)

| 프로젝트 | 상태 |
|---|---|
| ASCIIROG | ✅ 유튜브 영상 2개 |
| CarDrive | ✅ 유튜브 영상 2개 |
| Sandland | ✅ 유튜브 영상 1개 |
| 0MOJEON | ✅ 유튜브 영상 1개 |
| **RTXX** | ⬜ **비어 있음** — `rtxx.png` 필요 |
| **MX4** | ⬜ **비어 있음** — `mx4.png` 필요 |
| **SCPPJ** | ⬜ **비어 있음** — `scppj.png` 필요 |

## 이미지로 채우는 법

`index.html`에서 해당 프로젝트의 이 블록을 찾아,

```html
<div class="shot">
  <div class="placeholder"><b>▦</b>영상 · 스크린샷 자리<br>assets/rtxx.png</div>
</div>
```

아래처럼 바꿉니다. 이미지 파일은 이 폴더에 넣으면 됩니다.

```html
<div class="shot">
  <img class="still" src="assets/rtxx.png" alt="RTXX 전투 화면">
</div>
```

## 영상으로 채우는 법 (권장)

나중에 RTXX·MX4·SCPPJ 영상을 찍으면, 같은 블록을 **한 줄로** 바꾸면 끝입니다.
파사드 렌더링·썸네일·재생은 `index.html` 하단 스크립트가 알아서 처리합니다.

```html
<div class="shot" data-yt="영상ID" data-title="RTXX 플레이 영상"></div>
```

영상이 2개 이상이면 바로 아래에 전환 탭을 붙입니다 (ASCIIROG·CarDrive가 이 형태입니다).

```html
<div class="shot" data-yt="영상ID1" data-title="RTXX 플레이 영상"></div>
<div class="vidtabs" data-for="영상ID1">
  <button data-yt="영상ID1" aria-pressed="true">영상 1 · 대형 전투</button>
  <button data-yt="영상ID2" aria-pressed="false">영상 2 · 대형 재배치</button>
</div>
```

그리고 카드 하단 `.cta` 안에 유튜브 링크 버튼도 하나 추가해 주세요.

```html
<a class="btn" href="https://youtu.be/영상ID">유튜브에서 보기</a>
```

## 권장 사항

- **비율은 16:9.** 카드가 `aspect-ratio: 16/9`로 잡혀 있어서 다른 비율은 잘립니다.
- **정지 이미지보다 영상이 압도적으로 낫습니다.** 특히 RTXX의 대형 재배치는 *움직여야* 헝가리안 알고리즘이 무슨 일을 하는지 보입니다. 지금 비어 있는 3개 중 RTXX가 가장 아쉬운 자리입니다.
- 유튜브 영상은 **공개 또는 일부 공개(Unlisted)** 여야 합니다. 비공개면 썸네일도 재생도 안 됩니다.
