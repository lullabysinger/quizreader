# quizreader
HTML interface for QN-style CSV formats

The most up-to-date tested version is here: https://lullabysinger.github.io/quizreader/quizreader.html

Note: quizreader can be used offline on your local machine, and it runs **completely client-side with no server code**.
The code is open -- simply 'View Page Source' to see how it works.

The only two (three?) things it uses to keep state are: 
* query strings (the `?ready=true` etc in your browser URL bar) - allows for 'semi' Back-button navigation; 
* and Session Storage (https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage) which is stored temporarily on your local machine.
* and the Clipboard for saving state of the game (i.e. what topics have been picked = the boolean in the `?history=` part of the query string, as an emergency backup measure).

Not even cookies are used!


## Usage instructions - beta20220624

1. download a copy of quizreader.html or just use the live version above.
2. Open it in a modern browser (tested on FF101)
3. Type in the two team names, then select a correctly-formatted CSV file that looks like the following
```
Topic, Question, Answer
Topic1, Q1, A1
Topic1, Q2, A2
...
Topic12, Q1, A1
Topic12, Q2, A2
MysteryA, Q1, A1
MysteryA, Q2, A2
MysteryA, Q3, A3
MysteryB, Q1, A1
MysteryB, Q2, A2
MysteryB, Q3, A3
Spares, Q, A
```
The loader will be able to handle extraneous blank rows, or if a "packet" column is the leftmost column.
The loader will also (as of 20220624) automatically sort Topics in order. (but not the Mystery? and Spares)

4. Enjoy!
  
## Tech credits and tech stack used
* bootstrap 5.0.2 [https://github.com/twbs/bootstrap]
* font-awesome 6.1.1 - free version [https://fontawesome.com/license/free]
* jquery 3.2.1 [https://github.com/jquery/jquery]
* PapaParse 5.3.2 [https://github.com/mholt/PapaParse]
* https://medialize.github.io/URI.js
* easytimer 1.1.3 [https://libraries.io/npm/easytimer]

## Code attributions
* Sample code have been adapted from the documentations for the above libraries (bootstrap, font-awesome, jquery, PapaParse, URI.js, easytimer)
* Non-trivial code for 2D array manipulation credited to contributors in: https://stackoverflow.com/questions/24812371/deleting-a-column-from-a-multidimensional-array-in-javascript
* (Beta test) Card drawing for captains' draw credited to w3collective from: https://github.com/w3collective/random-playing-card/ (MIT License: https://github.com/w3collective/random-playing-card/blob/main/LICENSE)
