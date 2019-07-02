[QQ空间自动点赞js脚本](https://www.cnblogs.com/leixiao-/p/9829162.html)

```javascript
function autoLike()
{
    var list=document.getElementsByClassName("item qz_like_btn_v3 ");
    for(i=0;i<list.length;i++)
    {
        if(list[i].attributes[6].value=='like')
        {
            list[i].firstChild.click();
        }
    }
}
 
function renovate()
{
    document.getElementsByClassName("ui-icon  icon-refresh-v9")[0].click();
}
 
function likeAll()
{
    autoLike();
    window.scrollBy(0,500);
}
 
function likeNew()
{
    autoLike();
    renovate();
}
 
var choice=prompt("请输入功能选项:\n1:自动翻阅空间，点赞空间以往动态\n2:自动刷新，点赞最新动态\n\n———By:淚笑 QQ:1729888211","1");
if(choice=='1')
{
    var time=prompt("自动翻阅空间，点赞空间以往动态\n请输入翻阅时间间隔(建议5秒):\n\n———By:淚笑 QQ:1729888211","5")*1000;
    window.setInterval(likeAll,time);
}
else if(choice=='2')
{
    var time=prompt("自动刷新，点赞最新动态\n请输入刷新时间间隔(建议300秒):\n\n———By:淚笑 QQ:1729888211","300")*1000;
    window.setInterval(likeNew,time);
}
else
{
    alert('退出程序')
}
```



