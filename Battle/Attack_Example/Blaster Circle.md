________________________________________________________________________
# How to make a blaster circle

```gdscript
func circleexample():
	#no idea how to explain d 
	var d : float = 0
	
	#the distance between each blaster 
	var distance : float = 30.0
	
	#rad is the radius of the circle
	var rad : float = 160.0
	
	#the time between each blaster spawning
	var time_between_blaster : float = 0.1
	
	#the number of blaster
	var blasternb : int = 100
	
	for i in range(blasternb) :
		
		d += get_process_delta_time()
		var gb_pos_start:Vector2 = Vector2(cos(d * distance) * 600, sin(d * distance) * 400) + a_vars.battle_box.get_center()
		var gb_pos_end:Vector2 = Vector2(cos(d * distance) * rad, sin(d * distance) * rad) + a_vars.battle_box.get_center()
		
		var angle:float = rad_to_deg(a_vars.battle_box.get_center().angle_to_point(gb_pos_end)) + 90
		a_vars.attack_manager.gaster_blaster(0,gb_pos_start,gb_pos_end,angle,Vector2(0.5,1),30,0,false)
		
		await get_tree().create_timer(time_between_blaster).timeout

```


### This seems like a lot of code, so let’s break it down.

  

1. The d variable gets added by delta_time(get_process_delta_time() function)
   
2. There are two variables, gb_pos_start and gb_pos_end.

3. both of these variables move in a circle, which is done by putting the d variable in the cosine and sine functions, and multiplying it by the speed (cos(d * spd) / sin(d * spd)) which is multiplied by the rad variable.
   
4. for the gb_pos_start variable, the radius is outside the screen, while for the gb_pos_end variable, it’s much closer to the box.
   
5. the center point of both variables is at the center of the battle box (a_vars.battle_box.get_center())
   
6. There is a third variable, angle, which points the blaster at the center of the box from the gb_pos_end position, which is converted from radians to degrees.
   
7. the gaster blaster is summoned, and the start, end, and angle variables are replaced with gb_pos_start, gb_pos_end, and angle variables, respectively.
   
8. All of this leads to the following result:
