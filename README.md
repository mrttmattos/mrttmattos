
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Dark Mattos hub | idle hero ", HidePremium = false, SaveConfig = true, ConfigFolder = "idle hero"})
getgenv().level = false
getgenv().NextLevel = false
getgenv().npc = " "
getgenv().autofarmar = false
getgenv().farm = false
getgenv().player ={"Lost Soul","Robot Overlord","Dark Warlock","Goddess of Light","Blade Queen","Bounty Hunter","The Champion","Pig King", "Magma Mage","Wandering Fisherman","Assassin Zero","Ice Cube"}

-- variaveis
local bumtab = Window:MakeTab({
	Name = "destruir janela",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local passartab = Window:MakeTab({
	Name = "passar",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local reemcanartab = Window:MakeTab({
	Name = "Reencarnar",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local leveltab = Window:MakeTab({
	Name = "auto level up",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
-- funcoes
  function levelar (boneco)
	print(farm)
    while farm == true do
        game:GetService("ReplicatedStorage").Packages._Index:FindFirstChild("sleitnick_knit@1.4.7").knit.Services.HeroService.RF.BuyLevel:InvokeServer(boneco,0)
        wait(15)
    end
end	

	--tabs
bumtab:AddButton({
	Name = "destruir",
	Callback = function()
        OrionLib:Destroy()
  	end    
})
reemcanartab:AddButton({
	Name = "Reencarnar",
	Callback = function(Value)
        
  	end    
})
--drops

--liga desliga auto level
leveltab:AddToggle({
	Name = player[1],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
			levelar(player[1])
			
			else
				farm = false	
			end
		end	
})
leveltab:AddToggle({
	Name = player[2],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
			levelar (player[2])
			
			else
				farm = false	
			end
		end	
})
leveltab:AddToggle({
	Name = player[3],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
		    levelar (player[3])
			
			else
				farm = false
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[4],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
			levelar (player[4])
			
			else
				farm = false
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[5],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
		    levelar (player[5])
			
			else
				farm = false
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[6],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
			levelar (player[6])
			
			else
				farm = false
	
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[7],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
		    levelar (player[7])
			
			else
				farm = false
			
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[8],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = Value
		    levelar (player[8])
			
			else
				farm = false
			
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[9],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
		    levelarr (player[9])
			
			else
				farm = false
			
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[10],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
			levelar (player[10])
			
			else
				farm = false
			
	
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[11],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
		    levelar (player[11])
			
			else
				farm = false
			
	
			end
		end	
	
	
})
leveltab:AddToggle({
	Name = player[12],
	Default = false,
	Callback = function(Value)
		if Value then
			farm = true
		    levelar (player[12])
			
			else
				farm = false
			end
		end	
	
	
})
passartab:AddToggle({
	Name = "proximo",
	Default = false,
	Callback = function(Value)
		if Value then
			AutoNextLevel(Value)
			
			else
				Print("falso")
			
	
			end
		end	
	
	
})
passartab:AddToggle({
	Name = "farmar",
	Default = false,
	Callback = function(Value)
		if Value then
			AutoFarm(Value)
			
			else
				Print("falso")
			
	
			end
		end	
})


OrionLib:Init()
