<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>wise101的博客</title>
<link href="css/mymenu.css" rel="stylesheet" type="text/css" />
<script language="JavaScript" src="js/jquery.js"></script>
<script type="text/javascript">
$(function(){  
    //导航切换
    $(".menuson .header").click(function(){
        var $parent = $(this).parent();
        $(".menuson>li.active").not($parent).removeClass("active open").find('.sub-menus').hide();

        $parent.addClass("active");
        if(!!$(this).next('.sub-menus').size()){
            if($parent.hasClass("open")){
                $parent.removeClass("open").find('.sub-menus').hide();
            }else{
                $parent.addClass("open").find('.sub-menus').show();    
            }   
        }
    });
    // 三级菜单点击
    $('.sub-menus li').click(function(e) {
        $(".sub-menus li.active").removeClass("active")
        $(this).addClass("active");
    });

    $('.title').click(function(){
        var $ul = $(this).next('ul');
        $('dd').find('.menuson').slideUp();
        if($ul.is(':visible')){
            $(this).next('.menuson').slideUp();
        }else{
            $(this).next('.menuson').slideDown();
        }
    });
})  
</script>
</head>
<body style="background:#f0f9fd;">
    <div class="lefttop"><span></span>文章列表</div>
    <dl class="leftmenu">
    <dd>
    <div class="title">
    <span><img src="images/leftico01.png" /></span>IT技术
    </div>
        <ul class="menuson">
        <li  class="active">
            <div class="header">
            <cite></cite>
            <a target="rightFrame">C++</a>
            <i></i>
            </div>
            <ul class="sub-menus">
            <li><a href="IT/C++/VS2013编译zlib.html">VS2013编译zlib</a></li>
            <li><a href="javascript:;">001-001-02</a></li>
            <li><a href="javascript:;">001-001-03</a></li>
            <li><a href="javascript:;">001-001-04</a></li>
            </ul>
        </li>
        <li>
            <div class="header">
            <cite></cite>
            <target="rightFrame">Java</a>
            <i></i>
            </div>                
            <ul class="sub-menus">
            <li><a href="javascript:;">001-002-01</a></li>
            <li><a href="javascript:;">001-002-02</a></li>
            <li><a href="javascript:;">001-002-03</a></li>
            <li><a href="javascript:;">001-002-04</a></li>
            </ul>
        </li>
        </ul>    
    </dd>

    <dd>
    <div class="title">
    <span><img src="images/leftico02.png" /></span>Diary
    </div>
    <ul class="menuson">
        <li><cite></cite><a href="diary/counterattack of nephew.html" target="rightFrame">外甥的逆袭</a><i></i></li>
        </ul>     
    </dd> 
    </dl>
</body>
</html>