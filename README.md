--禁止倒卖,爱翻库的4000家

local OrionLib = loadstring(game:HttpGet("https://pastebin.com/raw/VeaMSRZK"))()
local LBLG = Instance.new("ScreenGui", getParent)
local LBL = Instance.new("TextLabel", getParent)
local player = game.Players.LocalPlayer

LBLG.Name = "LBLG"
LBLG.Parent = game.CoreGui
LBLG.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
LBLG.Enabled = true
LBL.Name = "LBL"
LBL.Parent = LBLG
LBL.BackgroundColor3 = Color3.new(1, 1, 1)
LBL.BackgroundTransparency = 1
LBL.BorderColor3 = Color3.new(200, 200, 200)
LBL.Position = UDim2.new(0.75,0,0.010,0)
LBL.Size = UDim2.new(0, 133, 0, 30)
LBL.Font = Enum.Font.GothamSemibold
LBL.Text = "Test"
LBL.TextColor3 = Color3.new(155, 155, 155)
LBL.TextScaled = true
LBL.TextSize = 14
LBL.TextWrapped = true
LBL.Visible = true

local FpsLabel = LBL
local Heartbeat = game:GetService("RunService").Heartbeat
local LastIteration, Start
local FrameUpdateTable = { }

local function HeartbeatUpdate()
	LastIteration = tick()
	for Index = #FrameUpdateTable, 1, -1 do
		FrameUpdateTable[Index + 1] = (FrameUpdateTable[Index] >= LastIteration - 1) and FrameUpdateTable[Index] or nil
	end
	FrameUpdateTable[1] = LastIteration
	local CurrentFPS = (tick() - Start >= 1 and #FrameUpdateTable) or (#FrameUpdateTable / (tick() - Start))
	CurrentFPS = CurrentFPS - CurrentFPS % 1
	FpsLabel.Text = ("标准时间:"..os.date("%H").."时"..os.date("%M").."分"..os.date("%S"))
end

OrionLib:MakeNotification({
                    Name = "正在开启反挂机...",
                    Content = "反挂机 开启中...",
                    Time = 2
                })     
                
		local vu = game:GetService("VirtualUser")
		game:GetService("Players").LocalPlayer.Idled:connect(function()
		   vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
		   wait(1)
		   vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
		end)      

OrionLib:MakeNotification({
                    Name = "开启成功",
                    Content = "不知道有没有用",
                    Time = 1
                })
Start = tick()
Heartbeat:Connect(HeartbeatUpdate)
local Window = OrionLib:MakeWindow({Name = "暗夜脚本", HidePremium = false, SaveConfig =true,IntroText="加载脚本中", ConfigFolder = "文件存放名"})
local Tab = Window:MakeTab({
	Name = "主页",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddParagraph("说模仿FIN已取得作者同意")
Tab:AddParagraph("作者","叫我暗夜")
Tab:AddParagraph("欢迎使用暗夜脚本","脚本将持续云更新")
Tab:AddParagraph("此脚本完全免费","永运会跑路")
Tab:AddParagraph("禁止倒卖")
Tab:AddParagraph("更新日志","被遗弃汉化更新")
Tab:AddParagraph("更新AUT海外脚本","更新被遗弃访客假防御")
Tab:AddParagraph("无","无")


Tab:AddButton ({--这个就相当于一个按钮
	Name = "复制作者q群",
	Callback = function ()
	 setclipboard("962857512")
	 OrionLib:MakeNotification({
                    Name = "信息",
                    Content = "请在粘贴板中查看",
                    Time = 2
                })
	end
})

local Tab = Window:MakeTab({
	Name = "通用",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddSlider({

	Name = "速度",

	Min = 16,

	Max = 200,

	Default = 16,

	Color = Color3.fromRGB(255,255,255),

	Increment = 1,

	ValueName = "数值",

	Callback = function(Value)

		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value

	end    

})
Tab:AddSlider({

	Name = "跳跃高度",

	Min = 50,

	Max = 200,

	Default = 50,

	Color = Color3.fromRGB(255,255,255),

	Increment = 1,

	ValueName = "数值",

	Callback = function(Value)

		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value

	end    

})

local Section = Tab:AddSection({
	Name = "通用功能"
})

Tab:AddToggle({--这是一个开关
	Name = "夜视",
	Default = false,
	Callback = function(Value)
		if Value then

		    game.Lighting.Ambient = Color3.new(1, 1, 1)

		else

		    game.Lighting.Ambient = Color3.new(0, 0, 0)		    		    

		end
--这里有一个判定
	end	
})

Tab:AddButton({
	Name = "速度更改",
	Callback = function()
     loadstring(game:HttpGet("https://pastebin.com/raw/Zuw5T7DP",true))()
  end    
})

Tab:AddButton({
  Name = "死亡笔记",
  Default = false,
  Callback = function(Value)
  loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/tt/main/%E6%AD%BB%E4%BA%A1%E7%AC%94%E8%AE%B0%20(1).txt"))()
  end
})

Tab:AddButton({
	Name = "踏空",
	Default = false,
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/Float'))()
	end
})

Tab:AddButton({
	Name = "无限跳",
	Default = false,
	Callback = function()
loadstring(game:HttpGet("https://pastebin.com/raw/V5PQy3y0", true))()
  end
})

Tab:AddButton({
	Name = "显示FPS",
	Default = false,
	Callback = function()
loadstring(game:HttpGet("https://pastefy.app/d9j82YJr/raw",true))()
  end
})

Tab:AddButton({
	Name = "玩家进入提示",
	Default = false,
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/boyscp/scriscriptsc/main/bbn.lua"))()
  end
})

Tab:AddButton({

	Name = "电脑键盘",

	Callback = function()

     loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt", true))()

  	end    

})

local Section = Tab:AddSection({
	Name = "光影与画质"
})

Tab:AddButton({
  Name = "光影",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/MZEEN2424/Graphics/main/Graphics.xml"))()
  end
})

Tab:AddButton({
  Name = "光影2",
  Default = false,
  Callback = function(Value)
-- Roblox Graphics Enhancher
local light = game.Lighting
for i, v in pairs(light:GetChildren()) do
	v:Destroy()
end

local ter = workspace.Terrain
local color = Instance.new("ColorCorrectionEffect")
local bloom = Instance.new("BloomEffect")
local sun = Instance.new("SunRaysEffect")
local blur = Instance.new("BlurEffect")

color.Parent = light
bloom.Parent = light
sun.Parent = light
blur.Parent = light

-- enable or disable shit

local config = {

	Terrain = true;
	ColorCorrection = true;
	Sun = true;
	Lighting = true;
	BloomEffect = true;
	
}

-- settings {

color.Enabled = false
color.Contrast = 0.15
color.Brightness = 0.1
color.Saturation = 0.25
color.TintColor = Color3.fromRGB(255, 222, 211)

bloom.Enabled = false
bloom.Intensity = 0.1

sun.Enabled = false
sun.Intensity = 0.2
sun.Spread = 1

bloom.Enabled = false
bloom.Intensity = 0.05
bloom.Size = 32
bloom.Threshold = 1

blur.Enabled = false
blur.Size = 6

-- settings }


if config.ColorCorrection then
	color.Enabled = true
end


if config.Sun then
	sun.Enabled = true
end


if config.Terrain then
	-- settings {
	ter.WaterWaveSize = 0.1
	ter.WaterWaveSpeed = 22
	ter.WaterTransparency = 0.9
	ter.WaterReflectance = 0.05
	-- settings }
end
if config.Lighting then
	-- settings {
	light.Ambient = Color3.fromRGB(0, 0, 0)
	light.Brightness = 4
	light.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
	light.ColorShift_Top = Color3.fromRGB(0, 0, 0)
	light.ExposureCompensation = 0
	light.FogColor = Color3.fromRGB(132, 132, 132)
	light.GlobalShadows = true
	light.OutdoorAmbient = Color3.fromRGB(112, 117, 128)
	light.Outlines = false
	-- settings }
end
local a = game.Lighting
a.Ambient = Color3.fromRGB(33, 33, 33)
a.Brightness = 5.69
a.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
a.ColorShift_Top = Color3.fromRGB(255, 247, 237)
a.EnvironmentDiffuseScale = 0.105
a.EnvironmentSpecularScale = 0.522
a.GlobalShadows = true
a.OutdoorAmbient = Color3.fromRGB(51, 54, 67)
a.ShadowSoftness = 0.18
a.GeographicLatitude = -15.525
a.ExposureCompensation = 0.75
b.Enabled = true
b.Intensity = 0.99
b.Size = 9999 
b.Threshold = 0
local c = Instance.new("ColorCorrectionEffect", a)
c.Brightness = 0.015
c.Contrast = 0.25
c.Enabled = true
c.Saturation = 0.2
c.TintColor = Color3.fromRGB(217, 145, 57)
if getgenv().mode == "Summer" then
   c.TintColor = Color3.fromRGB(255, 220, 148)
elseif getgenv().mode == "Autumn" then
   c.TintColor = Color3.fromRGB(217, 145, 57)
else
   warn("No mode selected!")
   print("Please select a mode")
   b:Destroy()
   c:Destroy()
end
local d = Instance.new("DepthOfFieldEffect", a)
d.Enabled = true
d.FarIntensity = 0.077
d.FocusDistance = 21.54
d.InFocusRadius = 20.77
d.NearIntensity = 0.277
local e = Instance.new("ColorCorrectionEffect", a)
e.Brightness = 0
e.Contrast = -0.07
e.Saturation = 0
e.Enabled = true
e.TintColor = Color3.fromRGB(255, 247, 239)
local e2 = Instance.new("ColorCorrectionEffect", a)
e2.Brightness = 0.2
e2.Contrast = 0.45
e2.Saturation = -0.1
e2.Enabled = true
e2.TintColor = Color3.fromRGB(255, 255, 255)
local s = Instance.new("SunRaysEffect", a)
s.Enabled = true
s.Intensity = 0.01
s.Spread = 0.146

print("RTX Graphics loaded! Created by BrickoIcko")
  end
})

Tab:AddButton({
	Name = "画质",
	Default = false,
	Callback = function(Value)
loadstring(game:HttpGet("https://pastebin.com/raw/jHBfJYmS"))()
  end
})

local Section = Tab:AddSection({
	Name = "18禁用"
})

Tab:AddButton({
	Name = "撸管R6",
	Default = false,
	Callback = function()
loadstring(game:HttpGet("https://pastefy.app/wa3v2Vgm/raw"))()
  end
})

Tab:AddButton({
	Name = "撸管R15",
	Default = false,
	Callback = function()
loadstring(game:HttpGet("https://pastefy.app/YZoglOyJ/raw"))()
  end
})

local Section = Tab:AddSection({
	Name = "飞行区"
})

Tab:AddButton({
  Name = "飞行",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
  end
})

Tab:AddButton({
	Name = "飞车",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/vb/main/%E9%A3%9E%E8%BD%A6.lua"))()
  end
})

local Section = Tab:AddSection({
	Name = "甩飞区"
})

Tab:AddButton({
  Name = "铁拳",
  Default = false,
  Callback = function(Value)
 loadstring(game:HttpGet('https://raw.githubusercontent.com/0Ben1/fe/main/obf_rf6iQURzu1fqrytcnLBAvW34C9N55kS9g9G3CKz086rC47M6632sEd4ZZYB0AYgV.lua.txt'))()
  end
})

Tab:AddButton({
  Name = "旋转甩飞",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/tt/main/%E6%97%8B%E8%BD%AC.lua"))()
  end
})

Tab:AddButton({
  Name = "碰到就飞",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/0Ben1/fe./main/Fling%20GUI"))()
  end
})

local Tab = Window:MakeTab({
	Name = "甩飞与传送",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "指定甩飞(简易版)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet(('https://pastefy.app/9SmQXduA/raw'),true))()
  end
})

Tab:AddButton({
  Name = "全图甩飞",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://pastebin.com/raw/zqyDSUWX"))()
  end
})

local Tab = Window:MakeTab({
    Name = "森林99夜",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "99夜虚空",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/VapeVoidware/VW-Add/main/nightsintheforest.lua", true))()
  end
})

Tab:AddButton({
  Name = "99夜H4x(要解卡)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/H4xScripts/Loader/refs/heads/main/loader.lua", true))()
  end
})

Tab:AddButton({
  Name = "99夜二狗子脚本(好用)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/gycgchgyfytdttr/shenqin/refs/heads/main/99day.lua"))()
  end
})

Tab:AddButton({
  Name = "99夜自动捡钻石",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/MQPS7/99-Night-in-the-Forset/refs/heads/main/Gfarm"))()
  end
})

local Tab = Window:MakeTab({
	Name = "巴掌模拟器",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
    Name = "巴掌大战1",
    Default = false,
    Callback = function(Value)
    loadstring(game:HttpGet(("https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/Slap%20Battles")))()
    end
})

local Section = Tab:AddSection({
	Name = "感谢lkun775给的脚本"
})

Tab:AddButton({
  Name = "自动刷向导(G爹代打)",
  Default = false,
  Callback = function(Value)
  loadstring(game:HttpGet(("https://raw.githubusercontent.com/Dusty1234567890/Guide/main/Guide")))()
  end
})

local Tab = Window:MakeTab({
	Name = "动感星期五",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "fnf脚本1(要卡密)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Nadir3709/ScriptHub/main/Loader"))()
  end
})

