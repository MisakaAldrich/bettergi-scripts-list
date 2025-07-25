# 1. JS脚本的关键配置和路径选择

 - **注意:**
	只有严格按照以下步骤配置后才能使用，否则将**无法运行**（也可以参考左下角的日志来确认下一步需要如何配置）

 - **配置步骤:** 
	
	未配置的情况下直接运行左下角日志会显示```请在assets/pathing文件夹手动添加路径文件夹后重新运行...```，代表你需要进行如下配置
	
	1. 将你的路径文件夹(该文件夹内尤其仅有.json后缀的路径文件)复制粘贴到```assets/pathing```路径
	
	2. 确保原神左上角有派蒙图像，在**调度器**直接运行脚本，左下角日志出现```JS脚本配置已更新，请重新选择路径...```字样代表JS脚本已经加载了上一步中的路径文件夹，此时脚本应该已经**结束运行**
	
	3. 在**调度器**右键脚本，点击**修改JS脚本自定义配置**选择你要执行的路径-配置好所有的JS配置（配置项**路径设置-选择要执行的路径文件夹**就是你刚放入的路径文件加名称）
	
	4. 该步骤根据你选择的加世界模式有所区别
	
		1. 手动加世界
	 
			确保在**多人模式**下，运行脚本，此时脚本会在聊天框发送校验信息，代表脚本正常运行
		
		2. 自动加世界
		
			确保在**单人模式**下，运行脚本，此时脚本会自动等待队员加入(作为领队)或加入队长世界(作为队员)，代表脚本正常运行
	
		

 - **更多的路径：**
	
	如果需要添加更多的路径文件，请重复以上**配置步骤**的```1-4```添加路径文件夹即可(文件夹名称不可重复)
	
	添加完成后在**JS脚本自定义配置**的**请选择要执行的路径文件夹**下拉菜单选择对应的路径

# 2. JS脚本自定义配置说明

 - **选择加入世界的方式**
 
	1. 自动加世界 \[推荐\]
		
		选择这个选项后，需要配置下方的```自动加世界```内的三个配置项
	
	2. 手动加世界
	
		选择这个选项后，需要配置下方的```自动加世界```内的两个个配置项

 - **手动加世界-请挑选你的玩家标识:**
 
	手动加世界模式下，在所有人都已经加入世界的情况下，你的玩家标识

 - **手动加世界-选择玩家总数:**
 
	手动加世界模式下，在所有人都已经加入世界的情况下的玩家总数

 - **自动加世界-请挑选你的身份:**
 
	自动加世界模式下，你作为领队还是队员（领队只能存在一个，选择多个可能会报错）

 - **自动加世界-文本输入框**
 
	1. 作为领队
	
		填入要加入你世界的所有玩家的昵称（顺序无关），每个玩家的名称ID使用单个空格隔开
	
	2. 作为队员
	
		填入你要加入的世界（队长）的UID
	
 - **自动加世界-名称匹配模式:**
 
	自动加世界模式下，匹配玩家名称的匹配方式（仅队长生效）
	
	1. 全字匹配（此模式下请使用玩家的全称）
	
		匹配玩家的完整名称，在玩家的名称便于识别时使用
	
	2. 部分匹配（此模式下请填入玩家名称内易于识别的**连续文本**）
	
		匹配玩家名称内包含的文本，在玩家的名称难以识别时使用
 
 - **路径设置-选择要执行的路径文件夹**
 
	初次使用时该下拉菜单为空，详情配置见下方```2. JS脚本的关键配置和路径选择```

# 3. 注意事项

	所有人使用的路径文件夹及其内容应当**完全一致**，否则验证失败会导致脚本异常终止

 - **路径文件夹存放位置:** ```assets/pathing```

	假设你有一个文件夹名为```死亡笔记-400```，这个文件夹内含有若干个```.json```后缀的路径文件，你需要将```死亡笔记-400```文件夹复制粘贴到```assets/pathing```文件夹内
	
 - **路径相关格式:** ```assets/pathing/你的路径文件夹名/若干路径文件.json...```
 
	路径```assets/pathing```内只能存放文件夹，存放其他文件无效
	
	路径```assets/pathing你的路径文件夹名```内只能存放```.json```后缀的文件

 - **assets/pathing文件夹下已经内置了部分路径**
	
	内置的路径已经做过联机情况下的适配，可以放心使用

# 4.适用场景

 - **同步运行同一组路径追踪文件**
 
	自行探索，理论上所有地图追踪文件都可以同步执行

 - **配置了本地远程，可以在一个设备上运行两套原神+BGI：**
 
	可以用两个账号实现双倍的锄地收益，例如在调度器内都配置两个锄地脚本，一个先作为房主后作为成员，另一个先作为成员后作为房主，可以自动实现两个号同时锄地，锄完两个世界的资源
	
 - **和其他BGI用户一起锄地：**
 
	所有人协商好，正确导入相同的路径后就可以实现2-4人的联机锄地（路线进度将保持同步，确保所有玩家都能获得相同的收益）
