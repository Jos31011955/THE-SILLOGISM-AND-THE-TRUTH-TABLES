"## Summary"
# THE-SILLOGISM-AND-THE-TRUTH-TABLES
1. Your idea in brief = “The Syllogism and truth tables”
2. Context = First teaching of the logic of the Syllogism to children
3. Data and AI techniques = a) Data Used: Major and Minor Premises: These are sentences entered by the user that represent logical statements.
Truth Values: The user enters the truth values ​​(true or false) for the major and minor premises.
b) Choice of Logical Connective: The user chooses the type of logical connective to apply between the premises.
C) AI techniques used:
1. Natural Language Processing (NLP):
Subject and Predicate Extraction: The program extracts the subject from the minor premise and the predicate from the major premise using simple string manipulation techniques.
Conclusion Formulation: Combines the subject of the minor premise with the predicate of the major premise to formulate a conclusion.
2. Boolean Logic:
3. Evaluation of Logical Connectives: Uses logical operators to calculate the result of the logical operations chosen by the user (e.g., AND, OR, XOR, implication, logical equivalence, negation).
Human-Computer Interaction:
User Input: The program requires input from the user for the premises, truth values ​​and the choice of the logical connective.
Result Output: Prints the result of the logical operation and the truth values ​​of the conclusions.
4. How it is used=by high school students
5. Challenges=to practically learn how the Syllogism works and the function of the Truth Tables
6. Thanks=Microsoft “Copilot” for helping in developing the code

def main():
    
    # Request the major premise
    major_premise = input("Enter the major premise (e.g., 'The sky is blue'): ")
    
    # Request the minor premise
    minor_premise = input("Enter the minor premise (e.g., 'The grass is green'): 
")

    # Request to choose the type of connective
    print("Choose the type of connective:")
    print("1. A and B")
    print("2. A or B")
    print("3. A xor B")
    print("4. A <=> B")
    print("5. A => B")
    print("6. not A")


    choice = input("Enter the number corresponding to your choice: ")

    # Extract the subject of the minor premise
    minor_subject = minor_premise.split()[0]






    # Extract the predicate of the major premise
    major_predicate = ' '.join(major_premise.split()[2:])
    
    # Print the subject of the minor premise followed by the predicate of the major premise
    conclusion = f"{minor_subject} {major_predicate}"
    print("\nConclusion: ", conclusion)
    
    # Request the truth values of the premises
    major_truth = input("The truth value of the major premise (T/F): ").strip().upper()
    minor_truth = input("The truth value of the minor premise (T/F): ").strip().upper()

    # Convert the truth values to booleans
    A = major_truth == 'T'
    B = minor_truth == 'T'







    # Calculate the truth values of the conclusions
    if choice == "1":
        result = A and B
    elif choice == "2":
        result = A or B
    elif choice == "3":
        result = A != B  # XOR
    elif choice == "4":
        result = A == B  # Logical equivalence
    elif choice == "5":
        result = not A or B  # Logical implication
    elif choice == "6":
        result = not A
    else:
        result = "Invalid choice"






    print(f"\nThe result of the operation is: {result}")

    # Print the truth values of the conclusions
    print("\nTruth values of the conclusions:")
    print(f"A and B: {A and B}")
    print(f"A or B: {A or B}")
    print(f"A xor B: {A != B}")
    print(f"A <=> B: {A == B}")
    print(f"A => B: {not A or B}")
    print(f"not A: {not A}")
    print(f"not B: {not B}")

if __name__ == "__main__":
    main()
