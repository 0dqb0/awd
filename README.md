game.StarterGui:SetCore("SendNotification", {
	Title = "OZU";
	Text = "OZU'S SCRIPTSSSSSS";
	Duration = 5;
})
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Phenom", "Synapse")
 
    -- MAIN
    local Main = Window:NewTab("OZU'S SCRIPTSSSSSS")
    local MainSection = Main:NewSection("OZU'S SCRIPTSSSSSS")

MainSection:NewButton("no HL nojumpbot", "x", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/WUiTmST1',true))();
end)

MainSection:NewButton("No HL T Aimbot", "x", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/J0K9mg1h'))()
end)

MainSection:NewButton("NormalSIlent (X)", "Jump then Press X", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/yPY7v700',true))();
end)

MainSection:NewButton("PLAYGROUND SILENT NO HL! (X)", "Jump then Press X", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/nc8NcPAu',true))();
end)

MainSection:NewButton("Bounce No HL", "x", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/gcKC08D9'))()
end)

MainSection:NewButton("Auto Score! (L)", "PEOPLE ARE SUCH L'S!!", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/2VH8kQty',true))();
end)

MainSection:NewButton("Follow Ball", "Press M", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/uWb3zfPe',true))();
end)
    
    MainSection:NewButton("Ball Mag (Press R)", "Gives you Ball Mag", function()
        local UIS = game:GetService('UserInputService')
        local plr = game.Players.LocalPlayer
        local Char = plr.Character or plr.CharacterAded:Wait()
        local Key = 'R'
        UIS.InputBegan:Connect(function(Input, IsTyping)
        if IsTyping then return end
        local KeyPressed = Input.KeyCode
        if KeyPressed == Enum.KeyCode[Key] then
        game.Workspace.Map.Basketball.Handle.CFrame = Game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
        end
        end)
    end)

    -- PLAYER
    local Player = Window:NewTab("Other SCWIPTSSSSS")
    local PlayerSection = Player:NewSection("Other SCWIPTSSSSS")
   

PlayerSection:NewButton("aimstudio checker", "click to see", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/vBPYpCaj'))()
end)
    PlayerSection:NewButton("Admin!", "Gives Admin", function()    
loadstring(game:HttpGet("https://raw.githubusercontent.com/fatesc/fates-admin/main/main.lua"))();
end)

    PlayerSection:NewButton("Infinite Jumps", "Gives you Infinite Jumps", function()    
    local InfiniteJumpEnabled = true
    game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
    end)

    end)


    --Settings
    local Settings = Window:NewTab("Settings")
    local SettingsSection = Settings:NewSection("Settings")

    SettingsSection:NewButton("Reset", "Resets your Characters", function()
        game.Players.LocalPlayer.Character.Humanoid.Health = 0
    end)

    SettingsSection:NewButton("Rejoins", "Rejoins your game", function()
        local TeleportService = game:GetService("TeleportService")
        local placeID = 623694595
        local player = Game.Players.LocalPlayer
         
        TeleportService:Teleport(placeID, player)
    end)

    SettingsSection:NewKeybind("Toggle", "Toggles the Gui", Enum.KeyCode.One, function()
        Library:ToggleUI()
    end)
