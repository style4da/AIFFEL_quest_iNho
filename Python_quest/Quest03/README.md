# Quest 03. Avengers 2-gram


```

다음 조건을 확인하여 Avengers Script에서 워드 단위의 2-gram을 구하고,  
Script에서 가장 빈도가 높은 2-gram 페어를 찾아라!  
조건 : Avengers.txt 파일을 사용한다.  
      모든 문자는 소문자로 변환한다.(string 다루는 메서드 참고)  
      모든 기호는 제거(정규표현식 참고)한 후, 2-gram을 구한다.  

```

- 난이도 : 🟡🟡🟡⚪⚪  
- 장르 :  내장함수 String, Collections, n-gram

## Peer Review

- 코더 :  정인호
- 리뷰어 :  김연


```
import re

# 파일을 읽고 소문자로 변환하여 text 변수에 저장
with open('06TheAvengers.txt', 'r', encoding='utf-8') as file:
  text = file.read().lower()

# 기호를 제거하고 zip()으로 단어를 분할
words = re.findall(r'\b\w+\b', text)
ngram = zip(words, words[1:])

ngram_dict = {}                # 빈 딕셔너리 생성
# 2-gram이므로 문자열 끝에서 한 글자 앞까지만 반복
# scrpit를 돌면서 2-gram 형식으로 출력하되 신규는 1로 생성
# 신규가 아닌 것들은 누적합
for i in range(len(words) -1):
  gram = (words[i], words[i + 1])
  if gram in ngram_dict :
    ngram_dict[gram] += 1
  else :
    ngram_dict[gram] = 1

# 가장 높은 빈도수 찾기
max_2gram = max(ngram_dict, key=ngram_dict.get)
ngram_frequency = ngram_dict[max_2gram]
#sorted_ngram = sorted(ngram_dict.items(), key=lambda x : x[i], reverse=True)

print('입력값 : \n'+ '06TheAvengers.txt')
print()
print('출력값: ')
print('max2gram:', max_2gram, ngram_frequency)
print("dic :", ngram_dict)

```


- [X] 1. 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?  
    >   네.  

- [X] 2. 주석을 보고 작성자의 코드가 이해되었나요?  
    
    ```
    # 신규가 아닌 것들은 누적합
        for i in range(len(words) -1):
        gram = (words[i], words[i + 1])
        if gram in ngram_dict :
            ngram_dict[gram] += 1
        else :
            ngram_dict[gram] = 1
    ```
    > 위 과정에 대한 설명이 있으면 좋을 것 같습니다.  


- [X] 3. 코드가 에러를 유발할 가능성이 없나요?  
    >   네.  

- [X] 4. 코드 작성자가 코드를 제대로 이해하고 작성했나요?  
    >   네.  

- [X] 5. 코드가 간결한가요?  
    >   네.  


## Review

max, findall 등의 메서드를 알 수 있었습니다. 딕셔너리를 활용한 문제풀이 방식을 알게 되어서 기쁩니다. 


