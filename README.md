# Korean-English-and-math-scores
# python
# In the first line N, enter the number of students in Korean, English, and math order, and write a report card in the order of increasing Korean scores, increasing Korean scores, decreasing math scores, and increasing names in dictionary order. 첫번째 줄 N에는 학생수를 입력하고 학생마다 국어,영어,수학순으로 성적을 입력하고 국어 점수가 감소하는 순서로 국어 점수가 같으면 영어 점수가 증가하는 순서로 국어 점수와 영어 점수가 같으면 수학 점수가 감소하는 순서로 모든 점수가 같으면 이름이 사전 순으로 증가하는 순서로 성적표를 작성한다.
import sys
input=sys.stdin.readline
N=int(input())
score=[]
for i in range(N):
    score.append(list(map(str,input().split())))
score.sort(key=lambda x:(-int(x[1]),int(x[2]),-int(x[3]),x[0]))
for i in range(N):
    print(score[i][0])
# input--> 12  Junkyu 50 60 100  Sangkeun 80 60 50  Sunyoung 80 70 100  Soong 50 60 90  Haebin 50 60 100  Kangsoo 60 80 100  Donghyuk 80 60 100  Sei 70 70 70  Wonseob 70 70 90  Sanghyun 70 70 80  nsj 80 80 80  Taewhan 50 60 90
# result--> Donghyuk Sangkeun Sunyoung nsj Wonseob Sanghyun Sei Kangsoo Haebin Junkyu Soong Taewhan
