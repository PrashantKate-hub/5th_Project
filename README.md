def reverse_characters(text):
    return text[::-1]

def reverse_words(text):
    return ' '.join(text.split()[::-1])

def save_to_file(text, filename="reversed_text.txt"):
    with open(filename, "w") as file:
        file.write(text)
    print(f"Reversed text saved to {filename}")

def main():
    while True:
        print("\nText Reverser - Choose an option:")
        print("1. Reverse Character Order")
        print("2. Reverse Word Order")
        print("3. Exit")
        choice = input("Enter your choice (1/2/3): ")
        
        if choice == "1":
            text = input("Enter text to reverse: ").strip()
            if text:
                print("Reversed Characters:", reverse_characters(text))
            else:
                print("Error: Input cannot be empty!")
        
        elif choice == "2":
            text = input("Enter text to reverse: ").strip()
            if text:
                print("Reversed Words:", reverse_words(text))
            else:
                print("Error: Input cannot be empty!")
        
        elif choice == "3":
            print("Exiting program. Goodbye!")
            break
        
        else:
            print("Invalid choice. Please enter 1, 2, or 3.")
        
        save = input("Do you want to save the reversed text? (yes/no): ").lower()
        if save == "yes":
            save_to_file(text)

if __name__ == "__main__":
    main()
