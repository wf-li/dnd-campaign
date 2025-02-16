---
layout: monster

# Monster template for Jekyll
name: "Ruin Machine (Melee)"
type: "Large machine"

# Basic Description
physical_description: |
  An ancient golem-like contraption that runs on a magical core. It stand 8ft tall and has 
  two legs and four arms. At the end of each arm is an enclosed ball that can be used as a blunt weapon.
  The ball can also open to fire a mana-based projectile.

# Combat Stats
combat_stats:
  armor_class: 
    value: 5
    type: "metal armor"
  hit_points:
    value: 50
    formula: "5d10 + 25"
  speed:
    walk: 30

# Attributes
attributes:
  strength:
    score: 22
    modifier: 6
  dexterity:
    score: 10
    modifier: 0
  constitution:
    score: 20
    modifier: 5
  intelligence:
    score: 10
    modifier: 0
  wisdom:
    score: 10
    modifier: 0
  charisma:
    score: 10
    modifier: 0

# Skills and Senses
skills:
  - name: "Melee"
    bonus: 5

senses:
  darkvision: 60
  passive_perception: 10

languages: []  # Empty array for no languages

# Special Abilities
special_abilities:
  - name: "Core"
    description: "The core has a separate HP value of 20."

# Actions
actions:
  - name: "Smash"
    type: "Melee Weapon Attack"
    reach: 5
    damage:
      dice: "2d6"
      modifier: 5
      type: "blunt"
    additional_effects: "If the target is Medium or smaller, it must succeed on a DC 15 Strength saving throw or be knocked down."
  
  - name: "Ground Slam"
    type: "Area of Effect Attack"
    reach: 5
    damage:
      dice: "2d4"
      modifier: 5
      type: "blunt"
    additional_effects: "DC 10 Strength saving throw or be knocked down."
  
  - name: "Beam"
    type: "Area of Effect Magical Attack"
    reach: 30
    damage:
      dice: "2d4"
      modifier: 5
      type: "fire"
    additional_effects: "Mark ground. On it's next turn, the ground erupts into fire, dealing burn damage."

# Ecology and Behavior
behavior_and_ecology: |
  Man-made creations of the ancient first civilization. They are capable of being remotely controlled from a short distance
  or functioning completely autonomously. Though their physical strength is exceptional, their magical laser is also highly
  dangerous. 

habitat_and_distribution:
  preferred_locations:
    - "Ancient forests with dense canopies"
    - "Deep cave systems"
    - "Ruins of forgotten civilizations"
    - "Areas with frequent magical anomalies"
  description: "Wherever their masters left them behind."

dm_notes:
  suggested_uses:
    - "A guardian of ancient ruins or artifacts"
    - "Those aligned with the first civilization."
  tactical_notes: "The core can be found by a variety of means."
--- 