This is a Tutorial for ROBLOX Studio, in this you'll learn about the basics in ROBLOX Studio!








--Basics--

Roblox Studio is a platform where you could make games on!
One of the most important things about Roblox games is their scripting, because it makes the whole game.
Now, once you log into Roblox Studio, you get this Toolbox, Explorer and sometimes Properties.





--Explorer--

The Explorer is one of the many things to make games work.
There are 14 items you can use from, these include Workspace, Players, Lighting, Replicated First, Replicated Storage, Server Script Service, ServerStorage, Starter GUI, 
StarterPack, StarterPlayer, SoundService, Chat, LocalizationService and finnalyTestService. 
Now, that may sound like a lot but I will show you everthing.





--Getting Scripting--

To create your first lines of code, you will need to hover over the Workspace item and press the plus button (or just right click and it says inster object).
Once you've pressed it, it will show up a screen of a lot of things. Press or search "Script".
That will attach a Script to your Worskspace, and now you can get coding!



--One Piece Of Code--

Before we end this, I will give you one piece of code for a day and night script, a.k.a it turns day and night every second (or how much you want it too).




local dayLength = 12
local cycleTime = dayLength*60 --Edit This--
local minutesInADay = 24*60 --Edit This--
local lighting = game:GetService("Lighting")
local startTime = tick() - (lighting:getMinutesAfterMidnight() / minutesInADay)*cycleTime
local endTime = startTime + cycleTime
local timeRatio = minutesInADay / cycleTime
if dayLength == 0 then
	dayLength = 1
end
repeat
	local currentTime = tick()
	if currentTime > endTime then
		startTime = endTime
		endTime = startTime + cycleTime
	end
	lighting:setMinutesAfterMidnight((currentTime - startTime)*timeRatio)
	wait(1/15)


until false


--Stay Tuned For Part 2, Getting Models and Scripting Them--

Stay tuned for Part 2, remember to Favorite this topic, and have a fabulous day!
