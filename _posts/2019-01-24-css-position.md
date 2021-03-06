---
layout: post
title: CSS - Position
tags:
  - CSS
---

position 속성은 웹 문서 안의 요소들을 자유롭게 배치해주는 속성입니다.

### 속성 값
* `static` (기본값) : 요소를 문서의 흐름에 맞추어 배치합니다.
* `relative` : 이전 요소에 자연스럽게 연결해 배치하되 위치를 지정할 수 있습니다.
* `absolute` : 원하는 위치를 지정해 배치합니다.
* `fixed` : 지정한 위치에 고정해 배치합니다.

속성 값 중 `static`을 제외한 나머지 속성 값에서는 좌표를 이용해 각 요소의 위치를 조절할 수 있습니다. 이때 위치는 `top`, `bottom`, `left`, `right`로 지정합니다. 

`top`이란 위쪽에서 얼마나 떨어져 있는지, `bottom`은 아래에서 얼마나 떨어져 있는지를 나타냅니다. 마찬가지로 `left`는 왼쪽에서 얼마나 떨어져 있는지, `right`는 오른쪽에서 얼마나 떨어져 있는지를 나타냅니다. 좌표값은 양수와 음수 모두 사용할 수 있습니다.

&nbsp;
#### 1. static - 문서의 흐름대로 배치하기
`static`은 position 속성의 기본값으로 요소를 나열한 순서대로 배치합니다.

&nbsp;
#### 2. relative - 문서 흐름 따라 위치 지정하기
`relative`도 `static`에서처럼 나열한 순서대로 배치되지만 `top`, `bottom`, `left`, `right`를 사용하여 좌표값으로 위치를 지정할 수 있습니다.

&nbsp;
#### 3. absolute - 원하는 위치에 배치하기
`absolute`를 사용하면 문서의 흐름과 상관 없이 `top`, `bottom`, `left`, `right`를 사용해 요소를 원하는 위치에 배치할 수 있습니다. 이때 기준이 되는 위치는 *가장 가까운 부모 요소*나 *조상 요소* 중 position 속성이 `relative`인 요소입니다. 그래서 `absolute`를 사용하려면 그 요소를 감싸는 `<div>`를 만들고 position을 `relative`로 지정해놓고 사용해야 합니다.

&nbsp;
#### 4. fixed - 브라우저 창 기준으로 배치하기
`fixed`도 `absolute` 처럼 문서의 흐름과 상관없이 위치를 좌표로 결정하지만 부모 요소가 아닌 *브라우저 창*이 기준이 됩니다. 브라우저 창의 왼쪽 위 꼭지점을 원점으로 두고 좌표값이 계산되며 한 번 배치되면 브라우저 창을 스크롤하더라도 계속 고정되어 표시됩니다.

&nbsp;

출처 : 고경희, HTML5 + CSS5 웹표준의 정석, 이지스 퍼블리싱