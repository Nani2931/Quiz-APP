# Quiz-APP
class MultipleChoiceQuiz:
    def __init__(self):
        self.questions = []
        self.choices = []
        self.answers = []

    def add_question(self, question, choices, answer):
        self.questions.append(question)
        self.choices.append(choices)
        self.answers.append(answer)

    def start_quiz(self):
        score = 0
        total_questions = len(self.questions)
        for i in range(total_questions):
            print(f"Question {i + 1}: {self.questions[i]}")
            for idx, choice in enumerate(self.choices[i]):
                print(f"{idx + 1}. {choice}")
            user_answer = input("Enter your choice (1, 2, 3, 4): ")
            if user_answer.isdigit():
                user_answer = int(user_answer) - 1
                if 0 <= user_answer < len(self.choices[i]):
                    user_choice = self.choices[i][user_answer]
                    if user_choice == self.answers[i]:
                        print("Correct!")
                        score += 1
                    else:
                        print(f"Wrong! The correct answer is: {self.answers[i]}")
                else:
                    print("Invalid choice!")
            else:
                print("Please enter a number.")
            print()
        print(f"Quiz complete! You scored {score}/{total_questions}")

def main():
    quiz = MultipleChoiceQuiz()

    # Add multiple-choice questions, choices, and answers
    quiz.add_question("Which country is famous for anime?",
                      ["Japan","USA","China","Korea"],"Japan")
    quiz.add_question("Who is often considered to be the Father of the Automotive industry?",
                      ["Hendry Ford","Ferdinand Porsche","Karl Benz","George Baldwin Selden"],"Karl Benz")
    quiz.add_question("What is the capital of France?",
                      ["London", "Paris", "Berlin", "Madrid"], "Paris")
    quiz.add_question("Which car was the first affordable automobile,which made car travel available to middle-class?",
                      ["Ford Model K","Mercedes-Benz F200","Victory Wagon","Ford Model T"],"Ford Model T")
    quiz.add_question("Which is the largest planet in our solar system?",
                      ["Mars", "Jupiter", "Venus", "Saturn"], "Jupiter")
    quiz.add_question("The first official motor race in the world was held in which year?",
                      ["1895","1910","1925","1935"],"1895")
    quiz.add_question("What is the powerhouse of the cell?",
                      ["Mitochondria", "Ribosome", "Nucleus", "Endoplasmic Reticulum"],
                      "Mitochondria")
    quiz.add_question("What was the first vehicle to go faster than the speed of sound?",
                      ["Bugatti Veyron","Hennessey Venom GT","Thrust SSC","Porsche 911"],"Thrust SSC")
    quiz.add_question("Whose body gained the properties of rubber after unintentionally eating a Devil Fruit?",
                      ["Goku","Monkey D.Luffy","Saitama"],"Monkey D.Luffy")
    quiz.add_question("What is the largest mammal on Earth?",
                      ["Elephant","Giraffe","Blue whale","seal"],"Blue whale")
    quiz.add_question("Which car manufacturer was the first to add seat Belts?",
                      ["Cadillac","Nash","Toyota","Volkswagen"],"Nash")
    quiz.add_question("Which bird is known for its wisdom in stories?",
                      ["Owl","Parrot","Dove","Sparrow"],"Owl")
    quiz.add_question("Who is main protagonist of Pokémon anime series?",
                      ["Pikachu","Ash Ketchum","Misty","Jessie"],"Ash Ketchum")
    quiz.add_question("What is the largest internal organ in the Human body",
                      ["Lungs","Heart","Kidneys","Liver"],"Liver")
    quiz.add_question("By the time when the World War I broke out,which country is the world's largest motorcycle manufacturer?",
                      ["The United States of America","India","Germany","China"],"India")
    quiz.add_question("Which one is a wall on Paradise Island that protected the remnants of Eldia in Attack on Titan?",
                      ["Maria","Sina","Rose","All of them"],"All of them")
    quiz.add_question("A common term used among anime watchers is 'The Big Three'.What show does this reference?",
                      ["Naruto,One punch man,Dragon Ball","One Piece,Bleach,Black Clover","One Piece,Naruto,Bleach","Dragon Ball,Black Clover,Attack on Titan"],"One Piece,Naruto,Bleach")
    quiz.add_question("When was the first internal combustion motorcycle fuelled by petroleum invented?",
                      ["1885","1900","1915","1880"],"1885")
    quiz.add_question("Who is the director of the Your Name anime movie?",
                      ["Hayao Miyazaki","Makoto Shinkai","Naoko Yamada","Shin'ichirō Ushijima"],"Makoto Shinkai")
    quiz.add_question("Who is the main Antagonist person in Attack on Titan?",
                      ["King Fritz","Zeke Yeager","Ymir","Eren Yeager"],"Eren Yeager")

    print("Welcome to the Multiple Choice Quiz!")
    print("Answer the following questions:")
    quiz.start_quiz()

if __name__ == "__main__":
    main()
