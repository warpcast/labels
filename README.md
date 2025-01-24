# Labels

Warpcast produces [labels](https://github.com/farcasterxyz/labels) to categorize Farcaster accounts which are made public here.

## [Spam](https://github.com/warpcast/labels/blob/main/spam.jsonl)

Warpcast's spam models predict the probability that an account might exhibit spammy behavior. Spam is defined as behavior that intentionally generates notifications for other users in a way that benefits the author and annoys users who receieve them. Some examples include replying with generic llm generated responses, bulk following accounts, posting irrelevant or generally offensive responses to other people's posts. Spamminess is not related to whether an account is being controlled by a human. There are many bots that are not spammy and many humans that are.

Our models make these predictions based on the combination of a number of factors including the account's historical activity, social graph, message content and the moderation actions that other users have taken on their account. No single factor will get an account labelled as spam. If you notice any obvious mislabelling, you can report them to @v on Warpcast DMs

Our dataset for spam has the label_type column is set to spam and the values can be one of:

| Value | Description                            |
|-------|----------------------------------------|
| 0     | Likely to engage in spammy behavior.   |
| 1     | Might engage in spammy behavior.       |
| 2     | Unlikely to engage in spammy behavior. |

Spam labels are updated weekly. Accounts that are not present are "unknown" either because there isn't enough data or because the account hasn't been active recently. 
