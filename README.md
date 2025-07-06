# Question-Answer-Short-Coding
def run_quiz(questions):
    score = 0
    for question_num, q_data in enumerate(questions):
        print(f"\nQuestion {question_num + 1}: {q_data['question']}")
        for i, option in enumerate(q_data['options']):
            print(f"  {chr(65 + i)}. {option}")

        user_answer = input("Your answer (A, B, C, etc.): ").strip().upper()

        if user_answer == q_data['answer']:
            print("Correct!")
            score += 1
        else:
            print(f"Wrong! The correct answer was {q_data['answer']}.")
    print(f"\n--- Quiz Finished ---")
    print(f"You scored {score} out of {len(questions)}.")

if _name_ == "_main_":
    quiz_questions = [
        {
            "question": "What is the capital of France?",
            "options": ["Berlin", "Madrid", "Paris", "Rome"],
            "answer": "C"
        },
        {
            "question": "Which planet is known as the Red Planet?",
            "options": ["Earth", "Mars", "Jupiter", "Venus"],
            "answer": "B"
        },
        {
            "question": "What is 7 * 8?",
            "options": ["54", "56", "64", "48"],
            "answer": "B"
        }
    ]

    run_quiz(quiz_questions)
