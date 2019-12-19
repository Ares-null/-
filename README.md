# -评教点“非常满意”点到手抽筋？
# -试试它
# -1、进入评教页面
![Aaron Swartz](https://github.com/Ares-null/-/blob/master/%E9%A1%B5%E9%9D%A21.png)
# -2、按键盘F12 进入浏览器调试
# -3、点击console（控制台）
![Aaron Swartz](https://github.com/Ares-null/-/blob/master/%E9%A1%B5%E9%9D%A22.jpg)
# -4、黏贴下列js代码
```
<p>function fun(){
	var inp=document.getElementsByTagName("input");
    var eg = /^pj.*1$/;
    var eg2 =  /^pj.*2$/; 
    var f = 0;
	for(let i = 0 ; i < inp.length ; i++){
	    var t = inp[i];
	    if(t.type == "radio"&&eg.test(t.id)){
	        t.checked = true;
        }
    }
    for(let i = 0 ; i < inp.length ; i++){
        var sp = inp[i];
        if(sp.type == "radio"&&eg2.test(sp.id)){
            f++
            if(f==10){
                sp.checked = true; //修改f==其他数字可改变“满意”所在位置
            }
        }
    }
};

fun();</p>
```
# -5回车运行即可

ps ： 理论上智科技教务系统均可如此操作，此程序除了第十条均会选择“非常满意”，如需修改可按注释操作
