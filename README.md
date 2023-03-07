local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("NARKO GUİ v0.31 (Free)", "BloodTheme")
--Main--
local Tab = Window:NewTab("Menü")
local Section = Tab:NewSection("Attack")
Section:NewButton("infinite yield", "Admin komutları içerir", function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)
Section:NewButton("Remote Spy", "Oyun Fonksiyonlarını gosterir", function()
loadstring(game:HttpGet("https://github.com/exxtremestuffs/SimpleSpySource/raw/master/SimpleSpy.lua"))()

end)
local Tab = Window:NewTab("Player")
local Section = Tab:NewSection("Player")
Section:NewSlider("Walk Speed", "Hızlı yürüme hilesidir.", 500, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
Section:NewSlider("Jump Power", "Jıplama yüksekliği hilesidir.", 500, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)
Section:NewToggle("God Mode", "Ölümsüz Yapar", function(state)
    if state then -- This script is made by Miyuki#7227



local player = game.Players.LocalPlayer

if player.Character then

if player.Character:FindFirstChild("Humanoid") then

player.Character.Humanoid.Name = "1"

end

local l = player.Character["1"]:Clone()

l.Parent = player.Character

l.Name = "Humanoid"; wait(0.1)

player.Character["1"]:Destroy()

workspace.CurrentCamera.CameraSubject = player.Character.Humanoid

player.Character.Animate.Disabled = true; wait(0.1)

player.Character.Animate.Disabled = false

end

print("finished.")
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)	
Section:NewButton("No Hide Name", "Oyuncu ismini siler", function()
loadstring(game:HttpGet("https://pastebin.com/raw/wpbSTjDW", true))()
end)
