---
layout: monster

# Monster template for Jekyll
name: "Shadowmaw Stalker"
type: "Large monstrosity"

# Basic Description
physical_description: |
  A Shadowmaw Stalker appears as a sleek, panther-like creature standing nearly 5 feet tall at the shoulder, 
  with jet-black fur that seems to absorb light. Its most distinctive feature is its oversized maw, 
  which can unhinge like a snake's to swallow larger prey. Peculiar purple markings along its flanks 
  emit a faint glow in darkness, serving as a natural lure for prey.

# Combat Stats
combat_stats:
  armor_class: 
    value: 15
    type: "natural armor"
  hit_points:
    value: 85
    formula: "10d10 + 30"
  speed:
    walk: 40
    climb: 30

# Attributes
attributes:
  strength:
    score: 18
    modifier: 4
  dexterity:
    score: 16
    modifier: 3
  constitution:
    score: 16
    modifier: 3
  intelligence:
    score: 7
    modifier: -2
  wisdom:
    score: 14
    modifier: 2
  charisma:
    score: 10
    modifier: 0

# Skills and Senses
skills:
  - name: "Stealth"
    bonus: 6
  - name: "Perception"
    bonus: 5
  - name: "Athletics"
    bonus: 7

senses:
  darkvision: 60
  passive_perception: 15

languages: []  # Empty array for no languages

challenge_rating:
  rating: 6
  xp: 2300

# Special Abilities
special_abilities:
  - name: "Shadow Camouflage"
    description: "The Shadowmaw Stalker has advantage on Stealth checks made in dim light or darkness."
  
  - name: "Pounce"
    description: "If the Shadowmaw Stalker moves at least 20 feet straight toward a creature and then hits it with a claw attack on the same turn, that target must succeed on a DC 15 Strength saving throw or be knocked prone."
  
  - name: "Light Sensitivity"
    description: "While in bright light, the Shadowmaw Stalker has disadvantage on attack rolls and Perception checks that rely on sight."

# Actions
actions:
  - name: "Multiattack"
    description: "The Shadowmaw Stalker makes two attacks: one with its bite and one with its claws."
  
  - name: "Bite"
    type: "Melee Weapon Attack"
    to_hit: 7
    reach: 5
    damage:
      dice: "2d10"
      modifier: 4
      type: "piercing"
    additional_effects: "If the target is Medium or smaller, it must succeed on a DC 15 Strength saving throw or be swallowed whole."
  
  - name: "Claws"
    type: "Melee Weapon Attack"
    to_hit: 7
    reach: 5
    damage:
      dice: "2d6"
      modifier: 4
      type: "slashing"
  
  - name: "Shadowmeld"
    usage: "1/Day"
    description: "As a bonus action, the Shadowmaw Stalker can magically become invisible until the end of its next turn or until it makes an attack."

# Ecology and Behavior
behavior_and_ecology: |
  Shadowmaw Stalkers are solitary ambush predators that prefer to hunt in twilight hours or complete darkness. 
  They make their lairs in dense forests or cave systems, often claiming territories spanning several miles. 
  Their glowing markings serve a dual purpose: attracting prey in darkness and communicating with others of 
  their kind during mating season.

  These creatures are known to be particularly intelligent for beasts, displaying complex hunting strategies 
  and an ability to remember and adapt to adventuring parties' tactics. They've been known to stalk groups 
  for days, learning their patterns before striking at the most opportune moment.

habitat_and_distribution:
  preferred_locations:
    - "Ancient forests with dense canopies"
    - "Deep cave systems"
    - "Ruins of forgotten civilizations"
    - "Areas with frequent magical anomalies"
  description: "They prefer regions where natural shadows are abundant and prey is plentiful."

dm_notes:
  suggested_uses:
    - "A recurring threat that stalks the party through a forest"
    - "A guardian of ancient ruins or artifacts"
    - "Part of a local noble's exotic creature collection"
    - "The source of mysterious disappearances in a village"
  tactical_notes: "The creature's intelligence and stealth capabilities make it an excellent choice for creating tension and encouraging players to think tactically. Its sensitivity to bright light gives players a clear advantage to exploit if they can figure it out."
--- 