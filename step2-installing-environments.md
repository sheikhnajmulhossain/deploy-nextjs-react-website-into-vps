# Installing environment

1. Installing git
`apt-get install git`

2.  Installing nodejs suing Docker with npm package manager

a. Pull the Node.js Docker image
`docker pull node:22-alpine`

b. Create a Node.js container and start a Shell session:
`docker run -it --rm --entrypoint sh node:22-alpine`

c. Verify the Node.js version:
`node -v`

d. Verify npm version:
`npm -v`