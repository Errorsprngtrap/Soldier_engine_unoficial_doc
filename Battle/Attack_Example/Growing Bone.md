________________________________________________________________________
# How to make a bone grow

```gdscript
#first you assign your bone to a variable 
#note that : Bullet isnt needed its just that i prefer using static variable 	#if you want godot to do the static variable assignment for you just do := and if you dont care just do =

var bone : Bullet = a_vars.attack_manager.bone(0,Vector2(600,384),-0.25,0,400,-40,0,0,true)

#time before the tween start
await get_tree().create_timer(1).timeout

#here you will create a tween
var tween : Tween = create_tween()

#here you apply the tween
tween.tween_property(bone,"offset_top",-100.0,3.0)
```

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdHCfLBM1Dk2epkdQVCnuHCTPcql3aXqtuHpPX2qzhsr92qujVTW8eRMRXB_SL0GsnhABMGAlPEV-SvfV90fWI5bLVr8ecxV7BF4tP124qzGnYepF8_94vS5DkfxFQ1SC70NoKNFA?key=Z7rSag-9Hv4hDbt9M4zfqu_3)
