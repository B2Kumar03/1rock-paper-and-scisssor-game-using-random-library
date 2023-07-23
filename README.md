import random
import os
my_dict = {'rock': '🥊 ', 'paper': '📄 ', 'scissor': '✂'}
random_key = random.choice(list(my_dict.keys()))
random_value = my_dict[random_key]
total1_score = 0
total2_score = 0
print("-----------WeLcOmE-----------")
print()
player = ['1.PLAYER1', '2.PLAYER2']
print("Choose player:-")
print("              ", '----------')
print("              ", '1.PLAYER1')
print("              ", '----------')
print("              ", '2.PLAYER2')
print("              ", '----------')
print("(Note:After choosing click enter on your keyword.)")
ch = int(input())
if ch == 1:
  print("Player1=", 'You')
  print("Player2=", 'Computer')
elif ch == 2:
  print("Player1=", 'Computer')
  print("Player2=", 'You')
print("************************************")
player1 = ''
player2 = ''
def clear_console_line():
    # ANSI escape code to clear from cursor to end of line
    print("\033[K", end="")

#print(random_value)

while True:
  clear_console_line()
  if ch == 1:
    player1 = input("Enter Your Choice (rock/paper/scissor) :")
    print('Entered by Player1 :', my_dict[player1])
    player2 = random_key
    print('Entered by Player2 :', my_dict[player2])
  elif ch == 2:
    player2 = input("Enter Your Choice (rock/paper/scissor) :")
    print('Entered by Player2 :', my_dict[player2])
    player1 = random_key
    print('Entered by Player1 :', my_dict[player1])

  if player1 == 'rock' and player2 == 'paper':
    print("Player2 is win")
    total2_score += 1
  elif player1 == 'paper' and player2 == 'rock':
    print("Player1 is win")
    total1_score += 1
  elif player1 == 'rock' and player2 == 'scissor':
    total1_score += 1
    print("Player1 is win")
  elif player2 == 'rock' and player1 == 'scissor':
    total2_score += 1
    print("Player2 is win")
  elif player1 == 'paper' and player2 == 'scissor':
    total2_score += 1
    print("Player2 is win")
  elif player2 == 'paper' and player1 == 'scissor':
    total2_score += 1
    print("Player1 is win")
  elif player1 == player2:
    total2_score -= 1
    total2_score -= 1
    print("Tie")
  print("\nWant to play Again.click Y/n:")
  h = input()
  if h == 'n' or h == 'N':
    break
  elif h == 'y' or h == 'Y':
    continue
print("----------Thank You ----------")
print("\nTotal Score :")
if total1_score > total2_score:
  print("               ", "Player1 :", total1_score,"Winner")
  print("               ", "Player2 :", total2_score)
elif total2_score > total1_score:
  print("               ", "Player1 :", total1_score)
  print("               ", "Player2 :", total2_score,"Winner")
# 1rock-paper-and-scisssor-game-using-random-library
