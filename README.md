# THE-SILLOGISM-AND-THE-TRUTH-TABLES

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
