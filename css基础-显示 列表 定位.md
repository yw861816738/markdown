# 显示
	
==显示方式==
	
	1.决定元素在网页中的表现形式
	
	2.语法
		属性：display
			取值：
				1、none
					不显示元素 - 隐藏
					特点：脱离文档流 - 不占据页面空间
				2、block
					让元素表现的与块级元素一致
				3、inline
					让元素表现的与行内元素一致
					特点：
						不允许修改尺寸
						多个元素在一行
						无法修改垂直外边距
				4、inline-block
					让元素表现的与行内块元素一致
					特点：
						允许修改尺寸
						多个元素在一行显示
				5、table
					让元素表现的与表格一致
					特点：
						尺寸以内容为准
						每个元素独占一行
						允许修改尺寸
						
==显示效果==
	
	1.显示/隐藏属性
		1、显示 / 隐藏属性
			属性：visibility
			取值：
				1、visible : 默认值，元素可见
				2、hidden : 元素不可见 - 隐藏
			==面试：
				Q:display:none 和 visibility:hidden 区别
					display:none 会脱离文档流，所以不占空间
					visibility:hidden,不脱离文档流，占据空间==
	2.透明度
		属性：opacity
			取值：0.0(完全透明) ~ 1.0(完全不透明)
			注意：
				rgba 与 opacity 的区别
				==rgba作用于背景 opacity 作用于背景和内容==
	3.垂直方向对齐方式   
	   属性：vertical-align
			场合：
				1、表格中使用
					取值：top / middle / bottom
				2、图片(img)中使用
					作用：控制图片两边的文本的垂直对齐方式
					取值：
						1、top 
						2、middle
						3、bottom
						4、baseline ：基线对齐,默认值
					注意：
						编写网页时，通常都会将所有图片的垂直对齐方式更改为除baseline以外的任何一个值
						img{
							vertical-align:bottom;
						}
==光标==
	
	1.作用
		改变鼠标悬停在元素上时，鼠标的状态

	2.取值
		1、default
		2、pointer ：小手
		3、crosshair ：+
		4、text ：I
		5、wait ：等待
		6、help ：帮助

# 列表
	1.列表项标志
		属性：list-style-type 
		取值  none
	2.列表项图像
		作用：使用自定义图像作为列表项标志
		属性：list-style-image
		取值：url();
	3.列表项位置
		作用：将默认的列表项标志的位置，放到li的里面
		属性：list-style-position
		取值：
			1、outside
				默认值，将标志放置与li的外面
			2、inside
				将标志放置于li的里面
	4.列表属性
		属性：list-style
		取值：type url() position;
		常用方式：
			list-style:none;
	5.列表使用场合
	   横向排列 或 纵向排列的内容，都可以使用列表来实现
	
# 定位
	
## 相对定位  绝对定位 固定定位
	==定位相关属性==
	
	 1.定位方式属性
	 	属性：position 
		取值：
			1.static
			2.relative 相对定位
			3.absolute 绝对定位
			4.fixed 固定定位
		**注意**
		==将元素的position设置为relative/absolute/fixed
		任何一种的时候 那么该元素就称为“已定位元素”==
	2.偏移属性
		top  /  right /  bottom   /  left
		以上属性取值均为数字
		**注意**
		==只有已定位的元素才能使用偏移属性==
	==定位方式==
		
		1、相对定位
			1.元素会相对于它原来的位置偏移某个距离
			2.场合
				位置微调时使用
			3.语法
				position: relative; 配合着【偏移属性实现微调】
		2、绝对定位
			1.** 1、绝对定位的元素会脱离文档流 - 不占空间
				2、绝对定位的元素会相对于离它最近的，已定位的，祖先元素 去实现位置的初始化
				3、如果没有已定位的祖先元素的话，那么元素就相对于body去实现位置的初始化
				4、配合 偏移属性 实现元素位置的修改**
		   2.语法
			   position：absolute配合着偏移属性实现微调
			3.使用场合
				1、有堆叠效果的元素
				2、弹出菜单
			4、注意
				1、脱离文档流-不占用空间
				2、绝对定位元素会变成块级元素
				