

# سكربت وضيفة الكهربائي بنضام العين




المتطلبات :
 - qb-core ( https://github.com/qbcore-framework/qb-core )
 - qb-target ( https://github.com/qbcore-framework/qb-target )
 - qb-pedzones ( https://github.com/ic71/qb-pedzones )
 - qb-cityhall ( https://github.com/qbcore-framework/qb-cityhall )


صور السكربت:

![ic7](https://cdn.discordapp.com/attachments/458964176870703114/1136040136128340069/image.png)
![ic7](https://cdn.discordapp.com/attachments/458964176870703114/1136039962677100634/image.png)
![ic7](https://cdn.discordapp.com/attachments/458964176870703114/1136039834616610876/image.png)
![ic7](https://cdn.discordapp.com/attachments/458964176870703114/1136039727577972766/image.png)
![ic7](https://cdn.discordapp.com/attachments/458964176870703114/1136039675576979496/image.png)


# بامكانك تغير موقع العمل عن طريق config.lua




# :طريقة التركيب


# 1 -  ادخل هذا المسار (qb-core/shared/job.lua) و ضيف هذه الوضيفة
```lua
     ['electrician'] = {
		label = 'electrician',
		defaultDuty = true,
		offDutyPay = true,
		grades = {
            ['0'] = {
                name = 'electrician',
                payment = 300
            },
            ['1'] = {
                name = 'electrician engineer',
                payment = 600
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

# 3 - ادخل المسار  (qb-cityhall/config.lua) و ضيف هذا الكود

```lua
["electricity"] = {["label"] = "electricity", ["isManaged"] = false},
```

# اكتب هذا في server.cfg
```lua
start [ic7]
```

تم تطوير السكربت بواسطة : ic7
