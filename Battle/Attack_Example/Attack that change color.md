________________________________________________________________________
# How to make a attack that change color

```gdscript
#first you assign your bone to a variable 
#note that : Bullet isnt needed its just that i prefer using static variable 
#if you want godot to do the static variable assignment for you just do := and if you dont care just do =

var bone : Bullet = a_vars.attack_manager.bone(0,Vector2(600,384),-0.25,0,400,-40,0,0,true)

#the amount of time you want before the bone change color
await get_tree().create_timer(3).timeout

#where you set the bone type from 0 (normal attack) to 1 (blue attack) 
#see the bone bullet type info on the doc to see the other type available
bone.type = 1

#here you use a funtion in the bone to change its color
bone.change_color()
```

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf6Cs9gK4mz5EkviU4yN3SQPWqZK7-Vx4SEYAIyIXFhLTFb8g0o8IvEWzAQzcdhyfyWNpeq75Wyj_bjZLtrZWGerwXgGoLsqqfHjp0NZwk86bQ5zGB6Pb1xMXuIPss131h_j6Cosg?key=Z7rSag-9Hv4hDbt9M4zfqu_3)
