# 기능 목록



## InputView
- 사용자가 입력한 값이 범위를 벗어날 경우, IllegalException을 발생시킨다.
- 사용자가 입력한 값을 return 시킨다(다리 사이즈, 게임 재시작 여부, 움직일 다리).


## OuputView

- 진행한 다리 사이즈만큼 출력한다.
- 성공/실패 여부를 출력한다.(단, 각각 method를 만들고, printResult에서 조건에 맞게 이를 호출한다.)
- 에러 메시지를 출력한다.

## BridgeCondition(Enum)

- 다리 상태에 따라, 유저에게 보여지는 형태(O,X), 데이터로 처리되는 형태(U, D), 입력을 처리하는 방법(0,1)에 대한 정보를 갖는다.

- 입력에 맞는 다리 오브젝트를 반환한다.

- 입력이 올바르지 않을 경우, IllegalException을 발생한다.

## BrideMaker

- size에 맞는 다리를 반환한다.(이 때, BridgeCondition Enum class를 이용한다.)

## BridgeGame

- 게임 전체 흐름을 담당하는 기능

- move() 메소드에서 사용자의 이동에 관한 기능을 처리
    - 실패나 성공했을 경우, 게임 재시작 여부에 관한 처리를 한다. 