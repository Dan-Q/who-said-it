# Who Said It?

A quick game I threw together to entertain some friends. It presents quotes from a shared WhatsApp group and challenges players to remember/guess who originally said them.

![Screenshot of a game in progress](https://user-images.githubusercontent.com/53293/156233526-4814d081-8980-4bbc-a36c-b97113dd535a.png)

Our private instance is not available, but you can take a copy of this project and adapt it for your own use by following the instructions below.

## Setup

1. Clone this repository.
2. Create a `data.json` file in its directory with the format described below.
3. Host the directory on a webserver and visit `index.html`.

### `data.json` format

The JSON data file is an array of objects. Each object must include a `"date"` (any format; used for display only), `"speaker"` (the person who said the quote), and `"message"` (either a string or an array of strings). It may also include an `"alwaysInclude"`, an array of names of strings of other speakers who will always appear in the list of possible guesses. E.g.:

```
[
	{
		"date": "01/02/2003",
		"speaker": "Alice",
		"message": [ "Hi, I'm Alice!", "I wrote two messages." ],
	},
	{
		"date": "02/03/2004",
		"speaker": "Bob",
		"message": "You might think this message was written by Alice. But was it?",
		"alwaysInclude": [ "Alice" ]
	},
	{
		"date": "03/04/2005",
		"speaker": "Chris",
		"message": "This is very quotable."
	},
	{
		"date": "04/05/2006",
		"speaker": "Chris",
		"message": "This is also very quotable."
	},
	{
		"date": "05/06/2007",
		"speaker": "Debbie",
		"message": [ "Hey, I made a game! Come to this URL and see if you can remember who-said-what:", "https://example.com/" ]
	}
]
```