Tab:AddButton({
  Name = "fnf脚本2(好像也要卡密)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Nadir3709/RandomScript/main/FunkyFridayMobile"))()
  end
})

local Tab = Window:MakeTab({
	Name = "刀刃球",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "红圈格挡",
  Default = false,
  Callback = function(Value)
--⭕Red Circle Auto-Block:

getgenv().visualizer = true

loadstring(game:HttpGet("https://raw.githubusercontent.com/1f0yt/community/main/RedCircleBlock"))()
  end
})

Tab:AddButton({
  Name = "刀刃球最强脚本",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/NodeX-Enc/NodeX/refs/heads/main/Main.lua"))()
  end
})

local Tab = Window:MakeTab({
	Name = "最强战场",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "自动格挡+自瞄",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Cyborg883/TSB/refs/heads/main/CombatGui"))()
  end
})

Tab:AddButton({
  Name = "垃圾桶战神",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/yes1nt/yes/refs/heads/main/Trashcan%20Man", true))()
  end
})

local Tab = Window:MakeTab({
	Name = "被遗弃",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "情云被遗弃",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/ChinaQY/Scripts/Main/Forsaken"))()
  end
})

Tab:AddButton({
  Name = "被遗弃(FIN汉化)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/FINED921/qq-155723303/refs/heads/main/Translation"))()
  end
})

