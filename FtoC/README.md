# Fahrenheit to Celsius Converter

##By Sebastian Garcia Miro

For this assignment, I left the classroom very scared because compared all of the previous classes and assignments we've had so far this semester, I understood nothing. Now, I don't want to blame the professor or anything like that because the whole confusion was on me. It was just so much new information about this language that I have never spoke (or in this case written) in my whole life. 

It was all fear and stress until I went to Dr. Rome's office hour on Tuesday, when all of my confusion suddenly disappeared in about 3 to 5 minutes. 

After knowking the couple of tips to guide me over this assignment, I started pseudocoding on what to do. I knew it had something to do with Template Literals and Variables, but I was still doubting how to do it. So I read the whole document once again to see if I could find anything else that could help me finish this assignment, and gladly I did.

I found the code:
`const pi = 3.14;` and I just changed it to `const f = 99;` and `const c = (f - 32) * 5 / 9;` so that it would be relevant to the assignment. I also used the "Division" and "Multiplication" examples to help me with the math for this problem.

After that, I was in good shape to continue searching for a way to find a solution for this assignment, so I went to follow the clues i was given during the office hours and I saw the example `console.log(${9/3} little pigs);` from Template Literals and changed it into
`console.log(`${f}°F is equal to ${c.toFixed(2)}°C`);` changing the code `console.log(z.toFixed(5));`into something that would fit into this assignment and changed the 5 to 2 so that I would only get 2 decimals.

Finally, I tried the code in [eloquentjavascript](https://eloquentjavascript.net/code/), where thankfully, it worked perfectly. So, I am glad that this whole assignment that started with fear and uncertainty turned into an assignment that was both interesting and fun.
;
The complete code I used to get the answer "99°F is equal to 37.22°C" was:
`
const f = 99;
const c = (f - 32) * 5 / 9;
console.log(`${f}°F is equal to ${c.toFixed(2)}°C`);`