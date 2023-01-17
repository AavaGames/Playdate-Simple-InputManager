# Simple InputManager for the Playdate

An input manager that keeps track of IsPressed, JustPressed, JustReleased, Held &amp; Held Long for all buttons (D-Pad included).

Example

main.lua
```
local function initializeGame()
  inputManager = InputManager()
  player = Player()
end

initializeGame()

function playdate.update()
  inputManager.update()
  player:update()
end
```
Player.lua
```
function Player:update()
  if inputManager.JustPressed(playdate.kButtonA) then
    self:Jump()
  end
end
```