Tab:AddButton({
  Name = "访客假防御",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/FINED921/qq-155723303/refs/heads/main/FIN%20false%20defense"))()
  end
})

local Section = Tab:AddSection({
	Name = "自制FIN被遗弃脚本"
})

Tab:AddButton({
  Name = "FIN被遗弃",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/FINED921/qq-155723303/refs/heads/main/Forsaken"))()
  end
})

local Tab = Window:MakeTab({
	Name = "ohio",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "宿摊ohio脚本(破解版)",
	Default = false,
	Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/XiProDev/XiPro/refs/heads/main/Free/宿傩Ohio破解版.lua"))()
  end
})

local Tab = Window:MakeTab({
	Name = "死铁轨",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "刷卷区"
})

Tab:AddButton({
  Name = "TX自动刷卷",
  Default = false,
  Callback = function(Value)
--[[by 退休不退休]]
QUN = "160369111"
TX = "死铁轨刷债券V3"
script = "死铁轨免费刷债券"
loadstring(game:HttpGet("https://raw.githubusercontent.com/JsYb666/Item/refs/heads/main/刷债券"))()
  end
})

Tab:AddButton({
  Name = "外国刷卷(执行后点一下屏幕哦)",
  Default = false,
  Callback = function(Value)

getgenv().BondFarmSetting = {
	Fast_Auto_Execute = true, -- Use queue_on_teleport to execute faster than your executor itself 
	Number_Of_Bonds_Targeted = 9e9, -- When your bonds reached the number you wanted, the will script automatically be stopped
	Tween_Duration = 23, -- The smaller number, the faster it goes (best is 23)
	Webhook_Url = "none",
	Main_Auto_SHOP_Delay = 70, -- auto server hop after time ended in main game
	Lobby_Auto_SHOP_Delay = 25, -- auto server hop after time ended in lobby
	Goto_Party_By_Walking_Only = false, -- if you set to false, it instantly teleport you to party creator, else it make you walk to party creator 
	Blackscreen_Save_Battery = true,
	Show_Bonds_Collected_On_Blackscreen = false
}
SaveNewSettings = true 
script_key = "DonjoSx_Was_Not_Here" -- Script key, don't remove this
loadstring(game:HttpGet("https://raw.githubusercontent.com/Umbrella-Scripter/Deadrails-Script/refs/heads/main/average-bond-farm.lua"))()
  end
})

