# Na Ui Library v2
## Library loadstring
```lua
local Library = loadstring(game:HttpGet(""))()
```



## Window
Create a Window
```lua
local Win = Ui:Window(' Title ')
```

## Notification
Create a Notification
```lua
local NotifyLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/Kinlei/Dynissimo/main/Scripts/AkaliNotif.lua"))()
local Notify = NotifyLibrary.Notify
```

## Notification Dc
```lua
			NotifyLibrary.Notify({
				Title = "Hi ",
				Description = "Welcome",
				Duration = 1
			})
```

## Tab
Create a Tab
```lua
local tab1 = Win:CraftTab('Title')
```
## Page
Create a Page
```lua
local page1 = tab1:CraftPage('title',1)
```



## Section
Create a Section
```lua
page1:Seperator('Dumb')
```


## Label
Create a Text Label
```lua
local Label1 = page1:Label('I love Cats')
```


## Button
Create a Button
```lua
page1:Button("Click this",function()
    print( hellow wolrd! )
end
)
```

## Toggle
Create a Toggle
```lua
local Toggle1 = page1:Toggle('Toggle',false,function(a)
    print("hello")
end
)
```

## Dropdown
Create a Dropdown
```lua
local Dropdown = Tab:AddDropdown({
local dropdown = page1:Dropdown("Dropdown",{'Item1',"Item2",'Item3'},'Item1',function(a)
    print(a)
end
)
```

## Slider
Create a Slider
```lua
local Slider = page1:Slider("Slider",true,0,100,20,function(v)
    print(v)
end)
```

## Toggle
Create a Minimize Button
```lua
repeat task.wait(0.25) until game:IsLoaded();
getgenv().Image = "rbxassetid://131188162442646"; --image id
getgenv().ToggleUI = "Enum.KeyCode.RightControl" --Toggle Settings

task.spawn(function()
    if not getgenv().LoadedMobileUI == true then getgenv().LoadedMobileUI = true
        local OpenUI = Instance.new("ScreenGui");
        local ImageButton = Instance.new("ImageButton");
        local UICorner = Instance.new("UICorner");
        OpenUI.Name = "OpenUI";
        OpenUI.Parent = game:GetService("CoreGui");
        OpenUI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling;
        ImageButton.Parent = OpenUI;
        ImageButton.BackgroundColor3 = Color3.fromRGB(105,105,105);
        ImageButton.BackgroundTransparency = 0.8
        ImageButton.Position = UDim2.new(0.9,0,0.1,0);
        ImageButton.Size = UDim2.new(0,50,0,50);
        ImageButton.Image = getgenv().Image;
        ImageButton.Draggable = true;
        ImageButton.Transparency = 1;
        UICorner.CornerRadius = UDim.new(0,200);
        UICorner.Parent = ImageButton;
        ImageButton.MouseButton1Click:Connect(function()
            game:GetService("VirtualInputManager"):SendKeyEvent(true,getgenv().ToggleUI,false,game);
        end)
    end
end)
```



