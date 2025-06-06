__________________________________________________________________
# bone(bullet,position,x,y,speed,offset_top,offset_bottom,rotation_speed,masked,duration)
##### Description: 
This function let you create a bone

#### Parameters:
type(bullet.e_type) : define the color of the attack
- 0 = normal attack
- 1 = blue attack
- 2 = fake blue attack
- 3 = orange attack
- 4 = Untouchable (not tested so far)

position (Vector2): The starting position of the bone.

x (float): Horizontal speed

y (float): Vertical Speed

speed (float): The movement speed.

offset_top / offset_bottom (float): Adjusts the bone size.

rotation_speed (float): Rotation speed.

masked (bool, optional): If true, the bone will not be visible outside the battle box.

duration (float, optional): The time before the bone disappears. Default value: -1 (unlimited).

#### Example : 
```gdscript
a_vars.attack_manager.bone(0,Vector2(0,325),3,0,40,0,60,0,true,-1)
```

the last value "-1" is not needed since the function automatically put -1 if we don't put any value

(false for masked should only be used for testing or attack that need to be visible from outside the box)

__________________________________________________________________
# bone_gravity(type, position, bone_count, offset_bottom, masked, duration:)
##### Description: 
Spawns multiple bones that fall with gravity.

#### Parameters:
type(bullet.e_type) : define the color of the attack
- 0 = normal attack
- 1 = blue attack
- 2 = fake blue attack
- 3 = orange attack
- 4 = Untouchable (not tested so far)

position (Vector2): The starting position of the bone.

bone_count (int): The number of bones spawned.

offset_bottom (float): Adjusts the bone size.

masked (bool, optional): If true, the bone will not be visible outside the battle box.

duration (float, optional): The time before the bone disappears. Default value: -1 (unlimited).

#### Example : 
```gdscript
a_vars.attack_manager.bone_gravity(0,Vector2(320,200),20,20,false,-1)
```

________________________________________________________________________
# bone_circle(type, position, bone_count, radius, rotation_speed, masked, duration)
##### Description: 
Spawns bones in a circular pattern around a central point.

#### Parameters:
type(bullet.e_type) : define the color of the attack
- 0 = normal attack
- 1 = blue attack
- 2 = fake blue attack
- 3 = orange attack
- 4 = Untouchable (not tested so far)

position (Vector2): The center of the circle.

bone_count (int): The number of bones spawned.

radius (float): The radius of the attack (smaller values place bones closer to the center).

rotation_speed (float): The speed the bone circle rotate at.

masked (bool, optional): If true, the bone will not be visible outside the battle box.

duration (float, optional): The time before the bone disappears. Default value: -1 (unlimited).

#### Example : 
```gdscript
a_vars.attack_manager.bone_circle(0,Vector2(320,320),30,60,20,true,-1)
```

________________________________________________________________________

# bone_stab(type, position, length, height, wait_time, up_time bone_rotation, masked)
##### Description: 
Spawns a bone stab/bone zone at a specified location.

#### Parameters:
type(bullet.e_type) : define the color of the attack
- 0 = normal attack
- 1 = blue attack
- 2 = fake blue attack
- 3 = orange attack
- 4 = Untouchable (not tested so far)

position (Vector2): The center position.

length (float): The length of the zone.

height (float): The height of the zone.

wait_time (float): Time before the bone appears.

up_time (float): Duration the bone remains active.

rotation_speed (float): The speed the bone circle rotate at.

masked (bool, optional): If true, the bone will not be visible outside the battle box.

#### Example : 
```gdscript
a_vars.attack_manager.bone_stab(0,Vector2(244,390),200,60,60,30,0,true)
```

________________________________________________________________________


