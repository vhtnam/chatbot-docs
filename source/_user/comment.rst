Comment Rule
==============

.. NOTE:: System will process comments from top to bottom. When it found a rule, it will ignore other Comment Rules.


==============
Create a Comment Rule
==============


- Open a Bot Dashboard.
- Click  Comments from the left menu.

- Click Add.

.. image:: ../assets/images/comment.jpg

.. image:: ../assets/images/comment2.jpg


- Set name for this rule.

- Post type: Apply rule for all posts or just a specific post.

- Include keywords: only process comments included these keywords.

- Exclude keywords: ignore all comments included these keywords.

- Hashtag: apply rule with comments contains these hashtags.
 
- Track First level comment only: ignore 2nd level comment.

- Inbox customer with block: send a private reply to the commenter inbox.

- Reply Comment with Message: post a comment reply to this comment.

- Extra action: like, hide or remove this comment.

==============
Sort Comment Rules
==============

- In the Comment page, drag the Arrow button to move the comment up and down. 

.. image:: ../assets/images/comment3.jpg


==============
Comment Settings
==============

- Enable Comment Auto: uncheck to disable auto comment for all Bots.
- Reply comment after: system will process comment after this amount of time.

.. NOTE:: Commnent Timeout require Laravel Queue installed and running. If not, Bot will reply comment immediately.