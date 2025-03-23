# -- Auto Quest Script
while true do
    for _, quest in pairs(game:GetService("ReplicatedStorage").Quests:GetChildren()) do
        if quest:IsA("Model") then
            local args = {quest}
            game:GetService("ReplicatedStorage"):WaitForChild("RemoteFunction"):InvokeServer(unpack(args))
        end
    end
    wait(5)
end
