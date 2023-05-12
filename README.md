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

## Usecases
Alright, so now that we already discussed the syntax and technicality of this method. Now let's try to understand the usecases of it. 

Let's assume that the array that we had decleared is actually from any sort of survey that resulted those states from top ranking to to lower ones.

> That means the `rajya` `'UP'` is in the top ranking of that list and the `rajya` `'DL'` is in the last.

Now let's say we need only the top three from this list and not others. So, to fullfill this requirement we can write some code, that we will see. But first let's map the `rajyas` to their index numbers for our better understanding.

> Seeing the array `rajyas` we can clearly say that <br>
***Element*** `'UP'` belongs to index ***0*** <br>
***Element*** `'WB'` belongs to index ***1*** <br>
***Element*** `'PB'` belongs to index ***2*** <br>
***Element*** `'BR'` belongs to index ***3*** <br>
***Element*** `'JH'` belongs to index ***4*** <br>
***Element*** `'DL'` belongs to index ***5*** <br>

Now we will see how we can fullfill our discussed requirements.

```js
const topthreerankers = rajyas.slice(0, 3)
```

Our requirements were, that we want top three placeholders in the new array. We declared a new array `topthreerankers` and assigned that to `slice` method applied to `rajyas` array. In the parameters of the `slice` method, we provided the first index `0` and the 4th index `3`. We particularly put 4th index, because we want all elements upto the 4th place, but not including the 4th. And the `slice` method exactly works like this. It does not gives you the element that is in the second parameter's index. 

I hope this article made the concepts clear. 