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
