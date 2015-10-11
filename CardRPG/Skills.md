##General
- 技能不会和职业绑定，不过技能会有职业限制
- 技能分为 Positive（主动技能）, 主动技能只能在准备阶段发动 ;Passive（被动技能）,~~被动技能会有一个发动触发器~~，改成附加状态或者Buff。
- 技能会有等级和熟练度，一定的熟练度可以提升等级

##Skills
- Attack
	- requirement: General
	- max level: 30
    - cost: Weapon * 1
    - cooldown: 0
    - type: Positive
    - target    //先不做，目前只做1v1
    	- type: emeny
    	- number: 1
    - effect: 根据消耗卡片进行一次攻击,伤害修正 * (1 + level * 0.02)

- Defense
	- requirement: General
	- max level: 30
    - cost：Armor * 1
    - cooldown: 0
    - type: Positive
    - target
    	- type: self
    	- ..
    - effect: 根据消耗卡片进行一次防御,防御修正 * （1 + level * 0.01）

- Power Attack
	- requirement: General
	- max level: 20
    - cost: Weapon * 2
    - cooldown: 1
    - type: Positive
    - target
    	- type: enemy
    	- number: 1
    - effect: 消耗卡片的damage sum * (0.9 + level * 0.02)

- Dartle
	- requirement: General
    - cost: *Bow* * 2
    - cooldown: 2
    - type: Positive
    - target
    	- type: enemy
    	- number: 1
    - effect: 武器damage * .7 连续3次攻击，每次攻击附带无视防御的伤害（Agi * 0.3）

- Magic Bullet
	- requirement: General
    - cost: element * 1
    - cooldown: 0
    - type: Positive
    - target: ...
    - effect: 造成Int * element.Purity * .5的伤害

- Reload
	- buff: reload to player
	- requirement: General
    - type: Passive
    - effect: 有 (Int/10)% ， 不超过10%的几率再抽一张牌