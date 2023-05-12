# `slice()` method in Javascript

`slice()` is a method in javascript that works with arrays. It essentially returns some elements from a target array to a very new array. That means it returns an array. Now what that array would contain is a matter of what parameters this method is given. We will discuss it's methodologies, syntax and usecases below in this article.

## Syntax
Let's say we have an array named rajyas as,
```js
const songs = ['UP', 'WB', 'PB', 'BR', 'JH', 'DL'];
```
Now the syntax of using `slice` method to fetching some data out and put in a new array would be, 
```js
const newarray = songs.slice(start, end);
```
The `newarray` being the new array will contain some data extracted (copied) from `songs`.


The `slice()` method accepts two number type parameters. These numbers are indexes of the mentioned array. The new array starts from the index of mentioned array's index of the number that is provided as the first parameter in the `slice` method, and will contain all the elements upto the index that is provided as the second parameter.


> **Note**
> It is important to remember that the index in the second parameter will not be contained in the new array. The one element behind that index will contain in the array. That is literally what ***"upto"*** means.
