# FizzBuzz
## By Sebastian Garcia Miro
Compared to last week's class, this time I went out of the class knowing exactly what to do. I understood everything we talked about in class and it makes me happy because this whole world of programming is very interesting to me and I'm glad I'm getting the hang out of it sooner than I expected. Well, I do have to admit that the procrastination took the best part of me as I did take long to do this assignment, not because I did not understand it but just because my lazy side was winning over my responsible one.

Well, getting back to the assignment, the first thing I did was to read through the [codealong.js](https://github.com/rdwrome/261sp25/blob/main/04ControlFlow/codealong.js) document, and thankfully my memory didn't take long to come back. After reading the document again, I realized that the `for` statement was the right thing to start with. 

I came up with the code `for (let i = 1; i <= 100; i++) {
` as the first part of my code to create a list from 1 to 100, but I still needed to add more stuff to make the code work.

Then, I just needed a way to check divisibility conditions and that's where the `if-else` statements came in. I first came up with `if (i % 3 === 0 && i % 5 === 0) {
  console.log("FizzBuzz");` to tell the console that every number divisible by 3 and 5 should say "FizzBuzz" instead of the number itself. After that, I used the statement `else if` to check additional conditions if the first statement was false. That's where `else if (i % 3 === 0) {
  console.log("Fizz");` and `else if (i % 5 === 0) {
  console.log("Buzz");` came from. What this does is that if the first statement was false, it would make the number say "Fizz" if it's divisible by 3, and if both of those statements were false and the number is divisible by 5 it would say "Buzz" instead of the number.
  
  Now, the final part needed to make this code work is to add a statement that tells the console that if all of those previous statements are false, the console will simply print the number itself. For that I used `else` because I am not adding any new conditions. The last part of the code is the following: `else {
  console.log(i);`
 
  Now, if you add all of these codes mentioned above in the same order to the JavaScript console, it should output a list from 1 to 100 that every multiple of 3 says Fizz, every multiple of 5 says Buzz, and every multiple of both 3 and 5 at the same time would say "FizzBuzz".