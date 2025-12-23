-- [[ Sami Menu: Teleport Version ]]
local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local TeleportBtn = Instance.new("TextButton")
local SubMenu = Instance.new("Frame")
local SpawnBtn = Instance.new("TextButton")

ScreenGui.Parent = game.CoreGui
MainFrame.Size = UDim2.new(0, 200, 0, 150)
MainFrame.Position = UDim2.new(0.5, -100, 0.5, -75)
MainFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
MainFrame.Active = true
MainFrame.Draggable = true
MainFrame.Parent = ScreenGui

TeleportBtn.Size = UDim2.new(0, 180, 0, 40)
TeleportBtn.Position = UDim2.new(0, 10, 0, 10)
TeleportBtn.Text = "TELEPORT"
TeleportBtn.Parent = MainFrame

SubMenu.Size = UDim2.new(0, 180, 0, 50)
SubMenu.Position = UDim2.new(0, 10, 0, 60)
SubMenu.Visible = false
SubMenu.Parent = MainFrame

SpawnBtn.Size = UDim2.new(1, 0, 1, 0)
SpawnBtn.Text = "Go to Spawn"
SpawnBtn.Parent = SubMenu

TeleportBtn.MouseButton1Click:Connect(function()
    SubMenu.Visible = not SubMenu.Visible
end)

SpawnBtn.MouseButton1Click:Connect(function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0, 50, 0)
end)
