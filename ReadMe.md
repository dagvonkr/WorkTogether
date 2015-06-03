Group Work Flow
===============
###Step 1: Create An Organization
- From your github dashboard create an Organization. Click on the + sign where you would add a repository, but select **New Organization**.

###Step: 2
- Once your organization has been created, it's time to include your team members. 

- You can add your team members as administrators or you can create a subteam and choose what kind of access they will have. 

- An administrator will be able to merge pull requests to the upstream master. If you -restrict your subteams they won't have this control.

- There are benefits and drawbacks to both ways, have your team decide what they'd like t do.

###Step: 3

Ok, now that you have your organization setup and you've invited your team, you need a repository to work from. 

1. Create a new repository within your organization

2. Now each team member should fork that repo to their personal github

3. Once you've forked the repo from the organization, clone **YOUR FORK** onto your local machine.

4. Now we need to set an **UPSTREAM MASTER** for the repo on your local machine.

5. Type ```git remote -v``` into the Terminal while in the directory of the repo you just forked. You'll see that your fork on github is the origin.

6. Now we'll add an **UPSTREAM MASTER**. Type ```git remote add upstream``` and paste the organizations repo url immediatley after the command. Hit enter.

Here is an example: ```remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git```






