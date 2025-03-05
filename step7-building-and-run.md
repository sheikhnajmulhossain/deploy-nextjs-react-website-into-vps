# Building the project 

1. navigate to your repo file in vps
`cd filename`   

2. Install bun/npm (the package manager your using)
`npm install -g bun`
`bun install`
or
`npm install`

3. Run this command for temporary run or just go to step 4
a. for one time run 
`bun dev`
or for npm
`npm start`

b. for continues run in the vps background 
`bun dev &`
or for npm
`npm start &` 

4. The project will keep on running even after closing the terminal
` npm install -g pm2
pm2 start "bun dev"
pm2 save
pm2 startup `




