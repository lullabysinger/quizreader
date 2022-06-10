# quizreader
HTML interface for QN-style CSV formats

The most up-to-date tested version is here: https://lullabysinger.github.io/quizreader/quizreader.html

Note: quizreader can be used offline on your local machine, and it runs **completely client-side with no server code**.
The code is open -- simply 'View Page Source' to see how it works.
The only two things it uses to keep state are: query strings (the `?ready=true` etc in your browser URL bar); and Session Storage (https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage) which is stored temporarily on your local machine.

Not even cookies are used!


## Usage instructions - beta20220610

1. download a copy of quizreader.html
2. Open it in a modern browser (tested on FF101)
3. Type in the two team names, then select a correctly-formatted CSV file that looks like the following
```
Topic, Question, Answer
Topic0, Q1, A1
Topic0, Q2, A2
...
Topic11, Q1, A1
Topic11, Q2, A2
<blank>
MysteryA, Q1, A1
MysteryB, Q2, A3
MysteryC, Q3, A3
<blank>
Spare, Q, A
```
4. Enjoy!
  
## Tech credits and tech stack used
* bootstrap 5.0.2
* font-awesome 6.1.1
* jquery 3.2.1
* PapaParse 5.3.2
* https://medialize.github.io/URI.js
* easytimer 1.1.3
