## Getting Loadstring
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/cueshut/saves/main/octohook%20ui%20lib"))({cheatname = "", gamename = ""})
```

## Creating Window
```lua
local Window = library.NewWindow({
title = "Octohook", -- title
size = UDim2.new(0, 500, 0.7, 20.7)}) -- size
```

## Creating a Tab
```lua
local Tab = menu:AddTab("Tab") -- tab name
```

## Creating a Section
```lua
local Section = Tab:AddSection("Section", 1) -- Section name, idk what the 1 means
```

## Creating a seperator
```lua
Tab:AddSeparator({text = "Separator"}) -- text
```

## Creating a TextBox
```lua
Section:AddBox({
  text = "Box",
  flag = "", 
  callback = function(Text)
      print(Text)
  end
})
```

## Creating a Toggle

```lua
Section:AddToggle(
   {
       text = "Toggle", -- text
       flag = "", -- flag
       callback = function(bool)
           if bool then
               print("Toggle")
           else
               print("Untoggle")
           end
       end
   }
)```

## Creating a Button

```lua
Section:AddButton(
   {
       text = "Button", -- text
       confirm = false, -- confirm to continue
       callback = function()
           Print("Button")
       end
   }
)```

## Creating a Keybind

```lua
Section:AddBind(
   {
       text = "Keybind", -- text
       flag = "", -- flag
       nomouse = true,
       noindicator = true,
       bind = Enum.KeyCode.BackSlash,
       callback = function()
           print("Pressed Backslash")
       end
   }
)
```

## Creating a Slider

```lua
Section:AddButton(
   {
       text = "Notification Sucess",
       callback = function()
           if res.Success then
               library:SendNotification(library.cheatname .. " | asss", 3)
           end
       end
   }
)```

## Creating a ColorPicker

```lua
Section:AddColor(
   {
       text = "Color",
       flag = "",
       callback = function(Color)
            print(Color)
       end
   }
)```

## Creating a Dropdown

```lua
Section:AddList(
   {
       text = "List",
       flag = "",
       values = "1", "2", "3",
       callback = function()
       end
   }
)```
