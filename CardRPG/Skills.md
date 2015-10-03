##General
- 技能不会和职业绑定，不过技能会有职业限制
- 技能分为 Positive（主动技能）, Passive（被动技能）

##Skills
- Attack: 
	requirement: General
    cost: Weapon * 1
    cooldown: 0
    type: Positive
    target: [type: emeny, number: 1]
    effect: 根据消耗卡片进行一次攻击
___

- Defense:
	requirement: General
    cost：Armor * 1
    cooldown: 0
    type: Positive
    target: [type: self, ..]
    effect: 根据消耗卡片进行一次防御
___

- Power Attack:
	requirement: WarriorOnly
    cost: Weapon * 2
    cooldown: 1
    type: Positive
    target: [type: enemy, number: 1]
    effect: 消耗卡片的damage sum * 0.9
___

- Dartle:
	requirement: ArcherOnly
    cost: *Bow* * 2
    cooldown: 2
    type: Positive
    target: [type: enemy, number: 1]
    effect: 武器damage * .7 连续3次攻击，每次攻击附带无视防御的伤害（Agi * 0.3）
___

- Magic Bullet:
	requirement: MagicianOnly
    cost: element * 1
    cooldown: 0
    type: Positive
    target: [...]
    effect: 造成Int * element.Purity * .5的伤害