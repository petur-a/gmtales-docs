# Definitions

The following is a rundown of the various elements that constitute GMTales.

## Campaigns

The focal object that contains everything else in a _campaign_. A campaign basically constitutes a group of players and a list of articles.

### Campaign visibility

A campaign is either public or hidden. If it is hidden, only the invited players will be able to access its content. 

## Players

_Players_ are the active users of the website. They have connections to campaigns based on certain roles. When a player writes a campaign article, we say that he is the _author_.

### Roles

A player which is connected to a campaign has a designated role. The possible roles are:

* _Creator_: The creator of the campaign. They have the following permissions:
  * Management of roles of other players.
  * Management of settings of the campaign (e.g. visibility).
  * Management of campaign status (i.e. whether it should be archived).
* _DM_: The main content writers of the campaign. Although everyone can contribute with articles, DMs are meant to symbolize the canonical world content. This is expressed in the following manner:
  * Their articles are considered for auto-linking.
  * Their articles are included under the DM author pane.

## Articles

_Articles_ are the content of the campaign. Their raison d'être is as a wall of text detailing the world, but they are complex objects containing an array of properties controlled through said text.

### Article visibility

Articles have three modes of visibility: 

* _All_ - Everyone (with access to the campaign) can see it.
* _DM_ - The author and the DMs can see it.
* _Secret_ - Only the author can see it.

### Labels

An article can have an indefinite collection of labels. Each label is a simple text snippet, and you can use them to categorize the article in various ways. Ultimately, the labels are meant to help with navigation.

### Types

An article can have one type. The type is meant to be a sort of "super-label", which precisely nails the article's nature. Ultimately, the type is meant to help with navigation.

### Relations

Articles have relations between them which are created dynamically, meaning any changes to the articles will be reflected in the relations if the heuristics conclude that a relation should be made.

Currently, there is a very simple heuristic: matching on the article's single-word title. The only additional rule is that non-alphanumeric symbols are pruned (e.g. plural apostrophe).

### Block visibility

Any subpart (block) of the article can have a fine-grained level of visibility decided by the author.

Again, there are two categories of block visibility: secret and DM blocks. Their behavior are identical to those of the visibility of the article.

### Notes

Articles can be appended with _notes_, which are a discussion board for the players around the article's content.

## Images

Images are another primitive in a campaign, next to articles. They are not uploaded with article writing, but they can be linked in articles. Any link to an image from an article will append a title and/or description to the image.
