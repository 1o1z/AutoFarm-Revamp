wait(4.0)
local a=0
local b="AWP"
for _,v in pairs(game.ReplicatedStorage.Weapons:GetChildren())do
    if v:FindFirstChild("DMG")then
        if v.DMG.Value>a then
            a=v.DMG.Value
            b=v
        end
    end
end
game.RunService.RenderStepped:Connect(function()
    if game.Players.LocalPlayer.Status.Team.Value~="Spectator"then
        if not(game.ReplicatedStorage.wkspc.Status.RoundOver.Value or game.ReplicatedStorage.wkspc.Status.Preparation.Value)then
            for _,v in pairs(game.Players:GetChildren())do
                if v.Team~=game.Players.LocalPlayer.Team or game.ReplicatedStorage.wkspc.FFA.Value then
                    if v.Character and not v.Character:FindFirstChild("ShuckyHAX")and v.Character:FindFirstChild("Spawned")and v~=game.Players.LocalPlayer then
                        game:GetService("ReplicatedStorage").Events.Burn:FireServer(
                            {
                                ["Parent"]=v.Character,
                                ["CFrame"]=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                            },
                            game.ReplicatedStorage.Weapons["Golden Gun"],
                            .99
                        )
                        game:GetService("ReplicatedStorage").Events.Burn:FireServer(
                            {
                                ["Parent"]=v.Character,
                                ["CFrame"]=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                            },
                            b,
                            1
                        )
                    end
                end
            end
        elseif game.ReplicatedStorage.wkspc.Status.RoundOver.Value then
            local a=true
            for _,v in pairs(game.Players:GetChildren())do
                if v~=game.Players.LocalPlayer then
                    if v.Character then
                        if v.Character and getsenv(game.Players.LocalPlayer.PlayerGui.GUI.Client).gun and not v.Character:FindFirstChild("ShuckyHAX")and v.Character:FindFirstChild("Spawned")and v~=game.Players.LocalPlayer then
                            if v.Team~=game.Players.LocalPlayer.Team or game.ReplicatedStorage.wkspc.FFA.Value then
                                if not v.Character.HumanoidRootPart:FindFirstChild("Engulfed")then
                                    game.ReplicatedStorage.Events.Burn:FireServer(
                                        v.Character.Head,
                                        b,
                                        1,
                                        v.Character.Head.Position)
                                    if a then
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=v.Character.HumanoidRootPart.CFrame
                                        game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
                                        a=false
                                        if game.ReplicatedStorage.wkspc.Status.RoundOver and game.ReplicatedStorage.Winner1 then
                                        local x = {}
    for _, v in ipairs(game:GetService("HttpService"):JSONDecode(game:HttpGetAsync("https://games.roblox.com/v1/games/286090429/servers/Public?sortOrder=Asc&limit=100")).data) do
        if type(v) == "table" and v.playing <= 15 and v.id ~= game.JobId then
            x[#x + 1] = v.id
        end
    end
    if #x > 0 then
        game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, x[math.random(1, #x)])
coroutine.wrap(function()
	    repeat wait() until not game:GetService("ReplicatedStorage").wkspc.Status.RoundOver.Value == true
	    wait(1)
	    game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("Players[0]")
	    game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	    game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
    		game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
    		game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
    		game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
    		game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    wait(1)
	    if game.Players.LocalPlayer.Status.Team.Value == "Spectator" then
	        game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("Players[0]")
	        game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	        game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
        	game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    end
	    wait(1)
	    if game.Players.LocalPlayer.Status.Team.Value == "Spectator" then
	        game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("TBC")
	        game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	        game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
        	game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    end
	    wait(1)
	    if game.Players.LocalPlayer.Status.Team.Value == "Spectator" then
	        game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("TRC")
	        game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	        game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
        	game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    end
	    wait(1)
	    if game.Players.LocalPlayer.Status.Team.Value == "Spectator" then
	        game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("TYC")
	        game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	        game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
        	game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    end
	    wait(1)
	    if game.Players.LocalPlayer.Status.Team.Value == "Spectator" then
	        game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("TGC")
	        game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	        game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
        	game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    end
	    wait(1)
	    if game.Players.LocalPlayer.Status.Team.Value == "Spectator" then
	        game:GetService("ReplicatedStorage").Events.JoinTeam:FireServer("Random")
	        game:GetService("ReplicatedStorage").Events.LoadCharacter:FireServer()
	        game.Players.LocalPlayer.PlayerGui.Menew.Enabled = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Enabled = true
        	game.Players.LocalPlayer.PlayerGui.GUI.TeamSelection.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.BottomFrame.Visible = false
        	game.Players.LocalPlayer.PlayerGui.GUI.Interface.Visible = true
	    end
	end)()
end
end
end
end
end
end
end
end
end
end
end
end)
