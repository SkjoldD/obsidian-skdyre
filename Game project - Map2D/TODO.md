
 AGENTMANAGERHOSTILE
 * - add all the values required for modperformdata
 * - check if all the ability mods has the responding needs and add logic in their perform and calculate
 
UnitAttackHandler
 * - _agentActionDecisionRewardChanges implemented.
 * - Needs to be used to calculate the change.  

AgenActionHostile
 * - Omskriv så reward er baseret på tidligere resultat
 *   - Reward kan kun komme når FORVENTET resultat er gavnet.
 *   - Definer FORVENTET resultat.
 * 
 * 
Describe the reward attributes
 *    - NEED TO BE THE SAME ON ALL (IT HAS TO WEIGHT ON CERTAIN VALUES IN CERTAIN 

SITUATIONS. SUCH AS MOVEMENT NEED TO BE THE SAME AS ATTACK
 *      - DISTANCE TO GOAL
 *      - AMOUNT OF TOWERS NEARBY
 *      - AMOUNT OF TOWERS BETWEEN THE NEXT MOVEPOINT AND THE UNIT
 *      - DISTANCE TO NEAREST TOWER
 *      - CURRENT HP
 *      - CURRENT MOVEMENT SPEED
 *      - AMOUNT OF ALLIED MONSTER NEARBY
 *      - 
 *      
 * - Fix and insert the agent action
 * - Save the IAgentManagerService data
 *    - Load it too
 * - Create the big algorithm.
 * [BIG TASK] INSERT AGENT LOGIC: https://lucid.app/lucidchart/98fd07a8-da8e-49bd-9ccf-f30c70182643/edit?invitationId=inv_40343375-979d-4c76-9708-22423161b949&page=0_0#
 * 
 UI: 
 *   Right click -> Take item into inventory
 *   Drag -> Make item add to tower on drop
 * 
 * 
 * 
 (DONE) OMSKREVET LOGIC FOR AIMOVEMENT TIL AT GÅ GENNEM AGENT
 * - MANGLER LOGIC FOR ANGREB
 * - PÅVIRKER OGSÅ TÅRN
 * - MANGLER UDVIDELSE TIL AGENTSERVICE
 * 
 Startside
 *  - lav en verden / Ø
 *     - huse som man kan trykke på der leder ind til alt.
 * 
 * 
 FIX:
 * (DONE)- Items on ground does not contain dependencyMan. Check fix for this? The dependencyman should be available in a global static stuff. but dangerous solution
 * 
 * X CATCHUP:
 * 
 * X - ItemDropableAreaComponent needs to get dependencyman updated
 * X- item that is picked up from ground and insertet into towers does not work. 
 * 
 *    
 Open inventory in World map
 *    - Sell items / Delete them
 *    - Need to create UI Manager GO for the worldmap.
 *    - Need to create 
 *    
 A system that can fetch specific button functions on specific managers.
 *    - Have a <key, feature> kinda setting?
 * 
 Inventory Limitation Solution
 *    (DONE) Only picked up items save
 *    (IGNORED) Pick up easy solution?
 *    (DONE) Only save items if you win?
 *       - Note: it reloads previous save when u lose/die.
 *          - Any progress should stay?
 *    
 *    (REJECTED) Save remaining stuff somewhere?
 *    (REJECTED) Save remaning stuff in a 'Adventures clean up leftover tavern'?
 *    (REJECTED) Make the remaning stuff into coins.
 *    (REJECTED) Display all remaining-unpickedup-items at the end?
 *    - 
 * 
 (DONE) CREATE ANIMATION SYSTEM
 *    - (DONE) ATTACKS HAVE CUSTOM ANIMATION
 *    - ADD TO COMMAND THAT IT CAN CREATE A RANDOM WEAPON
 * 
 CREATE RESTRICTION SYSTEM ON ITEM GAIN ON SCENE LEVEL 1.
 *    - Only make it playable once?
 *    
 CREATE LEVEL SYSTEM
 *    - FANCY GUI?
 *    - ITEM AND TOWER DISPLAY?
 *    - EXP GAIN DISPLAY?
 *    - LEVEL BAR?
 *    
 * 
 (DONE)FIX - the save file doesnt save arrows/attack mods correctly. Does not work on load.
 (DONE) FIX (REMOVE) BUILD WINDOW MANAGER - the ones that add a pop up on right click.
 * 
 (DONE) FIX SO THAT IT DOESNT GIVE ERROR ON ENDGAME
 *    - COULD JUST CLEAN UP IN TileMapManager LEVEL LOST SO THAT IT REMOVES ALL UNITS - ISSUE IS ITEM CREATION ON HOSTILE DEATH THAT STAYS ON SCENE CHANGE
 (DONE) FIX TOOLTIP THAT GETS DATA FROM CLASS INSTEAD OF SOMEWHERE ELSE
 TODO
 * CREATE BLANKPOINT MODATTACK
 * CREATE BLANKPROJECTILE MODATTACK  
 * 
 * MONSTERS AI PATHFINDING NEEDS TO WORK WITH UNITPROPERTIESGENERALCOMPONENT. THE ATTACK MIGHT BE USED WITH (TOWERATTACKHANDLER, NOW KNOWN AS: UNITATTACKHANDLER)
 * (DONE) MOVE TOWERGENERAL LOGIC TO UNITPROPERTIESGNERALCOMPONTENT!!
 * 
 * 
 * 
 UI
 * - Fix win screen ?
 * - Settings screen ?
 *  - Toggle healthbar
 *    - friends, foe, neutrals
 * 
 MAP EDITOR
 * - DATA MAPPING
 *    - SAVE AND LOAD FUNCTIONS
 * 
 PROPERTIES FUNCTIONALITY IMPLEMENT:
 * - (ATTACK) X ORB AROUND TOWER
 * - (ATTACK) OPHELIAS ORB. MOVE ONLY ORB AND NOTHING ELSE
 * - (ABILITY) THROW ENEMIES IN OPOSITE DIRECTION
 * - (ABILITY) LAY DOWN TRAPS
 * - (ABILITY) WALL AROUND TOWER
 *        - WORK WITH THORNS?
 * - (ABILITY) RAY BEAM ON GROUND FOLLOWING
 * - (ABILITY) ON HIT: IMMUNITY FOR 1S (CD 10s)
 * - (GENERAL) LIFESTEAL
 * - (GENERAL) ON KILL: GAIN % STATS OF RANDOM MOD FROM KILLED MOB (MAX X MODS?)
 * 
 (DONE) - AOE
 (DONE) - AOE DMG(should be aoe dmg + dmg)
 (DONE) - CHAIN 
 (DONE) - PIERCE
 (DONE) THORNS (Reflect damage)
 *        - Can be hard, cannot cycle. Same as Chain mby?
 *        
 * - CRIT
 * - CRIT DAMAGE
 * 
 ON (CRIT, LUCKY HIT)
 *    - ACTION / AURA / AMPLIFIER?
 * 
 * - POISON
 * - FIRE
 * - SLOW
 * - STUN
 * - GROUND EFFECT
 * - ABILITY: GUST (wave of knowckback or just dmg with pierce?)
 * - KNOCKBACK
 * - ABILITY: STOMP (aoe around tower)
 * - AURA: DMG BOOST
 * - AURA: RANGE BOOST
 * - AURA: LIFE REGEN
 * - AURA: ARMOR
 * - AURA: DMG REDUCTION
 * - AURA: ALL MODS TO OTHER TOWERS (Mby just 10%)
 * 
 * - ABILITY: HEAL NEARBY ON ATTACK
 * - ATTACK: CHARGE UP ATTACK
 *        - DEAL MORE DMG OVER TIME
 *        - EXPLODE WHEN CHARGED
 * - ABILITY: CYCLONE
 * - (IRREGULAR) ABILITY: TELKEPORT AWAY WHEN HIT BY PROJECTILE (30s CD?)
 * - (IRREGULAR) GENERAL: GIVE 10K EXP TO KILLER
 *      - CAN BUFF ENEMIES SO YOU GET BETTER DROP?
 *      - CAN BUFF ENEMIES SO YOU GET BETTER EXP?
 *      - CAN BE USED BY FRIENDLIES TO KILL AND LEVEL UP?
 * - (IRREGULAR) ABILITY: MAKE ITEMS ON THE GROUND UPGRADED ATLEAST TO NEXT TIER (?)
 * - (IRREGULAR)(HIDDEN): ATTRACT CRITTERS
 * - (IRREGULAR) ABILITY: CONVERT ITEMS TO MONEY ON DROP
 * - ABILITY: BOND BETWEEN THOSE WHO HOLDS THE MOD
 *      - CAN BE USED FOR DMG
 *      - CAN BE USED FOR SLOW
 *      - CAN BE USED FOR HEAL (?)
 * - (IRREGULAR) STEAL PROJECTILE AND SEND TO TARGET
 *      - CAN BE USED ON FRIENDLY PROJECTILES
 *      - CAN BE USED ON ENEMY PROJECTILES AND SEND BACK
 * - (IRREGULAR) MIND CONTROL
 *      - TAKE CONTROL OF NORMAL UNIT (30s CD after death)

 * 
 * 
BUILD A SETTING ENVIRONMENT THAT CAN GO FROM UI -> MAP -> LEVEL
 * GameClass (manager?)
 * - GameSettings
MapClass (... something to keep info about save if and stuff)
 * - MapSettings
 * LevelClass (
 * - LevelSettings
 * - 
 * FIX monsters (new setup binding, orc is done) maybe consider new setupways?
 * FIX UI
 * FIX Spawnsystem or recreate(?) combinbed with UI ofc.
 * INSERT HEALING / ABILITYACTIONS - so that they work and heal friendlies!
 *  Consider selftargeting function.   
 * 
 PROPERTIES
 * - HEALING %
 * - HEALING AOE
 * - HEALING AOE %
 * - CHAIN
 * 
 HEALING
 * - HOTS (?)
 * - CONVERT ALL DAMAGE DONE INTO HEALING DONE
 * Implement property actions on the towergeneral
 * - MANA
 * - COOLDOWN STUFF

 * (DONE)
 * PROPERTY
 * - HEALING
 * 
 * Implement property actions on the towergeneral
 * - HEALTH
 * 
 * 
 * (DONE)
 * Currently the tower general is not taking care of damage input
 * - Dmg input is done in CustomTileStructureDataComponent
 *   - Remake this onto towergeneral or something very general for all towers/structs to come
 * 
 * (DONE)
 * PROPERTY (?)
 *  - MANA COST
 *  - MANA REGEN
 *  - COOLDOWN
 *  - HAVENT DONE INTEGRATION OF FUNCTION
 * 
 * 
ITEM : (itemwindow) USER PROFILE DISPLAY
 *        - INCLUDE LEVEL PROGRESSION UPGRADE
 ITEM : (itemwindow) ADVANCED ITEM PROFILE DISPLAY
 * 
 * Fix win window items
 CREATE STATS
 *  - Kills
 *  - Damage done
 *  - Items found
 *    - Rarities
 *  - Healing done
 *  - Projectile fired
 *  - Everything
 *  
 CREATE STATS MANAGER

 * 
 UI MONSTERS
 * - DMG Taken numbers
 * - HEALTH BAR?
 * - Animation on dmg taken (blink red?)
 * 
ITEM RARITY SYSTEM
 * - Display on item
 * 
ITEM EXPERIENCE SYSTEM
 * - Monsters give EXP based on dmg taken towards: tower and mod
 * 
DONE 04/05/2021
ITEM
 * - WINDOW ITEM SYSTEM
 *   - DISPLAY CERTAIN WINDOW UPON THE SPECIFIC ITEM IN THE TOWER
 * 
DONE 03/05/2021
 * UI WINDOW INSPECT ITEM STATS
 * - HOVER
 *   - HOVER ON WORLD ITEM (LEFT OUT FOR NOW)
 *   - HOVER ON INVENTORY ITEM
 * 
 * DONE 20/04/2021:
 * DICTIONARY JSON https://odininspector.com/tutorials/serialize-anything/serializing-dictionaries
 * ITEMIZATION
 * - Items with random stats
 *  - Range
 *  - Damage
 *  - Damage %
 *  - Attack speed %
 *  - Projectile speed %
 *  - AOE range %
 *  - AOE damage
 *  - AOE damage %
 *  - Armor Penetration
 *  - Armor Penetration %
 *  - Poison Damage
 *  - Poison Damage %
 *  - Bleed Damage
 *  - Bleed Damage %
 *  
 *  - Armor
 *  - Armor %
 *  - Max Health
 *  - Max Health %
 *  - Health Regen
 *  - Health Regen %
 *  
 *  - Gold find %
 *  - Item Quantity Increase %
 *  - Item Quality Increase %
 *  - Experience Gain %
 *  - Experience Per kill
 *  
 *  - Life On Kill
 *  - Life On Hit
 *  
 *  - Slow on hit %
 *  - Knock back increase %
 * 
 * COMPLETE LIST WRITTEN FROM 14/04/2021
 * 
 * DONE 14/04/2021:
 * - BUG: Seems like WIN WINDOW appears multiple times (had a 3 time occurance spam)
 * - END SCREEN REWARD UI
 *    
 * 
 * __________________________________________________
 * 
 * OLD STUFF FOR INSPIRATION
 * __________________________________________________
 * CURRENCY (CURRENCIES)
 *    GOLD
 *    PLATINIUM
 *    DIAMONDS
 * 
 * ---------------------
 * 
 * TOWER
 *    CAN HAVE CUSTOM MODS APPLIFICATIONS
 *      HEALTH
 *      ARMOR
 *      RANGE
 *      DAMAGE APPLIFIER
 *      PROJECTILE SCALE
 *      PIERCE
 *      MORE... anything (?)
 *      
 *    DEFAULT HEALTH
 *    
 *    EXP SYSTEM (?)
 *      GROW THE CURRENT CUSTOM MODS
 *    UPGRADE SYSTEM
 *      UPGRADE SOME DEFAULT VALUES
 *        HEALTH
 *        RANGE (?)
 *      UPGRADE THE CURRENT CUSTOM MOD FURTHER
 *    
 * TOWER ITEM
 *    TOWER INVENTORY
 *    TOWER SYSTEM PLACEMENT
 *    TOWER VIEW STATS (MAYBE SOMETHING IN THE MAP CAN HELP HERE?)
 *    TOWER UPGRADE STATS (MAYBE SOMETHING IN THE MAP CAN HELP HERE?)
 * 
 * 
 * MORE MODS
 * ATTACK MODS
 *    RANGED:
 *    BEAM (PIERCE)
 *    BOOMERANG (PIERCE)
 *    BOMB (EXPLOSIVE)
 *    SPIKE (3 SHOTS HIT)
 *    ACCELERATE SPIKE(ACCELERATE)
 *    TRAP DROP (EXPLOSIVES)
 *      RANDOM ?
 *    SUMMON TANK
 *      
 *    NEAR:
 *      AOE WAVE
 *      AOE WING SWIPE ROTATE
 *    
 * SUPPORT MODS
 *    BUFF NEARBY TOWERS
 *    
 * GENERAL MODS
 *    PIERCE
 *      1-2-3-4 etc. (FIX)
 *    SLOW (hit)
 *      10%, 10.25%
 *    SLOW (on ground)
 *      20%, 20.20%, 2.4%,...
 *    EXPLOSIVE (applies current dmg*X)
 *      1, 1.05
 *    EXPLOSIVE RANGE
 *      1, 1.05
 *    
 *    FIRE (on ground)
 *    HOMING (Targets mobs)
 *    
 *    EXTEND DURATION (of mods)
 *    
 * 
 * ---------------------------
 * Save inventory system
 * ---------------------------
 * 
Create UI
 *  Make Building
 *  
Create AI
 *  Make Enemies
 *  Set criteria
 *  
 Create World Rules
 *  Waves?
 *  - Select wave
 *    - Select Wave Type
 *      - Fast
 *      - Heavy
 *      - Balanced
 *  - Boss wave
 *    - Every 10 waves
 *  - Random wave
 *    - Can come within other waves
 *    - Contains special units
 *      - Gold hoarders
 *      - Tower seekers (attack towers)'
 *  
Destroy?
 *  Levels?
 *  Resources
 *    Nature
 *      Gold, Wood, Stone, Jewels, Water,
Monsters
 *      Currency(?)
 *      Mods
 *        A monster drops a mod that can enhance towers abilities
 *        Mod types:
 *          Projektile
 *            Arrow - 1 target point high damage
 *            Bolt - 1 target follow medium damage
 *            Bomb - 1 target point low damage AOE
 *            Cutter - 1 target point damage all passing
 *            
 *            
 *        Mods levels:
 *          1. 
 *            
 *            
Mods types:
 * - Projectile
 * - Enhancers
 *    - Self Enhancer
 *      - Increase attack speed
 *      - Increase projectile speed
 *      - Increase attack damage
 *      - Decrease projectile speed
 *      - Increase projectile size
Other Enhancer (all projectiles nearby gets buff)
 *      - Increase attack speed
 *      - Increase projectile speed
 *      - Increase attack damage
 *      - Decrease projectile speed
 *      - Give projectiles splash
 *      - Increase projectile size
 Modifiers
 *    - 1,2,3,4~ Arrows per shot
 *    - Add splash
 *    
 * 
 Advance?
 *  Items
 *  Levels
 *  Upgrades 
 * Towers need ammunition
- Generate ammo on upgrades / levelups (?)
