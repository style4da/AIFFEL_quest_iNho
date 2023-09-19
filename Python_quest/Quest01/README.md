# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 정인호
- 리뷰어 : 김영진

# PRT(Peer Review Template)
- [ X ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
   
- [ X ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**

- [ X ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나”
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
       
- [ X ]  **4. 회고를 잘 작성했나요?**
       
- [ X ]  **5. 코드가 간결하고 효율적인가요?**
    두 함수를 사용해서 깔끔하게 잘 작성하셨다.

'''
def check_palindrome(word) :                         # 회문 판별
  for i in range(len(word) // 2):                    # 단어의 길이를 2등분하여 for문으로 삽입
      if word[i] != word[-1 - i]:                    # 각각의 단어word[i]를 역순의 단어[word[-1 - i]와 비교
        print("입력된 단어는 회문이 아닙니다,")
        break                                        # 출력값이 2번 출력되는 오류가 있어서 break로 제어하였음
      else :
        print("입력된 단어는 회문입니다.")
        break                                        # 출력값이 2번 출력되는 오류가 있어서 break로 제어하였음



def main() :
  word = input('단어를 입력하세요 : ')
  print('='*10)
  print("입력값 : \n" + word+'\n')
  reversed_word  = word[::-1]
  print("출력값 : \n" + "뒤집힌 단어는 : " + reversed_word)
  check_palindrome(word)

main()
'''