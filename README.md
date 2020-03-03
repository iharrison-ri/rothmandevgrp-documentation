# Documentation

*Deployment Method*

The application services are run with pm2. You can find documentation and a video tutorial here:

`https://pm2.keymetrics.io/`

`https://www.youtube.com/watch?v=53tT4-3dOYs&t=339s`

I recommend looking at the video first to get a high-level understanding of what pm2 is as a technology. Then jump into the documentation to get a more granular understanding of the module.

When initially starting a process on the server, use the following steps:

1. Open the terminal as an Administrator
2. run `pm2 ls` to check that pm2 is available. If so, move on to number 7
3. If you get an error that says `no such file or directory, open 'H:\.pm2\module_conf.json'` drive continues to step 4.
4. Open a folder and navigate to anywhere in the `H` drive
5. Right-click the folder location and run `Git Bash Here`
6. This will open a `Bash` terminal in that location. Try running `pm2 ls` again. This opens up a table in the terminal
7. The table that shows in the terminal should look like the following: `https://pm2.keymetrics.io/assets/pm2-list.png`
7. Navigate to the folder you want to start the app and continue to the next steps.

*PPA startup*

1. Navigate to the react route folder `cd C:\apps\qa\patientphotoapp\rothman_UI\Sprint-2_latest`
2. run `pm2 start node_modules/react-scripts/scripts/start.js --name <name>` 
3. Navigate to the node root folder `cd C:\apps\qa\patientphotoapp\restAPI_Dev`
4. run `pm2 start bin/www --name <name>`

*OrthoNav startup*

1. Navigate to the react route folder
2. run `npm run-script build:dev` or `npm run-script build:prod` depending on the environment
3. Navigate to the node root folder
4. run `pm2 start rothman-rest.js`

The `<name>` parameter could be anything you want. Just be sure to name is descriptively

*GitHub workflow*

Github is the version control system Rothman uses to store code from our custom apps. Knowing the basic git commands and having a high-level understanding of what GitHub is recommended before using it.

An easy to read document for Git can to found here:

`https://rogerdudler.github.io/git-guide/`

Always pull from the development branch before creating a new branch. This keeps your code up to date and prevents merging conflicts. Therefore, the best way to keep your branches clean is by keeping an updated version of QA on your machine. Run this command to update you QA branch

`git pull origin QA`

After pulling the lasts QA branch, create your own branch following the following naming convention:

`Bug/TicketDescription`

`Feature/TicketDescription`

Keeping this naming convention helps standardize the branch creation process and keeps branches organized. Be sure to give your branch a descriptive name. You should be able to reference it by looking at the name and not the code.

Then run the following code:

`git checkout –b BranchName`

`git checkout` is a command used to switch branches. Adding the `–b` flag indicates that we are creating the new branch. The branch name will following the naming convention outlined above.

Note: the only branch a new branch should stem from is the QA branch. Avoid making branches from other branches because this could cause errors and unforeseen side effects.

If you have been working on a branch for a while and you want to pull in all of the changes from QA run: git pull origin QA while on your branch.
