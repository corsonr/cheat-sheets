# Install or Update NVM
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash`

# Check version
`node -v || node --version`

# List installed versions of node (via nvm)
`nvm ls`

# Install specific version of node
`nvm install <version>`

# Uninstall specific version of node
`nvm uninstall <version>`
(might need to run `nvm deactivate` if trying to uninstall active version of NVM)

# Set default version of node
`nvm alias default <version>`

# Switch version of node
`nvm use <version>`
