放大镜：用于给用户提供一个查看商品详细信息的方式

界面、效果：左侧一个小图，鼠标悬浮移动，右侧显示对应位置的大图

实现要点：
1、设置小滑块move的移动事件,为了不让鼠标脱离move，就把移动事件作用在   move的父级元素small上
   var newLeft = e.pageX - move.offsetWidth / 2 - show.offestLeft;
   var newTop = e.pageY - move.offsetHeight / 2 - show.offsetTop;

注意：鼠标的参考点：一定要是文档的左上角，不能是可视区域屏幕的左上角


2、滑块临界点的判定
   水平方向的临界点：
	if(newLeft <= 0){ newLeft = 0 ;}
	if(newLeft >= (small.offsetWidth - move.offsetWidth)){
	    newLeft = (small.offsetWidth - move.offsetWidth;
	}
   垂直方向的临界点：
	if(newTop <= 0){ newTop = 0 ;}
	if(newTop >= (small.offsetHeight - move.offsetHeight)){
	    newTop = (small.offsetHeight - move.offsetHeight;
	}

3、当小滑块移动时，右边的大图如何进行移动显示？
   根据等比例显示原则：
	小滑块.newLeft / small.width = bigPic.newLeft / bigPic.width
        小滑块.newTop / small.Height = bigPic.newTop / bigPic.height


     newLeft / small.offsetWidth = newBigPicLeft / bigPic.offsetWidth
     newTop / small.offsetHeight = newBigPicTop / bigPic.offsetHeight

==>>var newBigPicLeft  
==>>var newBigPicTop

注意：滑块右移动，大图向左、向上移动，注意设置top和left是负值。

4、滑块的宽度 / small的宽度 = big的宽度 / 图片自身的宽度
==>>可以得出滑块的具体宽度

5、初始状态时，big和move不显示

6、设置small的鼠标移入、离开事件

7、定义商品列表,再定义商品列表各项的鼠标悬浮事件
   鼠标悬浮在商品列表，大小图区域内显示对应的图片