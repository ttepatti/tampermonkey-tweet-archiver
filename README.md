# tampermonkey-tweet-archiver
A tampermonkey script to make the archival of tweets easier. This script adds a copy button to the right side of a Tweet which exports the tweet in a CSV format, perfect for inserting into a spreadsheet.


## Overview

**Why?:** I wanted to archive tweets, but elon musk doesn't let me access the twitter API anymore

**How?:** Now that archiving tweets through the API is more difficult, one of the easiest ways to archive tweets is with a basic 'copy' button

This script is based off of screw-hand's amazing script [share-tweet-copy](https://github.com/screw-hand/tampermonkey-user.js/tree/main/share-tweet-copy).

I modified screw-hand's script to instead export tweets in a CSV format, that way they're easier to paste into a spreadsheet. I also added the tweet date and media URL fields.

## Example

Consider the below tweet from @github.

![GitHub Universe may be over for another year but you can keep on celebrating with our special #GitHubUniverse sale. Get your hands on all our awesome Universe swag, now discounted.](github_example_tweet.png)

Copying this tweet results in the following being added to your clipboard:

```
2024-11-28T11:11:11.000Z,@github,GitHub,"GitHub Universe may be over for another year but you can keep on celebrating with our special #GitHubUniverse sale. Get your hands on all our awesome Universe swag, now discounted. https://thegithubshop.com/sale",https://x.com/github/status/1862091865996005420,4,https://pbs.twimg.com/media/Gdd6nCtW0AAwur_?format=jpg&name=360x360,https://pbs.twimg.com/media/Gdd6oQMXgAELolw?format=jpg&name=360x360,https://pbs.twimg.com/media/Gdd6peXWEAAXApE?format=jpg&name=360x360,https://pbs.twimg.com/media/Gdd6qtTXYAEYdov?format=jpg&name=360x360
```

When split into a table, this leads to the following data:

| Date | Username | Display Name | Tweet Text | Tweet Link | Media Count | Media URL(s) |
| ---- | -------- | ------------ | ---------- | ---------- | ----------- | ------------ |
| 2024-11-28T11:11:11.000Z | @github | GitHub | "GitHub Universe may be over for another year but you can keep on celebrating with our special #GitHubUniverse sale. Get your hands on all our awesome Universe swag, now discounted. https://thegithubshop.com/sale" | https://x.com/github/status/1862091865996005420 | 4 | https://pbs.twimg.com/media/Gdd6nCtW0AAwur_?format=jpg&name=360x360,https://pbs.twimg.com/media/Gdd6oQMXgAELolw?format=jpg&name=360x360,https://pbs.twimg.com/media/Gdd6peXWEAAXApE?format=jpg&name=360x360,https://pbs.twimg.com/media/Gdd6qtTXYAEYdov?format=jpg&name=360x360 |

## Contributing

Feel free to file issues or PRs if you'd like to add on the script.

## Credits

This is basically just a dirty hack on top of screw-hand's existing script. Go check out screw-hand's other scripts, they're great and they built all of the base functionality!

[GitHub: screw-hand/tampermonkey-user.js](https://github.com/screw-hand/tampermonkey-user.js/tree/main)
