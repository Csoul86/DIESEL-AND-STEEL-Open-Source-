# DIESEL-AND-STEEL-Open-Source


``
by Jam and Zel
``

**Warning:**  
Some source only work on delta mostly Exp multiplier i recommended using delta, volcano, xeno and solara

## Files

- `DecompiledExp.txt`              → increase your exp if you on it with toggle and when you passanger goes to his destination it will work!
- `DecompiledAutoCash.txt`         → this is very op but slow! 
- `Decompiled_Autokm.txt`          → Auto drive your jeepney to increase the stats of km 
- `Decompiled_DuplCash.txt`        → Always have a toggle for this it's because of firing causes the game freezed make it on/off toggle then put the callback and only on it if you are taking fare or passanger giving you too much of your sukli
- `Decompiled_DuplCoins.txt`       → Coins duplication this is good if auto is patched but it have limit value of 300
- `Decompiled_JeepniesVelocity.txt`→ just execute it and your jeep will move you can still customize the velocity though 
- `Decompiled_UsernameProtector.txt`→ name and username hider

## Quick Fix for EXP Toggle

Many decompiled EXP scripts are missing or have a disabled toggle.  
Common pattern to make it work:

```lua
getgenv().ExpEnabled = true  -- change to false to stop

spawn(function()
    while getgenv().ExpEnabled do
        -- paste the original exp loop / give exp code here
        task.wait(0.3)  -- adjust to avoid detection/kick
    end
end)
