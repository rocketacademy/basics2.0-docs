# Day 10: Chat Bot

## Introduction

Today we will practice more complex code logic with nested objects and arrays.&#x20;

We will make a chat bot that asks questions when the submit button is clicked. The user can respond by typing and submitting input and the bot can respond further. Please read all exercises before beginning to see how the chat bot can become more complex.

{% hint style="info" %}
**Please read** [**this**](https://bootcamp.rocketacademy.co/course-logistics/coding-tool-and-language-tips#objects) **primer on different ways to access elements in JavaScript Objects before starting.**
{% endhint %}

### Sample Chat Bot Conversation

The following is a sample conversation between Bot and User.

```
Bot: Hey, wow you seem happy today! Have you been coding? (yes/no/maybe)
---
User: Yes.
---
Bot: Wow! Me too! I've been working on the Blackjack project. Makes my day!
```

### Store Chat Bot Responses in Object

We will use JavaScript Objects to encode the chat bot's potential responses.

```javascript
var answersAndResponses = {
  yes: `Wow! Me too! I've been working on the Blackjack project. Makes my day!`,
  no: 'Oh ok, just normally happy ;)',
  maybe: 'It seems the very thought of coding makes people happy!',
};
```

### Retrieve Chat Bot Responses with User Input

We can retrieve the relevant chat bot response by using user input to access the relevant response from the answers object.

```javascript
// value of input is 'yes'
var responseText = answersAndResponses[input];
```

## Base

### Single Chat Bot Answer Set

Implement the chat bot described above, that asks a yes/no/maybe question and can respond to a user's response of "yes", "no", or "maybe".

### Multiple Chat Bot Answer Sets

Extend the capabilities of the chat bot by storing question and answer text in the same object, like the following.

#### Sample Answer Set

```javascript
var questionAndAnswerSet = {
  question:
    'Hey, wow you seem happy today! Have you been coding? (yes/no/maybe)',
  answers: {
    yes: `Wow! Me too! I've been working on the Blackjack project. Makes my day!`,
    no: 'Oh ok, just normally happy ;)',
    maybe: 'It seems the very thought of coding makes people happy!',
  },
};
```

To have our chat bot support more than 1 question, put the above `questionAndAnswerSet` object into an array of chat bot answer sets, and add a 2nd answer set to our array. The bot will pick which question to ask and answer next.

#### Sample Array of Answer Sets

```javascript
var questionAndAnswerSets = [
  {
    question:
      'Hey, wow you seem happy today! Have you been coding? (yes/no/maybe)',
    answers: {
      yes: `Wow! Me too! I've been working on the Blackjack project. Makes my day!`,
      no: 'Oh ok, just normally happy ;)',
      maybe: 'It seems the very thought of coding makes people happy!',
    },
  },
  {
    question:
      'Do you enjoy coding most during the day, night, or both? (day/night/both)',
    answers: {
      day: 'Ah yes, when the sun is high in the sky, I can feel its energy too.',
      night: 'Under the calm and gentle moon, I also find my focus.',
      both: "Indeed, I could code 24/7 if I didn't have to sleep!",
    },
  },
];
```

Implement a chat bot that alternates between these 2 questions.

### Chat Bot Stores User's Name

Add a new chat bot question that asks for the user's name and responds with a sentence containing the user's name. After greeting the user, the chat bot proceeds with the question from previous exercises.

#### Sample Chat Bot Conversation

```
Bot: Hey! I'm Robocop. What's your name?
---
User: Kai
---
Bot: Kai! What a cool name.

