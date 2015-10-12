##General
- 技能不会和职业绑定，不过技能会有职业限制
- 技能分为 Positive（主动技能）, 主动技能只能在准备阶段发动 ;Passive（被动技能）,~~被动技能会有一个发动触发器~~，改成附加状态或者Buff。
- 技能会有等级和熟练度，一定的熟练度可以提升等级
- 技能满级后可能会有附加效果，见[max]后的内容

##Skills
- Attack
	- requirement: General
	- max level: 5
    - cost: Weapon * 1
    - cooldown: 0
    - type: Positive
    - target    //先不做，目前只做1v1
    	- type: emeny
    	- number: 1
    - effect: 根据消耗卡片进行一次攻击,伤害修正 * (1 + level * 0.1)

- Defense
	- requirement: General
	- max level: 5
    - cost：Armor * 1
    - cooldown: 0
    - type: Positive
    - target
    	- type: self
    	- ..
    - effect: 根据消耗卡片进行一次防御,防御修正 * （1 + level * 0.06）

- Power Attack
	- requirement: General
	- max level: 5
    - cost: Weapon * 2
    - cooldown: 1
    - type: Positive
    - target
    	- type: enemy
    	- number: 1
    - effect: 消耗卡片的damage sum * (0.9 + level * 0.08)

- Dartle
	- requirement: General
	- max level: 5
    - cost: *Bow* * 2
    - cooldown: 2
    - type: Positive
    - target
    	- type: enemy
    	- number: 1
    - effect: 武器damage * (.7 + level * .04) 连续3次攻击，每次攻击附带无视防御的伤害（Agi * 0.2 + level * .04）

- Purify
	- requirement: General
	- max level : 3
    - cost: element * 1
    - cooldown: 1
    - type: Positive
    - target: ...
    - effect: 有（30 + level * 20）%几率除去对方的活动型buff或自己的debuff

- Flash Shock
	- requirement: General
	- max level : 5
	- cost: element * 2
	- cooldown: 2
	- type: Positive
	- effect: 附加一个buff: 回避对方该回合的攻击，并且接下来一回合攻击丢失率（30 + level * 10）%. [max]: 效果附加一回合，丢失率为当前的一半。

- Reload
	- buff: reload to player
	- max level: 5
	- requirement: General
    - type: Passive
    - effect: 有 （level * 2）%的几率再抽一张牌， [max]: 成功发动效果后有10%的几率再抽一张