# Loot Table

根目录下只有`loot.yml`文件, 该文件用于控制战利品箱的资源产出. 提交代码后, 服务器会同步更新战利品表文件, 但需要在游戏内手动执行`/rc reload`才能使新的战利品表生效.

每20分钟重置服务器所有的战利品箱. 1个战利品箱可包含多个战利品表, 每个战利品表都将根据设定产生随机奖品, 将所有战利品表产出的奖品拼在一起, 即为战利品箱重置后的最终产出.

一份默认的战利品表模板如下.

```yaml
default_epic: # 战利品表名
  iron_ingot: # 当前战利品表下包含的战利品, 应使用自定义物品ID(游戏内指令获取)或1.16.4原版物品Material Name表示, 一律使用小写. Material Name列表可参考此链接: https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html
    chance: '50' # 当前战利品表下物品被成功抓取的概率
    min-quantity: '1' # 一旦抓取成功, 会产生战利品的最小数量, 占1格箱子物品栏
    max-quantity: '3' # 一旦抓取成功, 会产生战利品的最大数量, 占1格箱子物品栏
  gold_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
default_normal:
  iron_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
  gold_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
default_rare:
  iron_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
  gold_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
default_legendary:
  iron_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
  gold_ingot:
    chance: '50'
    min-quantity: '1'
    max-quantity: '3'
medical:
  bandage: # 绷带, 这是一件服务器自定义物品, 请在游戏中通过指令查询自定义物品ID
    chance: '43.5'
    min-quantity: '2'
    max-quantity: '5'
  adrenaline:
    chance: '16.6'
    min-quantity: '1'
    max-quantity: '1'
  antidote:
    chance: '3.7'
    min-quantity: '1'
    max-quantity: '1'
```