Kai, Hey, wow you seem happy today! Have you been coding? (yes/no/maybe).
```

Use the user's name in the bot's subsequent output. You may want to store the user name in a global variable.

#### Sample Subsequent Bot Output

```
Bot: Kai! Hey, wow you seem happy today! Have you been coding? (yes/no/maybe).
```

### Chat Bot Stores User's Age

Update the chat bot to ask for the user's age after their name. The chat bot's response will differ based on the user's age. For example, we can respond with different outputs if the user is under 20, between 20-60, and above 60.

#### Sample Chat Bot Conversation

```
Bot: Hey! I'm Robocop. What's your name?
---
User: Kai
---
Bot: Kai! What a cool name. How old are you?
---
User: 63
---
Bot: What a wise age, Kai! Hey, wow you seem happy today! Have you been coding? (yes/no/maybe).
```

## More Comfortable

### Chat Bot Named Answer Sets

Update our chat bot answer set array to be an object whose keys are answer set IDs and values are answer sets. Also add a `nextQuestion` key to each answer set object, whose value is always an answer set ID, enabling us to chain question sequences in a named manner. This doesn't add new functionality beyond ordering questions using an array, but it sets up the next exercise Dynamic Chat Bot.

#### Sample Answer Set Collection

```javascript
var questionAndAnswerSets = {
  hasBeenCoding: {
    question:
      'Hey, wow you seem happy today! Have you been coding? (yes/no/maybe)',
    answers: {
      yes: `Wow! Me too! I've been working on the Blackjack project. Makes my day!`,
      no: 'Oh ok, just normally happy ;)',
      maybe: 'It seems the very thought of coding makes people happy!',
    },
    nextQuestionId: 'timeOfDay',
  },
  timeOfDay: {
    question:
      'Do you enjoy coding most during the day, night, or both? (day/night/both)',
    answers: {
      day: 'Ah yes, when the sun is high in the sky, I can feel its energy too.',
      night: 'Under the calm and gentle moon, I also find my focus.',
      both: "Indeed, I could code 24/7 if I didn't have to sleep!",
    },
    nextQuestionId: 'weather',
  },
  weather: {
    question: "Are you most productive when it's sunny or raining? (sun/rain)",
    answers: {
      sun: 'The sun warms my heart and powers me to code.',
      rain: 'The rain washes away my distractions and allows me to focus.',
    },
    nextQuestionId: 'hasBeenCoding',
  },
};
```

### Dynamic Chat Bot

Update our chat bot to choose a next question based on the answer that the user gives. This next question's ID can be stored in the object that corresponds to the user's answer. See the following sample answer set collection for inspiration. Note that some questions have `nextQuestionId` nested within specific answers, and other question have `nextQuestionId` fixed for the question.

#### Sample Answer Set Collection

```javascript
var questionAndAnswerSets = {
  hasBeenCoding: {
    question:
      'Hey, wow you seem happy today! Have you been coding? (yes/no/maybe)',
    answers: {
      yes: {
        response:
          "Wow! Me too! I've been working on the Blackjack project. Makes my day!",
        nextQuestionId: 'timeOfDay',
      },
      no: {
        response: 'Oh ok, just normally happy ;)',
        nextQuestionId: 'happiness',
      },
    },
  },
  timeOfDay: {
    question:
      'Do you enjoy coding most during the day, night, or both? (day/night/both)',
    answers: {
      day: 'Ah yes, when the sun is high in the sky, I can feel its energy too.',
      night: 'Under the calm and gentle moon, I also find my focus.',
      both: "Indeed, I could code 24/7 if I didn't have to sleep!",
    },
    nextQuestionId: 'weather',
  },
  weather: {
    question: "Are you most productive when it's sunny or raining? (sun/rain)",
    answers: {
      sun: 'The sun warms my heart and powers me to code.',
      rain: 'The rain washes away my distractions and allows me to focus.',
    },
    nextQuestionId: 'hasBeenCoding',
  },
  happiness: {
    question: 'Do arrays or objects make you happier? (arrays/objects)',
    answers: {
      arrays: 'I knew it, arrays are my favourite too.',
      objects: "You're good at coding- objects are hard!",
    },
    nextQuestionId: 'timeOfDay',
  },
};
```

### Fortune Telling

Add questions to our chat bot that are purportedly for fortune telling, but where the bot always provides standard responses that anyone might believe are individualised. For example, the bot might ask "Let me tell your fortune. If you have a birthmark, where is it on your body?" and respond with "You have a great need for other people to like and admire you."

Such statements that people might feel are individualised but can apply to everyone are known as Barnum statements. Read more about the Barnum effect and statements [here](https://en.wikipedia.org/wiki/Barnum\_effect#Early\_research).

## Reference Solutions

[Here](https://github.com/rocketacademy/basics-starter-code/blob/day10/script.js) is a reference solution for Day 10 exercises. Please only view the reference solution for each exercise after you have attempted the exercise yourself. Note that there are many ways to implement these solutions and the reference solution is only 1 way.
