print("Welcome to the NBA Trivia Game!!!")
print(" ")
name = input("Entre your name: ")

questions = ("Who is the tallest NBA player ever?: ",
"Who is the NBA first draft pick 2026?: " ,
"Who has the most rings in NBA history?: " ,
"When did Lebron James retire?: ")

options = (("A. Kyrie Ivring ","B. Victor Wembanyama","C.Gheorghe Mureșan","D.Yao Ming"),
("A. Tyrese Haliburton","B. Steph Curry","C. AJ Dybantsa","D. Darryn Peterson"),
("A. Bill Russell","B. Micheal Jordan","C. John Havlicek","D. K.C. Jones"),
("A. 2020","B. 2003","C. 2012","D. he hasn't yet"))

answers = ("C", "C", "A", "D")
guesses = []
score = 0
question_num = 0

for question in questions:
    print("------------------------------------------")
    print(question)

    for option in options[question_num]:
        print(option)
        
    guess = input("Entre your guess: ").upper()
    guesses.append(guess)
    if guess == answers[question_num]:
        score += 1
        print("Correct!")
    else:
        print("Incorrect")
        print(f"{answers[question_num]} is the correct answer")
        
    question_num += 1

    
print("------------------------------------------")
print(" Your results are:")

print ("answers: ", end=" ")
for answer in answers:
    print(answer, end=" ")
print ()

print ("guesses: ", end=" ")
for guess in guesses:
    print(guess, end=" ")
print ()

score = int(score/ len(questions) * 100)

if score == 100:
    print(f"Congratulations {name}!" )
    print(f"your score is: {score}")
else:
    print(f"you made some mistakes {name}, try again!")
    print(f"your score is: {score}")




