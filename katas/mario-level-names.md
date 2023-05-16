# Mario Level Names

This kata will take multiple iterations to complete. Each iteration will build on the previous one. The goal is to create a system that can generate level names for a Mario game.

## Iteration 1

Create a system that can generate a level name for a Mario game. The level name should be a string that is a combination of a world and a level number. You will need to write a function that takes 2 parameters, one for the number of worlds and the other for the number of levels per world. The function should return a array of strings that represent the level names.

For example, if there are `2` worlds and `3` levels per world, the function should return the following array:

```javascript
["1-1", "1-2", "1-3", "2-1", "2-2", "2-3"]
```

## Iteration 2

The level designers have realised that they can't create the same number of levels for each world. They need to be able to specify how many levels are in each world. Update the function so that it takes an array of numbers that represent the number of levels in each world.

If a value in the array is `0` or less, then that world should get a default number of `1` level. For example, if the array is `[3, 0, 2]`, then the function should return the following array:

```javascript
["1-1", "1-2", "1-3", "2-1", "3-1", "3-2"]
```

The function should only return values for the worlds that have been specified. If the array is `[3, 0, 2, 1, 0]`, but the number of worlds is `4`, then the function should return the following array:

```javascript
["1-1", "1-2", "1-3", "2-1", "3-1", "3-2", "4-1"]
```

Notice that `5-1` is not returned because there are only `4` worlds.

## Iteration 3

The UI team is finding it hard to read the level names easily into the game. They have asked that your functions returns a object instead. Where the key represents the world number and the value is an array of level names for that world.

For example, if your function is called with `3` worlds and a levels array of `[3, 0, 2]`, then the function should return the following object:

```javascript
{
  1: ["1-1", "1-2", "1-3"],
  2: ["2-1"],
  3: ["3-1", "3-2"]
}
```

---

Nice! You've completed the kata. If you want to continue, then you can try the following:

- Add a parameter to the function that allows the level names to be reversed. For example, if the function is called with `3` worlds and a levels array of `[3, 0, 2]`, then the function should return the following object:

  ```javascript
  {
    1: ["1-3", "1-2", "1-1"],
    2: ["2-1"],
    3: ["3-2", "3-1"]
  }
  ```
- Add a parameter to the function to specify the level separator. For example, if the function is called with `3` worlds and a levels array of `[3, 0, 2]` and a separator of `:`, then the function should return the following object:

  ```javascript
  {
    1: ["1:1", "1:2", "1:3"],
    2: ["2:1"],
    3: ["3:1", "3:2"]
  }
  ```

If you've done a implementation of this kata, then please submit a PR to add it to the list below:

- ooooh... be the first one to submit a implementation! (you can delete this line when you do)
