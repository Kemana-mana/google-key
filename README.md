# google-key
Dynamic Keyboard Input NUI for RedM & FiveM

# Information
I created this resource because I couldn't find any good looking NUI resources to input text and have it return back for use, the menu is very dynamic and allows as many options as the screen allows, it's also Open source so feel free to pull request if you have any improvements.

![ShowCase](https://lithi.io/file/oqdY.png)
![ShowCase](https://lithi.io/file/VXJG.png)


# Setup
It's pretty simple, once you drop the google-key resource into your resources folder just make sure you put

ensure google-key

in your server.cfg. 

# Examples
If you want to have only one selection simply do something like this:
```
    local keyboard, item = exports["google-key"]:Keyboard({
        header = "Add Item", 
        rows = {"Spawn Name"}
    })
    if keyboard then
        if name then
            TriggerEvent('additem', name)
        end
    end
```
You can also add multiple listing and it would look something like this
```
    local keyboard, item, amount = exports["google-key"]:Keyboard({
        header = "Add Items", 
        rows = {"Spawn Name", "Amount"}
    })

    if keyboard then
        if item and tonumber(amount) then
            TriggerEvent('additem', item, tonumber(amount))
        end
    end
```

# Known Bugs
No known bugs

# Support
Feel free to report any issues you have in the GitHub [Issues](https://github.com/Kemana-mana/google-key/issues)

if you wish to add something to it, do a pull request on the github [Pull Requests](https://github.com/Kemana-mana/google-key/pulls)

