Group Work Flow
===============
###Step 1: Create An Organization
- From your github dashboard create an Organization. Click on the + sign where you would add a repository, but select **New Organization**.

###Step 2: Add Team Members
- Once your organization has been created, it's time to include your team members. 

- You can add your team members as administrators or you can create a subteam and choose what kind of access they will have. You will also have to specify which organization repositories the team will have access to. Look around the dashboard it's fairly intuitive.

- An administrator will be able to merge pull requests to the upstream master. If you restrict your subteams they won't have this control.

- There are benefits and drawbacks to both ways, have your team decide what they'd like t do.

###Step 3: Fork and add Upstream Master

Ok, now that you have your organization setup, and you've invited your team, you need a repository to work from. 

1. Create a new repository within your organization

2. Now each team member should fork that repo to their personal github

3. Once you've forked the repo from the organization, clone **YOUR FORK** onto your local machine.

4. Now we need to set an **UPSTREAM MASTER** for the repo on your local machine.

5. Type ```git remote -v``` into the Terminal while in the directory of the repo you just forked. You'll see that your fork on github is the origin.

6. Now we'll add an **UPSTREAM MASTER**. Type ```git remote add upstream``` and paste the organizations repo url immediatley after the command. Hit enter.

	Here is an example: 
	
		git remote add upstream ORIGINAL_OWNER ORIGINAL_REPO URL

	Just use the clone url from the organizations repository.

###Step 4: Update your Fork and the Upstream Master

- Now you can pull changes from the upstream master with 

		git pull upstream master
        
- To prepare for a pull request do the following.
	1. Push your changes to your forks origin master.

			git add (. OR * OR filename) - if you want to know exactly what these do google it
            git commit -m YOUR MESSAGE
			git push origin master
        
   	Now your fork has the changes you made on your machine.
    2. Submit a pull request from your fork. Then, whoever is administrating the repository for the organization can approve the pull request. This will update the upstream master incorporating your forks code.
   
- Everytime a new pull request is merged to the upstream master everybody on the team should update their forks. Run the following command.

		git pull upstream master

- That's it, you should now be able to work as a team. Good luck and may you have fewer merge conflicts.
