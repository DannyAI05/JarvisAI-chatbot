#python chatbot
def chatbot_response(user_input):
    user_input = user_input.lower()

    if "hello" in user_input or "hi" in user_input:
        return "Hey Danny! I'm your chatbot AI assistant."
    elif "how are you" in user_input:
        return "I'm very fine and feeling supercharged, ready to assist!"
    elif "what do i call you" in user_input:
        return "You can call me JarvisAI as named by my creator Wakhu!"
    elif "bye" in user_input:
        return "See you later, Danny!"
    else:
        return "I'm not sure about that yet. Can you rephrase your question?"


def main():
    print("JarvisAI - Type 'Bye' to end chat")
    while True:
        user_input = input("You: ")

        
        if user_input.lower() == "bye":
            print("JarvisAI: Goodbye!")
            break

        
        print("JarvisAI:", chatbot_response(user_input))


if __name__ == "__main__":
    main()
