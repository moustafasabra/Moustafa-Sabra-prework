# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Moustafa Mahmoud Sabra

Time spent: 1 hours spent in total

Link to project: https://glitch.com/edit/#!/moustafasabra?path=README.md%3A1%3A0

## Required Functionality

The following **required** functionality is complete:

* [ done ] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [ done ] "Start" button toggles between "Start" and "Stop" when clicked. 
* [ done ] Game buttons each light up and play a sound when clicked. 
* [ done ] Computer plays back sequence of clues including sound and visual cue for each button
* [ done ] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [ done ] User wins the game after guessing a complete pattern
* [ done ] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [ N/A ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ N/A ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ N/A ] More than 4 functional game buttons
* [ N/A ] Playback speeds up on each turn
* [ N/A ] Computer picks a different pattern each time the game is played
* [ N/A ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ N/A ] Game button appearance change goes beyond color (e.g. add an image)
* [ N/A ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ N/A ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ N/A ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
[ done ] http://g.recordit.co/pYkYld4Ifs.gif


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
- Coursera: Java Programming and Software Engineering Fundamentals: https://www.coursera.org/specializations/java-programming
- w3schools: https://www.w3schools.com/js/DEFAULT.asp
- Data Structures and Algorithms in Java: Goodrich, M. T., Tamassia, R., &amp; Goldwasser, M. H. (2015). Data structures and algorithms in Java. Singapore: John Wiley &amp; Sons Singapore Pte.


2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

Such a task has been accompanied by various challenges due to its transformative nature. The biggest challenge I have faced was 
related to the gameplay algorithm. Making sure that the code checks for the timing and consistency of the pattern played by the 
player relative to the supplied list of patterns was specifically hard. To keep track of the player guesses, the code must check 
whether it is the right button at that moment in time, in addition to keeping count of the attempted pattern through the progress variable. 
This process would be carried by the designated guess function as explained in the documentation. Accounting for all the possibilities of 
the gameplay made it hard to predict which variable to check first. As the logic games go, the player will only be allowed to continue the 
game if they managed to achieve the right sequence within an accepted time window. This process should not be active unless the game is already 
on. Therefore, checking the activity of the game is a first. Considering that the game is one, the player’s progress should be checked first to 
see if the pattern displayed is the terminal case for winning the game. Immediately afterward, we check for the validity of the pattern inserted
by the user. This is not obviously in case we tried to think of it logically, as you would think of checking if the pattern is correct first
then update the game variables such as the progress and the guess counter variables accordingly. But this doesn't account for the terminal cases
of having the last pattern match the user input or having the user enter the first pattern wrong as an error message would be displayed. I have 
solved this problem by realizing that the algorithm would be coded the other way around to achieve the intended gameplay structure.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

My major concern after conducting this experiment is the functionality of the CSS file concerning the Javascript file,
as the CSS has limited styling options that fail to function without the Javascript file algorithms. I am curious to 
what extend does the Javascript folder affects the website's overall functionality. I am aware that the inner working 
of the website relies on the Javascript folder compatibility relative to the HTML file and the CSS folder. Failing to 
optimize the website's inner communication between these three main components might increase the loading time, which 
reflects poorly on the performance of the website.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

I would invest more time into the gameplay algorithm to account for a reliable point system. Instead of comparing the user’s pattern to the original supplied ones, I would account for the accuracy of the user
input relative to the original ones in the code. The more precious is the player with the timing and the pattern the more points they get. In this scenario, the terminating conditions would change to count for 
a threshold score that if the player fails to accomplish, they lose the game. To accomplish this, I will first define two quantities: accuracy and timing that would be assigned to every pattern. That suggests 
that my simple array that had the pattern before would need to be an array of objects instead of numbers. Each object is a pattern that is distinguished by perfect timing and accuracy values that are used in 
comparison to the user’s input. The smaller the error margin between the user timing and the accuracy for a given pattern the more the user gets rewarded. So after checking for the timing and accuracy characteristic 
of the patterns as the game goes, the scores will be added accordingly to an accumulator variable to get track of the user score. Then eventually the game will automatically terminate the player by the end of the
last pattern if the accumulative score fails to fall in the range of accepted scores values with a high marginal error. Only then would the player get promoted to restart the game, where the message of You Lost 

    Copyright [MOUSTAFA MAHMOUD SABRA]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
