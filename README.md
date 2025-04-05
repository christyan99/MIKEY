--// Mikey Hub Base
local MikeyHub = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local Tabs = Instance.new("Frame")
local FarmTab = Instance.new("TextButton")
local TeleportTab = Instance.new("TextButton")
local MiscTab = Instance.new("TextButton")
local ConfigTab = Instance.new("TextButton")
local AutoAttackTab = Instance.new("TextButton")

--// GUI Settings
MikeyHub.Name = "MikeyHub"
MikeyHub.Parent = game.CoreGui
MikeyHub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = MikeyHub
Main.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
Main.BorderSizePixel = 0
Main.Position = UDim2.new(0.3, 0, 0.2, 0)
Main.Size = UDim2.new(0, 500, 0, 350)

Title.Name = "Title"
Title.Parent = Main
Title.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Title.Size = UDim2.new(1, 0, 0, 50)
Title.Font = Enum.Font.GothamBold
Title.Text = "Mikey Hub : Blox Fruits"
Title.TextColor3 = Color3.fromRGB(255, 255, 0)
Title.TextSize = 22.0

Tabs.Name = "Tabs"
Tabs.Parent = Main
Tabs.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
Tabs.Position = UDim2.new(0, 0, 0.15, 0)
Tabs.Size = UDim2.new(0, 120, 0, 295)

local function createTab(name, posY)
    local Tab = Instance.new("TextButton")
    Tab.Name = name .. "Tab"
    Tab.Parent = Tabs
    Tab.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
    Tab.Position = UDim2.new(0, 0, 0, posY)
    Tab.Size = UDim2.new(1, 0, 0, 40)
    Tab.Font = Enum.Font.GothamSemibold
    Tab.Text = name
    Tab.TextColor3 = Color3.fromRGB(255, 255, 255)
    Tab.TextSize = 16.0
    Tab.TextWrapped = true
    return Tab
end

FarmTab = createTab("Farm", 0)
TeleportTab = createTab("Teleport", 45)
MiscTab = createTab("Misc", 90)
AutoAttackTab = createTab("AutoAttack", 135)
ConfigTab = createTab("Config", 180)

--// Panel Ready!
print("Mikey Hub Base Loaded!")
