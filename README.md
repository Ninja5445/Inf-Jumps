local PabloLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/BatuKvi123/PabloLibV3/main/PabloLibV3"))()
local window = PabloLib:Create(
"Ninja Hub Test", -- Name here.
"Enabled", -- If you want draggable set here to "Enabled" if you dont want set to "Disabled".
"p" -- You can put any keybind here to open close.
)
local tab1 = window:CreateTab("Main")
local tab2 = window:CreateTab("Players")
local tab3 = window:CreateTab("Troll Animations Sus")
tab1:CreateInfo("Use This Script at your own risk of getting banned!!")
tab1:CreateSlider("Walk speed", 0,500, function(arg)
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

local slider = script.Parent:WaitForChild("Slider") -- Assuming the slider is a child of the script

slider.Changed:Connect(function()
    local speed = math.clamp(slider.Value, 0, 500)
    humanoid.WalkSpeed = speed
end)
