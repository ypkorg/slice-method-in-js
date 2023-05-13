# `slice()` method in Javascript

`slice()` is a method in javascript that works with arrays. It essentially returns some elements from a parent array to a very new array. That means it returns an array. Now what that array would contain is a matter of what parameters this method is given. We will discuss it's methodologies, syntax and usecases below in this article.

> ### Dictionary
> - **Rajya** -  *State (A centralized political organization under a nation that imposes rules over a certain geography)*
> - **Rajyas** - *Plural form of Rajya. It can be also written as Rajya(s)*
> - **'UP', 'WB', 'PB', 'BR', 'JH', 'DL'** - *Code names of some States in Republic of India (Bharat)*

## Syntax
Let's say we have an array named `rajyas` as,
```js
const rajyas = ['UP', 'WB', 'PB', 'BR', 'JH', 'DL'];
```
Now the syntax of using `slice()` method to fetch some data out and put it in a new array would be, 
```js
const newarray = rajyas.slice(start, end);
```
The `newarray` being the new array, will contain some data extracted (copied) from `rajyas`.


The `slice()` method accepts two `number type` parameters. These numbers are indexes of the parent array. The new array starts from the element that is in the parent array's that index that is provided as the first parameter in the `slice()` method, and will contain all the elements upto the index that is provided as the second parameter.


> **Note** 
>
> It is important to remember that the index in the second parameter will not be contained in the new array. The element that is one index behind of the second parameter provided to the `slice()` method will contain in the new array. That is literally what ***"upto"*** means.

> **Note** 
>### What if we do not provide a second parameter ?
> Well if we do not provide a second parameter and provide only one number, then the new array will start from the element on that index in the parent array and will continue to the end of that array.

## Usecases
Alright, so now that we already discussed the syntax and technicality of this method. Now let's try to understand the usecases of it. 

Let's assume that the array that we had decleared is actually from any sort of survey that resulted those states from top ranking to to lower ones.

> That means the rajya `'UP'` is in the top ranking of that list and the rajya `'DL'` is in the last.

Now let's say we need only the top three from this list and not others in the new array. So, to fullfill this requirement we can write some code, that we will see. But first let's map the rajyas to their index numbers for our better understanding.

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

Our requirements were, that we want top three placeholders in the new array. We declared a new array `topthreerankers` and assigned that to `slice()` method applied to `rajyas` array. In the parameters of the `slice()` method, we provided the first index `0` and the 4th index `3`. We particularly put 4th index, because we want all elements upto the 4th place, but not including the 4th. And the `slice()` method exactly works like this. It does not gives you the element that is in the second parameter's index. Rather it gives you the element that is just behind the index that is passed in the `slice()` method.

I hope this article made the concepts clear.    