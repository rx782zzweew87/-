# -第7組
組員名單:  機一B  0614127  機一B  楊智傑 機一A 0614018 曹鈞崴 機一B 0614151 汪佑安 營建4B 0312090 戴于凱 營建4B 0312092 陳伯任
主題:汲汲營營
程式碼
local bg = display.newImage ("nkfust.jpg") 
bg.x = display.contentCenterX
bg.y = display.contentCenterY 

local floor=display.newRect(0,0,800,300)
floor.x = 0
floor.y = 620
floor:setFillColor(0, 0, 0)

local balloon=display.newImage("ballon.png",display.contentCenterX,display.comtentCenterY)
balloon.x=150
local physics=require("physics")
physics.start()
physics.addBody(balloon,{bounce=0})
physics.addBody(floor,"static")
local function push()
    balloon:applyLinearImpulse(0,-2,balloon.x,balloon.y)
  end
  
balloon:addEventListener("tap",push)
