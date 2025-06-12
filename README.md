*******************
***Solution***
*******************

You can view the exact code changes needed to solve this coding challenge here: https://github.com/ScriabinOp8No12/avatar-name-enhancement-11xdev/pull/1/files#diff-b2d4e7413aed9dc28d0b0bff2da03c27287e6a913f633d142273f17379227410

This branch contains the avatar name enhancement - you can test that the functionality works as intended in your browser.   

1. First, we will want to move the refresh function out from the NameSelection child component and into the parent component, we will rename it to "regenerate" for clarity, then pass it down from parent to child.

2. Next we will combine all the original function logic (update, update_avatar, and refresh) together, otherwise you may notice that the local state doesn't sync properly.  This might appear as the avatar name rapidly changing before settling on a final avatar name.  Combining the logic also makes the code easier to follow and maintain later.

