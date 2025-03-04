#Installing environment

1. Installing git
`apt-get install git`

2.  Installing nodejs suing Docker with npm package manager

# Pull the Node.js Docker image
`docker pull node:22-alpine`

# Create a Node.js container and start a Shell session:
`docker run -it --rm --entrypoint sh node:22-alpine`

# Verify the Node.js version:
`node -v`

# Verify npm version:
`npm -v`