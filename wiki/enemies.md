# **Enemies**
  Health and Damage values vary with the Mission Difficulty, which is adjusted by: 
-  Campaign Difficulty Modifiers, 
-  Number of Marines, 
-  Difficulty Tier 

## **For Accurate Calculations** 
First, compute the mission difficulty:

| Skill Level     | Easy | Normal | Hard | Insane | Brutal |
| --------------- | ---- | ------ | ---- | ------ | ------ |
| Base Difficulty | 3    | 5      | 7    | 10     | 13     |

If `rd_difficulty_tier` is active, add 12 times its value to the mission difficulty.

If the campaign has a `DifficultyModifier` entry for this mission, add its value to the mission difficulty.

Next, add a modifier based on the number of marines present in the mission. 
-  If `rd_increase_difficulty_by_number_of_marines` is set (**Most ASBI-based modes**), the modifiers for marine counts **above 4** are applied.  
-  If `asw_adjust_difficulty_by_number_of_marines` is set (**most other modes**), the modifiers for marine counts **below 4** are applied.

| Marine Count | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   |
| ------------ | --- | --- | --- | --- | --- | --- | --- | --- |
| Modifier     | \-2 | \-2 | \-1 | \+0 | \+1 | \+2 | \+3 | \+4 |

The mission difficulty has a minimum value of 2. If it would be below 2, it is increased to 2.

Alien health is increased or decreased by 20% for each point of mission difficulty above or below 5 (normal).

Similarly to health, alien **damage** increases or decreases by 20% for each mission difficulty above or below Normal. 
-  In Source Engine, fractional damage carries over and there is no rounding.
-  All attacks deal a minimum of 1 damage before calculating any resistance for the victim. 

**The following values are based on 4 marines.**
---
## **Drones**
*Overwhelming Numbers + Razor-Sharp Claws + Attacks Doors.*  

| &nbsp;                 | Easy | Normal | Hard | Insane | Brutal |
| ---------------------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH** - Drone     | 25   | 40     | 56   | 80     | 104    |
| **HEALTH** - Uber      | 300  | 500    | 700  | 1000   | 1300   |
| **DAMAGE** - slash     | 9    | 15     | 21   | 30     | 39     |
| blocked while climbing | 12   | 20     | 28   | 40     | 52     |

- Drones only attack with their claws. Taking them out before they reach the squad will render them harmless.
- Certain drones have been known to leap large distances. Take extra precautions when using explosive weaponry, as targets may rapidly advance into unsafe range.
- Drones can crawl through ducts and under scaffolding. It is sometimes possible to block the drones' point of egress, trapping them in a location where they are not a threat to marines.

---
## **Rangers**
*Corrosive Spit + Long Range*  

| &nbsp;            | Easy | Normal | Hard  | Insane | Brutal |
| ----------------- | ---- | ------ | ----- | ------ | ------ |
| **HEALTH**        | 60.6 | 101    | 141.4 | 202    | 262.6  |
| **DAMAGE** - Spit | 3.6  | 6      | 8.4   | 12     | 15.6   |

- The ranger's acidic weapon travels at a constant height. Dodge roll out of the way for a clean escape.
- Rangers lack melee attack. The only risk in getting close to a ranger is a point-blank acid orb.
- Rangers cannot turn while firing. Use this opportunity to flank or get into melee range.

---
## **ShieldBug**
*Immune to Frontal Attacks + Knocks Marines Down*  

| &nbsp;             | Easy | Normal | Hard | Insane | Brutal |
| ------------------ | ---- | ------ | ---- | ------ | ------ |
| **Health**         | 600  | 1000   | 1400 | 2000   | 2600   |
| **DAMAGE** - Stomp | 15   | 25     | 35   | 50     | 65     |

- The large bone plates on the front of a shieldbug are completely invulnerable. Attack from the side or through gaps to do damage.
- Shieldbugs have two stances. The "offensive" stance moves and turns faster, but reduces coverage from the bone plates. The "defensive" stance moves and turns slower in exchange for having its shields up.
- Shieldbugs often switch to defensive stance when injured. It's often best to shoot one before attempting to flank to take advantage of its reduced movement speeds.

---
## **Boomer**
*Suicide Bomber + Explosive Projectiles + Inflates*  

| &nbsp;                 | Easy    | Normal | Hard    | Insane | Brutal   |
| ---------------------- | ------- | ------ | ------- | ------ | -------- |
| **HEALTH**             | 480     | 800    | 1120    | 1600   | 2080     |
| **DAMAGE** - Kick      | 2.4-3.6 | 4-6    | 5.6-8.4 | 8-12   | 9.6-14.4 |
| **DAMAGE** - Explosion | 55      | 55     | 55      | 55     | 55       |

- Boomers explode when provoked. If you see one inflating, it's wise to avoid the glowing blobs after it bursts.
- Boomers are mainly dangerous because they burst, but they may attempt to kick you if you get too close.
- Boomers are known to emerge from under walls or roll across the floor to menace marines.

---
## **Buzzer**
*Flight + Poison Blurs Vision*  

| &nbsp;             | Easy | Normal | Hard | Insane | Brutal |
| ------------------ | ---- | ------ | ---- | ------ | ------ |
| **HEALTH**         | 18   | 30     | 42   | 60     | 78     |
| **DAMAGE** - Sting | 9    | 15     | 21   | 30     | 30     |

- The buzzers main weapon is distraction. Their attack can disrupt a marine's vision for a few precious seconds at a crucial moment.
- Buzzers are small, quick and airborne. This makes them a challenge for projectile-based weapons. Wise marines often find it easier to "swat the flies" with melee attacks.
- Buzzers deal relatively little damage, but if left unchecked, they can be deadly.

