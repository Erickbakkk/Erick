-- Interface de usuário em Roblox Studio

-- Cria uma tela de interface GUI
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local AutoFarmButton = Instance.new("TextButton")
local AutoFruitButton = Instance.new("TextButton")

-- Adiciona o GUI à interface do jogador
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Configura o Frame
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Frame.Size = UDim2.new(0, 200, 0, 100)
Frame.Position = UDim2.new(0.5, -100, 0.5, -50)

-- Configura o botão Auto Farm
AutoFarmButton.Parent = Frame
AutoFarmButton.Text = "Auto Farm (Habilitar)"
AutoFarmButton.Size = UDim2.new(0, 180, 0, 40)
AutoFarmButton.Position = UDim2.new(0, 10, 0, 10)

-- Configura o botão Auto Fruit
AutoFruitButton.Parent = Frame
AutoFruitButton.Text = "Auto Frutas (Habilitar)"
AutoFruitButton.Size = UDim2.new(0, 180, 0, 40)
AutoFruitButton.Position = UDim2.new(0, 10, 0, 60)

-- Função para alternar o estado da janela
local function toggleWindow()
    Frame.Visible = not Frame.Visible
end

-- Atalho para abrir e fechar a janela (pressione "P")
game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.P then
        toggleWindow()
    end
end)

-- Evento de clique para os botões
AutoFarmButton.MouseButton1Click:Connect(function()
    print("Função Auto Farm ativada")
end)

AutoFruitButton.MouseButton1Click:Connect(function()
    print("Função Auto Frutas ativada")
end)
