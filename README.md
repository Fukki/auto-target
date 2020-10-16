# Auto-Target
Auto-Target and finish your skill.</br>
**Not work in duel mode**</br>
</br>
![](autoTarget.gif)</br>
# Feature
- Complete lockon skill type config PVP PVE GVG
- Auto Heal (priest and mystic)
- Auto Pulled if your friend in airborne or knockback (priest)
- Auto Cleanse (mystic, work in raid)
- Auto Plugue remove enemy buff (priest, remove valk ragnarok and zerk unleash)
- Auto DPS
- PVP/GVG Priority debuff skill to enemy healer first
- PVP/GVG Auto put red arrow to enemy healer

# Commands
```
- at on             #enable
- at off            #disable
- at reload         #reload the config file
```
# Config.json
```
    "enabled": true,        #Enable / Disable this module
    "markTarget": {         #Mark target follow class number
        "Alliance": {       #read in Job / Class to get the number
            "0": [],        #0 = red arrow
            "1": [],        #1 = yellow arrow
            "2": []         #2 = blue arrow
        },
        "Enemy": {
            "0": [
                6,
                7
            ],
            "1": [],
            "2": []
        }
    },
    "skills": {
        "4": {              #Job / Class
            "20": {         #skill base id
                ...         #read in skill info
            }
        }
    }
```
# Job / Class
```
0 = warrior           7 = mystic
1 = lancer            8 = reaper
2 = slayer            9 = gunner
3 = berserker         10 = brawler
4 = sorcerer          11 = ninja
5 = archer            12 = valkyrie
6 = priest
```
# Skill Info
```
name: x                 #Skill name *can ignore this because it's only noted
target: []              #Read in Target Tags*
type: x                 #Read in Skill Type*
dist: x                 #Max skill distance
--- only lockon type ---
maxTarget: x            #Max target skill can lock-on
lockSpeed: x            #Speed for lock target *if ghost must increase this
castSpeed: x            #Cast speed for auto cast *if ghost must increase this
autoCast: true/false    #enable/disable auto cast
--- lock class ---
lockClass: []           #Lock-on target follow class
*Used when "enemy-class" and "member-class"
--- npc ---
lockNpc: []             #Lock-on npc follow format 'Id_HuntingZone'
*Used when "npc"
--- buff ---
inBuff: []              #Lock-on follow buff or ignore buff
*Used when "enemy-inbuff", "enemy-notbuff", "member-inbuff" and "member-notbuff"
--- heal ---
hpCutoff: x             #Lock-on member lower x percant
*Used when "member-heal"
```
# Skill Type
```
lockon                  #yes, you know this is lock-on skill
projectile              #make projectile run to target *just some skill
projectile-spoof        #make projectile instant attack *just some skill
```
# Target Tags *Priority sort
```
boss              #lock only Boss Type
npc               #lock only NPC
npc-auto          #auto detect npc *need to touch npc 1 time
npc-all           #lock all npc near you *not recommend
enemy-healer      #lock only enemy healer
enemy-class       #lock only class in setting
enemy-inbuff      #lock only enemy got buff
enemy-notbuff     #lock only enemy not have buff
enemy-all         #lock all enemy near you
member-healer     #lock only alliance healer
member-class      #lock only alliance class in setting
member-inbuff     #lock only alliance got buff
member-notbuff    #lock only alliance not have buff
member-stuck      #lock only alliance in airbone or knockback
member-clean      #lock only alliance who has debuff
member-heal       #lock only alliance hp lower
member-all        #lock all alliance near you
*Noted:
enemy = PVP Only, member = party or raid.
maxTarget is Follow your skill max target and glyph.
Please decrease and increase maxTarget by your self it's not auto detect.
```
# Not working?
if your skill look like try to spam and can't cast</br>
goto your SP or PR config and disable that skill you want to auto-cast from this moudule

# Warning
This module has more effect in PVP and PVE</br>
So i need to hide my code with encryption</br>
If you don't trust please leave from this</br>
P.S. YES IT'S FREE, THIS MODULE SLOW UPDATE BECAUSE I'M SO BUSY
