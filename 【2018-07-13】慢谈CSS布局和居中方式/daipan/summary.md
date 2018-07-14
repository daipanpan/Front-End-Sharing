# 1.0 演讲课题：漫谈CSS布局和居中方式
方式：思路+应用场景+对应实例。（摘取自己平和是项目中会应道的实例场景）
演讲思路：总——分——总

1.margin: 0 auto; width: 固定值
2.width:100%；margin: 0 200px 0 400px; +position/float
3.display: inline-block; text-align:center; font-size:0;
4.（居中元素定宽高）position:absolute; top:50%; left:50%; margin-left: 负的元素的宽度的一半; margin-top:  负的元素高度的一半。
5.（元素定宽高）也可用calc实现，calc的坑calc（100% - 100px）”减号左右要有空格”
6.position: absolute; top:0; left:0; right:0; bottom:0; margin:auto;
7.垂直居中：
	line-height  文字单行垂直居中
8.文字单行居中和多行居中。display:table -cell + vertical-align:middle
	
布局：
div+ css，float，position，table，flex，百分比布局


7.水平垂直居中，图片按比例等比缩放，sticky footer。


推荐书籍《css世界》——基础进阶  《css禅意》—-进阶css技术

问题：1.一直有一些代码洁癖，喜欢代码架构，如何进阶这块是个问题？时间是否充裕、通过什么方式进阶？（多研究别人的好代码，多看一下前端架构的文章，可能会涉及到一些设计模式）