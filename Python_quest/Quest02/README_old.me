# *코드 리뷰*

- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - turtle 패키지 설치가 되지 않아서 결과물이 출력되지 않았습니다.
    - turtle 패키지 관련 코드를 제외하고 실행하면 미로를 찾아가는 로직은 잘 작동합니다.
        - turtle 패키지 참조를 지운 코드
```python
#from turtle import Turtle, Screen

maze = [
    [0, 1, 0, 0, 0],
    [0, 0, 0, 1, 0],
    [0, 1, 1, 0, 0],
    [0, 0, 1, 1, 0],
    [0, 0, 0, 0, 0],
]

# 시작 위치와 목적지 위치
start_x, start_y = 0, 0
end_x, end_y = 4, 4

#window = Screen()
#window.setup(width=300, height=300)

#t = Turtle()
#t.speed(1)
#t.showturtle()


def solve_maze(x, y):
    if x == end_x and y == end_y:
        print("미로를 찾았습니다")
        return True

    if 0 <= x < 5 and 0 <= y < 5 and maze[y][x] == 0:
        maze[y][x] = 2  # 갔던 길
        #t.goto(x * 10 + 5, y * 10 + 5)  # 거북이 다음 위치로 이동
        #t.pendown()
        #t.goto(x * 10 + 5, y * 10 + 5)
        #t.penup()

        # 다음 위치로 이동
        if (
            solve_maze(x + 1, y)
            or solve_maze(x, y + 1)
            or solve_maze(x - 1, y)
            or solve_maze(x, y - 1)
        ):
            return True

        # 돌아가기
        #t.goto(x * 10 + 5, y * 10 + 5)
        #t.pendown()
        #t.goto(x * 10 + 5, y * 10 + 5)
        #t.penup()
        maze[y][x] = 0  # 표시된 길 지우기

    return False


# 시작 위치에서 미로 찾기 시작
#t.penup()
#t.goto(start_x * 10 + 5, start_y * 10 + 5)
solve_maze(start_x, start_y)
#window.update()
#window.mainloop()
import pprint
pprint.pprint(maze)

### 코드 실행결과
# 미로를 찾았습니다
# [[2, 1, 2, 2, 2],
#  [2, 2, 2, 1, 2],
#  [0, 1, 1, 0, 2],
#  [0, 0, 1, 1, 2],
#  [0, 0, 0, 0, 0]]
```



- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 주석이 별로 없지만 코드만으로도 로직이 이해되게 작성했습니다.
    
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - ColabTurtlePlus 패키지 설치가 안되어서 여러가지 문제해결을 시도해 보신 것 같습니다.
    - 문서화 되어 있지는 않습니다.
    - ColabTurtlePlus 패키지 설치 방법은 다음과 같습니다.
        - 다음 코드를 쥬피터 노트북에 새로운 셀을 만들어서 복사합니다.
        - 셀을 실행합니다.
    ```
    !pip install ColabTurtlePlus # ColabTurtle 라이브러리 설치
    ```
    
- [x]  **4. 회고를 잘 작성했나요?**
    - 회고를 잘 작성했습니다.

- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 변수가 범위안에 있는지 확인할 때 편리한 문법을 사용하였습니다. 좋은 방법 알게되어서 감사합니다.
    ``` 
    if 0 <= x < 5 and 0 <= y < 5 and maze[y][x] == 0:
    ```
    
    - 문제의 코드 템플릿은 for문 안에서 현위치(x,y)를 갔던 길로 표시했다 지웠다를 반복하는데, 이 코드에서는 현위치를 갔던 길로 표시하고 다음 위치 이동을 모두 시도해 본 후 실패하면 현위치를 안갔던 길로 표시합니다. 상식에 더 맞는 방법이라 생각합니다.
    ```python
       if 0 <= x < 5 and 0 <= y < 5 and maze[y][x] == 0:
        maze[y][x] = 2  # 갔던 길
        t.goto(x * 10 + 5, y * 10 + 5)  # 거북이 다음 위치로 이동
        t.pendown()
        t.goto(x * 10 + 5, y * 10 + 5)
        t.penup()

        # 다음 위치로 이동
        if (
            solve_maze(x + 1, y)
            or solve_maze(x, y + 1)
            or solve_maze(x - 1, y)
            or solve_maze(x, y - 1)
        ):
            return True

        # 돌아가기
        t.goto(x * 10 + 5, y * 10 + 5)
        t.pendown()
        t.goto(x * 10 + 5, y * 10 + 5)
        t.penup()
        maze[y][x] = 0  # 표시된 길 지우기
    ```
    
    
    - maze[x][y]를 maze[y][x]로 행열을 바꾸었는데, maze를 참조하는 모든 expression에서 일관성 있게 바뀌어 있어서 제대로 작동은 했습니다. 하지만, 코드를 읽는데 어려움이 있었습니다.
