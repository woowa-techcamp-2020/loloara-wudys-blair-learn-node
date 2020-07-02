# 디버깅 관련해서 작성해보기
- [링크](https://github.com/woowa-techcamp-2020/loloara-wudys-blair-learn-node/blob/master/debugging.md)

# 워밍업: 벽돌깨기 es6 및 클래스화
- [과제 링크](https://github.com/woowa-techcamp-2020/woowa-honux/blob/master/week1-day2-new-js-mission.md#%EC%9B%8C%EB%B0%8D%EC%97%85-%EB%B2%BD%EB%8F%8C%EA%B9%A8%EA%B8%B0-%EA%B5%AC%ED%98%84%ED%95%98%EA%B8%B0)

## [기존 구조]
draw -> drawAll -> window.requestAnimationFrame(draw);

* window.requestAnimationFrame()
브라우저에게 수행하기를 원하는 애니메이션을 알리고 다음 리페인트가 진행되기 전에 해당 애니메이션을 업데이트하는 함수를 호출하게 합니다. 이 메소드는 리페인트 이전에 실행할 콜백을 인자로 받습니다.

## [새 구조]

[게임 클래스]
- 점수, 남은목숨, bricks, brickRowCount, brickColumnCount
- 충돌여부(collisionDetection)
- drawScore, drawLives
- drawAll

[볼 클래스]
- x, y, dx, dy
- drawBall(canvas)

[벽돌 클래스]
- brickWidth
- brickHeight
- brickPadding
- brickOffsetTop
- brickOffsetLeft

[패들 클래스]
- paddleHeight
- paddleWidth
- paddleX
- drawPaddle()
