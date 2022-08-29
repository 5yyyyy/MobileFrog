# MobileFrog
## 该说明仅针对此项目 此项目为手机游戏
### Unity版本 2022.1.8  

### 关于Game窗口转换为手机屏幕
在Game窗口左上方下拉栏选择Simulator为预览手机屏幕窗口  
在右侧下拉栏中可以选择开发的合适机型  

### 关于俯视角叠层渲染  
Edit --> Project Settings --> Graphics 选择Camera Settings --> Transparency Sort Mode --> Default更改为Custom Axis 之后将Transparency Sort Axis更改为以y轴为判定基准 即x为0 y为1 z为0(该功能仅针对需要俯视角叠层渲染的项目)

### 关于素材锚点更改
选择需要更改的素材在Inspector窗口中选择Sprite Editor后进入编辑界面 拖动图片中心锚点(蓝圈)进行锚点位置移动位置 也可以通过下方Custom Pivot直接赋值 Apply后将物体的排列点改为Pivot 方法为选中物体后在Inspector窗口中选择Sprite Sort Point --> Center更改为Pivot即可

### 关于图层排序  
选中物体后在Inspector窗口中选择Addtional Settings --> Sorting Layer --> Add Sorting Layer在其中增加或删除排列的图层 图层排序中越在下面则在游戏中越处于上层


### 关于更改使用新输入系统
Edit --> Project Settings --> Player --> Other Settings --> Configuration --> Active Input Handling将Input Manager(old)改为Input System Package(New) 更改完毕后在Windows --> Package Manager下找到Input System进行安装即可 Unity中报输入系统的错误可以将此项改为Both


### 关于新输入系统
新建输入系统在Project窗口中Create --> Input Actions 打开Input Actions即可编辑Input系统 在Action Maps中可以添加一套输入系统 Action中为对应的操作按键模式 一个行为对应着一套按键 Action Properties中Action --> Action Type可以设置输入类型 Interaction可以设置按键的规则

### 关于挂载新输入系统使用
在想要添加该输入系统的物体下添加Player Input组件 将Input Actions添加到Player Input --> Actions中即可 将Player Input --> Behavior中的Send Messages改为Invoke Unity Events做为事件即可使用新输入系统与脚本的方法 此项目使用回调函数获取输入行为做为判定依据 单点按为执行中执行逻辑 长按为按住后判定长按状态后进入松开执行逻辑 位置信息为判定按键位置时执行逻辑

### 关于动画挂载事件
添加对应动画后需要Add Event后选择脚本中的对应函数即可

### 关于相机镜头自适应
使用offset+transform.position.y控制镜头的偏移 写在LateUpdate方法中在下一帧执行保证镜头移动流畅度 