local Tab = Window:MakeTab({
	Name = "doors",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "doors(很好用)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("\104\116\116\112\115\58\47\47\112\97\115\116\101\98\105\110\46\99\111\109\47\114\97\119\47\54\53\84\119\84\56\106\97"))()
  end
})

Tab:AddButton({
  Name = "doorsrooms(不要碰屏幕！)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://" .. "raw.githubusercontent.com/DaRealGeo/roblox/master/rooms-autowalk"))()
  end
})

Tab:AddButton({
  Name = "doors暗夜汉化",
  Default = false,
  Callback = function(Vale)
 loadstring(game:HttpGet("https://raw.githubusercontent.com/jgyccjfcfuxufigx-glitch/-/refs/heads/main/anydoorsmshax"))()
   end
})

local Tab = Window:MakeTab({
	Name = "M.E.G",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "修改钱数(买一次再修改一次)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/FINED921/qq-155723303/refs/heads/main/MEG"))()
  end
})

local Tab = Window:MakeTab({
    Name = "压力",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "压力1(全英文且要解卡密)",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/H4xScripts/Loader/refs/heads/main/loader.lua", true))()
  end
})

local Tab = Window:MakeTab({
    Name = "偷走脑红",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "Delfi",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://pastefy.app/UTq45GC2/raw"))()
  end
})

local Tab = Window:MakeTab({
    Name = "AUT",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
  Name = "老外AUT1",
  Default = false,
  Callback = function(Value)
loadstring(game:HttpGet("https://raw.githubusercontent.com/AkatsukiHub1/A-Universal-Time/refs/heads/main/README.md"))()
  end
})
