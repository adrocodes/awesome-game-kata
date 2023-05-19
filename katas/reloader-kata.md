# Reloader

## Iteration 1

You're building the next big FPS, your next task is to build a reloading function for the player's gun. The function will get 3 inputs:

- `ammo` - the current ammo count in the gun
- `clipSize` - the max ammo count for the gun
- `ammoInClip` - the current ammo in the clip

The function should return an object with 2 properties:

- `ammo` - the new ammo count in the gun
- `ammoInClip` - the new ammo in the clip

The function should return the following:

- `reload(10, 10, 0)` should return `{ ammo: 0, ammoInClip: 10 }`
- `reload(100, 7, 3)` should return `{ ammo: 96, ammoInClip: 7 }`
- `reload(2, 7, 3)` should return `{ ammo: 0, ammoInClip: 5 }`

## Iteration 2

Your game has pivoted to be a more realistic shooter. When they reload, regardless of how much ammo is left in the clip, the player will lose all the ammo in the clip. Update the function so that it returns the following:

- `reload(10, 10, 0)` should return `{ ammo: 0, ammoInClip: 10 }`
- `reload(100, 7, 3)` should return `{ ammo: 93, ammoInClip: 7 }`
- `reload(2, 7, 3)` should return `{ ammo: 0, ammoInClip: 2 }`
