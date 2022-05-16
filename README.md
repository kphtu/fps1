-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local TextLabel = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

TextLabel.Parent = ScreenGui
TextLabel.BackgroundColor3 = Color3.fromRGB(114, 193, 210)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(-0.0001090765, 0, -0.00116956513, 0)
TextLabel.Size = UDim2.new(0, 90, 0, 37)
TextLabel.Font = Enum.Font.Creepster
TextLabel.Text = "Fps:"
TextLabel.TextColor3 = Color3.fromRGB(5, 186, 65)
TextLabel.TextSize = 25.000
TextLabel.TextStrokeColor3 = Color3.fromRGB(255, 0, 0)

-- Scripts:

local function BOLHFYC_fake_script() -- TextLabel.LocalScript 
	local script = Instance.new('LocalScript', TextLabel)

	local RS = game:GetService("RunService")
	local frames = 0
	
	RS.RenderStepped:Connect(function()
		frames = frames + 1
	end)
	
	while wait(1) do
		script.Parent.Text = frames .. " FPS"
		frames = 0
	end
end
coroutine.wrap(BOLHFYC_fake_script)()
