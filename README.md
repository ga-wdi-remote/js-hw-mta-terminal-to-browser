# mta-terminal-to-browser


# MTA Terminal

Tonight you will build your first interactive command line application.

## Background
There are 3 subway lines:
  - The **N** line has the following stops: *Times Square, 34th, 28th, 23rd, Union Square, and 8th*
  - The **L** line has the following stops: *8th, 6th, Union Square, 3rd, and 1st*
  - The **6** line has the following stops: *Grand Central, 33rd, 28th, 23rd, Union Square, and Astor Place*.
  - All 3 subway lines intersect at *Union Square*, but there are NO other intersection points.

## Data structure

In class you experimented with ways to represent the MTA. Feel free to use any data structure you find comfortable, but we suggest you use the following

```javascript
var mta = {
"N": ["Times Square", "34th", "28th", "23rd", "Union Square", "8th"],
"L": ["8th", "6th", "Union Square", "3rd", "1st"],
"6": ["Grand Central", "33rd", "28th", "23rd", "Union Square", "Astor Place"]
}
```

## Features
1. A user can list the available lines.

  ```bash
  node mta.js lines
  N
  L
  6
  ```

2. A user can see all of the stops for a line.
  ```bash
  node mta.js stops L
  8th, 6th, union_square, 3rd, 1st
  ```

3. A user can calculate the total number of stops between two stations.
  ```bash
 node mta.js calculate L union_square 6 33rd
 3
 ```

 ```bash
  node mta.js calculate L union_square L 8th
  2
 ```

4. A user is notified if they don't provide the correct number of arguments.
  ```bash
  node mta.js calculate sadasd
  You must provide the 4 arguments - STARTINGLINE STOP ENDINGLINE STOP
  ```

## Keep in mind
- Break it down and follow your errors! Maybe try getting the program to work for a single train line before trying to tackle multiple lines.
- Reference the [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript) for arrays and objects. How can we grab the index number if we already know the value of an element inside an array?

  ``` javascript
  var greeks = ["euripides", "aesop", "sappho"]
  greeks.indexOf("euripides")
  // 0
  ```


## Bonus
Make your output more informative.

   ```bash
   node mta.js calculate L union_square 6 33rd
   Your trip from the Union Square L station to the 33rd 6 station is 3 stops long.
   You will have to make 1 transfer at Union Square to the 6 line.
   ```


## Bonus 2
- Add the following line without making major modifications to your code:
- The Q line has the following stops: 57th, Herald Square, Union Square, Canal St.
- All lines still only intersect at Union Square!

## Ultra Bonus
Add the S line which has only two stops Times Square and Grand Central. You now have multiple intersections. Can you modify the code to handle this.




# MTA in Browser

You are tasked with making a website for customers of the MTA. You need to implement the following user stories:

1. A user can see a list of all lines in the MTA
2. A user can click on a line and see all stops for that line
3. A user can select two stops out of all available stops and they should receive a summary of their trip between the two stops.
- First focus on displaying the number of stops they need to travel
- Then try displaying all stop they will visit during their trip

## Suggestions

1. First spend some time designing a rough mockup of the layout. You have to display certain data and allow for user interactions. You as a developer need to decide how to deliver that information to the user.
2. After you have a rough layout think about your html structure. You do not need to worry about styling at first, but you must have an idea of the building blocks that will make up your page. What do you need to wrap in a `div` tag so that you can style it later?
3. Decide whether you will write the html statically (in the index.html file) or you are actually going to build up the DOM with javascript. Both ways are possible and carry their own sets of challenges. Make sure you have a reason for choosing one over the other.
4. After you have static content on the webpage, start implementing the event listeners to respond to user actions. Try to keep everything modular. Wrap everything in functions and reuse those functions.
5. Practice your css. Make it pretty!
0
