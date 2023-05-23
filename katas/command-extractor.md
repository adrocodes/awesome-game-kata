# Command Extractor

## Iteration 1

You are building a text adventure where the player can enter a command made up of a verb and a noun. For example, `go north` or `take sword`. You need to extract the verb and noun from the command so you can process it. The verb will always be a single word and the noun can be one or more words.

### Examples

| Command | Verb | Noun |
|---------|------|------|
| `go north` | `go` | `north` |
| `take sword` | `take` | `sword` |
| `use magic wand` | `use` | `magic wand` |

Your function should accept a string and return an object with two properties: `verb` and `noun`.

## Iteration 2

You have realised that it is tedious to use 1 item at a time, you want to update the command to allow for a quantity of items to be used. For example, `use 3 magic wands` or `use 1 magic wand`. This quantity is optional and if not provided should default to 1, the quantity will always be numeric and a whole number.

### Examples

| Command | Verb | Noun | Quantity |
|---------|------|------|----------|
| `use magic wand` | `use` | `magic wand` | `1` |
| `use 3 magic wands` | `use` | `magic wands` | `3` |
| `use 1 magic wand` | `use` | `magic wand` | `1` |

Your function should accept a string and return an object with three properties: `verb`, `noun` and `quantity`.
