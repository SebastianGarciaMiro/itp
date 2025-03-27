# Midterm Project
## by Sebastian Garcia Miro
It's hard for me to figure out where to start. I remember I went out of the class a little confused due to the midterm changing all of the sudden, and I was very worried that it would be a super difficult project that would demand me days to complete. Thankfully, that was not the case.

This part of the story is not very "project-related", but I'll still mention it to provide context.

I went back home to Peru for the brerak and had some good time with my family and friends. That was a blessing and a curse at the same time, because all of this fun made me completely forgot about not only this project, but also all of the other ones I had to do for this week.

This project all of the sudden became super stressful to me because I came back to Boston two days before its due date, and I was worried that it would be super hard. It was all stress and fear until I opened the [p5js.org website](editor.p5js.org) where my saved file from last class saved my life.

The code I had saved during class was:

`let myFirstSound;
function preload() {
  myFirstSound = loadSound('cello_sample.wav');
}
function setup() {
  createCanvas(400, 200);
  myFirstSound.play();
}
function draw(){
  background(0);
  let mouseXNormalized = map (mouseX, 0, width, 0.5, 2.0);
  myFirstSound.rate(mouseXNormalized);
    fill(255);
    text('Pitch:'+ mouseXNormalized.toFixed(2),20,20)
  }
`

I remember this code as the funny try to make the computer produce sound and having the movement of the mouse affect it. The good thing about this is that I had somewhere to start.

The first thing I did was to add 3 different sounds in the `function preload`. From then I created a canvas with both `function setup` and `function draw` to create a canvas where it would tell the users which key to press for each specific sound.

From then,  I added the actions. I stated that:

`function keyPressed() {
  if (key === '1') {
    playSound1();
  } else if (key === '2') {
    playSound2();
  } else if (key === '3') {
    playSound3();
  }
}`

Therefore, I would have 3 keys that would play a different sound each.

Then, I added the part of the code to state that if I pressed these keys, then I would get a confirmation message in the console that would either say "Playing Sound X" or "Sound X not loaded yet". For which I came up with the following code:

`function playSound1() {
  if (sound1.isLoaded()) {
    sound1.play();
    console.log("Playing Sound 1");
  } else {
    console.log("Sound 1 not loaded yet.");
  }
}`

And then I repeated it for the other 2 sounds remaining.

The last part I needed to complete my masterpiece was to find 3 sounds that were worth using considering that I might present it in front of the whole class. In order to figure out which sounds to use, I called my brother, because he is basically the "humor master".

We found 3 sounds worth presenting to the class and we tested the code. For some reason that I really can't explain why, the code was not working. The weird part about it is that it didn't show any errors but it was just simply not working. I would press either 1, 2, or 3 and nothing would happen. My brother (the humor master) is also the coding master, as he majored in computer science when he was in college. He saw my code and just suggested me to change the number keys to trigger the sounds into letter keys (for example to use "L" instead of "1").

I changed the Sound 1 to L, Sound 2 to A and Sound 3 to S. Magically, it worked as normal. I asked him why did it fix the code and he said that errors like this might happen and I just need to try changing the minimun things, which can sometimes fix the problem.

Everything was working great, I was about to finish the project when I try testing it again and it also didn't work. I was about to fix the problem by changing the letters again and I figured out that all of the keys used to trigger the sounds were capital letters (I had forgotten that this language is case-sensitive) so I added to the code that the lowercase versions of the letters could also trigger the sounds. This might also have something to do with the number keys that were not working for me in the first place.

The whole code ended up being:
`
let sound1, sound2, sound3;
function preload() {
  sound1 = loadSound('Amongus.wav');
  sound2 = loadSound('ROBLOX.wav');
  sound3 = loadSound('cucaracha.wav');
}
function setup() {
  createCanvas(400, 200);
  textSize(16);
  textAlign(CENTER, CENTER);
}
function draw() {
  background(30);
  fill(255);
  text("Press 'L' for Sound 1\nPress 'A' for Sound 2\nPress 'S' for Sound 3", width / 2, height / 2);
}
function keyPressed() {
  if (key === 'L' || key === 'l') {
    playSound1();
  } else if (key === 'A' || key === 'a') {
    playSound2();
  } else if (key === 'S' || key === 's') {
    playSound3();
  }
}
function playSound1() {
  if (sound1.isLoaded()) {
    sound1.play();
    console.log("Playing Sound 1");
  } else {
    console.log("Sound 1 not loaded yet.");
  }
}
function playSound2() {
  if (sound2.isLoaded()) {
    sound2.play();
    console.log("Playing Sound 2");
  } else {
    console.log("Sound 2 not loaded yet.");
  }
}
function playSound3() {
  if (sound3.isLoaded()) {
    sound3.play();
    console.log("Playing Sound 3");
  } else {
    console.log("Sound 3 not loaded yet.");
  }
}`

And I'm happy to say that it works perfectly.

### Link to p5js.org

Click [here](https://editor.p5js.org/SebastianGarciaMiro/full/pfXUSNBLX) to view the final result in p5js.org.