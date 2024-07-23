import random
game_data=[
    
    {"question" :"What is python primarily known for ?",
     "options":["A.System programming","B.Web development","C.Data analysis","D.Game development","E.All of the above"], 
     "answer":"E"
     },
    {
     "question" : "Which of the following is not a valid python data type ?",
     "options":["A.List","B.Tuple","C.Dictionary","D.Array","E.Set"],
     "answer":"D"
     },
    {
     "question" :"Which keyword is used to defne function in python?",
     "options":["A.func","B.def","C.function","D.defne","E.create"], 
     "answer":"B"
    },
    {
     "question" :"What is the correct fle extension for python fle ? ",
     "options":["A.py","B.python","C.pyt","D.pt","E.pyn"], 
     "answer":"a"
    },
    ]
def quest_question(question_data):
    print(question_data["question"])
    for option in question_data["options"]:
        print(option)
    my_answer = input("Enter your answer (A,B,C,D,E): ").upper()
    if my_answer == question_data["answer"]:

        return True

    else:

        return False

if __name__=="__main__":

score=0
    for i in range(1,4):
        print("Question",i,"of 3")
        if quest_question(game_data[i]):
            print("Correct!\n")
            score += 1
        else:
            print("Wrong! The correct answer is",game_data[i]['answer'],".\n")
    print("You scored",score,"/3.")
