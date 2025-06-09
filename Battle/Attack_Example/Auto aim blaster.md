________________________________________________________________________
# How to make a blaster Spam

```gdscript
func blasterspam():
	
	# the amount of blaster
	var blasternb : int = 60
	
	#the time between the spawn of each blaster
	var timer : float = 1.5
	
	for i in range(blasternb):
		randomize()
		var ang = randi() % 360
		var xy = Vector2(cos(ang), sin(ang))
		var start = Vector2(xy.x * 300.0, xy.y * 400.0)
		var end = Vector2(xy.x * 200.0, xy.y * 200.0)
		
		var heart = a_vars.player_heart
		
		end += heart.position
		start += heart.position
		
		end.x = clamp(end.x, 50, 440)
		end.y = clamp(end.x, 40, 590)
		
		var angle = rad_to_deg(heart.position.angle_to_point(end)) + 90
		a_vars.attack_manager.gaster_blaster(0,start,end,angle,Vector2(1,1),0,0)
		
		await  get_tree().create_timer(timer).timeout
```



