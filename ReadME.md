# Basically Skidded Orion Library

# Getting The Loadstring
```lua
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/Unknownkellymc1/Orion/main/source')))()
```
# Creating Window
```lua
local Window = OrionLib:MakeWindow({Name = "Title of the library", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

--[[
Name = <string> - The name of the UI.
HidePremium = <bool> - Whether or not the user details shows Premium status or not.
SaveConfig = <bool> - Toggles the config saving in the UI.
ConfigFolder = <string> - The name of the folder where the configs are saved.
IntroEnabled = <bool> - Whether or not to show the intro animation.
IntroText = <string> - Text to show in the intro animation.
IntroIcon = <string> - URL to the image you want to use in the intro animation.
Icon = <string> - URL to the image you want displayed on the window.
CloseCallback = <function> - Function to execute when the window is closed.
]]
```
# Custom Key System
```lua
Delete The Orion Library Window Btw
local Window = OrionLib:MakeWindow({Name = "Key System", HidePremium = false, SaveConfig = true, IntroEnabled = false})

local GameId = game.PlaceId 
local GameName = 
game:GetService("MarketplaceService"):GetProductInfo(GameId).Name 

local plrs = game:GetService("Players") 
local plr = plrs.LocalPlayer 
local plrname = plr.name 
local plrid = plr.UserId local plrchr = plr.Character 
local plrage = plr.AccountAge 
local plrcount = #plrs:GetPlayers()

OrionLib:MakeNotification({
	Name = "Logged In!",
	Content = "Logged In As " .. plrname .. " ",
	Image = "rbxassetid://4483345998",
	Time = 2
})

getgenv().Key = " "
getgenv().KeyInput = "string"

function Destroy()
         OrionLib:Destroy()
end;

function CheckKey()
         if Key == KeyInput 
         then
               Destroy()
               CorrectKey()
               Script Here!
         end
end;

function CorrectKey()       
               OrionLib:MakeNotification({
	Name = "Correct Key!",
	Content = "Entered Correct Key",
	Image = "rbxassetid://4483345998",
	Time = 2
})
end

function IncorrectKey()       
               OrionLib:MakeNotification({
	Name = "Incorrect Key",
	Content = "Entered Incorrect Key, Please Enter The Correct Key",
	Image = "rbxassetid://4483345998",
	Time = 2
})
end


local Tab = Window:MakeTab({
	Name = "Key",
	Icon = "rbxassetid://7733960981",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Enter Key",
	Default = "",
	TextDisappear = false,
	Callback = function(Value)
		KeyInput = Value
	end	  
})

Tab:AddButton({
	Name = "Check Key",
	Callback = function()
              IncorrectKey()
              CheckKey()
    end
})

Tab:AddButton({
	Name = "Get Key",
	Callback = function()
              Key Link Here!
              OrionLib:MakeNotification({
	Name = "Key Link",
	Content = "Key Link Copied",
	Image = "rbxassetid://4483345998",
	Time = 2
})
    end
})

-- [
getgenv().Key = <string> - The Key
```