---
## **Parasite**
*Infests Marines + Jumping Attack + Hatches from Eggs*  
| &nbsp;     | Easy | Normal | Hard | Insane | Brutal |
| ---------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH** | 15   | 25     | 35   | 50     | 65     |
*Infestation **DAMAGE** is special.*

- Parasites reproduce with the help of human heads. If a parasite latches onto a marine, prompt medical attention is required to keep them from exploding into more parasites.
- Electrified armor is the only non-medical way to prevent parasites from coupling to a marine's head once they attach. Fire, applied either to the parasite itself or the egg, will render the specimen infertile and unable to initiate the process.
- Infested marines report their vision turning red. If medical care is unavailable, the wise and merciful option is to put them down with friendly fire before their body can be used to scatter more parasites.

---
## **Mortarbug**
*Explosive Projectiles + Long Range + Corrosive Skin*  

| &nbsp;                 | Easy | Normal | Hard | Insane | Brutal |
| ---------------------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH**             | 210  | 350    | 490  | 700    | 910    |
| **DAMAGE** - Skin      | 5    | 5      | 5    | 5      | 5      |
| **DAMAGE** - Explosion | 50   | 50     | 50   | 50     | 50     |

- Mortarbugs are larger, stronger rangers. Capable marines keep an eye out for mortar shots coming over walls.
- Instead of acid, mortarbugs spit bombs that explode after a constant length of time.
- Mortarbug bombs are capable of damaging aliens and marines alike. Swift marines can take advantage of this to help clear densely-packed swarms.

---
## **Harvester**
*Explosive Spawn + Corrosive Skin*  

| &nbsp;            | Easy | Normal | Hard | Insane | Brutal |
| ----------------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH**        | 120  | 200    | 280  | 400    | 520    |
| **DAMAGE** - Skin | 5    | 5      | 5    | 5      | 5      |

- Instead of attacking directly, harvesters spawn xenomites to attack for them.
- Marines should exercise caution when approaching a Harvester. They don't attack directly, but their skin is corrosive.
- Harvesters are one of the few know specimens that will walk away from marines. You may have to chase them down to stem the tide of xenomites.

---
## **Xenomite**
*Jumping Attack + Suicide Bomber*  

| &nbsp;             | Easy | Normal | Hard | Insane | Brutal |
| ------------------ | ---- | ------ | ---- | ------ | ------ |
| **HEALTH**         | 6    | 10     | 14   | 20     | 26     |
| **DAMAGE** - Burst | 9    | 15     | 21   | 30     | 39     |

- The only dangerous part of a xenomite is the acid sac on its behind.
- Xenomites will attempt to jump onto marines and detonate themselves. Marines can refuse xenomites by killing them first.
- Xenomites often indicate that a Harvester is nearby, but they're also known to exist independently.

---
## **Mender**
*Heals Other Aliens*  

| &nbsp;     | Easy | Normal | Hard | Insane | Brutal |
| ---------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH** | 35   | 59     | 82   | 118    | 153    |

- The mender is capable of healing its fellow aliens with its stretchy, red and green tongue. Wise marines will find it difficult to stem the tide until it's dealt with.
- Menders are considerably rarer than other alien species. Novice marines often panic their first time seeing one and waste precious ammunition causing quickly-healed wounds.
- Menders are known to run away and regroup when the going gets tough. Cut them off before they get the chance.

---
## **Biomass**
*Only Vulnerable to Fire + Corrosive Skin*  
Damage Resistance: N/A  
| &nbsp;            | Easy | Normal | Hard | Insane | Brutal |
| ----------------- | ---- | ------ | ---- | ------ | ------ |
| **DAMAGE** - Skin | 10   | 10     | 10   | 10     | 10     |
*Max one damage event per second, per biomass.*

- Biomass is thought to fill a role in the alien life cycle. It cannot attack directly, but it is corrosive to the touch.
- The only way to actually eliminate a biomass is to burn it off. Marines have to consider whether to bring fire or simply accept some damage to cross.
- Some, but not all, biomass releases pheromones that can call in a swarm when burned. Be prepared to fight when lighting unfamiliar biomass.

---
## **Grub**
*Harmless + Hatches from Sacs*  

| &nbsp;     | Easy | Normal | Hard | Insane | Brutal |
| ---------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH** | 1    | 1      | 1    | 1      | 1      |

- Grubs have no weapons and very little health. They can be killed simply by stepping on them.
- Parasites are often, but not always, nearby when grubs are present. Capable marines take advantage of this early warning.
- A grub's only natural defense against boots is their ability to climb walls.

---
## **Antlion Guard**
*Knocks Down Marines + Charging Attack + Resistat to Damage*  

| &nbsp;              | Easy | Normal | Hard | Insane | Brutal |
| ------------------- | ---- | ------ | ---- | ------ | ------ |
| **HEALTH**          | 300  | 500    | 700  | 1000   | 1300   |
| **DAMAGE** - Shove  | 6    | 10     | 14   | 20     | 26     |
| **DAMAGE** - Charge | 12   | 20     | 28   | 40     | 52     |

- Marines who have fought uber drones will find the anlion guard familiar, albeit faster and larger.
- The antlion guard's primary weapon is the chitinous battering ram on their snout, giving them a distinctively long face.
- Antlion guards come in two flavors: brown guards and glowing yellow guardians. They have otherwise identical bodies but behave differently.

Data Sources: Official Content
