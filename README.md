## For facilitating randomized gift exchange between hubbers (or whatever group of folks) using issue comments :gift:

### Setup:
- Make sure `EMAIL_DOMAIN`, `MAILGUN_API_KEY`, `GITHUB_ACCESS_TOKEN`, `MAILGUN_DOMAIN`,  `FROM_ADDRESS`, `CONTACT_HUBBER`, and `SUGGESTED_AMOUNT` in `gifthubber.rb` get changed to something relevant
- Figure out how you want to associate github usernames with email addresses; ideally this would be an API call to find the user and using the public email associated with them, but githubbers don't tend to set that field so I'm doing a hackier thing. :sob:

### To use:
- Make sure everyone's shipping address is accessible to the group somewhere (for githubbers, plz set a public address on Team). This ensures that I'm not storing private info anywhere that it isn't already available.
- Create an issue where participants can post a comment with their wishlist
- When there are enough people run `GiftHubber.distribute_gifts(repo, issue_number)` where the `repo` and `issue_number` correspond to the issue where everyone posted their wishlist. There doesn't need to be an even number of recipients.
- Emails pairing gift senders/recipients get sent!

### Thanks to

- [Dr Hannah Fry](https://www.youtube.com/watch?v=5kC5k5QBqcc) for the simple solution to the gift exchange problem
