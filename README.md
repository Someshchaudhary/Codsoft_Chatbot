# Chatbot with Python's NLTK

This project is a simple chatbot implementation using Python's NLTK library. The chatbot interacts with users through predefined patterns and responses.

## Features
- Responds to general greetings.
- Handles queries about the chatbot's creator, purpose, and name.
- Provides basic weather-related responses.
- Discusses sports, health, and other casual topics.
- Handles gratitude, apologies, and farewell messages.

## How It Works
The chatbot uses a list of predefined patterns and responses. The user's input is matched against these patterns using regular expressions, and the corresponding response is generated.

### Code Example
```python
pairs = [
    # General Greetings
    [
        r"(hi|hey|hello|hola|holla)(.*)",
        ["Hello! How can I assist you today?", "Hey there! What's on your mind?", "Hi! How's your day going?"]
    ],

    # Questions about creation
    [
        r"(.*)created(.*)",
        ["Somesh Chaudhary created me using Python's NLTK library.", "That's a secret, but let's just say Python was involved!", "I was created to assist you!"]
    ],

    # Goodbye
    [
        r"quit",
        ["Goodbye for now! Hope to chat again soon!", "Take care! See you next time!"]
    ]
]
```

## Reflection Mapping
To make conversations more natural, a `reflections` dictionary is used to reverse the user's perspective in responses:
```python
reflections = {
    "i am": "you are",
    "i was": "you were",
    "i": "you",
    "i'd": "you would",
    "i've": "you have",
    "i'll": "you will",
    "my": "your",
    "you are": "I am",
    "you were": "I was",
    "you've": "I have",
    "you'll": "I will",
    "your": "my",
    "yours": "mine",
    "you": "me",
    "me": "you"
}
```

## Prerequisites
- Python 3.x
- NLTK Library

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/chatbot-nltk.git
    ```
2. Navigate to the project directory:
    ```bash
    cd chatbot-nltk
    ```
3. Install the required dependencies:
    ```bash
    pip install nltk
    ```
4. Run the chatbot:
    ```bash
    python chatbot.py
    ```

## How to Use
- Start the chatbot by running the script.
- Type a message or question, and the chatbot will respond based on its predefined patterns.
- Type `quit` to exit the conversation.

## Contribution
Feel free to fork this repository and submit pull requests for improvements or new features.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
