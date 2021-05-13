# Athens-Research-SRS-System-With-Alfred
SRS System for Athens and Roam using Athens
## Requirements
* Mac with Alfred Installed 
* Alfred Powerpack
## Instructions to use “As is”
1. Download the `.alfredsnippets` file
2. Double click it
3. In the prompt that appears, uncheck the “Strip snippets of 'auto expand' flag” option
4. Change the keyword to auto expand if you want
5. Whenever you type the word in a page/block, it will auto expand
6. On every day that you have to review the note, it will appear on the unlinked referecned of the day you are in
## Instructions to recreate
1. Open Alfred preferences
2. Go to “features”
3. Click “Snippets” in the list that comes up
4. Click the `+` button to add a new item
5. Name the new item whatever you want
6. In the main “Snippet section”, type the following:
	Spaced Repetition Calendar
		First Review: [[{date +1d:MMMM dd, y}]]
		Second Review: [[{date +7d:MMMM dd, y}]]
		Third Review: [[{date +15d:MMMM dd, y}]]
		Fourth Review: [[{date +30d:MMMM dd, y}]]
		Fifth Review: [[{date +100d:MMMM dd, y}]]
		Sixth Review: [[{date +365d:MMMM dd, y}]]
7. Set the Keyword to what you want to type to trigger the SRS on the specific page. 
8. Check the “Auto Expansion option”
## Making changes to the system
### Change review interval
To ch ange the time between reviews, simply change the number in the edit snippet window. 
``+{"change this number"d:MMMM dd, y``
 
### Add a new review
Write the following syntax and put it after the the last review
		``{Review Number} Review: [[{date +{Time in days goes here}d:MMMM dd, y}]]``
### Remove a review
Simply delete line that contains the interval you want to delete
