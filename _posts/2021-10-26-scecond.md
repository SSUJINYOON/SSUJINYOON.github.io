**padding**: 요소의 '내부(안) 여백'을 지정[단축]

속성 값

|  값  |                의미                 | 기본값 |
| :--: | :---------------------------------: | :----: |
| 단위 |             px, em, em              |   0    |
|  %   | 부모 요소의 너비에 대한 비율로 지정 |        |

사용법

| padding: 위 우 아래 좌;<br />padding: 위 [좌, 우] 아래;<br />padding: [위, 아래] [좌, 우];<br />padding: [위, 아래, 좌, 우]; |
| ------------------------------------------------------------ |

| .box {<br />padding: 10px 20px 30px 40px<br />padding: 10px 20px 40px<br />padding: 10px 40px<br />padding: 10px<br />} |
| ------------------------------------------------------------ |

**padding-top**: 요소의 '내부(안) **위쪽** 여백'을 지정[개별]

**padding-bottom**: 요소의 '내부(안) **아래** 여백'을 지정[개별]

**padding-left**: 요소의 '내부(안) **왼쪽** 여백'을 지정[개별]

**padding-right**: 요소의 '내부(안) **오른쪽** 여백'을 지정[개별]



| .box1 {<br/>	padding: 10px 20px 30px 40px; /* 단축속성 */<br/>}<br/>.box2 {<br/>	/* 개별속성*/<br/>	padding-top: 10px;<br/>	padding-right: 20px;<br/>	padding-bottom: 30px;<br/>	padding-right: 40px;<br/>} |
| ------------------------------------------------------------ |

**크기 증가**: 추가된 padding 값만큼 요소의 크기가 커지는 현상.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="PoKmYyr" data-user="ssuni" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ssuni/pen/PoKmYyr">
  Untitled</a> by sujin (<a href="https://codepen.io/ssuni">@ssuni</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>



