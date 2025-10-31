# chatbot.py

def chatbot_response(user_input, user_name):
    user_input = user_input.lower()

    if "hello" in user_input or "hi" in user_input:
        return f"Hey {user_name}! I'm JarvisAI, your Python chatbot assistant."
    elif "how are you" in user_input:
        return "I'm feeling fantastic and fully charged! How about you?"
    elif "your name" in user_input:
        return "I'm JarvisAI, created by Wakhu. Nice to meet you!"
    elif "bye" in user_input:
        return f"Goodbye {user_name}, talk to you later!"
    elif "help" in user_input:
        return "I can chat, tell jokes, or answer simple questions. Try asking me something!"
    elif "joke" in user_input:
        return "Why did the programmer quit his job? Because he didn’t get arrays "
    else:
        return "Hmm... I'm not sure about that yet. Could you rephrase your question?"


def main():
    print(" JarvisAI - Your Python Chatbot")
    user_name = input("Before we start, what's your name? ")

    print(f"\nJarvisAI: Hey {user_name}! Type 'bye' anytime to end the chat.\n")

    while True:
        user_input = input(f"{user_name}: ")

        if user_input.lower() == "bye":
            print(f"JarvisAI: Goodbye {user_name}! ")
            break

        response = chatbot_response(user_input, user_name)
        print("JarvisAI:", response)


if __name__ == "__main__":
    main()
