
##jQuery选择器
###基本选择器
1. 标签名选择器
	$("div")  匹配文档中所有div
2. id选择器
	$("#id") 
3. 类选择器
	$(".类名")
4. 分组选择器
	$("div,#id,.class")
5. 所有元素选择器
	$("*")
###层级选择器
1. $("div span") 匹配div下所有的span元素
2. $("div>span") 匹配div下所有span的子元素
3. $("div+span") 匹配div后面紧邻的span兄弟元素
4. $("div~span") 匹配div后面所有的span兄弟元素

###层级函数
1. 获取元素的所有兄弟元素
				$("#two").siblings("div")
2. 获取元素的哥哥元素
				$("#two").prev("div")
3. 获取元素的哥哥们元素
				$("#two").prevAll("div")
4. 获取元素的弟弟元素
				$("#two").next("div")
5. 获取元素的弟弟们元素
				$("#two").nextAll("div")

###过滤选择器
1. $("div:first") 匹配所有div中的第一个元素
2. $("div:last") 匹配所有div中的最后一个元素
3. $("div:even") 匹配所有div中偶数div 从0开始
4. $("div:odd") 匹配所有div中奇数div 从0开始
5. $("div:eq(n)")匹配所有div中下标为n元素从0开始
6. $("div:lt(n)")匹配所有div中下标小于n元素0开始
7. $("div:gt(n)")匹配所有div中下标大于n元素0开始
8. $("div:not(.one)")匹配所有div中 class不为one的元素

###内容选择器
1. $("div:has(p)") 匹配所有包含p标签的div
2. $("div:empty") 匹配所有空的div
3. $("div:parent") 匹配所有 非空的div
4. $("div:contains('id')") 匹配文本内容包含id的div
###可见选择器
1. $("div:hidden") 匹配所有隐藏的div元素
2. $("div:visible") 匹配所有可见的div元素 

###jq中显示相关的函数
			//让隐藏的元素显示
			//$("div:hidden").show();
			//让显示的元素隐藏
			//$("div:visible").hide();
			//切换元素的显示状态
			//$("div").toggle();
###属性选择器
1. $("div[id]") 匹配有id属性的div元素
2. $("div[id='d1']")匹配id属性等于d1的div
3. $("div[id!='d1']")匹配id属性不等于d1的div

###子元素选择器
1. $("div:nth-child(n)") n从1开始，匹配div中第n个子元素
2. $("div:first-child") 匹配div中第1个子元素
3. $("div:last-child") 匹配div中最后一个子元素

###表单选择器
1. $(":input") 匹配所有的 input中 文本框 密码框 单选，复选框 下拉选 文本域(textarea) button
2. $(":password") 匹配所有密码框
3. $(":radio") 匹配所有单选
4. $(":checkbox")匹配所有复选框
5. $(":checked")匹配所有被选中的 单选/复选/下拉选option
6. $("input:checked")匹配所有被选中的单选和复选
7. $(":selected")匹配所有被选中的下拉选option

##文档操作
1. 创建元素
	var $d = $("<div>abc</div>");
2. 添加元素
- $("#big").append($d); //最后面
- $("#big").prepend($d)；//最前面
3. 插入元素
- 兄弟元素.after($d);//插入到兄弟元素的后面
- 兄弟元素.before($d);//插入到兄弟元素的前面
4. 删除元素
- 通过自己删除 $("#id").remove();
- 先得到所有的li 然后删除里面id为sh的
		 $("li").remove("#sh");
5. 修改样式
	
		$("#id").css("width","40px")//设置宽度
		$("#id").css("width")//获取宽度
6. 属性
		
		$("#id").attr("id","xx")//设置id属性
		$("#id").attr("id") //获取id
7. 文本
		
		$("#id").text("xxx")//设置元素文本
		$("#id").text()//获取文本
8. html
		
		$("#id").html("xxx")//设置元素html代码
		$("#id").html()//获取html代码




#选择器
###基本
1. 标签名
2. id
3. 类
4. 分组
5. *
###层级
1. div span
2. div>span
3. div+span
4. div~span
###层级函数
siblings 所有兄弟
next 弟弟  nextAll所有弟弟 prev哥哥 prevAll哥哥们
###过滤
1. div:first
2. last
3. even
4. odd
5. eq()
6. not()
7. lt()
8. gt()
###内容
1. div:has(p)
2. div:empty
3. div:parent
4. div:contains('a')
###可见
1. div:hidden
2. div:visible
show()  hide() toggle()
###属性
1. div[id]
2. div[id='xx'];
3. div[id!='xx'];
###子元素
1. div:nth-child(n) 1开始
2. div:first-child
3. div:last-child
###表单选择器
1. :input
2. :password
3. :radio
4. :checkbox
5. :checked 单选、多选、下拉选
6. input:checked 单选、多选
7. :selected 下拉选

###文档操作：
1. 创建  var $d = $("<div></div>");
2. 添加  上级.append  上级.prepend()
3. 插入 兄弟.after()  兄弟.before()
4. 删除  元素.remove()  $("li").remove("#id");
5. 样式 元素.css("width","20px")
6. 属性 元素.attr("id","xx")
7. 文本 元素.text()
8. html 元素.html()

