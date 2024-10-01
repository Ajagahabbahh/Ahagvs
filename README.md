 
```lua
-- Exemplo de script para Blox Fruits

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Função para ativar um poder
local function activatePower(powerName)
    local power = character:FindFirstChild(powerName)
    if power then
        power:Activate()
    else
        print("Poder não encontrado!")
    end
end

-- Função para teleportar o jogador
local function teleportTo(location)
    character:SetPrimaryPartCFrame(location.CFrame)
end

-- Função principal
local function main()
    -- Exemplo de ativar um poder
    activatePower("GumPistol")

    -- Exemplo de teleportar para uma localização específica
    local targetLocation = game.Workspace:FindFirstChild("SpawnLocation")
    if targetLocation then
        teleportTo(targetLocation)
    else
        print("Localização não encontrada!")
    end
end

-- Executa a função principal
main()
```
