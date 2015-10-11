##General
- 战斗中双方的附加状态
- Buff分为可见和不可见，固有和动态的。
- 可见Buff会在战斗中的状态栏显示出来
- 固有和动态是为了驱散buff效果（净化等）做准备
- 被动技能是不可见，固有的buff
- buff有发动时机，当前的时机有回合每个阶段开始时，在结算阶段造成伤害、收到伤害
- buff分为增益和减益
- buff有持续时间属性，可以为infinate（永久）

##Buffs
- Reload 再装载
	- Invisible, Inherent
	- isDebuff: false
	- timing: 抽牌阶段
	- effect: 有一定几率再抽一张牌

- Dizzy 眩晕（其他同样效果的状态可以继承）
	- visible, normal
	- isDebuff: true
	- timing: 准备阶段
	- effect: 有几率跳过准备阶段

- Flash Shock
	- visible, normal
	- isDebuff: true
	- timing: 攻击时
	- effect: 见Flash Shock技能