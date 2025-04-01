# Sprint02

## Day One

### Tasks Completed
Began work on styling the second section of the quiz. Added in images to match the paths department. Worked on updating the the progression bar however this was later changed again.

### Tasks To Do
Fix some of the sliders as currently their state is not always recognised when the user wants to go to the next section. Start work on the results page.  

### Issues
At the end of day one the the database was disabled. This was due to the server being set up on the wrong mode where the credit would deplete very quickly.

## Day Two

### Tasks Completed
Fixed the database by migrating it from Shehabs account to mine and selecting the correct mode so we could continue working on the project. Started work on the results page by taking the fraction of their role score and converting it into a percentage and using that percentage to display 1/3 colours: green, orange or red.
Updated session management to make sure users with no account could still view their results using a UserID of "-1" in the URL so the results page knows which prompts and page layouts to display. Fix the sliders so that the user can continue the quiz after going down particular paths.

### Tasks To Do
Start on the recruitment page. Update database to create recruiter accounts.

### Issues
The chances of a user receiving a acore above 60% on any particular role was very small as they had to follow an exact path and so when they view their results, a lot of the compatibility percentages where very low which could push them away from applying. We added a boost to the results they got by looking at what a 100% compatability ratio would look like.

## Day Three

### Tasks Completed
Built the recruitment page. First designed a layout for the page and then begin pulling the data from the results table. First pull the top roles, then departments and then the top roles for each department so the recruiter could view them individually. Also displayed the top candidates depending on the compatibility percentage they recieved on the quiz.
Also removed the Next button at the top left (which would navigate to the index) as we couldnt send the sessionID or UserID when a user clicks that button. Updated the database to remove columns which we no longer needed on "User". 

### Tasks To Do
Remove user answers when a user completes the quiz as the database pulls all records every time which slows down the website. Add the sessionID to the icon button in the top left.

### Issues
The icon login button in the top right needs to transfer the sessionID however the button is apart of the blazor layout and not the page and so, using an event call back, we could send the data. Although the layout now had the correct data, a blazor layout cannot have an interactive rendermode and so buttons cannot not work, only nav links which themselves cannot send data.

## Day Four

### Tasks Completed
Change the icon button layout to be displayed on the main page but to be displayed on top of the nav bar to appear as though it is still apart of the layout. This meant the button could transfer the sessionID. Removed the borders for the buttons which were changed from nav links to <button>. Fixed the sessionID not incrementing correctly when a user overtakes another user when taking the quiz at the same time.
The sessionID would only take the last value and not the highest which meant a new user would get a previous users answers already selected. 

### Tasks To Do
Start on the final touches for the website such as the department images and and titles. 

### Issues
When a user wants to register after completing the quiz, they are unable to do so as the database is not updated and so the results that would be displayed after they sign in would not exist as the that particular UserID wouldnt have results in the results table.

## Day Five

### Tasks Completed
Fixed the issue with the user registering after completing the quiz. The issue with the results table not updating to include the UserID was to do with async operations on the database. If one action is not finished, another action cannot be started. After looking online I found that this is an issue with threading as they share threads and so you need to just work around it.
Completed some final touches: updated the images and updated the second progress bar to look the same as the first one.

### Tasks To Do
Begin planning the presentation. Finish the slides to include all stages of the project. Record a backup video displaying how the website works if it breaks on the day. Script a demonstration. 

### Issues
Only final issue is disappearing icons which we have not been able to fix since the first sprint however this is only a minor problem with the functionality of the page.
