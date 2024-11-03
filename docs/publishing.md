# Publishing to LuaRocks
This guide explains how to prepare and publish your Teal package to LuaRocks.

## Prerequisites

1. **LuaRocks Account**: Create an account on [LuaRocks](https://luarocks.org/) if you don’t have one.
2. **Rockspec File**: A `.rockspec` file describing your package.

## Test Locally
Before publishing, you can verify your `.rockspec` file by installing it locally:

```bash
luarocks make RandAO-0.1-1.rockspec
```
This ensures the package installs correctly and that dependencies are met.

## Publishing
1. Increment the Version Number:
 - Update the version field in your .rockspec file to reflect the new release (e.g., from 0.1-1 to 0.2-1).
 - Use a versioned source URL for stability, such as linking to a specific Git tag on GitHub.
2. Log in to LuaRocks from the command line (if prompted):
```bash
luarocks login
```
3. Upload your package:
```bash
luarocks upload RandAO-0.2-1.rockspec
```
LuaRocks will validate your .rockspec file and upload the package, making it publicly available for others to install.