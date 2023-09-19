# *코드 리뷰*

- 코더 : 정인호
- 리뷰어 : 이혁희

-----

- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 주어진 문제를 해결하는 완성된 코드가 제출 되었습니다.
    - 시작위치 = [0, 0], 목적지 = [4, 4]
    ```python
    # 시작 위치와 목적지 위치
    start_x, start_y = 0, 0
    end_x, end_y = 4, 4
    ```
    
    - 목적지를 찾았으면 '미로를 찾았습니다' 출력 후 리턴
    ```Python
        # 현재 위치가 목적지에 도착한 경우
        if x == end_x and y == end_y:
            print("미로를 찾았습니다")
            return True
    ```
    
    - 상하좌우로 움직일 수 있는 방향으로 탐색
    - 지나간 길은 '2'로 표시
    - 되돌아 갈 때 '0'으로 표시
    ```Python
        # 현재 위치에서 갈 수 있는 방향 탐색
        for dx, dy in [(0, 1), (1, 0), (0, -1), (-1, 0)]:
            nx, ny = x + dx, y + dy

            # 미로 범위(0,0 ~ 4,4) 내에 있고, 갈 수 있는 길(0)이며, 이미 방문하지 않은 길인 경우(2가 아닌 경우)
            if 0 <= nx < len(maze) and 0 <= ny < len(maze[0]) and maze[nx][ny] == 0:
                # 갔던 길 표시
                maze[nx][ny] = 2

                pendown()
                # 다음 위치로 이동
                goto(nx*10, ny*10)  # 거북이 다음 위치로 이동
                penup()

                if solve_maze(nx, ny):  # 재귀 호출
                    return True
                else:
                    # 다시 이전으로 돌아가기
                    goto(x*10, y*10)

                    # 표시된 길 0표시(지우기)
                    maze[nx][ny] = 0

        # 길을 찾지 못한 경우
        print("길을 찾을 수 없습니다")
        return False
    ```


- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 주석이 잘 작성되어 있습니다.
    
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 오류를 해결한 과정을 주석으로 남겼습니다.
    ```python
    # 첫 실행 후 오류발생#
    # Put clearscreen() as the first line in a cell (after the import command) to re-run turtle commands in the cell
    # ---------------------------------------------------------------------------
    # NameError                                 Traceback (most recent call last)
    # <ipython-input-10-a2665c7158f2> in <cell line: 20>()
    #      18 # 터틀 초기 설정
    #      19 window = (100, 100)
    # ---> 20 initializeTurtle(window, 'logo')
    #      21 speed(1)
    #      22

    # NameError: name 'initializeTurtle' is not defined

    # /////// 해결
    #import * 하니 제대로 실행됨."""
    ```
- [x]  **4. 회고를 잘 작성했나요?**
    - 회고를 잘 작성했습니다.

- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 코드가 간결하고 효율적입니다.
    - 변수가 범위안에 있는지 확인할 때 편리한 문법을 사용하였습니다. 좋은 방법 알게되어서 감사합니다.
    ``` 
    if 0 <= nx < len(maze) and 0 <= ny < len(maze[0]) and maze[nx][ny] == 0:
    ```
    
    - 문제 코드에서 "# 다시 이전으로 돌아가기"가 무슨 뜻인지 몰라서 작성을 안했는데 작성하신 코드를 보고 길을 못찾았을 때 돌아가는 것을 그리는 것이라는 것을 알았습니다. 감사합니다.
    ```python
                goto(x*10, y*10)
    ```
    - 그런데, pendown, penup하는 과정이 코드로 들어가야 할 것 같습니다.
    ```python
                pendown()
                goto(x*10, y*10)
                penup()
    ```
