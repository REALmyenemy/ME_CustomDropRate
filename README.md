# ME_CustomDropRate
A simple plugin to manage droprate.


0% progress


By default, rpg maker considers only the rate of items to make drops. It also always gives you the same coins based on the dead monsters
at the end of the battle.  
But what if our character, had a better lootrate than the others? Maybe due to a potion, or to a enchanted piece of gear, or even themselves?  
It can also happen the other way! Your character might have gotten blind in battle, so they won't notice the loot they wanted is in front of them!  
Only double option exists in editor, and it can't be edited midplay.  
This plugin means to enable you to increase or decrease droprates together or separately with gold rate, depending on the actors in your party at the end of the battle.  


Notetags:  
```<ME_CDR: X>```  
When applied to an actor, the actor will have X droprate percent by default. If not set, it defaults to 100.  
```<ME_CDR: 120> //Makes the actor have 20% extra droprate```  
When applied to states, armors, weapons, items... It adds the ammount to the affected/equiped actors  
```<ME_CDR: 10> //Will make the affected actor/s have 10% extra droprate```  
```<ME_CGR: X>```  
When applied to an actor, the actor will have X goldrate percent by default. If not applied, 100.  
When applied to states, armors, weapons, items... It adds the ammount to the affected/equiped actors.  


Parameters:  
Mode:  
CDR Only  
ME_CGR tags and its plugin commands will be ignored, and ME_CDR will be used instead for both  
CDR and CGR  
ME_CDR tags and its plugin commands will be used for droprate, and ME_CGR will be used for gold drop rate.  
Gold Only  
ME_CDR tags and its plugin commands will be ignored, and ME_CGR will be used for gold drop rate. 

Drop Only  
ME_CGR tags and its plugin commands will be ignored, and ME_CDR will be used for drop rate


Plugin commands  
```ME_CDR Add x y```  
```ME_CDR Set x y```  
They add and set x droprate on actor y:  
X can be a number. If you set the letter v before the number, it will be treated as a variable (v2 refers to variable2).  
Y is the actor index, if set to 0 it will be applied to the party, if -1, to everyone in the database.  

```ME_CDR Add x y[z]```
```ME_CDR Set x y[z]```  
They add and set x droprate on whatever Y is number z:  
X can be a number. If you set the letter v before the number, it will be treated as a variable (v2 refers to variable2).  
Y must be a char. It is the kind of element to apply it to, s will be status, a for armor, w for weapon, i for item, c for class, h for actor.  
Z is the index, if set to and it's an actor 0 it will be applied to the party, if -1, to everyone in the database.  

```ME_CGR Add x y```  
```ME_CGR Set x y```  
They add and set x gold rate on actor y:  
X can be a number. If you set the letter v before the number, it will be treated as a variable (v2 refers to variable2).  
Y is the actor index, if set to 0 it will be applied to the party, if -1, to everyone in the database. 

```ME_CGR Add x y[z]```  
```ME_CGR Set x y[z]```  
They add and set x gold rate on whatever Y is number z:  
X can be a number. If you set the letter v before the number, it will be treated as a variable (v2 refers to variable2).  
Y must be a char. It is the kind of element to apply it to, s will be status, a for armor, w for weapon, i for item, c for class, h for actor.  
Z is the index, if set to and it's an actor 0 it will be applied to the party, if -1, to everyone in the database. 
