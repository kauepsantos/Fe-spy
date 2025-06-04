--[[

Scripts by ._.kinzin 👻  
UI by deusferrinho 👑  
(All Discord usernames)
Converted by G2L by @uniquadev  

]]

local INJECTION_METHOD = "CoreGui"
--[[^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Methods:
"CoreGui" (Create Gui on CoreGui)
"PlayerGui" (Create Gui on PlayerGui)
"Bypass" (Bypass most Gui AntiCheats)

local INJECTION_METHOD = "CoreGui"
local INJECTION_METHOD = "PlayerGui"
local INJECTION_METHOD = "Bypass"
]]


if _G.Stelly == true then
	local Notify = _G.Notify
	Notify("StellySpy V3", "StellySpy V3 Already Executed!", 10);
else
	_G.Stelly = true
	_G.InjectMethod = INJECTION_METHOD
	local G2L = {};
	if INJECTION_METHOD == "Bypass" then
		local p=game.Players.LocalPlayer
		local g=p:WaitForChild("PlayerGui")

		local f=function() 
			local t={}
			for _,v in pairs(g:GetChildren()) do
				if v:IsA("ScreenGui") then table.insert(t,v) end
			end
			if #t>0 then return t[math.random(1,#t)] end
		end

		local s=f()
		if s then
			s.ResetOnSpawn=false
			s.Enabled=true
			G2L["1"] = s
		end
	else
		G2L["1"] = Instance.new("ScreenGui");
		G2L["1"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;
		G2L["1"]["ResetOnSpawn"] = false;
		if INJECTION_METHOD == "PlayerGui" then
			G2L["1"]["Parent"] =  game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui");
		elseif INJECTION_METHOD == "CoreGui" then
			G2L["1"]["Parent"] =  game:GetService("CoreGui")
		end
	end

G2L["2"] = Instance.new("Folder", G2L["1"]);
G2L["2"]["Name"] = [[Client]];


-- StarterGui.AAGGXENOSS.Client.SetCore
G2L["3"] = Instance.new("LocalScript", G2L["2"]);
G2L["3"]["Name"] = [[SetCore]];


-- StarterGui.AAGGXENOSS.Client.Name
G2L["4"] = Instance.new("LocalScript", G2L["2"]);
G2L["4"]["Name"] = [[Name]];


-- StarterGui.AAGGXENOSS.Client.Notify
G2L["5"] = Instance.new("ModuleScript", G2L["2"]);
G2L["5"]["Name"] = [[Notify]];


-- StarterGui.AAGGXENOSS.Frame
G2L["6"] = Instance.new("Frame", G2L["1"]);
G2L["6"]["Visible"] = false;
G2L["6"]["BorderSizePixel"] = 0;
G2L["6"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["6"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
G2L["6"]["Size"] = UDim2.new(0, 425, 0, 250);
G2L["6"]["Position"] = UDim2.new(0.5, 0, 0.5, 0);
G2L["6"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["6"]["BackgroundTransparency"] = 1;


-- StarterGui.AAGGXENOSS.Frame.TopBar
G2L["7"] = Instance.new("Frame", G2L["6"]);
G2L["7"]["BorderSizePixel"] = 0;
G2L["7"]["BackgroundColor3"] = Color3.fromRGB(39, 37, 40);
G2L["7"]["AnchorPoint"] = Vector2.new(0.5, 0);
G2L["7"]["Size"] = UDim2.new(1, 0, 0.08, 0);
G2L["7"]["Position"] = UDim2.new(0.5, 0, 0, 0);
G2L["7"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["7"]["Name"] = [[TopBar]];


-- StarterGui.AAGGXENOSS.Frame.TopBar.X
G2L["8"] = Instance.new("ImageButton", G2L["7"]);
G2L["8"]["BorderSizePixel"] = 0;
G2L["8"]["ScaleType"] = Enum.ScaleType.Fit;
G2L["8"]["BackgroundColor3"] = Color3.fromRGB(38, 36, 39);
G2L["8"]["AnchorPoint"] = Vector2.new(1, 0.5);
G2L["8"]["Image"] = [[rbxassetid://10002373478]];
G2L["8"]["Size"] = UDim2.new(0.04706, 0, 1, 0);
G2L["8"]["BackgroundTransparency"] = 1;
G2L["8"]["Name"] = [[X]];
G2L["8"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["8"]["Position"] = UDim2.new(1, 0, 0.5, 0);


-- StarterGui.AAGGXENOSS.Frame.TopBar.X.LocalScript
G2L["9"] = Instance.new("LocalScript", G2L["8"]);



-- StarterGui.AAGGXENOSS.Frame.TopBar.X.2
G2L["a"] = Instance.new("LocalScript", G2L["8"]);
G2L["a"]["Name"] = [[2]];


-- StarterGui.AAGGXENOSS.Frame.TopBar.V3
G2L["b"] = Instance.new("TextLabel", G2L["7"]);
G2L["b"]["TextWrapped"] = true;
G2L["b"]["BorderSizePixel"] = 0;
G2L["b"]["TextSize"] = 12;
G2L["b"]["TextScaled"] = true;
G2L["b"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["b"]["FontFace"] = Font.new([[rbxasset://fonts/families/GothamSSm.json]], Enum.FontWeight.Bold, Enum.FontStyle.Normal);
G2L["b"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["b"]["BackgroundTransparency"] = 1;
G2L["b"]["Size"] = UDim2.new(0.06059, 0, 1, 0);
G2L["b"]["BorderColor3"] = Color3.fromRGB(255, 255, 255);
G2L["b"]["Text"] = [[V3]];
G2L["b"]["AutomaticSize"] = Enum.AutomaticSize.X;
G2L["b"]["Name"] = [[V3]];
G2L["b"]["Position"] = UDim2.new(0.15294, 0, 0, 0);


-- StarterGui.AAGGXENOSS.Frame.TopBar.V3.UITextSizeConstraint
G2L["c"] = Instance.new("UITextSizeConstraint", G2L["b"]);
G2L["c"]["MaxTextSize"] = 15;
G2L["c"]["MinTextSize"] = 15;


-- StarterGui.AAGGXENOSS.Frame.TopBar.V3.LocalScript
G2L["d"] = Instance.new("LocalScript", G2L["b"]);



-- StarterGui.AAGGXENOSS.Frame.TopBar.V3.mobile
G2L["e"] = Instance.new("LocalScript", G2L["b"]);
G2L["e"]["Name"] = [[mobile]];


-- StarterGui.AAGGXENOSS.Frame.TopBar.V3.2
G2L["f"] = Instance.new("LocalScript", G2L["b"]);
G2L["f"]["Name"] = [[2]];


-- StarterGui.AAGGXENOSS.Frame.TopBar.Name
G2L["10"] = Instance.new("TextLabel", G2L["7"]);
G2L["10"]["TextWrapped"] = true;
G2L["10"]["BorderSizePixel"] = 0;
G2L["10"]["TextSize"] = 12;
G2L["10"]["TextScaled"] = true;
G2L["10"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["10"]["FontFace"] = Font.new([[rbxasset://fonts/families/GothamSSm.json]], Enum.FontWeight.Bold, Enum.FontStyle.Normal);
G2L["10"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["10"]["BackgroundTransparency"] = 1;
G2L["10"]["Size"] = UDim2.new(0.16933, 0, 1, 0);
G2L["10"]["BorderColor3"] = Color3.fromRGB(255, 255, 255);
G2L["10"]["Text"] = [[StellySpy]];
G2L["10"]["AutomaticSize"] = Enum.AutomaticSize.X;
G2L["10"]["Name"] = [[Name]];
G2L["10"]["Position"] = UDim2.new(-0.00227, 0, 0, 0);


-- StarterGui.AAGGXENOSS.Frame.TopBar.Name.UITextSizeConstraint
G2L["11"] = Instance.new("UITextSizeConstraint", G2L["10"]);
G2L["11"]["MaxTextSize"] = 15;
G2L["11"]["MinTextSize"] = 15;


-- StarterGui.AAGGXENOSS.Frame.TopBar.Name.LocalScript
G2L["12"] = Instance.new("LocalScript", G2L["10"]);



-- StarterGui.AAGGXENOSS.Frame.TopBar.Name.2
G2L["13"] = Instance.new("LocalScript", G2L["10"]);
G2L["13"]["Name"] = [[2]];


-- StarterGui.AAGGXENOSS.Frame.resizer
G2L["14"] = Instance.new("Frame", G2L["6"]);
G2L["14"]["SizeConstraint"] = Enum.SizeConstraint.RelativeXX;
G2L["14"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["14"]["ClipsDescendants"] = true;
G2L["14"]["Size"] = UDim2.new(0.07059, 0, 24.064, 0);
G2L["14"]["Position"] = UDim2.new(0.92941, 0, 0.872, 0);
G2L["14"]["BorderColor3"] = Color3.fromRGB(28, 43, 54);
G2L["14"]["Name"] = [[resizer]];
G2L["14"]["BackgroundTransparency"] = 1;


-- StarterGui.AAGGXENOSS.Frame.resizer.dragger
G2L["15"] = Instance.new("ImageButton", G2L["14"]);
G2L["15"]["BorderSizePixel"] = 0;
G2L["15"]["BackgroundColor3"] = Color3.fromRGB(255, 86, 0);
G2L["15"]["ZIndex"] = 2;
G2L["15"]["Size"] = UDim2.new(1.9, 0, 0.04338, 0);
G2L["15"]["BackgroundTransparency"] = 1;
G2L["15"]["Name"] = [[dragger]];
G2L["15"]["BorderColor3"] = Color3.fromRGB(28, 43, 54);


-- StarterGui.AAGGXENOSS.Frame.resizer.dragger.UICorner
G2L["16"] = Instance.new("UICorner", G2L["15"]);
G2L["16"]["CornerRadius"] = UDim.new(0.5, 0);


-- StarterGui.AAGGXENOSS.Frame.reziserMain
G2L["17"] = Instance.new("LocalScript", G2L["6"]);
G2L["17"]["Name"] = [[reziserMain]];


-- StarterGui.AAGGXENOSS.Frame.resizerModule
G2L["18"] = Instance.new("ModuleScript", G2L["6"]);
G2L["18"]["Name"] = [[resizerModule]];


-- StarterGui.AAGGXENOSS.Frame.Remotes
G2L["19"] = Instance.new("ScrollingFrame", G2L["6"]);
G2L["19"]["Active"] = true;
G2L["19"]["ZIndex"] = 10;
G2L["19"]["BorderSizePixel"] = 0;
G2L["19"]["CanvasSize"] = UDim2.new(0, 0, 0, 0);
G2L["19"]["ElasticBehavior"] = Enum.ElasticBehavior.Always;
G2L["19"]["BackgroundColor3"] = Color3.fromRGB(21, 21, 21);
G2L["19"]["Name"] = [[Remotes]];
G2L["19"]["ScrollBarImageTransparency"] = 1;
G2L["19"]["HorizontalScrollBarInset"] = Enum.ScrollBarInset.Always;
G2L["19"]["AnchorPoint"] = Vector2.new(0, 0.5);
G2L["19"]["AutomaticCanvasSize"] = Enum.AutomaticSize.Y;
G2L["19"]["Size"] = UDim2.new(0.29412, 0, 0.92, 0);
G2L["19"]["ScrollBarImageColor3"] = Color3.fromRGB(0, 0, 0);
G2L["19"]["Position"] = UDim2.new(0, 0, 0.54, 0);
G2L["19"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["19"]["ScrollBarThickness"] = 0;
G2L["19"]["LayoutOrder"] = 1;


-- StarterGui.AAGGXENOSS.Frame.Remotes.UIPadding
G2L["1a"] = Instance.new("UIPadding", G2L["19"]);
G2L["1a"]["PaddingTop"] = UDim.new(0, 10);
G2L["1a"]["PaddingLeft"] = UDim.new(0, 10);


-- StarterGui.AAGGXENOSS.Frame.Remotes.Infoupdts
G2L["1b"] = Instance.new("TextButton", G2L["19"]);
G2L["1b"]["TextWrapped"] = true;
G2L["1b"]["BorderSizePixel"] = 0;
G2L["1b"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["1b"]["TextSize"] = 14;
G2L["1b"]["TextScaled"] = true;
G2L["1b"]["BackgroundColor3"] = Color3.fromRGB(25, 25, 25);
G2L["1b"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.SemiBold, Enum.FontStyle.Normal);
G2L["1b"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
G2L["1b"]["Size"] = UDim2.new(0, 100, 0, 22);
G2L["1b"]["BackgroundTransparency"] = 0.8;
G2L["1b"]["Name"] = [[Infoupdts]];
G2L["1b"]["BorderColor3"] = Color3.fromRGB(94, 97, 103);
G2L["1b"]["Text"] = [[Info & updts]];
G2L["1b"]["Position"] = UDim2.new(0.45248, 0, 0.32273, 0);


-- StarterGui.AAGGXENOSS.Frame.Remotes.Infoupdts.border
G2L["1c"] = Instance.new("Frame", G2L["1b"]);
G2L["1c"]["BorderSizePixel"] = 0;
G2L["1c"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["1c"]["Size"] = UDim2.new(0.04, 0, 1, 0);
G2L["1c"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["1c"]["Name"] = [[border]];


-- StarterGui.AAGGXENOSS.Frame.Remotes.Infoupdts.UITextSizeConstraint
G2L["1d"] = Instance.new("UITextSizeConstraint", G2L["1b"]);
G2L["1d"]["MaxTextSize"] = 17;


-- StarterGui.AAGGXENOSS.Frame.Remotes.Infoupdts.Animate
G2L["1e"] = Instance.new("LocalScript", G2L["1b"]);
G2L["1e"]["Name"] = [[Animate]];


-- StarterGui.AAGGXENOSS.Frame.Remotes.Infoupdts.UIStroke
G2L["1f"] = Instance.new("UIStroke", G2L["1b"]);
G2L["1f"]["Transparency"] = 0.5;
G2L["1f"]["ApplyStrokeMode"] = Enum.ApplyStrokeMode.Border;
G2L["1f"]["Color"] = Color3.fromRGB(224, 224, 224);


-- StarterGui.AAGGXENOSS.Frame.Remotes.Infoupdts.Function
G2L["20"] = Instance.new("LocalScript", G2L["1b"]);
G2L["20"]["Name"] = [[Function]];


-- StarterGui.AAGGXENOSS.Frame.Remotes.Remote1
G2L["21"] = Instance.new("TextButton", G2L["19"]);
G2L["21"]["TextWrapped"] = true;
G2L["21"]["BorderSizePixel"] = 0;
G2L["21"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["21"]["TextSize"] = 14;
G2L["21"]["TextScaled"] = true;
G2L["21"]["BackgroundColor3"] = Color3.fromRGB(25, 25, 25);
G2L["21"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.SemiBold, Enum.FontStyle.Normal);
G2L["21"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
G2L["21"]["Size"] = UDim2.new(0, 100, 0, 22);
G2L["21"]["BackgroundTransparency"] = 0.8;
G2L["21"]["Name"] = [[Remote1]];
G2L["21"]["BorderColor3"] = Color3.fromRGB(94, 97, 103);
G2L["21"]["Text"] = [[RemoteName]];
G2L["21"]["Visible"] = false;
G2L["21"]["Position"] = UDim2.new(2.328, 0, 0.81304, 0);


-- StarterGui.AAGGXENOSS.Frame.Remotes.Remote1.border
G2L["22"] = Instance.new("Frame", G2L["21"]);
G2L["22"]["BorderSizePixel"] = 0;
G2L["22"]["BackgroundColor3"] = Color3.fromRGB(0, 171, 255);
G2L["22"]["Size"] = UDim2.new(0.04, 0, 1, 0);
G2L["22"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["22"]["Name"] = [[border]];


-- StarterGui.AAGGXENOSS.Frame.Remotes.Remote1.UITextSizeConstraint
G2L["23"] = Instance.new("UITextSizeConstraint", G2L["21"]);
G2L["23"]["MaxTextSize"] = 14;


-- StarterGui.AAGGXENOSS.Frame.Remotes.Remote1.Animate
G2L["24"] = Instance.new("LocalScript", G2L["21"]);
G2L["24"]["Name"] = [[Animate]];


-- StarterGui.AAGGXENOSS.Frame.Remotes.Remote1.UIStroke
G2L["25"] = Instance.new("UIStroke", G2L["21"]);
G2L["25"]["Transparency"] = 0.5;
G2L["25"]["ApplyStrokeMode"] = Enum.ApplyStrokeMode.Border;
G2L["25"]["Color"] = Color3.fromRGB(224, 224, 224);


-- StarterGui.AAGGXENOSS.Frame.Remotes.UIListLayout
G2L["26"] = Instance.new("UIListLayout", G2L["19"]);
G2L["26"]["Padding"] = UDim.new(0, 5);
G2L["26"]["SortOrder"] = Enum.SortOrder.LayoutOrder;


-- StarterGui.AAGGXENOSS.Frame.Remotes.CanvasSize
G2L["27"] = Instance.new("LocalScript", G2L["19"]);
G2L["27"]["Name"] = [[CanvasSize]];


-- StarterGui.AAGGXENOSS.Frame.Assets
G2L["28"] = Instance.new("Folder", G2L["6"]);
G2L["28"]["Name"] = [[Assets]];


-- StarterGui.AAGGXENOSS.Frame.Buttons
G2L["29"] = Instance.new("ScrollingFrame", G2L["6"]);
G2L["29"]["Active"] = true;
G2L["29"]["SizeConstraint"] = Enum.SizeConstraint.RelativeYY;
G2L["29"]["ZIndex"] = 12;
G2L["29"]["BorderSizePixel"] = 0;
G2L["29"]["CanvasSize"] = UDim2.new(0, 0, 0, 0);
G2L["29"]["BackgroundColor3"] = Color3.fromRGB(21, 21, 21);
G2L["29"]["Name"] = [[Buttons]];
G2L["29"]["AutomaticCanvasSize"] = Enum.AutomaticSize.XY;
G2L["29"]["Size"] = UDim2.new(0, 300, 0, 85);
G2L["29"]["ScrollBarImageColor3"] = Color3.fromRGB(0, 0, 0);
G2L["29"]["Position"] = UDim2.new(0.29412, 0, 0.66, 0);
G2L["29"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["29"]["ScrollBarThickness"] = 0;


-- StarterGui.AAGGXENOSS.Frame.Buttons.UIPadding
G2L["2a"] = Instance.new("UIPadding", G2L["29"]);
G2L["2a"]["PaddingTop"] = UDim.new(0, 5);


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear
G2L["2b"] = Instance.new("TextButton", G2L["29"]);
G2L["2b"]["TextWrapped"] = true;
G2L["2b"]["BorderSizePixel"] = 0;
G2L["2b"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["2b"]["TextSize"] = 14;
G2L["2b"]["TextScaled"] = true;
G2L["2b"]["BackgroundColor3"] = Color3.fromRGB(28, 28, 30);
G2L["2b"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["2b"]["Size"] = UDim2.new(0, 95, 0, 18);
G2L["2b"]["Name"] = [[Clear]];
G2L["2b"]["BorderColor3"] = Color3.fromRGB(151, 151, 151);
G2L["2b"]["Text"] = [[]];
G2L["2b"]["Position"] = UDim2.new(0, 0, 0.32941, 0);


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.Border
G2L["2c"] = Instance.new("Frame", G2L["2b"]);
G2L["2c"]["BorderSizePixel"] = 0;
G2L["2c"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["2c"]["Size"] = UDim2.new(0.05, 0, 1, 0);
G2L["2c"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["2c"]["Name"] = [[Border]];


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.TextLabel
G2L["2d"] = Instance.new("TextLabel", G2L["2b"]);
G2L["2d"]["TextWrapped"] = true;
G2L["2d"]["BorderSizePixel"] = 0;
G2L["2d"]["TextSize"] = 14;
G2L["2d"]["TextScaled"] = true;
G2L["2d"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["2d"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["2d"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["2d"]["BackgroundTransparency"] = 1;
G2L["2d"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
G2L["2d"]["Size"] = UDim2.new(0.89474, 0, 1, 0);
G2L["2d"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["2d"]["Text"] = [[Clear Output]];
G2L["2d"]["Position"] = UDim2.new(0.53684, 0, 0.48382, 0);


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.TextLabel.UITextSizeConstraint
G2L["2e"] = Instance.new("UITextSizeConstraint", G2L["2d"]);
G2L["2e"]["MaxTextSize"] = 14;


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.UITextSizeConstraint
G2L["2f"] = Instance.new("UITextSizeConstraint", G2L["2b"]);
G2L["2f"]["MaxTextSize"] = 14;


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.UIStroke
G2L["30"] = Instance.new("UIStroke", G2L["2b"]);
G2L["30"]["Transparency"] = 0.5;
G2L["30"]["ApplyStrokeMode"] = Enum.ApplyStrokeMode.Border;
G2L["30"]["Color"] = Color3.fromRGB(151, 151, 151);


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.Animate
G2L["31"] = Instance.new("LocalScript", G2L["2b"]);
G2L["31"]["Name"] = [[Animate]];


-- StarterGui.AAGGXENOSS.Frame.Buttons.Clear.LocalScript
G2L["32"] = Instance.new("LocalScript", G2L["2b"]);



-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL
G2L["33"] = Instance.new("TextButton", G2L["29"]);
G2L["33"]["TextWrapped"] = true;
G2L["33"]["BorderSizePixel"] = 0;
G2L["33"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["33"]["TextSize"] = 14;
G2L["33"]["TextScaled"] = true;
G2L["33"]["BackgroundColor3"] = Color3.fromRGB(28, 28, 30);
G2L["33"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["33"]["Size"] = UDim2.new(0, 95, 0, 18);
G2L["33"]["Name"] = [[ClearL]];
G2L["33"]["BorderColor3"] = Color3.fromRGB(151, 151, 151);
G2L["33"]["Text"] = [[]];
G2L["33"]["Position"] = UDim2.new(0, 0, 0.32941, 0);


-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL.Border
G2L["34"] = Instance.new("Frame", G2L["33"]);
G2L["34"]["BorderSizePixel"] = 0;
G2L["34"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["34"]["Size"] = UDim2.new(0.05, 0, 1, 0);
G2L["34"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["34"]["Name"] = [[Border]];


-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL.TextLabel
G2L["35"] = Instance.new("TextLabel", G2L["33"]);
G2L["35"]["TextWrapped"] = true;
G2L["35"]["BorderSizePixel"] = 0;
G2L["35"]["TextSize"] = 14;
G2L["35"]["TextScaled"] = true;
G2L["35"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["35"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["35"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["35"]["BackgroundTransparency"] = 1;
G2L["35"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
G2L["35"]["Size"] = UDim2.new(0.89474, 0, 1, 0);
G2L["35"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["35"]["Text"] = [[Clear Log]];
G2L["35"]["Position"] = UDim2.new(0.53684, 0, 0.48382, 0);


-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL.TextLabel.UITextSizeConstraint
G2L["36"] = Instance.new("UITextSizeConstraint", G2L["35"]);
G2L["36"]["MaxTextSize"] = 14;


-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL.UITextSizeConstraint
G2L["37"] = Instance.new("UITextSizeConstraint", G2L["33"]);
G2L["37"]["MaxTextSize"] = 14;


-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL.UIStroke
G2L["38"] = Instance.new("UIStroke", G2L["33"]);
G2L["38"]["Transparency"] = 0.5;
G2L["38"]["ApplyStrokeMode"] = Enum.ApplyStrokeMode.Border;
G2L["38"]["Color"] = Color3.fromRGB(151, 151, 151);


-- StarterGui.AAGGXENOSS.Frame.Buttons.ClearL.Animate
G2L["39"] = Instance.new("LocalScript", G2L["33"]);
G2L["39"]["Name"] = [[Animate]];


-- StarterGui.AAGGXENOSS.Frame.Buttons.CopyC
G2L["3a"] = Instance.new("TextButton", G2L["29"]);
G2L["3a"]["TextWrapped"] = true;
G2L["3a"]["BorderSizePixel"] = 0;
G2L["3a"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["3a"]["TextSize"] = 14;
G2L["3a"]["TextScaled"] = true;
G2L["3a"]["BackgroundColor3"] = Color3.fromRGB(28, 28, 30);
G2L["3a"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["3a"]["Size"] = UDim2.new(0, 95, 0, 18);
G2L["3a"]["Name"] = [[CopyC]];
G2L["3a"]["BorderColor3"] = Color3.fromRGB(151, 151, 151);
G2L["3a"]["Text"] = [[]];
G2L["3a"]["Position"] = UDim2.new(0, 0, 0.08235, 0);


-- StarterGui.AAGGXENOSS.Frame.Buttons.CopyC.Border
G2L["3b"] = Instance.new("Frame", G2L["3a"]);
G2L["3b"]["BorderSizePixel"] = 0;
G2L["3b"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["3b"]["Size"] = UDim2.new(0.05, 0, 1, 0);
G2L["3b"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
G2L["3b"]["Name"] = [[Border]];


-- StarterGui.AAGGXENOSS.Frame.Buttons.CopyC.TextLabel
G2L["3c"] = Instance.new("TextLabel", G2L["3a"]);
G2L["3c"]["TextWrapped"] = true;
G2L["3c"]["BorderSizePixel"] = 0;
G2L["3c"]["TextSize"] = 14;
G2L["3c"]["TextScaled"] = true;
G2L["3c"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
G2L["3c"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Regular, Enum.FontStyle.Normal);
G2L["3c"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["3c"]["BackgroundTransparency"] = 1;
G2L["3c"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
G2L["3c"]["Size"] = UDim2.new(0.89474, 0, 1, 0);
G2L["3c"]["BorderColor3"] = Color
