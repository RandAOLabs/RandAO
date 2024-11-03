# RandAO Library

![Lua Version](https://img.shields.io/badge/lua-5.3%2B-blue.svg)
![Teal Version](https://img.shields.io/badge/teal-0.10%2B-lightblue.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/github/workflow/status/yourusername/RandAO/CI/main)](https://github.com/RandAOLabs/RandAO/actions)
[![LuaRocks](https://img.shields.io/badge/luarocks-RandAO-blue.svg)](https://luarocks.org/modules/yourusername/RandAO)
[![Issues](https://img.shields.io/github/issues/yourusername/RandAO)](https://github.com/RandAOLabs/RandAO/issues)

RandAO is a Teal library designed for requesting Verifiable randomness on AO.

## Installation

Install the package via [LuaRocks](https://luarocks.org/):


```bash
luarocks install RandAO
```
## Usage
```lua
local RandAO = require("RandAO")

local providers = { "provider1", "provider2", "provider3" }
local request_id = RandAO.request_randomness(providers)
local status = RandAO.check_request_status(request_id)

print("Request ID:", request_id)
print("Status:", status.fulfilled and "Fulfilled" or "Pending", status.result or "No result yet")
```