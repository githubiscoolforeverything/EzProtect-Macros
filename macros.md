***MACROS:***

EP_ENCRYPTCONSTANT - encrypts a constant

EP_CRASH - crashes the vm

EP_EQ - prevents most eq hooking [beta]

***Examples:***
```lua
local encryptedprint = EP_ENCRYPTCONSTANT(print)
encryptedprint("hello")
```

```lua
local key = "asd"

if key ~= "asd" then
EP_CRASH()
end
```

```lua 
EP_ENCRYPTCONSTANT(12345) 
```
- numbers are allowed

```lua
local username = "jjthegamer"
if EP_EQ(game.Players.LocalPlayer.Name,username) then
print("you are whitelisted!")
end
```

***Incorrect Usages:***

EP_CRASH:

EP_CRASH(true) - no arguments should be provided

EP_ENCRYPTCONSTANT:

EP_ENCRYPTCONSTANT(script.Parent)- there should only be one variable [note: i might make this work in a future update of ezprotect]

EP_ENCRYPTCONSTANT("print") - no strings should be provided

EP_EQ:

```lua
if EP_EQ(true) then - there is only one argument there must be 2 arguments
return
end
```
