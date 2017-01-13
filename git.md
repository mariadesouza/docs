#GIT 

## Known Errors and Solutions

* error: src refspec [branch] does not match any.

Created a new branch. Committed files. 
Tried git push origin [branch]. Got above error.
Resolved by:
>> git push origin HEAD:[branch] 

>> git show-ref to see what refs do you have. 

