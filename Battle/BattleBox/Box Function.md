________________________________________________________________________
# **The following functions allow you to resize the battle area:**
________________________________________________________________________
# set_box_size(target, resize_speed)
##### Description: 
This function let you chose the precise placement of each part of the box .

#### Parameters:
target(Array): An array containing four values representing the positions of each wall (left, top, right, bottom).

resize_speed(float)(automatic value of 500.0): A float number that decide at what speed the box will resize

#### Example : 
```gdscript
a_vars.battle_box.set_box_size([0,200,600,400]) 
```

and if you want to use custom speed 

```gdscript
a_vars.battle_box.set_box_size([0,200,600,400],200.0) 
```

________________________________________________________________________
# reset_box_size(resize_speed)
##### Description: 
This function let you put back the box to its normal size

#### Parameters:
resize_speed(float)(automatic value of 500.0): A float number that decide at what speed the box will resize

#### Example : 
```gdscript
a_vars.battle_box.reset_box_size()
```

and if you want to use custom speed 

```gdscript
a_vars.battle_box.reset_box_size(200.0)
```


________________________________________________________________________
# insta_box_size(target)
##### Description: 
This function  change the size of the box with 0 animation.

#### Parameters:
target(Array): An array containing four values representing the positions of each wall (left, top, right, bottom).

#### Example : 
```gdscript
a_vars.battle_box.insta_box_size([244,250,399,390])
```

________________________________________________________________________
