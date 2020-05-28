### Tips from Day 4
#### Lecture tips

  * Today we learned about callbacks. Essentially writing code on the side and bringing it by via a call back, instead of intergrating a function, within a function. (See example below)

* Arrow functions can be used to make code look tidier, and its also the industry standard.

Instead of doing this `const genre = fucntion(movie) {if (movie.genre === 'Comedy') {return true}};`

`const genre = movie => movie.genre === 'Comedy';`



#### DRY - Don't Repeat Yourself
I have to make sure I make it a habit of not repeating myself. 
Seperate each function by itself, and put it aside. Use callbacks to bring it up if needed.

Another goal, start using arrow functions. Make the code nicer.

## Callback and Arrow Function
````javascript
const filter = function (movieArr, callback) {
  let bestMovies = [];
  movieArr.forEach(movie => {
    if (callback(movie)) {
      bestMovies.push(movie.title)
    }
  });
  return bestMovies;
}
