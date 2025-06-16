*******************
**Solution**
*******************

You can view the exact code changes needed to solve this coding challenge here: https://github.com/ScriabinOp8No12/avatar-name-enhancement-11xdev/pull/1/files#diff-b2d4e7413aed9dc28d0b0bff2da03c27287e6a913f633d142273f17379227410

This branch contains the avatar name enhancement code changes - you can test that the functionality works as intended in your browser.   

1. Move the refresh function from the child component NameSelection up to parent component CharacterSelection.  Rename it to regenerateUsername for clarity, then pass it down as a prop to the child component NameSelection. We also want to combine separate update functions into a single handleRaceChange async function.  This function detects when the race changes (not the race idx) so we can update the avatar name. These adjustments make it less likely we run into state synchronization bugs, and makes reading and maintaining the code easier. 

2. Make a helper function mimicking original data store logic so that the local data stores stay synchronized.  We can verify this works by refreshing the page after changing avatar types and/or indexes.  If you don't have these blocks of code, refreshing the page will lose the avatar changes.  

*******************
**Conclusion**
*******************

Combining related functions and centralizing coordinated logic in parent components can often reduce the likelihood of state synchronization bugs and also make the code more readable and maintainable!
