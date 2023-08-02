تم تطوير السكربت بواسطة : ic7

# :طريقة التركيب


# 1 -  ادخل هذا المسار (qb-core/shared/job.lua) و ضيف هذه الوضيفة
```lua
   ['electricity'] = {
		label = 'Electricity',
		defaultDuty = true,
		offDutyPay = true,
		grades = {
            ['0'] = {
                name = 'Electricity',
                payment = 300
            },
            ['1'] = {
                name = 'Electrical engineer',
                payment = 900
            },
        },
	},
```

# 2 - ادخل سكربت البيد (qb-pedzones) و ضيف هذه الكود
```lua
CreateNPC(4,"s_m_y_dockwork_01","mini@strip_club@idles@bouncer@base","base",{x = 2854.71, y = 1501.96, z = 23.72, h = 71.43},"") 

NewPed(`s_m_y_dockwork_01`, "electrician", {
    coords = vector3(2857.47, 1527.8, 24.57 - 1),
    radius = 30.0,
    heading = 166.43,
    useZ = false,
    debug = false
}, {
    invincible = true,
    canMove = false,
    ignorePlayer = true,
    clipboard = true
})

```

# 3 - ضيف هذا في سكربت (qb-cityhall/config.lua)

```lua
["electricity"] = {["label"] = "Electricity", ["isManaged"] = false},
```

# اكتب هذا في server.cfg
start [ic7]
