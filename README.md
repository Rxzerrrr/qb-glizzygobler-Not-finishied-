Please add these when you want to use the resource or it will not work!

Note I got some of this code from qb-burgershot and B1ackBeard#1430. Hope you enjoy this!

Preview ()

qb-smallresources -> server -> consumables.lua
```
QBCore.Functions.CreateUseableItem("hotdog1", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("hotdog2", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
```

qb-core -> shared.lua
```
["hotdog1"]                		 = {["name"] = "hotdog1",                 		["label"] = "HotDog w/ Ketchup",                ["weight"] = 50,        ["type"] = "item",      ["image"] = "hotdog.png",              		    ["unique"] = false, 	["useable"] = true, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "I AM EDIBLE... EXCUSE THE GRAMMER AND JUST EAT MEEE!"},
	["hotdog2"]                		 = {["name"] = "hotdog2",                 		["label"] = "HotDog w/ Mustard",                ["weight"] = 50,        ["type"] = "item",      ["image"] = "hotdog.png",              		    ["unique"] = false, 	["useable"] = true, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "I AM EDIBLE... EXCUSE THE GRAMMER AND JUST EAT MEEE!"},
	["hotdogbun"]                	 = {["name"] = "hotdogbun",                 	["label"] = "HotDog Bun",                		["weight"] = 15,        ["type"] = "item",      ["image"] = "hotdogbun.png",              		["unique"] = false, 	["useable"] = true, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "You can eat me mf... :)"},
	["mustard"]                		 = {["name"] = "mustard",                 		["label"] = "Mustard",                			["weight"] = 15,        ["type"] = "item",      ["image"] = "mustard.png",              		["unique"] = false, 	["useable"] = false, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "I am Mustard"},
	["ketchup"]                		 = {["name"] = "ketchup",                 		["label"] = "Ketchup",                			["weight"] = 15,        ["type"] = "item",      ["image"] = "ketchup.png",              		["unique"] = false, 	["useable"] = false, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "I am Ketchup"},
	["uncookedwienie"]               = {["name"] = "uncookedwienie",                ["label"] = "Uncooked Wienie",                	["weight"] = 15,        ["type"] = "item",      ["image"] = "uncookedwienie.png",               ["unique"] = false, 	["useable"] = false, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "I'm uncooked please cook me!"},
	["cookedwienie"]                 = {["name"] = "cookedwienie",                 	["label"] = "Cooked Wienie",                	["weight"] = 15,        ["type"] = "item",      ["image"] = "cookedwienie.png",                 ["unique"] = false, 	["useable"] = false, 	        ["shouldClose"] = true,            ["combinable"] = nil,   		   ["description"] = "I'm cooked no eating me without putting me in a bun ;)"},
```

qb-core -> shared.lua
```
["glizzygobler"] = {
		label = "GlizzyGobler Employee",
		defaultDuty = true,
		grades = {
			['0'] = {
				name = "Trainee",
				payment = 150
			},
			['1'] = {
				name = "Employee",
				payment = 290
			},
			['2'] = {
				name = "Burger Flipper",
				payment = 315
			},
			['3'] = {
				name = "Manager",
				payment = 345
			},
			['4'] = {
				name = "CEO",
				isboss = true,
				payment = 400
			},
		},
	},
```

qb-target -> config.lua
```
    ["glizzygobler"] = {
        models = {
            "mp_m_execpa_01",
        },
        options = {
            {  
            event = "qb-glizzygobler:DutyB",
            icon = "far fa-clipboard",
            label = "Go On/Off Duty",
            job = "glizzygobler",
            },
        },
        distance = 4.0
    })
```
