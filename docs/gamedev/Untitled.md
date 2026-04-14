# SSB Melee Physics

## Physics step logic

1. pass thru platforms = false
2. update last pos var
3. update last facing dir var
4. deepObjectMerge()
5. if in hitlag:
	1. dec hitlag timer
	2. calc knockback
	3. calc SDI/ASDI
6. if not in hitlag:
	1. dec shieldstun timer
	2. update can walljump
	3. update turnaround timer
	4. update last state var
	5. process current state