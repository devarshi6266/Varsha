<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
 
    <b:include data='blog' name='all-head-content'/>

<b:if cond='data:blog.pageType == &quot;index&quot;'>
<title><data:blog.pageTitle/></title>
<b:else/>
<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
<title><data:blog.pageName/> - <data:blog.title/></title>
</b:if></b:if>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
<title>Page Not Found - <data:blog.title/></title>
<meta content='3;/' http-equiv='refresh'/>
</b:if>

<!-- [ Social Media meta tag ] -->
<b:if cond='data:blog.url == data:blog.homepageUrl'> 
<b:if cond='data:blog.pageType == &quot;item&quot;'> 
<b:if cond='data:blog.pageType == &quot;static_page&quot;'>  
<b:if cond='data:blog.url'>
<meta expr:content='data:blog.url' property='og:url'/>
</b:if>
<meta expr:content='data:blog.title' property='og:site_name'/>
<b:if cond='data:blog.pageName'>
<meta expr:content='data:blog.pageName' property='og:title'/>
</b:if></b:if></b:if></b:if>
 
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<meta content='article' property='og:type'/>
<b:else/>
<meta content='website' property='og:type'/>
</b:if>
<meta expr:content='data:blog.canonicalUrl' property='og:url'/>
<b:if cond='data:blog.postImageUrl'>
<meta expr:content='data:blog.postImageUrl' property='og:image'/>
<b:else/>
<b:if cond='data:blog.postImageThumbnailUrl'>
<meta expr:content='data:blog.postThumbnailUrl' property='og:image'/>
<b:else/>
<meta expr:content='data:blog.blogspotFaviconUrl' property='og:image'/>
</b:if></b:if>
<b:if cond='data:blog.metaDescription'>
<meta expr:content='data:blog.metaDescription' property='og:description'/>
</b:if>
<meta expr:content='data:blog.title' property='og:site_name'/>
<meta content='en_US' property='og:locale'/>

<!-- Customize meta tags here -->

<b:if cond='data:blog.url == data:blog.homepageUrl'> 
<meta content='YOUR-KEYWORD-HERE' name='keywords'/>
<meta content='AUTHOR-NAME-HERE' name='Author'/>
<link href='AUTHOR-URL-HERE' rel='author'/>
</b:if>

<meta content='GOOGLE-META-TAG' name='google-site-verification'/>
<meta content='BING-META-TAG' name='msvalidate.01'/>
<meta content='ALEXA-META-TAG' name='alexaVerifyID'/>


<meta content='width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1' name='viewport'/>

<link href='//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css' rel='stylesheet'/>

<script src='https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js' type='text/javascript'/>

<link href='https://fonts.googleapis.com/css?family=Oswald:300' rel='stylesheet' type='text/css'/>

<b:skin><![CDATA[/*-----------------------------------------------

Platform: Blogger
Name:     Best Mag Blogger Template
Designer: Bloggertheme9
URL:      http://www.bloggertheme9.com
License: Free Version 

----------------------------------------------- */

/* Variable definitions
   ====================
   <Variable name="keycolor" description="Main Color" type="color" default="#1a222a" value="#e6e9ee"/>
   <Variable name="body.background" description="Body Background" type="background"
       color="$(body.background.color)" default="#111111 url(//themes.googleusercontent.com/image?id=1OACCYOE0-eoTRTfsBuX1NMN9nz599ufI1Jh0CggPFA_sK80AGkIr8pLtYRpNUKPmwtEa) repeat-x fixed top center" value="#e6e9ee url(//themes.googleusercontent.com/image?id=1-QeziT_xhEvxfBl8wPx5qvDh7FrTqJvLJR2vQYW-ZkaGhxc2p1Zzl4P1_LVa2rRTUapD) no-repeat fixed top center /* Credit: Storman (http://www.istockphoto.com/googleimages.php?id=5972475&amp;platform=blogger) */"/>

   <Group description="Page Text" selector="body">
     <Variable name="body.font" description="Font" type="font"
         default="normal normal 15px Arial, Tahoma, Helvetica, FreeSans, sans-serif" value="normal normal 15px Arial, Tahoma, Helvetica, FreeSans, sans-serif"/>
     <Variable name="body.text.color" description="Text Color" type="color" default="#333333" value="#797979"/>
   </Group>

   <Group description="Backgrounds" selector=".body-fauxcolumns-outer">
     <Variable name="body.background.color" description="Outer Background" type="color" default="#296695" value="#437fcb"/>
     <Variable name="header.background.color" description="Header Background" type="color" default="transparent" value="rgba(118, 118, 118, 0)"/>
     <Variable name="post.background.color" description="Post Background" type="color" default="#ffffff" value="#ffffff"/>
   </Group>

   <Group description="Links" selector=".main-outer">
     <Variable name="link.color" description="Link Color" type="color" default="#336699" value="#517cc5"/>
     <Variable name="link.visited.color" description="Visited Color" type="color" default="#6699cc" value="#84a3d6"/>
     <Variable name="link.hover.color" description="Hover Color" type="color" default="#33aaff" value="#5ca6ff"/>
   </Group>

   <Group description="Blog Title" selector=".header h1">
     <Variable name="header.font" description="Title Font" type="font"
         default="normal normal 36px Arial, Tahoma, Helvetica, FreeSans, sans-serif" value="normal normal 36px Arial, Tahoma, Helvetica, FreeSans, sans-serif"/>
     <Variable name="header.text.color" description="Text Color" type="color" default="#ffffff"  value="#ffffff"/>
   </Group>

   <Group description="Tabs Text" selector=".tabs-inner .widget li a">
     <Variable name="tabs.font" description="Font" type="font"
         default="normal normal 15px Arial, Tahoma, Helvetica, FreeSans, sans-serif" value="normal normal 15px Arial, Tahoma, Helvetica, FreeSans, sans-serif"/>
     <Variable name="tabs.text.color" description="Text Color" type="color" default="#ffffff" value="#ffffff"/>
     <Variable name="tabs.selected.text.color" description="Selected Color" type="color" default="$(link.color)" value="#336699"/>
   </Group>

   <Group description="Tabs Background" selector=".tabs-outer .PageList">
     <Variable name="tabs.background.color" description="Background Color" type="color" default="transparent" value="rgba(118, 118, 118, 0)"/>
     <Variable name="tabs.selected.background.color" description="Selected Color" type="color" default="transparent" value="rgba(118, 118, 118, 0)"/>
     <Variable name="tabs.separator.color" description="Separator Color" type="color" default="transparent" value="rgba(118, 118, 118, 0)"/>
   </Group>

   <Group description="Post Title" selector="h3.post-title, .comments h4">
     <Variable name="post.title.font" description="Title Font" type="font"
         default="normal normal 18px Arial, Tahoma, Helvetica, FreeSans, sans-serif" value="normal normal 18px Arial, Tahoma, Helvetica, FreeSans, sans-serif"/>
   </Group>

   <Group description="Date Header" selector=".date-header">
     <Variable name="date.header.color" description="Text Color" type="color" default="$(body.text.color)" value="#333333"/>
   </Group>

   <Group description="Post" selector=".post">
     <Variable name="post.footer.text.color" description="Footer Text Color" type="color" default="#999999" value="#adadad"/>
     <Variable name="post.border.color" description="Border Color" type="color" default="#dddddd" value="#e7e7e7"/>
   </Group>

   <Group description="Gadgets" selector="h2">
     <Variable name="widget.title.font" description="Title Font" type="font"
        default="bold normal 13px Arial, Tahoma, Helvetica, FreeSans, sans-serif" value="bold normal 13px Arial, Tahoma, Helvetica, FreeSans, sans-serif"/>
     <Variable name="widget.title.text.color" description="Title Color" type="color" default="#888888" value="#a0a0a0"/>
   </Group>

   <Group description="Footer" selector=".footer-outer">
     <Variable name="footer.text.color" description="Text Color" type="color" default="#cccccc" value="#d8d8d8"/>
     <Variable name="footer.widget.title.text.color" description="Gadget Title Color" type="color" default="#aaaaaa" value="#bbbbbb"/>
   </Group>

   <Group description="Footer Links" selector=".footer-outer">
     <Variable name="footer.link.color" description="Link Color" type="color" default="#99ccee" value="#afcff1"/>
     <Variable name="footer.link.visited.color" description="Visited Color" type="color" default="#77aaee" value="#93aff1"/>
     <Variable name="footer.link.hover.color" description="Hover Color" type="color" default="#33aaff" value="#5ca6ff"/>
   </Group>

   <Variable name="content.margin" description="Content Margin Top" type="length" default="20px" min="0" max="100px" value="30px"/>
   <Variable name="content.padding" description="Content Padding" type="length" default="0" min="0" max="100px" value="15px"/>
   <Variable name="content.background" description="Content Background" type="background"
       default="transparent none repeat scroll top left" value="transparent url(//www.blogblog.com/1kt/transparent/white80.png) repeat scroll top left"/>
   <Variable name="content.border.radius" description="Content Border Radius" type="length" default="0" min="0" max="100px" value="15px"/>
   <Variable name="content.shadow.spread" description="Content Shadow Spread" type="length" default="0" min="0" max="100px" value="3px"/>

   <Variable name="header.padding" description="Header Padding" type="length" default="0" min="0" max="100px" value="30px"/>
   <Variable name="header.background.gradient" description="Header Gradient" type="url"
       default="none" value="url(//www.blogblog.com/1kt/transparent/header_gradient_shade.png)"/>
   <Variable name="header.border.radius" description="Header Border Radius" type="length" default="0" min="0" max="100px" value="10px"/>

   <Variable name="main.border.radius.top" description="Main Border Radius" type="length" default="20px" min="0" max="100px" value="0"/>
   <Variable name="footer.border.radius.top" description="Footer Border Radius Top" type="length" default="0" min="0" max="100px" value="10px"/>
   <Variable name="footer.border.radius.bottom" description="Footer Border Radius Bottom" type="length" default="20px" min="0" max="100px" value="10px"/>
   <Variable name="region.shadow.spread" description="Main and Footer Shadow Spread" type="length" default="3px" min="0" max="100px" value="0"/>
   <Variable name="region.shadow.offset" description="Main and Footer Shadow Offset" type="length" default="1px" min="-50px" max="50px" value="0"/>

   <Variable name="tabs.background.gradient" description="Tab Background Gradient" type="url" default="none" value="url(//www.blogblog.com/1kt/transparent/tabs_gradient_shade.png)"/>
   <Variable name="tab.selected.background.gradient" description="Selected Tab Background" type="url"
       default="url(//www.blogblog.com/1kt/transparent/white80.png)" value="url(//www.blogblog.com/1kt/transparent/tabs_gradient_shade.png)"/>
   <Variable name="tab.background" description="Tab Background" type="background"
       default="transparent url(//www.blogblog.com/1kt/transparent/black50.png) repeat scroll top left" value="transparent none no-repeat scroll top left"/>

   <Variable name="tab.border.radius" description="Tab Border Radius" type="length" default="10px" min="0" max="100px" value="0"/>
   <Variable name="tab.first.border.radius" description="First Tab Border Radius" type="length" default="10px" min="0" max="100px" value="10px"/>
   <Variable name="tabs.border.radius" description="Tabs Border Radius" type="length" default="0" min="0" max="100px" value="10px"/>

   <Variable name="tabs.spacing" description="Tab Spacing" type="length" default=".25em" min="0" max="10em" value="0"/>
   <Variable name="tabs.margin.bottom" description="Tab Margin Bottom" type="length" default="0" min="0" max="100px" value="0"/>
   <Variable name="tabs.margin.sides" description="Tab Margin Sides" type="length" default="20px" min="0" max="100px" value="0"/>

   <Variable name="main.background" description="Main Background" type="background"
       default="transparent url(//www.blogblog.com/1kt/transparent/white80.png) repeat scroll top left" value="transparent none repeat scroll top center"/>
   <Variable name="main.padding.sides" description="Main Padding Sides" type="length" default="20px" min="0" max="100px" value="5px"/>

   <Variable name="footer.background" description="Footer Background" type="background"
       default="transparent url(//www.blogblog.com/1kt/transparent/black50.png) repeat scroll top left" value="transparent url(//www.blogblog.com/1kt/transparent/black50.png) repeat scroll top left"/>

   <Variable name="post.margin.sides" description="Post Margin Sides" type="length" default="-20px" min="-50px" max="50px" value="-20px"/>
   <Variable name="post.border.radius" description="Post Border Radius" type="length" default="5px" min="0" max="100px" value="10px"/>
   <Variable name="widget.title.text.transform" description="Widget Title Text Transform" type="string" default="uppercase" value="uppercase"/>

   <Variable name="mobile.background.overlay" description="Mobile Background Overlay" type="string"
       default="transparent none repeat scroll top left" value="transparent none repeat scroll top left"/>

   <Variable name="startSide" description="Side where text starts in blog language" type="automatic" default="left"/>
   <Variable name="endSide" description="Side where text ends in blog language" type="automatic" default="right"/>
*/

/* Content
----------------------------------------------- */

html, body, div, span, applet, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, pre, a, abbr, acronym, address, big, cite, code,
del, dfn, em, font, img, ins, kbd, q, s, samp, small, strike, strong, sub, sup, tt, var, dl, dt, dd, ol, ul, li, fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td, figure { margin: 0; padding: 0;}
article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section {display:block;}
table {border-collapse: separate; border-spacing: 0;}
caption, th, td {text-align: left; font-weight: normal;}
blockquote:before, blockquote:after,
q:before, q:after {content: "";}
blockquote, q {quotes: "" "";}
sup{ vertical-align: super; font-size:smaller; }
code{ font-family: 'Courier New', Courier, monospace; font-size:12px; color:#272727; }
a img{border: none;}
ul ul, ol ol { padding: 0; }

ol, ul { padding: 0px;  margin: 0; }
ol li { list-style-type: none;  padding:0;  }
ul li { list-style-type: none;  padding: 0;  }

h1, h2, h3, h4, h5, h6 {color: #777; letter-spacing:0.1px; font-weight:500;}

a{ color: $(link.color); outline:none; text-decoration: none; }
a:hover { color: $(link.hover.color); text-decoration:none; }
body{ background: $(body.background); color: $(body.text.color); height: 100%; padding: 0; font-family:"Open Sans",Helvetica,Arial,sans-serif; font-size: 15px; line-height: 24px; }
.clear { clear:both; float:none; }


.ct-wrapper {background:#fff; padding:0px 0px; max-width:1200px; position:relative; margin: 20px auto;}
.outer-wrapper { position: relative; padding:0px 0 }
.header-wrapper {display: inline-block; float: left; padding: 0; width: 100%; -moz-box-sizing: -webkit-border-box; box-sizing: border-box; }
.main-wrapper {background: $(main.background); width:auto; margin-right:330px; }
#content { box-sizing: border-box; -moz-box-sizing: border-box; -webkit-box-sizing: border-box; position: relative;}
.main-inner-wrap {background:$(post.background.color); float:left; position: relative; width:100%;}
.sidebar-wrapper { width:300px; float: right;}
.container {margin: 0 auto; padding: 0 15px; position: relative; max-width: 1150px;}


body#layout #top-nav { margin-top: 40px; } 
body#layout #header, body#layout .header-right, body#layout .ganed { width: 46%; }
body#layout .main-wrapper { margin-right: 300px; }
body#layout .widget-content { margin: 0; }
body#layout .footer {width:30%;}
body#layout .outer-wrapper, body#layout .sidebar-wrapper, body#layout .ct-wrapper { margin: 0; padding: 0; }
.ct-wrapper, .crosscol, .post, .sidebar-wrapper, .buzed{overflow:hidden;}


#header{ float:left; width: 30%; }
#header-inner{ margin: 22px 0 22px 18px; padding: 0; }
#header h1, #header h2 { font-size: 36px; text-transform: uppercase; font-varient: small-caps; line-height: 46px; letter-spacing:0;}
#header h1 a, #header h2 a{ color:#444; }
#header h1 a:hover,#header h2 a:hover { color:$(link.color); }
#header p.description{font-family: georgia; color:#444; font-size: 14px; letter-spacing: 0.8px; font-style: italic; text-transform: capitalize; disply: inline-block; }
#header img{ border:0 none; background:none; height:auto;}


.lefter{margin-left:10px; margin-right:10px;}

.header-right { float: right; }
.header-right .widget-content { margin: 12px 0px 5px; }

.item-control a img{}

#peekar{position:relative; width:auto; float:right; margin:8px 10px 0 0; }
#peekar input{float:left; font-size:12px; margin: 0px 0 0; padding: 8px 0px; text-indent:7px; width:140px; color:#c5c5c5; border:1px solid #ccc; -o-transition:width .7s,color .4s;-webkit-transition:width .7s,color .4s;-moz-transition:width .7s,color .4s;transition:width .7s,color .4s;-webkit-border-radius:0;-moz-border-radius:0;border-radius:0}
#peekar input:focus{}
#peekar button{border: 0; background:$(body.background.color); line-height: 22px; cursor: pointer; color:#fff; font-size:16px; padding:5px 6px;}
#peekar button:hover{background:$(link.hover.color);}

.top-nav{background:#2C2C2C; overflow:hidden; box-shadow:0 6px 8px -1px rgba(0, 0, 0, 0.2); border-bottom:4px solid $(body.background.color); width: 100%;}

.Pagemenu {display: block; float:left; }
.Pagemenu li {display: inline-block; position: relative; z-index: 10; margin:0;}
.Pagemenu li a {font-size: 12px; text-transform: uppercase; font-weight: 600; margin-left:-5px; text-decoration: none; padding: 6px 12px; border-right:1px solid #424242; display: block; color: #ddd; transition: all 0.2s ease-in-out 0s;}
.Pagemenu li a:hover,.Pagemenu li:hover>a, .Pagemenu li a.home {background:$(body.background.color); color:#fff;}

.main-nav {position:relative; background:#2C2C2C; margin:0 0 25px; border-top:1px solid rgba(255, 255, 255, 0.5); border-bottom:4px solid $(body.background.color); display: block; width:100%; box-shadow:0 6px 8px -1px rgba(0, 0, 0, 0.2);}

.menu {display: block;}

.menu li {display: inline-block; z-index: 10;}

.menu li.home, .menu ul li ul li{margin:0;}

.menu ul li a, .menu ul li ul li a{border:0;}

.menu li{margin-left: -4px;}

.menu li a {font-size: 16px; padding: 15px 20px; font-weight:600; letter-spacing:0.6px; text-transform: uppercase; text-decoration: none; line-height:18px; display: block; color: #ddd; transition: all 0.2s ease-in-out 0s; font-family: 'Oswald', sans-serif;}

.menu li a:hover,.menu li:hover>a {color:#fff;}

.menu ul {visibility: hidden; transform: translate(0,20px); opacity: 0; margin: 0; padding: 8px 0; width: 100%; position: absolute; left: 0px;  background: #2D2D2D; border-top:4px solid $(body.background.color); z-index: 9;  transition: all 0.2s ease-out;}


.menu ul li {display: block; float: none; width:190px; margin: 0; padding: 0;}

.menu ul li a, .menu ul li ul li a{border-bottom:1px solid #222;}

.menu ul li a {font-size: 15px; padding:12px 18px; display: block; color: #ddd;}

.menu ul li a:hover,.menu ul li:hover>a {}

.menu li:hover>ul {visibility: visible; opacity: 1; transform: translate(0,0);}

.resp-desk,.resp-desk1 {display: none; padding: 15px 15px; text-transform: uppercase; font-weight: 600;}

.resp-desk {background:#2c2c2c; border-bottom:4px solid $(body.background.color);}
.resp-desk1 {padding: 12px 15px !important;}

.resp-desk a, .resp-desk1 a{color: #fff;}

.social-ico{float:right; display:inline; overflow:hidden;}
.social-ico a{color: #fff; float: left; font-size: 18px; opacity: 0.9; height: 36px; line-height: 36px; text-align: center; width: 30px;}
.social-ico a:hover{opacity:1}

.social-ico a:hover.tt1{background:#3B5998;}
.social-ico a:hover.tt2{background:#D64136;}
.social-ico a:hover.tt3{background:#19BFE5;}
.social-ico a:hover.tt4{background:#D88B43;}
a.homer {}

.post { margin: 0px 0 0; padding: 0px 0px; }
.post-title {font-size: 22px; color:#606060; font-weight: 500; margin: 8px 0 0px; line-height: normal; }
.post-title a {color:#444;}
.post-title a:hover {}
.post-body { padding: 0; margin:0; text-transform: auto; word-wrap:break-word;  }
.post-header {color: #999999; font-size: 12px;}
.title-secondary a, .title-secondary{color:#aaa; font-size:13px; color:#909090; margin:10px 0 0;}
.post-body img {}

.tagz a{color: #c62021; font-family: 'Oswald', sans-serif; font-weight:600; font-size:15px; margin-right: 10px; text-transform: uppercase;}

#breadcrumbs a:hover, .sidebar a:hover, .post-title a:hover, .title-secondary a:hover{color: $(link.color);}

.with-ul:after {border-color: #ddd transparent transparent; border-image: none; border-style: solid; border-width: 4px; content: ""; height: 0; margin-left: 5px; margin-top: -2px; position: absolute; top: 50%; width: 0;}

.sidebar{font-size: 14px;  margin: 0;  padding: 0;  display: block;  }
.sidebar .widget{  clear: both; margin-bottom: 25px;  }
.sidebar ul{ margin:0; padding:0; list-style:none; }
.sidebar li{border-bottom: 1px solid #eee; margin: 0; padding: 7px 0 7px 7px; text-transform: capitalize;}
.sidebar a{color:#444;}

.in-lefter{margin:0 10px;}

h2.btitle{font-size:22px; line-height: 26px; margin: 0 0 3px; transition: all 0.2s ease-in-out 0s;}
h2.btitle a{color:#606060;}
h2.btitle a:hover{color:#4775A3;}

.blog-cent p{height:;}

.blog-cent{margin: 0px 0 0; padding: 0px 0px;}

.threetabs{margin: 0 0 27px;}
.tabber{list-style:none; float:left; width:100%; margin:0 0 7px; padding:0;background:#2C2C2C; }
.tabber li{list-style:none; padding:0; margin:0; float:left;}
.tabber li a{display:block;padding:6px 10px; text-decoration:none; color:#fff;}
.threetabs h2 {display:none;}
.tabber li a.tabs-current, .tabber li a:hover{background:$(body.background.color); color:#fff !important;text-decoration:none;}

.boner li{border-bottom: 1px solid #e6e6e6; padding:10px 3px !important; margin:0; float:left; width:100%; text-transform:none;}
.boner li img{float:left; border-radius:10%; height: 68px; margin-right: 10px; width: 80px;}

.rees-cmt li span{display: block; line-height: 1.4;} 
.rees-cmt li p{color: #444; font-size: 12px;}

.bukshan img{height:100%; width: 100%; transition:all .3s ease-out;}
.bukshan{width:32%; position:relative; height:172px; margin:3px 20px 16px 0; float:left; overflow:hidden;}

.meta-date{color: #aaa; font-size: 13px; font-weight: 500;}

a.button {color: #fff; padding: 7px 14px; margin:8px 0 0; cursor: pointer; display: inline-block; font-size: 13px; font-weight: 700; overflow: hidden; text-transform: uppercase; transition: background-color 0.2s ease-in-out 0s;}

.greden{padding:1.1em 0; margin:20px 0 0; overflow:hidden; background:#fafafa;border:1px solid #e6e6e6; }
.reg-bent{width:50%;float:left;margin:0;text-align:left;color:#bbb;transition:all .3s ease-out;}
.fed-bent{width:50%;float:right;margin:0;text-align:right;color:#bbb;transition:all .3s ease-out}
.fed-bent:hover .two-left,.reg-bent:hover .two-left{color:#ddd!important;}
.reg-bent a,.fed-bent a{color:#999;}
.fed-bent a:hover,.reg-bent a:hover{color:#666!important;}
.reg-bent a,.fed-bent a,.one-left,.one-right{font-size:14px;font-family: &#39;Open Sans&#39;,Helvetica,Arial,sans-serif;font-weight:400;background:none;text-decoration:none}
.one-left{padding:0 0 0 15px;}
.one-right{padding:0 15px 0 0;}
.two-left{font-family: &#39;Open Sans&#39;,sans-serif;font-size:22px;font-weight:700;text-transform:uppercase;transition:all .3s ease-out}
.reg-bent2{margin:0}
.fed-bent2{margin:0}
#blog-pager-newer-link{float:left;padding:0 0 0 20px;}
#blog-pager-older-link{float:right;padding:0 15px 0 0;}
.blog-pager,#blog-pager{clear:both;text-align:center; padding:1em 0;}
.home-link{display:none;}

.btf-thumb{display:block; margin:8px 0 0;}
.btf-thumb li{float: right !important; width: 25% !important; margin:0 2.2% 0 0 !important;}
.btf-thumb li a{padding:0 !important; border:0 !important;}
.btf-thumb .teetli a{}
.btf-thumb img{width:100%; opacity:0.8; height:158px; transition:all .3s ease-out;}
.btf-thumb img:hover{opacity:1;}
.boped{float:left;}

.spinner{margin:30px auto auto;}
.spinner li{list-style:none; display:inline;}
.spinner li a{color: #fff; border-radius:6%; font-size: 14px; font-weight: 600; line-height:42px; padding: 10px 12px;}
.spinner li a{margin-right:4px;}

.nread{overflow:hidden; margin:8px 0;}

.feet-icons{float:right;}
.feet-icons a{float: left; font-size: 18px; line-height: 2em; text-align: center; width: 42px;}

a.facebook-ico{color:#3B5998; border-bottom:3px solid #3B5998;}
a.twitter-ico{color:#19BFE5; border-bottom:3px solid #19BFE5;}
a.plus-ico{color:#D64136; border-bottom:3px solid #D64136;}
a.email-ico{color:#23A215; border-bottom:3px solid #23A215;}
a.pinterest-ico{color:#c62021; border-bottom:3px solid #c62021;}

.sit{margin-left:3px;}
.spinner li a i{font-size:15px;}

a:hover.fb-ico, a:hover.twi-ico, a:hover.go-ico{opacity:8;}

.post-labels .fa-stack {font-size:25px;}
.post-labels .fa-circle {color:#F1F1F1;}
.post-labels .fa-tags {color:#DDDDDD; font-size:20px;}
.post-labels a{font-family:Arial; font-weight: 600; color:#777; letter-spacing: 0.6px;}
.post-labels a:hover{color: $(link.color);}

blockquote {border-color: #CCCCCC; border-style: dashed; border-width: 2px 0; color: #888; font-style: italic; margin: 10px 0 10px 0; padding:1% 16px 2%;}
blockquote:before{font-family:fontawesome; content:"\f10d"; color:#ddd; float: left; font-size: 40px; font-style: normal; font-weight: normal; margin: 1% 14px 0 0;}

.crosscol{display:none; text-align:center; margin:10px 0 10px;}
.buzed{text-align:center; }

.footer{width:31.5%; margin-bottom:20px; float:left;} 

ul.social-profile-icons { float: right; width: auto; margin: 4px 0 0; }
ul.social-profile-icons li {border: none !important; list-style-type: none !important; margin: 0 !important; padding: 0 !important; }
ul.social-profile-icons li a, ul.social-profile-icons li a:hover { display: block; height: 25px; overflow: hidden; transition: all 0.25s linear 0s; width: 25px; padding: 0; }


#breadcrumbs {border-bottom:1px solid #eee; margin-bottom:6px; padding-bottom:6px; font-size:13px; }
#breadcrumbs ul { margin: 0; padding: 0;}
#breadcrumbs ul li { display: inline-block; position:relative; margin: 0 0 0 18px;}
#breadcrumbs a{color:#768187; margin:0; }
#breadcrumbs ul li:first-child a{margin:0px;}
#breadcrumbs ul li::before {border-color: transparent transparent transparent #aaa; border-image: none; border-style: solid; border-width: 4px; content: ""; height: 0; left: -12px; position: absolute; top: 8px; width: 0;} 
#breadcrumbs ul li:first-child::before{border:none;}

.seat-bottom{margin-bottom:10px;}

.PopularPosts li,.PopularPosts li img,.PopularPosts li a,.PopularPosts li a img{margin:0;padding:0;list-style:none;background:none;outline:none}
.PopularPosts ul{margin:0;list-style:none;}
.PopularPosts ul li img{background:#fafafa;display:block;margin:0 10px 0 0;width:80px;height:68px; overflow:hidden;float:left; transition:all .3s ease-out}
.PopularPosts ul li{position:relative;background-color:#fff;margin:0; border-bottom: 1px solid #e6e6e6; padding:.7em 0!important;position:relative;}
.PopularPosts ul li:last-child{border-bottom:none}
.PopularPosts ul li .item-title a,.PopularPosts ul li a{font-weight: normal;}
.PopularPosts .item-thumbnail{margin:0;}
.PopularPosts .item-snippet{display:none}
.PopularPosts .item-title{padding:0 0px}
.PopularPosts h2{margin-bottom:0 !important;}

.tagcloud1 a, .tagcloud1 .list-label-widget-content ul li span {background: #555555; color: #fff !important; text-transform:none !important; display: block; float: left; font-size: 13px !important; line-height: 12px; margin: 0 3px 3px 0; padding: 12px 17px;}
.tagcloud1 a:hover, .tagcloud1 .list-label-widget-content ul li span {background: $(body.background.color) !important; color: #fff !important;}
.tagcloud1 li{padding:0 !important; margin:0 !important;} 

.showpageNum a, .showpage a, .showpagePoint {border:1px solid #dbdbdb; color: #888; cursor: pointer; font-size: 14px; font-weight: 600; padding: 8px 15px; text-decoration: none; display: inline-block; }
.showpageNum a:hover, .showpage a:hover, .showpagePoint {background:$(body.background.color); color: #fff; text-decoration: none; }
.showpageOf {display:none; margin-right:30px; margin-left:8px; }
.showpagePoint, .showpage a, .showpageNum a { margin: 0 3px 0 0; }

.instagram li{float:left; height:90px; list-style:none; width:31.3%; margin:0 !important; padding:0 3px 6px !important;}
.instagram img{height:100%; width:100%; transition:all .3s ease-out;}
.instagram img:hover, .PopularPosts ul li img:hover, .related-post img:hover, #recent-posts img:hover{opacity:0.7; }


#footer { width: 100%; color: #d0d0d0; }
.footer {}
.footer h2 {background-image: -webkit-repeating-linear-gradient(135deg, rgba(0,0,0,.3), rgba(0,0,0,.3) 1px, transparent 2px, transparent 2px, rgba(0,0,0,.3) 3px); background-image: -moz-repeating-linear-gradient(135deg, rgba(0,0,0,.3), rgba(0,0,0,.3) 1px, transparent 2px, transparent 2px, rgba(0,0,0,.3) 3px); background-image: -o-repeating-linear-gradient(135deg, rgba(0,0,0,.3), rgba(0,0,0,.3) 1px, transparent 2px, transparent 2px, rgba(0,0,0,.3) 3px); background-image: repeating-linear-gradient(135deg, rgba(0,0,0,.3), rgba(0,0,0,.3) 1px, transparent 2px, transparent 2px, rgba(0,0,0,.3) 3px); -webkit-background-size: 4px 4px; -moz-background-size: 4px 4px; background-size: 4px 4px; 

color: #eeeeee; font-size: 16px; margin: 0 0 10px; padding: 5px 0 6px; text-transform: uppercase;}
.footer h2 span{background:$(link.color); color: #fff; padding: 7px 12px;}

.footer .widget{ clear: both; margin: 0px 0px; }
.footer ul{ margin:0; padding:0; list-style:none; }
.footer li{ margin: 0 0 0 5px; padding: 0 0 5px; text-transform: capitalize; list-style:none;}
.mage1{background:#353738; border-bottom:2px solid #555555; border-top:4px solid $(body.background.color); padding:30px 0 25px;}

.footer-credits { padding: 0px 0; color: #999; }
.footer-credits .attribution { font-size:14px; }
#footer a, .footer-credits a { color:#d0d0d0;  }
#footer a:hover, .footer-credits a:hover { color: #fff; }
.mage2{background:#353738; padding:16px 18px;}
.deen{float:right;}

.form-go{ border: medium none; box-shadow: none; color: #fff; cursor: pointer; float: right; font-size: 13px; font-weight: 700; height: 40px; line-height: 18px; margin: -40px 0 0; padding: 10px 15px; position: relative; text-transform: uppercase; transition: all 0.2s ease-in-out 0s; z-index: 5;}
.form-bar{background-color: #505050; border: medium none; color: #808080; float: left;    font-size: 13px; font-weight: 600; height: 20px; line-height: 18px; margin-top: 15px; padding: 10px 14px; position: relative;  transition: all 0.2s ease-in-out 0s; width: 85%; z-index: 1;}

#related-article{width:100%;font-size:16px;display:inline-block;margin:auto;text-align:center;padding:8px 0px 0}
#related-article h4{font-size:16px;text-transform:uppercase;margin:0 0 25px;padding-bottom:15px;font-weight:700;letter-spacing:1px;text-align:center;position:relative}
#related-article h4:after{content:'';position:absolute;width:4px;height:4px;background:#aaa;border-radius:50%;bottom:0;left:47%;box-shadow:1em 0 0 0 #aaa,2em 0 0 0 #aaa}
#related-article ul {padding:0;margin:0;}
#related-article ul li{list-style:none;display:block;float:left;width:32.3%; margin:0 12px 18px 0; padding:0; text-align:center;position:relative;overflow:hidden;}
#related-article ul li:last-child{margin-right:0;}
a.related-title{text-align:center; padding:2px 0px; color:#606060; font-size:15px; line-height:20px; display:block; transition:all .3s;}
#related-article ul li:hover a.related-title{color:$(link.color);}
#related-article img{transition:all .3s ease-out; border: 1px solid #bbb; width: 99%; height:175px;}

#comments{background:#fff; clear:both; margin-top:20px; line-height:1em; padding:20px; border:1px solid #e6e6e6; }

.comments .comments-content {margin: 25px 0 10px;}

.comments .comments-content .comment-header{overflow:hidden; width:100%;}

.datetime{float:right;}
.datetime a{color: #666 !important; font-size: 11px; font-weight: 400; opacity: 0.9; padding: 1px 6px; text-align: center; text-decoration: initial; text-transform: none; transition: all 0.3s ease-out 0s;}
.user a{color: #666; font-size: 15px; font-weight: 700; text-decoration: none;}

.datetime a:hover, .user a:hover{color:$(link.color) !important;}

#comments h5 {border-left: none !important; border-top: none !important; background: #fff none repeat scroll 0 0; border:1px solid #e6e6e6;   color: #999; display: inline; font-size: 14px; font-family:inherit; font-weight: 700; line-height: 20px; margin-bottom: 20px; margin-left: -20px; margin-top: -20px; padding: 10px 20px 10px 20px;  position: absolute; text-transform: uppercase;}

.comments .continue a, .comments .comment .comment-actions a {background: #fdfdfd; border: 1px solid #ccc; border-radius: 2px; color: #999 !important; display: inline-block; font-size: 11px; margin: 0 6px 0 0; padding: 2px 6px 4px; text-align: center; }

.comments .continue a:hover, .comments .comment .comment-actions a:hover{border: 1px solid #bbb; color: #666 !important; text-decoration:none;}

.comment-actions .item-control a{position: absolute; right: 0; top: 10%;}

.deleted-comment{
    background: #eee none repeat scroll 0 0;
    border-radius: 3px;
    color: #999;
        font-size: 13px;
    padding: 10px;
}

.comments .continue{cursor:default;}

.comments .comments-content .comment-content {
    background: #fafafa none repeat scroll 0 0;
    border: 1px solid #ddd;
    border-radius: 6px;
    color: #666;
    font-size: 14px;
    line-height: 1.6em;
    margin: 16px 0 16px;
    padding: 30px 20px;
    position: relative;
    transition: all 0.3s ease-out 0s;
    word-wrap: break-word;
}

.comments .comments-content .comment-content:hover{ border: 1px solid #bbb;}

.comments .comment-block{margin:0 0 0;}


#comments .buffer {background:#FFFFFF;
  border-bottom-color:#E6E6E6;
  border-bottom-width:1px;
  border-left-color:#E6E6E6;
  border-left-width:1px;
  border-style:none none solid solid;
  color:#999999;
  display:inline;
  float:right;
  font-size:14px;
  font-weight:700;
  line-height:20px;
  margin-bottom:20px;
  margin-right:-20px;
  margin-top:-20px;
  padding:10px 20px;
  text-decoration:none;
  text-transform:uppercase;
}

#comments .buffer:hover{background:#fafafa;color:#666;}

#comment-editor{max-height:380px; max-height:300px;}

.avatar-image-container{padding:4px; border-radius:10%; background:#F9F9F9; width:46px !important; height:46px; max-width:46px !important; max-height:46px !important; overflow:hidden;}

.avatar-image-container img{width:46px; height:46px; border-radius:10%; max-width:46px !important; background:url(http://4.bp.blogspot.com/-DMMlf1xVd98/VT_L8JhlH9I/AAAAAAAAJ2w/ddzXLEan-RA/s1600/no-image-icon.png) no-repeat;}

.comments .comment-replybox-single {margin:0;}

.comments .comments-content .icon.blog-author:before {font-family:fontawesome; content:"\f00c"; background:#5890FF; display:block; color:#fff; border-radius:50%; margin-left:5px; font-size:10px; height: 18px; line-height: 19px; overflow:hidden; text-align: center; width: 18px;}

.comments .thread-toggle{display:none;}

h2.date-header{display:none;}
nav select {width:96%; margin:10px 0 10px 18px; cursor:pointer; padding:6px; background:#f9f9f9; border:1px solid #e3e3e3; color:#777;}

.auth-panel {margin:30px 0 15px; padding:20px 15px; border: 1px solid #eee; background:#FAFAFA; overflow:hidden; }
.auth-panel h4{display: block; font-size: 16px; font-weight: 400; margin-bottom:4px;}
.auth-panel p {font-size: 14px; line-height: 1.7;}
.auth-panel img {float: left; margin: 0 18px 0 0; width:90px; height:auto;}

.contact-form-widget {margin-left:0; margin-right:auto; width: 600px; max-width: 100%; padding: 0px; color: #000;}
.fm_name, .fm_email {float:left; padding:5px; width:48%}
.fm_message {padding:5px;}
.contact-form-name, .contact-form-email {width: 100%; max-width: 100%; margin-bottom: 10px; height:40px; padding:10px; font-size:16px;}
.contact-form-email-message {width:100%; max-width: 100%; height:100px; margin-bottom:10px; padding:10px; font-size:16px; }
.contact-form-button-submit {border-color: #C1C1C1; background: #E3E3E3; color: #585858; cursor:pointer; width: 20%; max-width: 20%; margin-bottom: 10px; height:30px; font-size:16px; }
.contact-form-button-submit:hover{background: #eee; color: #000000; border: 1px solid #ccc; }

 .sub-dd{margin:25px 0 0px; border: 1px solid #e6e6e6; border-bottom:0; padding: 6px 0; text-align: center; font-size:14px; font-style: italic; font-family: Georgia,"Nimbus Roman No9 L",serif;}

.tob-contid{margin-bottom:20px;}

.beanz{display:block; margin:0 0; box-shadow:0 0px 4px 0 rgba(0, 0, 0, 0.26);}
.beanz li{list-style:none; float: left; height:120px; width: 33.3%; margin:0 0 0 0;}
.beanz li a{}
.teetli{font-size: 15px; line-height:24px; padding: 18px 6px;}
.beanz img{width:50%; float:left; opacity:0.8; height:100%; margin-right:10px; transition:all .3s ease-out;}
.beanz img:hover{opacity:1;}

.sidebar h2, h4.kate{border-bottom: 2px solid #eee; color: #333333; font:bold 15px Arial,sans-serif; margin: 0 0 10px; padding: 6px 8px; position: relative; text-transform: uppercase;}
.sidebar h2 span, h4.kate span {border-bottom: 2px solid #c62021; bottom: -2px; color: #474747; padding: 6px;}

.pigment h4 a{background: $(body.background.color); position:relative; font-size: 17px; font-style: normal; line-height: 1; margin-bottom: 10px; padding: 6px 10px; text-shadow: none; color:#fff; }

.pigment h4 a:before {border-color: $(body.background.color) transparent transparent; border-style: solid; border-width: 32px 7px; content: ""; left: -7px; position: absolute; top: 0;}
.pigment h4 a:after {border-color: transparent transparent $(body.background.color); border-style: solid; border-width: 33px 7px; bottom: 0; content: "";   position: absolute; right: -7px;}

.pigment {background-image: -webkit-repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px); background-image: -moz-repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px); background-image: -o-repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px); background-image: repeating-linear-gradient(135deg, #eaeaea, #eaeaea 1px, transparent 2px, transparent 2px, #eaeaea, #eaeaea 3px); -webkit-background-size: 4px 4px; -moz-background-size: 4px 4px; background-size: 4px 4px; 

margin-bottom:15px; padding:0; position:relative; border-bottom: 4px solid $(body.background.color);}

.inner-content h2 a {color:#444;}
.inner-content h2 a:hover{color:$(link.color);}

.bozo li:first-child{border-bottom: 0; padding:0; margin:0 0; height: 337px; float: left; width: 43%; position:relative;}
.bozo li{float: right; margin: 0 0 16px 16px; height:160px; width: 27.1%; overflow: hidden; position:relative;}
.bozo li img {float: left; height: 160px; width:100%; margin:0; overflow: hidden;}

.bozo li:first-child img {overflow: hidden; height:337px; width: 100%;}

.bozo li .inner-content .denz{background:rgba(0, 0, 0, 0.4); bottom:0; padding:12px; position:absolute;}
.bozo li .inner-content .denz span, .bozo li .inner-content .denz a{color:#fff;}

.bozo .post-meta i, .bozo .post-meta .comt{display:none; }


.bozo .post-meta :before{border-color: $(body.background.color) transparent transparent; border-style: solid; border-width: 21px 7px; content: ""; left: -7px; position: absolute; top: 0;}
.bozo .post-meta :after{border-color: transparent transparent $(body.background.color); border-style: solid; border-width: 21px 7px; bottom: 0; content: "";   position: absolute; right: -7px;}
.bozo .post-meta {background: $(body.background.color); bottom: 100%; display: block; font-size: 12px; font-style: normal; letter-spacing: 0; line-height: 1;  margin-bottom: 10px; padding: 5px 10px; position: absolute; }

.doze li:first-child {border-bottom: 0; padding:0; float: left; width: 52%; position:relative;}
.doze li {float: right; border-bottom: 1px solid #e6e6e6; margin: 0 0 8px; padding: 0 10px 8px; width: 43%; overflow: hidden;}

.doze li img {display:none; float: left; height: 100px; margin: 0 10px 0 0; overflow: hidden; width: 150px;}
.doze li:first-child img {display:block; margin:8px 0 10px; height: 300px; overflow: hidden; width: 100%;}

.tob-contid1{margin:25px 0 40px;}

.doze li:first-child .inner-content .denz{}
.doze li:first-child .inner-content .denz span, .doze li:first-child .inner-content .denz a{}

.doze .inner-content h2{font-size:20px; line-height:1.4em; }

.inner-content h2{font-size:18px; line-height:1.4em; }

.bozo .inner-content p{display:none;}

span.post-meta {color: #aaa; font-size: 11px; padding: 10px 0;}

.uj_thumb img:hover, .bukshan img:hover, #related-article img:hover{opacity:0.8; }
.uj_thumb img {width:100%; height:auto; transition:all .3s ease-out; }
.beex, .ganed li:first-child .beex { float: left; position: relative; width: 100%;}

.ganed li .beex { float: left; position: relative; width: auto;}

.ganed{width:48%; }
.gone1{float:left;}
.gone2{float:right;}

.ganed li:first-child {border-bottom: 0; margin-bottom:25px; padding:0; float: left; position:relative;}
.ganed li {float: left; width:100%; overflow: hidden; border-bottom: 1px solid #e6e6e6; margin: 0 8px 12px 0;
padding: 0 0 12px;}

.ganed li img {float: left; height: 90px; margin: 0 14px 0 0; overflow: hidden; width: 115px;}
.ganed li:first-child img {height: 210px; margin:0 0 10px; overflow: hidden; width: 100%;}

.ganed .inner-content h2{font-size:18px; line-height:1.3;}
.ganed li:first-child .inner-content h2{font-size:20px; line-height:1.4;}

#ad-460 h2{display:none;}
#ad-460{overflow:hidden;}

.proof li {float: left; width:19.7%; overflow: hidden; margin: 0 1px 0; height:164px;}

.proof li img {height: 162px; width: 100%;}

.proof h2, .proof denz, .proof p, .proof .post-meta{display:none;}

.bukshan:hover .overlay-icon:before, .beex:hover .overlay-icon:before{opacity:1;-webkit-transform:scale(1);-moz-transform:scale(1);-ms-transform:scale(1);-o-transform:scale(1);transform:scale(1)}
.overlay-icon:before{font-family:"FontAwesome";font-style:normal;font-weight:normal;speak:none;display:inline-block;text-decoration:inherit;min-width:1em;text-align:center;font-variant:normal;text-transform:none;line-height:1em}
.overlay-icon:before{content:'\f15c';color:#FFF;display:block;position:absolute;top:50%;left:50%;border:3px solid #FFF;border-radius:100%;width:40px;height:40px;text-align:center;font-size:18px;line-height:35px;margin:-20px 0 0 -20px;opacity:0;-webkit-backface-visibility:hidden;-webkit-transform:scale(0);-moz-transform:scale(0);-ms-transform:scale(0);-o-transform:scale(0);transform:scale(0);-webkit-transition:all .3s ease-in-out;-moz-transition:all .3s ease-in-out;-ms-transition:all .3s ease-in-out;-o-transition:all .3s ease-in-out;transition:all .3s ease-in-out}

.tibber {position: fixed; right: 32px; bottom: 0; z-index: 999;}
.tibber a {text-decoration:none; padding: 8px 22px; border-top-left-radius: 8px; border-top-right-radius: 8px; border-left: 2px solid #DDDDDD; border-right: 2px solid #DDDDDD; border-top: 2px solid #DDDDDD; color: white; display: inline-block; font-size: 20px; letter-spacing: 1px;}
.tibber a{background:$(body.background.color); $(header.background.gradient)}

@media screen and (-webkit-min-device-pixel-ratio:0) { 

#peekar button {padding:5px 9px;}
.post-meat :after {right: -7px;}

}

@media (max-width: 1050px) {
.ct-wrapper{margin:0 auto;}
#header {width: 25%;}
.main-wrapper { margin-right:330px; width:auto; }
.sidebar-wrapper{ float: right; width:300px;}
blockquote:before{margin: 2% 14px 0 0;}
.bukshan{}
.btf-thumb li{width:24% !important;}
.bozo li:first-child{width:40%}
.bozo li{width:28%}
.proof li{width:19.6%;}
.footer{width:31.2%;}
.post-title{font-size:22px}

}

@media (max-width: 1190px) {
#related-article ul li{width:32.1%;}
.bozo li:first-child{width:42.6%}
.bozo li{width:27%}
}

@media (max-width: 1000px) {

#header {width: 32%;}
.menu li a{padding:15px;}
.main-wrapper { margin-right:315px; width:auto; }
.sidebar-wrapper{ float: right; width:300px;}
.doze li img{width:100px; height:100px;}
.bozo li:first-child{width:42%}
#related-article ul li{width:32%;}
.footer{width:30%;} 
.footer-credits .attribution{text-align:center;}
.deen{float:none;}

}

@media (max-width: 950px) {


.btf-thumb li{width:23.4% !important;}


}


@media (max-width: 800px) {

.menu, .Pagemenu {display: none;}
.resp-desk,.resp-desk1 {display: block; margin-top:0px;}
.mainWrap {width: 768px;}
nav {margin: 0; background: none;}
.main-nav{background:none; border-bottom:none;}
 .Pagemenu li a, .Pagemenu li a:hover, .Pagemenu li a.home{background:#2C2C2C; color:#fff; border:0; margin:0;}
.menu li, .Pagemenu li{display: block; margin: 0;}
.menu ul li a{margin-left:25px; border:0; color:#909090;}
.menu li a{background: #fbfbfb; border:0; color: #909090;}
.menu li a:hover,.menu li:hover>a,.menu ul li a:hover,.menu ul li:hover>a {background: #F6F6F6; color: #909090;}
.menu ul {visibility: hidden; border-bottom:0; opacity: 0; top: 0; left: 0; padding:0; width: 100%; background:none; transform: initial;}
.menu li:hover>ul {visibility: visible; opacity: 1; position: relative; transform: initial;}
.menu ul ul {left: 0; transform: initial;}
.menu li>ul ul:hover {transform: initial;}
.with-ul::after,.menu ul::after{top:auto; margin:7px 0 0 6px; border-color: #909090 transparent transparent;}
.btf-thumb{display:none;}
.boped{float:none;}
#peekar{margin-top:-47px;}
.social-ico{margin-top:-42px;}

}


@media (max-width: 800px) {

#header {width: 45%;}
.header-right {display:block; }
.ct-wrapper{ padding:0 0px;}
.main-wrapper { margin-right:0px; width:auto; }
.sidebar-wrapper{float:left;}
.bukshan{width: 28%;}
.footer{width:30.6%;}
.bozo li:nth-child(3), .bozo li:nth-child(4){display:none;}
.bozo li:first-child { width: 56%;}
.bozo li {width: 41%;}

}

@media (max-width: 700px) {

#header{ float: none; text-align: center; margin-left:0; width: 100%;}
.header-right{display:none;}
.sidebar-wrapper{}
.main-wrapper {width: 100%;}
.bukshan{width: 38%;}
.footer{width:46.4%;}
#bont{width:20%;}
.fence{display:none;}
.doze li{padding:0 0 8px;}
.proof li {width: 24.6%;}
#related-article ul li{width:31.9%;}

}

@media (max-width: 600px) {

}

@media (max-width: 500px) {

.bukshan {width: 28%; height:100px; margin-right:12px;}
.doze li:first-child, .doze li{width:100%;}
.sit{display:none;}
.footer {width: 100%;}
.in-lefter{margin:0 0px;}
#related-article ul li{width:48%;}
.bozo li:first-child{width:100%;}
.ganed{width:100%;}
.bozo li {float: left; margin: 2px 1px 0; width: 49.5%;}
.proof li {width: 32.6%;}

}


@media (max-width: 400px) {

.container{padding:0 8px;}
.bukshan {width:32%}
#related-article ul li{width:90%; margin:0 4% 12px;}
#peekar input{width:115px;}
.bozo li {margin: 2px 0px 0; width: 100%;}
.proof li {width: 48.4%;} 

}

@media (max-width: 300px) {
#header img{width:100%;}
.sidebar-wrapper{}
.lefter{margin-left:0; margin-right:0;}
.proof li {width: 98%;} 
#peekar input{width:95px;}

}

@media (max-width: 260px) {
.container{padding:0 3px;}
#peekar{display:none;}
#related-article ul li{width:99%; margin:0 1% 12px;}
.bukshan{width:100%; margin-bottom:5px;}
.doze li img{width:100%;}


}

]]></b:skin>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
<style type='text/css'>

.post-body h1 { font-size: 44px; line-height: 34px; margin: 10px 0; }
.post-body h2 { font-size: 24px; line-height: 40px; margin: 10px 0; }
.post-body h3 { font-size: 20px; line-height: 34px; margin: 10px 0; }
.post-body h4 { font-size: 26px; line-height: 36px; margin: 10px 0; }
.post-body h5 { font-size: 24px; line-height: 34px; margin: 10px 0; }
.post-body h6 { font-size: 18px; line-height: 24px; margin: 10px 0; }

.blog-pager, #blog-pager{border:1px solid #e6e6e6; padding:1em 0; margin:0;}

@media screen and (min-width: 240px){

}


@media screen and (min-width: 320px){

}


@media screen and (min-width: 1024px) {


}

</style>
</b:if>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<style type='text/css'>
.blog-cent p{overflow:hidden;}
.post{overflow:hidden; width:100%; float: left; margin:0 0px 10px;}
#blog-pager {clear: both; float: left; border:0;}

@media screen and (min-width: 240px){

}


@media screen and (min-width: 320px){

}


@media screen and (min-width: 480px){

}


@media screen and (min-width: 603px){

}


@media screen and (min-width: 768px){

}


@media screen and (min-width: 960px) {

}



@media screen and (min-width: 1024px) {

}

@media (min-width:1280px) {
   
}

        
</style>
</b:if>
</b:if>

<b:if cond='data:blog.pageType == &quot;static_page&quot;'>
<style type='text/css'>

.post-title{margin-bottom:10px;}
#comments{padding-top:0;}
@media screen and (min-width: 240px){
.in-lefter{margin:0 2px;}
}

@media screen and (min-width: 320px){
.in-lefter{margin:0 10px;}
}
</style>
</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
<style type='text/css'>
.post-body ol,.post-body ul { padding: 10px 0 20px;  margin: 0 0 0 25px;  text-align: left;  }
.post-body ol li { list-style-type: decimal;  padding:0 0 5px;  }
.post-body ul li { list-style-type: square;  padding: 0 0 5px;  }
.post-body img{max-width:89%; height:auto;}
.title-secondary{float:left;}
</style>
</b:if>

<style type='text/css'>
.ct-wrapper{background:#fff;}
</style>

<script type='text/javascript'>
//<![CDATA[

var summary = 32;

var ry = "<h4>Similar Posts</h4>";
rn = "<h5>No related post available</h5>";


eval(function(w,i,s,e){var lIll=0;var ll1I=0;var Il1l=0;var ll1l=[];var l1lI=[];while(true){if(lIll<5)l1lI.push(w.charAt(lIll));else if(lIll<w.length)ll1l.push(w.charAt(lIll));lIll++;if(ll1I<5)l1lI.push(i.charAt(ll1I));else if(ll1I<i.length)ll1l.push(i.charAt(ll1I));ll1I++;if(Il1l<5)l1lI.push(s.charAt(Il1l));else if(Il1l<s.length)ll1l.push(s.charAt(Il1l));Il1l++;if(w.length+i.length+s.length+e.length==ll1l.length+l1lI.length+e.length)break;}var lI1l=ll1l.join('');var I1lI=l1lI.join('');ll1I=0;var l1ll=[];for(lIll=0;lIll<ll1l.length;lIll+=2){var ll11=-1;if(I1lI.charCodeAt(ll1I)%2)ll11=1;l1ll.push(String.fromCharCode(parseInt(lI1l.substr(lIll,2),36)-ll11));ll1I++;if(ll1I>=l1lI.length)ll1I=0;}return l1ll.join('');}('197fe1u212a29333918263q01311o27212q1b3x3e1d3q01112m3q01322m3x2u37262v322p11323a251s27352116212x25211c2u2911113a251s2735211632381y11121611153x2b2q1931261u3u2v312p113w263e153x2b2q19312611121o252e1i3e2b38182x3u12111o380y12113b233x313b38182x3u12111o3e182v3b233x2b233x3b233x2b233x11113u2911323u291u3u291r2q1i27323q3e1z23141b3x111132243516312q1b3x111k1v35211d323p3e113w2o211q1g27311q1o25111s273t192126163e1e2e3b381c3y2b341x3w2u3q3u39323b3r3732391916311611121o253e1q11113w263e1d373a3x111z23141i1i1l181f1k1g1l1f1j3e181e1t3e1c1g1d3f143g1m3g1k1e1w1g141f172e1t2e102e1u2e112e1t2f1u2e1s1e152e1v2g1y2e1u2e152e1t3g1w2e1u1e1k2e1u1e1z2e1w1e1x2e1s2f1w2e1t2e1v2e1s2f172e1t2e1u2e1u2e1e2e1u2g1t2e1u2f1t2e1s3g1x2e1s3g142e1w2g1y2e1t2g1z2e1s1e1u2e1s2g1v2e1t2e1v2e1v2e1v2e1s3f1w2e1u3e1s2e1s3g1h2e1s2f192e1u3f102e1s2f182e1s3f1j2e1s3f172e1s3g102e1u3f172e1u3f1u2e1s3f1b2e1s3f1t2e1s2f172e1w3f1v2e1s3f192e1t3e1e2e1s3f182e1u3f1y2e1u3f192e1u3f182e1s1f1b2e1u3f1e2e1s3f172e1u3g1r2e1s2f192e1s3g1e2e1s3f192e1s3g1w2e1u1f172e1s3f192e1s3f192e1s3f1b2e1s2e1u2e1u1e1f1e1b1f1e3g1c1e1k1f1m3g1r3d1f3f1f3f1k2f123f1l2f1f2f1m1e1d3e1f3g1c3f1m1g1f1g1s3g1f3e1f1f1f3e1d1f181g1s1f1b1f1c3f1f3g1i3f1g2e1f1e1d1e1f1g1r3e1f1e183f131g1h2e1d1f1k3g1d3e1g1g1j3g1l3g1j3g143f1e3f1m1g1r1g1i3g1b2e1f1g1h3d1f2f1c1e1s2g1f1f1f3g143e1f3f1f3e1m3f1l3e1f3g181g1d3e121e1b1f1b1f1f1f1d1f1j1g1f2e1q2e1f1e1f1e1d3f1f1e1a1d1f1g1h1e152e1u2g122e1u3g1b2e1u1g1b2e1w1g1h2e1u2f1h2e1u2g1q2e1u2e1h2e1u3g1v2e1v2g1e2e1u2g1u2e1t1f1w2e1u1e1u2e1t3g1h2e1u1e1h2e1u1e1i2e1u1e1d2e1u2g1j2e1s3e1z2e1u1f1z2e1r2e1k2e1u1e1c2e1u2e102e1t1g1m2e1u1e1l2e1t3g1r2e1t3g1j2e1t2g1y2e1u2g102e1w2f1s2e1s2e1f2e1s1f1j2e1s1f1r2e1t2e1r2e1u2g1h2e1t1e1w2e1t1e1s2e1u2e1h2e1u1g1h2e1w3g1l2e1s1f102e1r3f1a2e1u2e1y2e1s2f1h2e1u2g102e1t2e1v2e1u2f172e1r3g1z2e1t1g1w2e1v3e192e1u1e1i2e1r3e1j2e1u2g1l2e1t2g1h2e1w1g1v2e1t1g1h2e1t2f1y2e1s1g152e1s3e1h2e1v2g1h2e1u2g1j2e1u1f172e1t1g1l2e1t2g1y2e1w2g1t2e1u2e1x2e1t2g1e2e1t3g1t2e1t2g1h2e1t2g152e1s1e1y2e1t2g182e1u2g1j2e1r2g1t2e1u3g1q2e1s2g1r2e1t1e1v2e1u1e102e1u2e1s2e1v2e1l2e1r2g1y2e1u1g1m2e1u2g1t2e1u2g1t2e1v1e1h2e1t3e1r2e1u2e122e1t2g1h2e1t2e1d2e1v3f1v2e1t2g1j2e1r3e1l2e1u1g102e1t2f1z2e1t2e1e2e1t3g1j2e1t1f1j2e1u1e1h2e1r2e1w2e1v2e1t2e1u1e1x2e1u3g1h2e1u2e1h2e1u3g1r2e1v2f1l2e1u1e1s2e1u2e102e1s1e1h2e1u2g1z2e1v2f102e1t3e1k2e1t2e1h2e1u2g1v2e1t3g1s2e1w2e1r2e1t2e1x2e1t3e122e1t2e152e1u3g142e1v1e1h2e1u3e1t2e1t3e102e1u1f102e1u2e142e1v1g1l2e1s2g1r2e1t2f122e1t1e1z2e1s3e162e1v2f1h2e1t3e1v2e1t2e1h2e1t1e1x2e1s3e1d2e1w2g1l2e1u1e1x2e1s3g1r2e1t2g1r2e1u3f1q2e1w3f1i2e1t1f1h2e1t3e1j2e1u1g1l2e1t1e1r2e1v3e1r2e1t2e162e1u2g1a2e1s1g1m2e1u3e1z2e1u3e1j2e1s2e1y2e1s3e1u2e1u2e1w2e1u2e1s2e1v3e1x2e1t2g1f2e1u1g1i2e1u1e1u2e1t3f1h2e1v1g1s2e1r2e1x2e1u2e1u2e1t1e1r2e1t2e1s2e1v2e1v2e1u3e1t2e1t1g162e1r2g1i2e1t3f1y2e1u2g1e2e1u2e1u2e1u3e112e1t1g1l2e1t1e1j2e1v2g1i2e1u1e1z2e1s2f162e1t2e1q2e1t2e152e1v2g102e1s2g1s2e1t2e1m2e1u2g1r2e1t2e1x2e1u1e1s2e1u1e1j2e1t3e1x2e1t2f1h2e1u1e1u2e1v2f1y2e1u2f1t2e1t1g1z2e1s2f1y2e1t3g1j2e1u1e1l2e1t1e1i2e1r2f1u2e1u1e1v2e1s3e1s2e1w3g102e1u2f1s2e1s1g1h2e1u2g1v2e1u2g1h2e1v2g142e1s2g1f2e1t2g1v2e1s3f1w2e1t3f1x2e1u3e1y2e1u2e1f2e1t2e102e1s2g1t2e1u2g1q2e1u2e1w2e1u1e1i2e1s3g1u2e1s2e1s2e1s1g1w2e1v1g102e1t1g1i2e1t2e112e1t2e1v2e1t1g1z2e1w1g1t2e1r3e1f2e1u2e192e1s1f1s2e1s3g142e1v1f1f2e1t1e162e1t2g1d2e1u1e182e1t1f1v2e1u3f1u2e1s2f1c2e1s2e1j2e1s1g1t2e1t2f1w2e1u3e192e1t2e1w2e1s2e1f2e1u2g1h2e1t1e1d2e1u1g1s2e1t2g1d2e1t1e1w2e1t3g1m2e1u2g1e2e1v2g1t2e1r2f1d2e1t2e1f2e1s3g1t2e1t1f1f2e1t3f182e1t2e1r2e1u2e1v2e1s3f1e2e1s3e102e1w2g1t2e1u2g1y2e1r2f102e1t2f1e2e1u2g1a2e1v3g1q2e1t3g1v2e1s1e1f2e1t3f1d2e1r3g1f2e1v1e1z2e1s1g1z2e1s3f112e1t1g1y2e1s3e1h2e1w3f1f2e1u3e1r2e1s2g112e1r3g1h2e1u1g1f2e1w1e152e1s1g1g2e1t2g1u2e1u1g1z2e1u3g1h2e1w2e1u2e1s2g1d2e1t1g112e1t1g1j2e1t2g1j2e1u2e1r2e1t3g1x2e1u1g1v2e1u2e1z2e1s1g1f2e1t2g1w2e1t3e1m2e1r1e1e2e1r2e1h2e1t2f1s2e1t2e1l2e1t2e1y2e1u2g1t2e1t2g1f2e1t1g1d2e1v2g1d2e1s2f1z2e1t3f1w2e1t1e1d2e1t2g1t2e1v1g1w2e1t1e1f2e1t2e112e1u1g1t2e1u1e1r2e1u1e1a2e1t2g1f2e1r2e182e1t3f1u2e1u2e1t2e1u2e1l2e1t3e152e1u1g1w2e1s2g172e1t1g1w2e1u2g1t2e1s2e1l2e1t2g1u2e1u2e1t2e1t1g1t2e1w2e1l2e1t2f1w2e1s2f1v2e1u2f1z2e1s3e1i2e1w2g102e1u2e1b2e1s3f122e1s1g1t2e1u3f1g2e1v2e1r2e1t2e1t2e1s2g1u2e1t1g1h2e1t2g1d2e1v1e1c2e1s1f1r2e1t1e112e1u3g1l2e1t1g1d2e1t2g1s2e1u3g1i2e1r1g1c2e1t2e1e2e1s1g1d2e1t2f1f2e1u2g1j2e1u2g1z2e1u2g1d2e1s1g1f2e1w1g1z2e1s1g1r2e1u2g1m2e1u2f1h2e1u2e142e1w3f1s2e1s3g1x2e1r3e192e1t2g1f2e1t1g1z2e1u1g142e1s3f1x2e1t1g102e1s1e1f2e1t1f1m2e1w2g1i2e1t2f1g2e1r2f1e2e1t1g1h2e1t2g1z2e1u2g1t2e1u3e1j2e1t2e122e1u2g1r2e1t2g1f2e1v1g1d2e1t2g1e2e1s3f122e1t2g1e2e1u2g1e2e1v1e1x2e1s2e1t2e1u2e1v2e1u2e1m2e1r1e1s2e1t2g1w2e1u2f1m2e1r2g1q2e1t1e102e1u3g1s2e1w2g1v2e1s1e1k2e1u1e1s2e1t2e102e1t2g162e1h2e1u2e1r2e1u2f1y2e1v2e1f2e1t1e1k2e1t3f1h2e1u1e1w2e1t2f1v2e1w1e1u2e1u2g1i2e1t2e1v2e1u2g1r2e1u2f1q2e1w2g1i2e1t1g1w2e1t2f1h2e1t2e1q2e1s2e1s2e1w2e1h2e1u2g1e2e1t2g1v2e1r1e1i2e1u3e1m2e1u1g1l2e1u2e1j2e1t2g102e1u1g1w2e1u1g162e1u1e1s2e1u1e1s2e1t2e1l2e1u3e1a2e1t3e1w2e1v2g1y2e1u3g1w2e1t2g1s2e1t2g1i2e1t3e1x2e1w2e1e2e1u2e1g2e1u1g1h2e1u2g152e1u1e1t2e1v3f1r2e1t1e1j2e1u2g162e1t2e1f2e1t1g142e1v2g1j2e1s1g1k2e1s2e1h2e1t3g1z2e1u2e102e1t3g1x2e1r2f1q2e1u1e1v2e1s2g1f2e1u3e1x2e1w2f1m2e1u3g1f2e1u1e122e1u2f1f2e1u2g1q2e1u1g1s2e1s2f1w2e1u2e1s2e1t1g1d2e1t3g1m2e1w1f1y2e1t2g1y2e1u3g1t2e1u1g1w2e1s2e1f2e1u2g1t2e1t1f1g2e1t2g1t2e1t1g1j2e1t1f1y2e1w2e162e1t1e1s2e1s2g1w2e1t3e1f2e1u2e1u2e1u2e1x2e1s1g1y2e1r1g1s2e1u3e1m2e1s2g1j2e1u1g1r2e1s2g1w2e1r1g1i2e1s3g1f2e1r2e1r2e1w2e1u2e1u1g1e2e1t2g1t2e1t3g1r2e1u2e1u2e1u3g1s2e1s2g1t2e1t2e1j2e1t2e1w2e1s2e1y2e1u1e1r2e1u1g1f2e1s1e1t2e1t2e1j2e1t1e1w2e1v2e1s2e1t1g162e1u2g102e1r1g102e1t2e1m2e1v2g1e2e1r1e1s2e1u2g112e1t2g1j2e1r2f1x2e1v1e1y2e1u2g1k2e1u2e112e1s1g1g2e1r2e1w2e1v1e1z2e1t3g1j2e1t2f1h2e1u2g1a2e1u3g1u2e1t1g152e1s1g1f2e1u3g1l2e1t1g102e1s2g1z2e1w2g1j2e1t3e162e1t2e122e1s1e1r2e1t1g1y2e1u1e1l2e1t1e1e2e1u2g1r2e1u1g1t2e1t2e152e1u1f1v2e1t2g1z2e1t1g1h2e1t2e1q2e1t1f142e1t1e1j2e1u1g1t2e1s2e1l2e1u1e1z2e1s2e102e1v1e1t2e1t3e1f2e1s1g1v2e1u2f162e1t2e102e1u1g1v2e1u1g1r2e1t2g1j2e1s1e1z2e1u2f142e1t1g1j2e1s1g1w2e1t2e1d2e1u2g1w2e1r2g1f2e1w2g1h2e1t3e1h2e1r2f1z2e1u2e1h2e1u1g1t2e1w1g1t2e1s2f142e1r2e122e1t1f1i2e1u2g1w2e1w2g1y2e1s1g1y2e1u2e1v2e1s1g1s2e1u2e1z2e1u2g1t2e1t2e1t2e1t1e112e1t1g1d2e1t1g1v2e1w3e1k2e1t3g1v2e1u2f1c2e1t3g1s2e1u1e1i2e1u2g1v2e1s1e1q2e1u1g1l2e1t3g1t2e1t2f1f2e1w1e1s2e1t2f1w2e1u2f1m2e1u2g1s2e1r3e1r2e1v2e1r2e1s2g1j2e1t1f1t2e1t1g1t2e1u3f1u2e1u1f142e1s1g162e1s2e102e1t2g1f2e1r3e1y2e1v2e1j2e1u1g152e1t1e1b2e1u2f1t2e1u1e1s2e1u2e1l2e1t1g1d2e1t2e1h2e1t2g1y2e1t3g1t2e1u2f1x2e1s2f1c2e1t1g1t2e1t1f1t2e1u1e1g2e1w2e1w2e1s2g1d2e1t1g1e2e1s3g1y2e1t2f1w2e1v2g1d2e1t3f1d2e1t1g1x2e1t3f1j2e1u3g1e2e1v1f1s2e1s3f1x2e1u2g1l2e1r3f1s2e1r2f1t2e1v2f1r2e1u2e1w2e1t1g1r2e1s1f1f2e1r2g182e1w2e1r2e1s3f1y2e1u2g1y2e1u1g1z2e1u1f1d2e1v3f1g2e1r1g1r2e1r1g1i2e1s2f1m2e1s1g1v2e1v2f1e2e1s2e142e1t3e1t2e1u3g1d2e1r1g1r2e1u2e1x2e1t3f1e2e1t2g1t2e1u3f1r2e1s1f1f2e1v1g1h2e1r2g1r2e1u2f1c2e1t3e1d2e1t3g1c2e1u2f1r2e1u1e162e1t2e1f2e1u3e1d2e1r1g1r2e1w1f1r2e1r1e1f2e1t3g1i2e1s1g1r2e1u3e1w2e1u1e1g2e1t1e1s2e1r1e1r2e1r3g1f2e1t2g1g2e1t2g1m2e1r2g1x2e1t2f1i2e1u2e1x2e1s2e1f2e1t1e1m2e1s1g142e1u1g1j2e1u2g1r2e1r3g1j2e1w1g1d2e1s1g1d2e1s1g1j2e1u2e1i2e1r1f1y2e1v2g1c2e1u1g1c2e1t1e172e1t2g152e1s2f1s2e1v2g1j2e1u2g1j2e1u3g1v2e1s3g1r2e1t1e1x2e1w2e1z2e1u3e1q2e1s2e1x2e1u2g1x2e1s1f152e1w3e1x2e1u2f1r2e1s3f162e1t2f192e1s1e1d2e1w2f1r2e1s2g1i2e1u2g1d2e1t1g1f2e1u3e1w2e1u1f1y2e1s2e1e2e1u2g1f2e1s2g1z2e1t2e1x2e1w2e1j2e1s1e1x2e1u3f1d2e1s3f1d2e1s1e162e1w1e1d2e1u2g1k2e1t1g1s2e1t3e172e1t3g1r2e1u3f1s2e1r2g1w2e1t1e1f2e1t3g1r2e1t2e1a2e1v1g152e1r3g1r2e1r3e1f2e1u2g1c2e1t1g1g2e1w1f1u2e1t1g172e1s1e1e2e1s2e1m2e1t3e1r2e1v2g1c2e1t3e1j2e1t1f1e2e1u2e1u2e1s3e142e1u2e1e2e1r3e1d2e1s3g162e1t2g1r2e1t2g1y2e1t2g1r2e1u2f1a2e1t3e1f2e1t3g1c2e1s2f1m2e1u1g1m2e1s2e1t2e1s1g1f2e1t2g1f2e1t3g102e1w1g142e1t1e1g2e1u2e1f2e1s1g1h2e1u2e1i2e1t1f1y2e1t2g1c2e1u1g1e2e1t1e1v2e1t3g1f2e1v2e1q2e1t2g1e2e1r2g1d2e1u2f1s2e1u1e102e1w2g1y2e1t1g1j2e1s1e1d2e1u2g1l2e1t1g1m2e1w2e1t2e1t1e1y2e1u3e1s2e1t2e1j2e1t2g1m2e1w2g1r2e1s1e1x3f1j2e1w3f1s2e1u2g1y2e1u1g1j2e1t3g162e1t1e1f2e1v2g1l2e1t1e1h2e1u1e1w2e1s3g1r2e1u2e1t2e1w1e1v2e1u1e1v2e1s3g1v2e1t3g1h2e1t3g1t2e1w2g1m2e1t2e102e1u2e112e1u2g1f2e1t3g1e2e1w2e1s2e1s1g102e1t1e122e1t2g1c2e1u2e1j2e1u2e1l2e1u2g1u2e1u2f122e1u1g1t2e1s3e1e2e1v1g182e1t2g1y2e1t1e122e1s2g1e2e1u2g1w2e1v2g1q2e1t1e1s2e1s2e1u2e1t2e1s2e1u3e1u2e1u3e1h2e1u2g182e1t3g1v2e1u1e1k2e1s3g1j2e1w2g1w2e1s2f142e1s2g172e1s2g142e1t2g1v2e1v1e1h2e1t1g142e1t3g1h2e1u1e172e1t2f102e1u1e1y2e1u2e142e1t1e122e1t3f1h2e1t2f1a2e1w2f152e1s1g1a2e1u2e1q2e1r1e102e1u2g1l2e1v1g102e1r2e1t2e1t1g1v2e1u2f162e1u1e1x2e1u2g1v2e1t1f1y2e1u2g1y2e1t2g1t2e1u3g1h2e1w1g1k2e1s2e1j2e1u1g182e1t2g1t2e1u1g1t2e1v1e102e1u3g1j2e1r2f1e2e1s3g1t2e1u3e1z2e1w1e1y2e1t3g1q2e1t2e1l2e1u1g1u2e1t3e1w2e1v2g1l2e1s3e1x2e1u2e1d2e1t2e1h2e1t2g102e1u1e102e1t2f1i2e1t2g1v2e1r2g1s2e1u2g1r2e1u2g1y2e1s2g1y2e1r1e1w2e1t2g1y2e1u2g1h2e1w2g1z2e1s1g1u2e1s1g1q2e1u3e1t2e1t3g1e2e1u2g1s2e1u2e102e1s1g112e1r2e102e1u2g1s2e1w1g1z2e1s2g1f2e1u1e1q2e1t3e1s2e1t3g1q2e1w2g1e2e1u3g1r2e1t3g1u2e1s2g142e1r3e1d2e1w2e1s2e1u3g1r2e1u2e1w2e1s2e1f2e1s3g1d2e1u2e1h2e1s3e182e1t2g1q2e1t2g1l2e1s2f1m2e1v2g1e2e1t3g1q2e1t3g122e1t3e1t2e1t2e1a2e1v2g1w2e1t1e1i2e1r1g1r2e1r2g1w2e1u2g1h2e1u1g1w2e1t3g1g2e1s1e1j2e1t3g1z2e1u3e1g2e1v1e1l2e1s2g1h2e1u2g102e1s2g102e1s3e1j2e1u2g1g2e1s3e1y2e1s3e102e1t2g1h2e1u1f1r2e1w1e1j2e1r2g1l2e1u1g1q2e1s2g1s2e1t2e1h2e1u2g1u2e1s1e102e1u2g1f2e1s1g1s2e1u1e1j2e1w1e162e1t1e1r2e1t2e112e1s2g1g2e1s3g1f2e1w3e1s2e1t1e1w2e1s2e1v2e1u1e1k2e1u3g1u2e1v3e1a2e1s1e1t2e1s3g1y2e1t1g1l2e1t3g1t2e1w2g1u2e1s2e1k2e1s2g1u2e1u3e102e1r1g1j2e1u2e1w2e1u2e1q2e1t2e1x2e1t1e142e1t2g1d2e1v1g1x2e1u3e1m2e1t1g1z2e1u2f1c2e1u2e162e1v3g1s2e1u3g1s2e1t2g1v2e1u2g182e1t3g1t2e1t2e1w2e1u1f1x2e1t2g1q2e1u3f1q2e1t1e1r2e1w2g1t2e1r2e1y2e1t1e192e1s1g1h2e1t3e1d2e1v2e172e1u2g1t2e1s2g1u2e1u2g182e1t2g1r2e1u2g1t2e1u3f1q2e1u2f102e1u1g1t2e1t2g1f2e1u1e1t2e1t1e1u2e1u2e172e1t1g102e1s3f1y2e1v1g1y2e1s1g1u2e1u1g1h2e1u3g1d2e1t1g1d2e1v2e1d2e1r3f1t2e1s2g1h2e1s1e1e2e1u2g1d2e1v3g1l2e1s1f1t2e1t2e1v2e1t2g1t2e1t3g1e2e1w2g1c2e1s2f1j2e1t2f1a2e1r1e1w2e1t3f1c2e1v2f1f2e1r2g1f2e1s1g1t2e1u2g1h2e1r3f1w2e1t1f1h2e1t2g1f2e1s2f112e1r2g1s2e1u3e1v2e1w1g1m2e1s2e162e1s1g182e1t2g1h2e1s1f1d2e1v2g192e1t3g1l2e1t3g112e1u3e102e1u3g192e1w2g1f2e1u2f1f2e1t2e1w2e1t2g1z2e1r2e1r2e1w2g1f2e1t2e1l2e1t1g112e1u1g1i2e1s2g142e1w1e1s2e1s2g1x2e1s2g1j2e1u3g1b2e1t2g1e2e1u1g162e1t2g1t2e1t2g1t2e1r1g1v2e1s3e1f2e1t1e1h2e1u1g1c2e1t2e1e2e1u2e1s2e1r1e1f2e1v3g1z2e1t1e162e1t3g1y2e1t1f1w2e1u2e1x2e1v2g1t2e1t3g1h2e1t2e1u2e1t2g1d2e1u1g1y2e1w2e172e1t1g1u2e1r2e1v2e1u3f142e1t2f1d2e1w2f1s2e1t2f1l2e1r2e1c2e1u2g182e1s1e1f2e1v1f1l2e1u1e1i2e1u2e1l2e1s1g1c2e1s2g1r2e1w2e1d2e1s1e1t2e1s2g1w2e1r3e1q2e1t1g1t2e1v3e1v2e1r3e162e1r3g1u2e1t2e1t2e1t2g1j2e1t2g1j2e1s2f1d2e1t2e112e1s1e1x2e1s3f1d2e1u1e1t2e1r1e1v2e1s2e1h2e1r1g1e2e1t3g1x2e1w2g1y2e1t2g182e1t2g1j2e1s1g1z2e1r2f1w2e1w1g1s2e1t1g1t2e1t2g1d2e1t2g1i2e1t3e1r2e1u3g1s2e1t2f1f2e1t1g122e1t3f1u2e1t3e1f2e1u1f1z2e1t2g1c2e1t1g1v2e1u1g1t2e1t2f1z2e1v1e1s2e1s3g1l2e1u3g1u2e1u2f142e1s2g1j2e1u3g1s2e1t3g1z2e1u3e122e1u2g1b2e1u2g1d2e1w2f1f2e1t1e1s2e1t2g1i2e1t3g1y2e1s1g1d2e1v3g1w2e1s1e1z2e1u1g1c2e1r2f1z2e1t1f1u2e1w2e1z2e1t2g1t2e1t3g1j2e1t2e1s2e1t2g1e2e1w2g1t2e1t2g1f2e1t2g1w2e1s1g1l2e1u2e1v2e1v2f1j2e1t2e1v2e1u1g1a2e1u3f1l2e1r1e142e1v1g1r2e1u1e1v2e1u2g1t2e1s1e1s2e1t2g1f2e1v3g1j2e1u3f1q2e1s3f1m3e1s2e173e102e1h141l243e161e1m3g1g2g1f3f162e1i3f1c1g1g1f1q1g1l1e123g1e1e1r3g142e1w2g1r2e1u2e1z2e1u2e1i2e1u3e1v2e1u3g1w2e1v3e1t2e1w2g1g2e1t2e1z2e1u2f102e1u2e182e1u2g1x2e1w2g1b2e1s1f182e1s2e112e1s1g1g2e1w1e1u2e1v2e1k2e1u2e182e1s2g1r2e1s1f192e1w2g1m2e1w1g1x2e1s2g102e1s3f122e1s3e1w2e1u1f1k2e1t2g1v2e1t3g1i2e1s1f1b2e1u3g182e1u3f192e1v3f162e1s3f192e1u3f1e2e1s2f172e1w3g1g2e1u3f192e1u3f1f2e1s3f1a2e1u3g1e2e1u3f172e1u3f172e1s2f192e1u3e1c2e1s3f182e1u3f1a2e1u3f182e1s3f1c2e1s1f192e1t3f1b2e1u3f192e1u3f152e1s2f192e1u3g1y2e1s1f172e1u3f1e2e1u3f172e1s3e112e1s2e1y2e1k1e123f1q1g1k1f163f121g141g1u2g1f3f163f103g1i1f1f3e1d1f181g1f1f1b1f1s3f1f3g1i3f1g1e1d1e1e1e1f1g1r3e1f1e183f151g1h2e1d1f1k1f1f1e1i2e1s1g1l3g1d1e1j3e1e2f1b3f1l1f181e122e1b2f1b1f1d1f1b2f1b3e1a1e1d3f1a3f153e1i1f1u3f1f1g1e3f1f1e1f3e1d1e191f1t1f1s1g123e1w1f143f1e3f171g1h1f1u2f1j2g1r1e1a3g181f1r3g1d1e1j3e1f1e1g2e1e1g1h2e1k1g1f3f1f2e1t1e1t2e1w3g162e1t3g1q2e1u3g172e1u3g142e1u3g1k2e1w1e102e1u2e172e1t3g162e1t2f1x2e1w2g1l2e1v2g1r2e1u3g1q2e1u2g1m2e1u3g1r2e1v3e1m2e1w1g1f2e1t3g1q2e1u2g122e1t1g1y2e1u2e1s2e1u2e1s2e1t3e102e1t1g1q2e1t3f1d2e1w2e1y2e1w2e1l2e1u1g1q2e1t2e1w2e1t2e1j2e1v3f1s2e1w1g1y2e1u2f102e1u3f1u2e1u3f1w2e1w3e1y2e1w2e1t2e1u2e112e1t2e1u2e1u3e1t2e1u1g1m2e1u1g102e1t1g112e1u2f182e1u3g1s2e1t3f1y2e1u1e1l2e1r1e1v2e1t3e102e1s3g1f2e1w3g1t2e1w2g1z2e1u1e1b2e1u2e1z2e1t3g1j2e1u3g1r2e1v1e1h2e1t1g1j2e1u1g1j2e1u2g182e1v3g1f2e1u1g1l2e1u3g1z2e1t3g112e1s3e1t2e1v1e1y2e1u2e1h2e1r3e112e1s3f1e2e1t1g1r2e1u3g1t2e1u1g1j2e1s3e1j2e1u2e1q2e1s2g1r2e1w1e1i2e1w2g1v2e1s1g1h2e1t2g1x2e1u1e1f2e1w2f1j2e1w3e1s2e1u1g1h2e1s2g1e2e1s3g1z2e1w3e1m2e1u3e1a2e1t2f182e1r3f1u2e1t2g1z2e1u3e1h2e1w1f1s2e1s2g192e1t2f182e1t2e1e2e1v2f1a2e1w2e1s2e1u2e1y2e1t1f1v2e1u1g1i2e1w1e1h2e1t2e1l2e1u3e1q2e1u2g1j2e1u3e1j2e1u2e1u2e1v2e1s2e1t1e1q2e1s3g1q2e1t3g1z2e1u2e1h2e1v2g1y2e1t1e1u2e1u3f1v2e1t2e1c2e1v2g1s2e1v2g1s2e1t2g1r2e1t1e1t2e1t2g1m2e1w3g1k2e1w1g1i2e1t1g1y2e1s3f1z2e1s2g102e1v2g1z2e1v2g1l2e1t3e182e1t2f1j2e1t3e1v2e1u2f172e1v2g102e1t1g1j2e1s2f1u2e1t3f1t2e1v1g102e1u1e1m2e1u1f1w2e1u3g1w2e1s2g1q2e1u2e1q2e1w2e1y2e1t3g1y2e1u3e1t2e1u2f1i2e1t3g1t2e1u1e1l2e1s2e1k2e1t2f1f2e1t1e1j2e1u2e1w2e1v2f1t2e1t3e1z2e1u3e1z2e1s1g1u2e1u1g1z2e1t1f1i2e1t1e192e1r2e162e1s1e1f2e1w1g1v2e1v1e1e2e1t1g122e1s3g102e1s3e1y2e1v2e1r2e1v2e1h2e1r2g112e1u2e1l2e1u3e1x2e1w2g152e1u2f1g2e1u3e1v2e1t2e1q2e1t1g1h2e1v1g1j2e1u2e1s2e1u2g112e1u2g162e1u2g1j2e1w2e1s2e1v1g1x2e1s2e1t2e1s2f1w2e1u2f102e1w3g1q2e1v2e142e1u3g1u2e1s1f1t2e1s2g1x2e1u2e1y2e1u1e1s2e1t1g1j2e1u3e1t2e1u3g1f2e1v2e1x2e1w2e1w2e1t3g1u2e1s2g1z2e1s2e1d2e1w2e1f2e1u3e1i2e1t1g1j2e1u3g1v2e1t1e1f2e1v2e1q2e1w1e102e1u3e1v2e1s3g1q2e1t3f1r2e1v3g1t2e1w2f1u2e1s2g1v2e1t2e1h2e1t3e102e1v2g1f2e1v1e1v2e1u3g1k2e1t3e1s2e1t2f1l2e1w1e1u2e1v3f1e2e1t2g1x2e1t2e1j2e1t1g1h2e1w1g1t2e1v2e1z2e1t1g1x2e1t3e1c2e1s3e1c2e1v1g1f2e1u1g102e1t1g1q2e1t3g1h2e1t1e1r2e1u1e1e2e1t1g1f2e1t1f1r2e1u2f1i2e1t3g1e2e1t2e1e2e1u2g102e1s3f1t2e1r2g1t2e1s2g1z2e1v2f182e1v2f1d2e1u2f1v2e1s1g1h2e1t2g1k2e1t1e192e1t2g1a2e1t2g1i2e1s2f122e1u2g1b2e1v3f1h2e1u2g1h2e1s1g182e1t2g102e1s2g1r2e1w2e1t2e1t2g1l2e1t1g1i2e1t2e1y2e1s3e1r2e1t1g1h2e1t2g1f2e1r1g1s2e1s1f1u2e1r3g152e1w3e102e1v2g1x2e1u2e1h2e1t2f1v2e1s1g1f2e1v1g1t2e1w2g1h2e1u1e1q2e1s2e1i2e1u2f1r2e1w3e1g2e1v2g1s2e1r2g1t2e1s2g1u2e1u2g162e1u2f1i2e1u2e1g2e1r2f162e1r2f1k2e1t3e1z2e1u3g1w2e1v2f1w2e1u2f1a2e1s1g1x2e1u1g1h2e1u2g1m2e1w1g172e1u2f1i2e1t1g1d2e1u2g192e1w3g1y2e1w1f1y2e1u1g122e1r3g1h2e1r1e1r2e1v2e1h2e1w2e1f2e1r2e172e1r2e1d2e1u3e1v2e1w2f1x2e1v3f1k2e1r2e162e1u3g1z2e1s3f1l2e1w2e102e1v1f1q2e1t2e172e1u3g112e1s2g162e1u2e1q2e1v3f182e1t2e122e1t2e1j2e1u1g1s2e1t2e1s2e1w2g1s2e1t2g1x2e1t2g1k2e1t3e1r2e1v2g1z2e1v1e1t2e1r3g1v2e1u2g1v2e1r2g162e1v3g102e1u2f1t2e1t2e1r2e1s3g1f2e1u3g172e1t2g1z2e1t2f1t2e1u2g1h2e1s2g1q2e1t1g1a2e1v2g1t2e1v2f1s2e1u1e122e1s2e1f2e1t1g1d2e1v2f1s2e1v3f1k2e1t2f1c2e1r2g1w2e1u1g1t2e1w2g1t2e1v3f1t2e1r2f1e2e1s3f1d2e1s3e1y2e1w2g1t2e1w2g102e1r2f102e1t2f1q2e1u2e152e1t1e192e1u3f102e1s1f1u2e1r2g192e1u3e1y2e1v2g1x2e1w1e1f2e1s2f1l2e1t2g1k2e1r3g1x2e1u2g1h2e1w1e1z2e1u3e1v2e1s2f1a2e1s2g1r2e1w2g1b2e1w2g1y2e1u1f102e1u1g122e1r3g1d2e1t1e1t2e1v2f1e2e1s2g1k2e1s3g1j2e1u1g102e1v2g1d2e1u1e1v2e1s1e1y2e1u2g1k2e1u3f1l2e1t2g1v2e1w3g1h2e1s2g1l2e1u3g102e1s3e1f2e1v2e102e1w2e1v2e1t1f1x2e1u3f1m2f1m2e1u2e102e1t3g1j2e1u1f1j2e1v2e192e1w2e102e1u2e1v2e1r1e1t2e1u1g1y2e1v3g1j2e1v2f1x2e1s1g1m2e1u2e102e1u1e1s2e1u2e192e1w3g152e1u2f1q2e1u2g1u2e1r2e1d2e1t2g1w2e1w2g1f2e1t2e1j2e1u2g1v2e1u2g1s2e1u2g1v2e1w1e1j2e1t2f1s2e1u3e1r2e1t2g1x2e1w1g1t2e1w2g162e1s2e172e1u1e1x2e1u3e1e2e1w1e162e1u1e1k2e1t2e1v2e1u2e1j2e1r2g1h2e1t1e1y2e1u1g102e1s2e102e1t3g1v2e1s2e1q2e1w1e102e1t3g1v2e1s1g122e1s2g1h2e1u1g1t2e1v3f1v2e1w2e1u2e1t2e1t2e1s1e1l2e1s1e1j2e1t1g1y2e1w2e1r2e1r2g112e1u2g122e1u1e1k2e1w1e1j2e1u1g1y2e1u1g1h2e1u2f1y2e1u3g1z2e1v1g1t2e1u1g1r2e1r2g112e1r2g1r2e1t3e1w2e1v2g142e1w2g1r2e1u1g1i2e1t2e1u2e1s1e102e1v2f1v2e1u2e102e1u2e182e1u2f1h2e1t2g1r2e1v1e1r2e1v2f1a2e1u2e1v2e1s2e1z2e1u2g1g2e1w3e1t2e1w2e1t2e1u2g1q2e1r2g1w2e1t2g1x2e1u2g1u2e1t2e1y2e1u2e102e1u3e1t2e1t2f1j2e1t2g1j2e1w3g1v2e1r1e1t2e1u2e1t2e1t2e1d2e1v1e1x2e1t2e1r2e1t3g1l2e1t2e1v2e1t1f162e1w1e1z2e1w2g1w2e1u2g102e1u1g1j2e1t2e1w2e1w1g1y2e1v2g1f2e1u2g1a2e1r1g102e1u3e1t2e1v1g1j2e1v1g1d2e1u1g102e1t2g1e2e1t2e102e1v2g1r2e1v3e1r2e1u2e1z2e1u3g162e1s3g142e1u1g1j2e1w2g1t2e1u1g1y2e1u1g1h2e1s1g1f2e1w3g1j2e1t1f1u2e1u2g1s2e1s2f1v2e1t3f1x2e1u3g1z2e1v2g1c2e1t3g1q2e1t3e1h2e1s3e1e2e1v2g1t2e1w1g1s2e1t1e1i2e1s1g1f2e1t3e1d2e1v3e1y2e1u2g1s2e1s3e122e1s2g1h2e1t3g1u2e1w2g162e1v2g102e1t3g102e1u2g1c2e1u2e1j2e1w2e1m2e1u1g1x2e1u3g1f2e1u2g172e1u1g1w2e1u1g1r2e1u2e1r2e1t1g1v2e1t2g1z2e1t2e1w2e1w3e1y2e1v2g1k2e1r1g1i2e1u1g1r2e1t2e1x2e1v3e142e1u3e1t2e1t2f1g2e1t2e1k2e1r2f1g2e1u1g102e1w2g1x2e1u1f112e1u3e102e1s3e1y2e1v1e1u2e1v2e1v2e1t3g1u2e1u1e1k2e1s1e1t2e1w3e1v2e1v2e1t2e1s3g1l2e1s1f1u2e1t1f1z2e1u1e1j2e1u1g1z2e1u2e1r2e1t2g112e1s2e1s2e1w2f102e1w2g1l2e1t3e112e1u3g1s2e1s1e1m2e1u2g1x2e1u1e142e1u2e1h2e1s2e102e1s2e172e1w3f162e1v1g1t2e1u2f1h2e1t2e1v2e1t3g142e1u2f1b2e1t2e1c2e1t2e1h2e1r2e102e1s1g1f2e1v2f152e1v3g1f2e1u2g1h2e1t2e1v2e1t2g1t2e1u3g1d2e1u1e1t2e1u2f1z2e1t3g1e2e1s1g1y2e1u1g1f2e1u3e1j2e1u1g172e1u2g1u2e1t3g1t2e1u3e182e1u3g1y2e1r1f1k2e1u1g182e1s2g1w2e1v3g1r2e1u1f1r2e1u3g1u2e1s2g192e1t1e1d2e1u2g1c2e1w3g1j2e1t3f1w2e1u3f182e1t3g1t2e1v2g1j2e1t1f1d2e1t1g1d2e1t3e1t2e1u2f182e1w3f1a2e1v1g1e2e1u1g1t2e1u1f1h2e1s3e1b2e1v2e1y2e1w2g1d2e1u2e1w2e1t3f1v2e1s3g1x2e1v1e1d2e1v2f1h2e1u1g1j2e1s2g1i2e1t1g1u2e1u3f1r2e1v2g1r2e1t2g1t2e1r1g1t2e1u1g1e2e1v2g1w2e1u3e1q2e1s2g1q2e1s2e1d2e1t2e1e2e1u3g1e2e1v2f1y2e1r1e1f2e1s1e1h2e1t2g182e1w1e162e1w2e1f2e1s1g1f2e1t1g1f2e1t1e1g2e1v2e1d2e1w1g172e1t2f1t2e1s2g1h2e1s2g1f2e1v3g1f2e1v2f1u2e1u2f182e1u1e182e1t1g1k2e1u2e1m2e1t2g1t2e1u2e1s2e1u1e1g2e1s2g1t2e1v2e1u2e1v2e1m2e1u2e1x2e1t2f1e2e1s2g1g2e1u3g1f2e1u3g1t2e1s3e1u2e1u2g1s2e1t1g1y2e1w2e152e1v2e1f2e1t1g1f2e1u2g1t2e1t3e1l2e1w2e1d2e1u2e1h2e1u2g1a2e1s2g102e1t3e1i2e1w3f1j2e1v3f1q2e1t1g1a2e1r1g1j2e1t2g1f2e1v2e1c2e1t1g1u2e1t2f1e2e1u2g162e1t2f1r2e1t2g1t2e1u2g1e2e1s2f1h2e1t2g1x2e1t3e1j2e1u2g1y2e1v3g1y2e1s2f192e1s1g1u2e1r3f1t2e1w2e152e1w2g1m2e1t3g1d2e1s2e1a2e1u3f1j2e1w1g1a2e1u1f1r2e1s2g192e1t2e1t2e1s3f1s2e1v2g1r2e1w2g1m2e1s3g1f2e1u2f1t2e1r1g1u2e1v3f1c2e1v2f1q2e1u3f1f2e1u2g1l2e1s1g1v2e1v2f1e2e1u2e142e1t3e1t2e1u3g1f2e1r1g1r2e1u2e1e2e1v2g1r2e1u3f1f2e1s1g1d2e1t2g1w2e1u3e1q2e1u2g1l2e1s2e1d2e1t2g182e1r2g1x2e1v2g1r2e1u2f1s2e1u2e1z2e1t2e1l2e1s3f1e2e1v1e1g2e1v2e1u2e1t2e1r2e1u2e1x2e1t2f1c2e1u2g1g2e1u2g1f2e1u1g1x2e1u2e1k2e1t2e1u2e1t3f1d2e1t3g1l2e1u2e182e1s1e1s2e1t3e1x2e1w2e142e1v2g1r2e1t2e1i2e1r2f122e1t1e1g2e1v1g1y2e1w2g1t2e1u3e1s2e1s1g162e1t3e152e102e1u2f1q2e1t1g192e1v1e1z2e1w2g1l2e1s3e1y2e1t2e1t2e1u3g1u2e1w3f1z2e1w1g142e1u2g102e1t2g1r2e1t2e1v2e1v3e1h2e1v2g1l2e1u1e1l2e1s1e1s2e1s1e1y2e1v3g1u2e1w2g1s2e1u2e172e1t3g112e1u3e1t2e1w1e1f2e1v1f152e1s2e1u2e1u1g102e1t1e1m2e1v3g1u2e1w3e1y2e1t1e1u2e1u2g1y2e1u3e1q2e1w2e142e1u3e1h2e1u3e122e1u1g1u2e1u2e1v2e1w2g1l2e1w2g1t2e1t1e1y2e1t2f1j2e1u1g102e1w3e1h2e1u3e1h2e1u2g162e1u3g102e1t2f1z2e1t2f1s2e1w1e1c2e1t2f1s2e1r3g1q2e1s2g152e1u2f1h2e1u2g102e1t2e1q2e1u1g1u2e1t2f1y2e1u3e1h2e1v2e1h2e1u2g1h2e1s2f102e1s1f1v2e1u2e102e1w3g1z2e1s2g1v2e1u2g1l2e1t2g1f2e1u2g1t2e1v1g1z2e1r1e1z2e1r3e1v2e1t2e182e1v2g1v2e1v1g1x2e1u1g1v2e1s2e1l2e1u2e1w2e1u2g1r2e1w2g1y2e1s2g1l2e1t1f1r2e1t2g1v2e1u2e1z2e1w2e1s2e1u3e1v2e1t3e1y2e1u3g1w2e1u2f102e1v1e1t2e1u2g192e1t1e1m2e1u2f1l2e1v1g142e1u1g1a2e1t3e1s2e1u2g1t2e1t3e1t2e1w2g172e1w2g102e1t1g1u2e1s2g1v2e1s3g142e1u3g1l2e1u2e1t2e1s3e1z2e1u2e1m2e1u2e1r2e1v3g1i2e1v1e102e1u1g102e1t2e122e1u3g1x2e1v3e1r2e1t2g1z2e1t2e1k2e1t1e1j2e1u2g1h2e1v2f1z2e1v2g1k2e1r1g1s2e1t3e172e1t3e1t2e1w1f192e1v2g1l2e1t2e1u2e1s1f1w2e1t1f102e1w3e1u2e1u2e1f2e1s2g1w2e1s3e122e1u2e1h2e1u1g142e1w2g152e1t1g102e1u1g1f2e1t2g1h2e1w3g1l2e1w3g1z2e1t1e1m2e1t2g1w2e1u2g152e1u1g1y2e1t2g1v2e1t1e1y2e1r3g1j2e1t1f1x2e1v2g1f2e1v2e1s2e1t2g1x2e1s2g1y2e1u2e1j2e1v3e1s2e1u2e1w2e1s2f1r2e1u3e1j2e1t3e102e1w3e182e1w3e1t2e1s1e1u2e1u2e1h2e1t2g1s2e1w2g1u2e1w2f1d2e1u1g1y2e1r2g1q2e1t2e172e1u2f1r2e1v1g162e1u2e1g2e1u1g1i2e1s1g1t2e1t2g1z2e1v1g1s2e1t3e102e1t1f1i2e1u2f1l2e1w1f1l2e1w2g1l2e1t2g1s2e1s1g1q2e1s2e1w2e1t3e142e1w2e1j2e1u2g1f2e1t2e1w2e1u2e1r2e1v2g172e1v1e142e1u1g1x2e1u3f1w2e1s1g152e1v2e1v2e1w3e1x2e1t2e1v2e1s3g1q2e1s1f1u2e1v1f142e1u1f1l2e1s1g1s2e1t3f1w2e1t3g172e1v1e1t2e1v1f102e1s3g1e2e1s2e1s2e1u3g1q2e1u2g142e1u2f182e1u2g1r2e1r2e1q2e1u2g1t2e1t2g102e1v3g1t2e1u1g1t2e1s2e1i2e1u2g1g2e1u2g1t2e1u2e1q2e1t2g1s2e1u2e1v2e1t1g1t2e1w2e1l2e1v2f1y2e1s2f1t2e1u2f112e1s2e1i2e1w2g102e1w2e1d2e1s3f102e1s3g1b2e1u1e1r2e1v2g1a2e1u1f1s2e1r3e1f2e1t1e1j2e1t3f1u2e1v1g1v2e1u1e1w2e1t1e1h2e1t3g1h2e1u3e192e1w1f1l2e1t3g1c2e1u1g192e1s2g1v2e1t2g1t2e1t3e1f2e1v2e1d2e1t3g1u2e1s1e1a2e1u2f1d2e1u1e1t2e1w1f1h2e1s3f1u2e1t1e172e1s3g1f2e1u1f162e1w2g1d2e1r1g122e1r3f1d2e1t2e1f2e1u2g1h2e1u2f1j2e1u3g1w2e1s1f1q2e1t3g1y2e1v1e1c2e1v1f1e2e1s2f1t2e1s1g162e1s3f1z2e1u1f1r2e1v1e1d2e1t3g1i2e1r3g1j2e1s2e1z2e1v2g1j2e1u2e1t2e1r2e1h2e1s3g1t2e1u3g1t2e1t2g1a2e1w1g1j2e1s1f1z2e1s2g1h2e1s1f1u2e1u1g1u2e1u2g1m2e1s1g182e1u1e1v2e1u2e1h2e1u2g1z2e1w2g162e1t2g1t2e1t1e162e1s1e1z2e1u3e162e1u2g1w2e1s3g1s2e1u1e1h2e1u1g1x2e1w3e1k2e1v2e1w2e1r3g112e1t2f1r2e1t2e102e1u3g1u2e1v2e102e1u1g112e1s3g1u2e1t2e102e1w2g1v2e1u3e1b2e1t1e1z2e1u3e1s2e1t3f1s2e1u1g1j2e1w2f1t2e1u2f182e1t1g122e1s3g1w2e1w1f1t2e1v2g1z2e1u1g1e2e1u3g1l2e1t1e1v2e1w2g1d2e1v3g1m2e1u3e1h2e1u2f192e1r3g1h2e1t2g1w2e1v3f102e1s1g102e1s1e1a2e1r3f1l2e1v3g1f2e1v2f1h2e1s1e1e2e1s2g1d2e1r2g1y2e1v2e182e1v3e1r2e1s3e1d2e1r2g1u2e1u2g182e1w2f1f2e1v2g1w2e1s1f1t2e1u2f1c2e1t3e1t2e1w1g1r2e1w2g1x2e1u2g1d2e1u2e1a2e1r2f102e1w2f1h2e1v2g1f2e1s2f1z2e1r2g1u2e1u3e1x2e1w1g1m2e1v3g1l2e1s2g1z2e1u2e1h2e1u1e1c2e1v1f1e2e1u2f1t2e1s1g112e1s3f112e1s1g1l2e1v3g1y2e1u1g1f2e1u3e1t2e1s3e1x2e1u1g1z2e1t3g1g2e1u2g1b2e1r2g1w2e1s3g1u2e1u1e1f2e1w2g1x2e1w2e1k2e1t2e1w2e1r3f1w2e1t1e1d2e1v2g1t2e1v1g1a2e1u1g1t2e1t2e1z2e1u1e182e1u3g102e1v1e102e1t2g162e1u1g1q2e1t1g162e1v2g1m2e1w2g1h2e1t3e1a2e1u2e1q2e1u2f1v2e1w3g1v2e1h2e102e173e1x3e1h191f1h2g1e3g1e1e1i3e1m1g1j1f1k1e1f3e1g1f1g1f1g2e1h1g1d2e152e1u1e1l2e1t2e172e1s1e1l2e1s3g1f2e1w1e1e2e1s3g1g2e1u1f1z2e1t2g1j2e1u3g1t2e1w2g1z2e1s2e1c2e1u1e1z2e1u2e1h2e1s1e1u2e1u2e1w2e1t2e102e1u2e112e1t2f1u2e1s1e152e1v2g1y2e1u2e152e1t3g1w2e1u1e1k2e1u1e1z2e1w1e1x2e1s2f1w2e1t2e1v2e1s2f172e1t3e1z2e1u3f182e1s3e1e2e1s3f1b2e1u3f1d2e1s3f182e1u3f1d2e1s2f172e1t3f112e1s3f172e1s3e1k2e1u3f172e1s3f162e1s1f1b2e1s3f152e1s3f182e1u3f1v2e1s2f192e1s3g1i2e1s2f192e1s3f1e2e1u3f172e1s3e1q2e1s3f1b2e1u3f1t2e1s3f182e1w3g1y2e1s3f172e1s3f1b2e1s3f172e1s2e1u2e1u2g1f1e123g193f1q1e1r3f1r3d1d3f1f3e1b2e1r3e1y2f1k3g1f1e1f1g1r3e1d1e183f131g1h2e1d1f1k1f1f3e1g2e1s1g1e3g1f1e1j3e1d2f1b3f1l3f183e122e191g1f1g1i3f1g2e1f3f1s1g1k3e1q1e1i1f1h3f1c2g1k3f1m1f1k3f1k3f1f3f1f3g1l3g1h3f143e1f2g1f3f1u3e1d1e1f1e1i2g121f163f1f1f1b1f1h3d1s2f1u1f1f3e1d2f141g1l1g1c1g1i3e1j1e1f2g1f3e1z3e122e193f1s2f1b3f1y1g1s1g1f3e1r2e1u2e1v2e1u1e1s2e1u1g1y2e1u1g1y2e1s3g1h2e1s2e1w2e1t3g1r2e1s1e1r2e1t1e1w2e1s3e1h2e1u2g1q2e1u2g1y2e1u2f102e1v2g1i2e1s1g1m2e1u1g1x2e1s2g1f2e1u3e1l2e1w2g1h2e1u1e1h2e1s1g112e1u2e1h2e1t3g1z2e1w1g162e1t1e1h2e1t2f122e1t3e1f2e1s3e1l2e1v3g102e1u3e1s2e1t1g102e1u1g1u2e1u2g1h2e1u1g1y2e1u1g1l2e1u2g1r2e1u2e102e1u2g1y2e1w2f1t2e1s2g1v2e1t3f1u2e1t1e1h2e1s3g1z2e1v1e1u2e1t3e172e1u1e1x2e1t3f162e1s3g1r2e1v2f1x2e1s2g152e1s1f102e1r3e1y2e1s3g152e1t1g1z2e1t1g1v2e1u2e1c2e1u2g1q2e1r2f152e1w2e102e1t3e1y2e1u1g1x2e1u3g1r2e1t2e1h2e1v1e1x2e1u2g1j2e1t1e102e1u2f1h2e1t2g1t2e1t2g1r2e1t2g102e1s2e112e1r2e1y2e1u1e1j2e1v2f1g2e1u2g1j2e1t1g1c2e1s3g1q2e1s2e1u2e1v2e1y2e1s2e102e1u2g1v2e1u2g1j2e1r2e1s2e1u2g1r2e1t2f1j2e1u1e1u2e1s3e1l2e1s3e1s2e1v2f1c2e1t3e1s2e1u2e1j2e1s1g1w2e1s2g142e1u2e1v2e1r1f1w2e1u2g102e1u2g142e1s1g1s2e1w2g1s2e1r1g1l2e1t2f1j2e1r1e1y2e1r1e1u2e1v3e1t2e1r1g102e1u2g1q2e1t1g1y2e1s3e1f2e1v3e1d2e1t1e1s2e1s3e1s2e1t2g1k2e1u2f102e1t1e1t2e1u3e1y2e1t3f1v2e1u3g1d2e1t2f1l2e1w3g1j2e1r2e102e1t2f1u2e1u2g1h2e1t3e162e1v2g1j2e1u2g1w2e1s2e162e1t3g1h2e1t3f1h2e1v3e1v2e1s1f182e1s1e1s2e1u2g1e2e1s1f1r2e1u2e1h2e1u3g1q2e1t3e1j2e1s3e1d2e1t2f1s2e1v2f1t2e1u3g1h2e1s2e1x2e1u1g1i2e1t1g142e1w2f1q2e1t1e1h2e1s1e1u2e1t3g1t2e1s3f1r2e1v1f1u2e1t2g182e1t3e112e1u3e1s2e1s2e102e1u1f1r2e1t3e102e1t1g112e1s2g1q2e1t3e1w2e1u2g152e1t3g1l2e1t1e1f2e1u1g1g2e1t1e1s2e1v1e1h2e1s2f1r2e1r1g122e1u1e1l2e1s3e1t2e1v2e1d2e1s1g1i2e1u2f1k2e1s1g1h2e1t3g1s2e1v1g142e1s2g1q2e1r1e1v2e1u1e1s2e1s2e1s2e1v2g1r2e1u1g152e1s2e102e1s1e1s2e1u2e1u2e1w1g1s2e1t3g1x2e1t2f1u2e1t3e1y2e1u2g1f2e1u1e1s2e1s2e1c2e1s1g1x2e1s2g1f2e1t2f102e1v1g1j2e1t3g1z2e1u2e102e1u3g1s2e1s3f1u2e1u2f102e1s2e102e1s2g1x2e1u2e1h2e1u3g102e1u2g152e1t3e1k2e1t2g1w2e1u3e1v2e1t3e1w2e1u2f152e1t3g102e1s1g1v2e1u2g1q2e1s3g102e1u1g1i2e1s2g1e2e1s3e1v2e1t1e1i2e1u1g1z2e1v2g1r2e1u2g162e1u3e1u2e1u2e1e2e1t3g1l2e1w2g1l2e1t1f1e2e1s2e1v2e1t2g142e1u2e1t2e1u2g1d2e1t3g182e1s3g1h2e1u2g1y2e1t3g1x2e1u3f1r2e1t1e1w2e1t3g1j2e1u1g1s2e1t1g1m2e1u3f1k2e1r3g1h2e1s3e1d2e1r3e1f2e1u1g1s2e1t3g1a2e1t2e1f2e1t2g162e1r2f1e2e1s2e1r2e1v3e1r2e1t2e1s2e1t3g102e1t1f1f2e1s1g1t2e1v1f1r2e1t3e1s2e1u2g172e1t1f1h2e1s3f1j2e1v2g1r2e1t1e1s2e1s1e1c2e1t3g1c2e1r1g1a2e1v3f1z2e1t1f142e1s3g1u2e1s1f1v2e1t1e1f2e1v1g1e2e1s3g1e2e1s1f112e1s3g1i2e1s3f102e1v2f162e1t1f1t2e1t1e1u2e1t2f1g2e1t1g1y2e1u1g1d2e1t3g1w2e1s2g1j2e1s2g1f2e1t3f182e1v2g1z2e1t2g1z2e1s1g112e1r1g1h2e1u3g1h2e1t2e1r2e1u2f1f2e1u1g1m2e1u1e1s2e1t2g1z2e1v1g1e2e1r2f1f2e1r1g122e1s2e162e1s2g1g2e1v3e1f2e1t3g1h2e1t2g1v2e1t2e1w2e1u2g1u2e1v2g1t2e1t3e1x2e1u2f122e1s2g1u2e1r1g1v2e1u2g182e1u3g1k2e1u3e1s2e1t2g1c2e1t3g1s2e1u1g1d2e1u2g1v2e1u2g1j2e1t2f1m2e1s3e152e1v3e152e1s2f1z2e1u1g192e1t1e1b2e1u2g1s2e1w2g1f2e1t2e1b2e1t3g1v2e1u2g1j2e1t2g1t2e1t2e142e1u2e102e1t2g1h2e1s1e1z2e1u2e1h2e1u2e1u2e1s3g172e1s2f1h2e1s1g1l2e1s2e1f2e1t3e102e1t3g1d2e1s3e1f2e1t2g1l2e1t1g1f2e1w3g1w2e1t2g182e1t2g1u2e1r2f102e1t2g1e2e1u2e1x2e1t1f1t2e1t2g1z2e1t2e1s2e1t1g1u2e1v2g1e2e1t1g1t2e1u3g1h2e1t2e1s2e1r2g1h2e1u1g142e1t2g1y2e1s2g1v2e1u2e1t2e1r2g1l2e1w1f1w2e1t1f162e1t3f1h2e1t2g1f2e1t2g1d2e1u3g1c2e1s1f1z2e1s3g1k2e1s3g1s2e1r3g1r2e1t2g1f2e1r1g1f2e1u2e1l2e1s2g1h2e1s3g1i2e1v1e162e1s1e1h2e1t3g1j2e1t3g1t2e1t2e1w2e1w2g1s2e1t2g1v2e1t3f162e1s1e1t2e1u2g1r2e1t2g1y2e1u2e1e2e1r2e1e2e1t2e1k2e1r1g1r2e1t1g1m2e1t3e1t2e1t1e1t2e1s2g1e2e1s3e1v2e1v1e142e1u1g1x2e1t2g1u2e1t3e1h2e1t2g1j2e1h3e1u2e1f2e1s1e1f2e1u2e1m2e1t2g1f2e1u2f122e1t1g1y2e1u2g192e1u1g1f2e1t1g1q2e1u2e1v2e1r3e1f2e1s2e1w2e1v1e1t2e1u1g1z2e1u2e1l2e1s1e1f2e1u2e1y2e1u1e1f2e1u2e1t2e1r2e1f2e1u2g1k2e1r2e1f2e1v2g1y2e1s1e1j2e1t2g1u2e1u2g1a2e1t1g1s2e1w3g102e1s2g1t2e1t2e1v2e1u2f1j2e1s1e1y2e1u2e1f2e1t1e1y2e1u2e1q2e1t2e1q2e1u2e1j2e1u2e1x2e1s2e1r2e1t2g1s2e1u1e162e1u2g1z2e1w1f142e1t2g1j2e1s1g1m2e1s2e1f2e1u2g172e1w2e1v2e1t3g1j2e1r2e1y2e1t2f1v2e1s3g1t2e1v3f1y2e1u2g1x2e1t3g1t2e1t1e1r2e1t1e1i2e1w2g1f2e1t2e1r2e1u1g1v2e1u1e1x2e1u3e1w2e1v2g1w2e1u3g1f2e1t1e1h2e1r3g1x2e1t2e1r2e1w2g142e1t3g1q2e1u1f1c2e1s2g1m2e1u3g152e1v2e1r2e1t2g1u2e1r1e182e1u2g1f2e1t2g1z2e1w1e1k2e1s1g1j2e1u2e1v2e1s2f1t2e1t1e1f2e1w3g1j2e1t1g1r2e1u1g122e1u2f1q2e1t1e1w2e1v2g1r2e1u3g1u2e1t2g1v2e1u2e1y2e1u2g1y2e1v2g1d2e1u2g1x2e1u3g162e1t2f1h2e1s3e1f2e1u2f1c2e1u3e1f2e1t2g1v2e1u2e1d2e1u2g1d2e1w2g1d2e1t1g1j2e1t2g1f2e1s3e1s2e1u2g182e1u1e102e1t1g1s2e1t2e122e1u1g1q2e1s2g1f2e1w2e1w2e1t2g1r2e1u2e1l2e1t2g1e2e1t2e1y2e1v2g1j2e1t1e1y2e1u1g1x2e1u1g1m2e1u3e1t2e1u3g1t2e1s1f142e1t1e112e1u2e1f2e1r2e1i2e1w1g1f2e1u3g1j2e1r1f1l2e1u2g1w2e1s2e1u2e1u1e1g2e1u3e1m2e1t1e1d2e1t2g1f2e1u2g1j2e1v1g1f2e1s2g1r2e1u1e1l2e1t2g1h2e1s2e1m2e1v2g1f2e1t2e1j2e1u2g1v2e1t3e1r2e1t2g1r2e1w1g1x2e1t2g182e1s2g1v2e1t2g1d2e1t1e1w2e1u2g1k2e1u2f1m2e1u3g1l2e1u2g1x2e1r2e1t2e1u1g1t2e1u3g1h2e1u2e1z2e1s1g1y2e1t1e1r2e1w2g1f2e1t1g1t2e1t1e1z2e1u2g1x2e1u1e1f2e1v2e1j2e1s2f1u2e1t3e1t2e1t2e162e1s2g1f2e1v2g1k2e1r2g1x2e1t1e1v2e1s2g1x2e1u2e152e1u2e1j2e1t1g102e1t1e102e1t1g1z2e1u2e1m2e1v1e1f2e1u1e1q2e1t3g1l2e1u1g1d2e1u3g1t2e1v3f1v2e1u2f1s2e1u2e1v2e1t2e1u2e1u3g1z2e1w2e1s2e1u1g1s2e1t2g1x2e1t2f1q2e1t3e1w2e1w1g1d2e1s1e1s2e1s2e1c2e1u2e1u2e1u1f102e1u1e1r2e1t3e142e1u2g1h2e1s1g1f2e1u1e172e1v2g1t2e1t1g142e1s3g1w2e1s1e1y2e1t3e1z2e1t1e1y2e1t2g1c2e1t3g1f2e1u2e1m2e1u1g1s2e1w3e1f2e1r1g1r2e1s2e1d2e1r1e1u2e1r2f1f2e1v3g1r2e1u2e1u2e1s1g162e1u2g1j2e1t2g1i2e1v2e1z2e1t1e1d2e1t3g102e1s3f1f2e1t3e1d2e1v3g1r2e1t3f1d2e1t2g192e1t2f1c2e1u1f1c2e1u2g1w2e1r3f1d2e1t2g1e2e1t2f1r2e1u1g1m2e1v2e1a2e1u2g1e2e1u1g1s2e1u1g1j2e1r3g1j2e1v1e1j2e1s1f1h2e1t2g1t2e1s1g1c2e1u1g1r2e1v2f1g2e1t2g1d2e1t3g1t2e1s3e1s2e1t3g1c2e1w1e152e1r3g1f2e1s2f172e1s3f162e1t1g1y2e1w1g1a2e1t1f1c2e1u3e1s2e1s1f162e1u1g1e2e1v2g1r2e1s2g1r2e1u1e1f2e1u2f162e1u2f1f2e1t2e1d2e1r1g162e1r3g1t2e1r2f152e1r2g1d2e1v1g1g2e1t3g1m2e1t1f1w2e1u1g1g2e1s2e1r2e1t2g1e2e1t2g1d2e1u1g1k2e1u1f1w2e1s3g142e1w2e1d2e1u1g1h2e1t2e1g2e1u1e1t2e1t2e1e2e1v1g1m2e1r1g1z2e1r2g1h2e1t2g1z2e1s2f1t2e1t2g1g2e1s2g1r2e1t3g1t2e1r2g1m2e1r2g1z2e1u1e1r2e1u2g1m2e1r2g1v2e1t2e1f2e1u3e1i2e1v2g1t2e1u2e1r2e1s2f1e2e1u3f1r2e1s2g1t2e1w2e1a2e1t2f1s2e1r3e1t2e1t2e1r2e1s3g1j2e1v3f1t2e1s3g1y2e1s1f1z2e1u2e152e1s1g1f2e1v2e1d2e1u1e1c2e1s2g1z2e1t3g1u2e1u2e1c2e1u3g1t2e1u1g102e1u2e1t2e1r1g1f2e1t2e1z2e1t2e1t2e1t1g1q2e1t2f1y2e1s2f162e1t1g1f2e1v3g1f2e1r1g1x2e1s3g1e2e1u1f1k2e1r3f1e2e1u1f1t2e1u3e1d2e1t3g1s2e1u1f1e2e1t3g1e2e1u3g182e1t3f1y2e1s2f1u2e1u1g1m2e1t3g1m2e1v1g152e1t2g1s2e1s3g102e1u2e1m2e1s1f1f2e1w3g1u2e1t3f1t2e1s2g1z2e1t1e1d2e1t2f1h2e1w1g1h2e1s2f1d2e1r3f1f2e1r1g1r2e1t3g1c2e1u2g1r2e1u1e1d2e1u2f182e1u2f1f2e1r3e1r2e1v2g1f2e1r2g1s2e1t2g1t2e1t2e1j2e1s2f1e2e1v2g1x2e1s1g1e2e1t1e1t2e1t3g1r2e1r2g1m2e1t1g1z2e1s1e1r2e1u2g1r2e1r2g1y2e1s3f1t2e1w2e1i2e1u2g1y2e1t2e1z2e1u1g1r2e1u1g1s2e1w2g1j2e1t2g1m2e1u1g1l2e1s1g1t2e1t2g1k2e1v2e1m2e1r2g1u2e1t2e1u2e1s2g1q2e1u2g1t2e1u3g1y2e1s2e1w3e1v2e1w2f1h2e1t3e1j2e1u3g122e1u3f1u2e1t2g162e1w3e1u2e1r2g162e1r3g1j2e1u2f1w2e1s2g1v2e1v1g1e2e1u1g182e1u1f1w2e1t3f1j2e1t3f1s2e1w2e1w2e1t1e1z2e1t2e1q2e1t2g1h2e1s2f172e1u2g1u2e1t1g102e1u2g112e1u2g1f2e1s2e1a2e1w2g152e1s2e1s2e1t2e1y2e1s1g1f2e1t2e1r2e1w2g1u2e1u1e1r2e1t2g1q2e1u1e1m2e1t1g1r2e1u2e1u2e1u2g1u2e1u3e1w2e1u2e1r2e1u1e172e1t2f152e1t3e1t2e1s3f162e1s2g102e1s2f1r2e1w1e1h2e1s1e1l2e1r1g122e1u3g1s2e1s2g1w2e1w2g1e2e1u2g1c2e1u2f182e1u2g1s2e1u2g1h2e1w1g1h2e1t1e1x2e1u2g1q2e1u2f1x2e1u2e1h2e1w1e1v2e1t3g142e1t1e1q2e1u2g1y2e1t3g102e1w2g1l2e1s2e1t2e1r3g112e1r1e1r2e1u2g1u2e1u2e1y2e1u2g1f2e1t2e1j2e1s2g1h2e1t2f102e1w2g1t2e1t1e1z2e1s2g112e1u2e162e1u3g1l2e1w3g102e1t1f1i2e1u1g1v2e1u2f1t2e1t2e1f2e1v2g1y2e1t1f1j2e1t2e112e1t2g1a2e1t3e1a2e1u2e102e1s2f1y2e1s2e162e1s2e1u2e1t3g1l2e1w2g1s2e1u2e1g2e1t2e1l2e1u1g1f2e1t2e1c2e1u2e162e1t3e162e1u1g1v2e1u2e142e1u2g1m2e1v1e1i2e1u3g1k2e1s2g172e1s2f1x2e1s2f172e1v1e102e1t2e1e2e1u3g1v2e1t1e1z2e1u1g152e1t1g142e1t2g1y2e1t2g1u2e1t2f1t2e1u2f1t2e1w2e142e1s3f1q2e1t3f122e1s1g1b2e1u1e1t2e1w2g1l2e1t2e1u2e1s2e1h2e1s2g1u2e1u1e1h2e1v1e1v2e1t2e1r2e1t1e1l2e1t2g1q2e1t1g1u2e1v2e182e1t3f1s2e1u3f1v2e1t1e1d2e1s2g1t2e1w2e1m2e1t2g1s2e1u3g102e1t2e1y2e1t1g1m2e1t2g1h2e1r2e172e1t2g1d2e1u1e1y2e1s2f1j2e1w1g1v2e1t1e1j2e1u1e162e1u1e1q2e1u3f1l2e1u2g1l2e1t2f1t2e1s3f1f2e1s1e1a2e1t1g1z2e1v2g102e1s1e1s2e1t1g1t2e1t2g1t2e1r1e162e1w2e1z2e1t1g1t2e1r1e1k2e1t3g1r2e1s1g1t2e1u2g1u2e1s2g1s2e1u1g122e1s1g1k2e1t3e1l2e1t2f1z2e1u3g1z2e1u2g1x2e1u1g1f2e1s2f1c2e1w3f1u2e1s1g1h2e1u1e172e1u2g1w2e1s2e1v2e1v3e1w2e1u2g152e1s2e1x2e1u1f1u2e1u2g1x2e1w3e1r2e1s2e152e1u2e1u2e1t3g1j2e1u2g1f2e1w3g1v2e1t3f1x2e1u2g1w2e1u3e1t2e1u2e182e1w3f1h2e1t2f1u2e1u2g192e1s2e1y2e1t2e1u2e1w2e1r2e1u2g1t2e1t1e1q2e1u1f1t2e1u2g1t2e1t2e1u2e1t3g1t2e1s2g1e2e1t3g1v2e1t1e1d2e1t2e1t2e1s1e1s2e1u1g1w2e1r2e1t2e1u2g1s2e1w2g1v2e1t2f1i2e1t3e1v2e1t1g1x2e1t2e1t2e1t3g1t2e1u2g1t2e1r2g1a2e1t3g1y2e1s3f1f2e1v2g1l2e1u1g1t2e1s2g1j2e1r2f1y2e1s1g1t2e1u2e1x2e1t1f1y2e1t3g1h2e1t3g1s2e1s2g1f2e1v3f1h2e1t1g1s2e1u3e1y2e1u1e1y2e1t3f1e2e1w1g1s2e1t2g1m2e1r1e1b2e1r2g182e1t3f1h2e1w3e1z2e1t2g1w2e1r2g1w2e1u2g182e1t1e1t2e1u3g182e1s2e1d2e1t2g1v2e1r3e182e1t2f1s2e1u1g1t2e1u1e1z2e1s3g1v2e1s3e1r2e1s1g182e1w3e1f2e1u3f1t2e1t3f1k2e1t3e1e2e1t1e1w2e1w2e102e1t2g172e1u2g112e1s3g1h2e1u1g1h2e1w1g1l2e1s2g1t2e1u2g182e1t1g1s2e1u1e1h2e1v1g1l2e1t1g1h2e1s2g1t2e1s3e1x2e1u2e1r2e1u2g1z2e1t2e1z2e1t2e1e2e1r1g1f2e1t2e1g2e1v1g162e1u1g1z2e1u2g112e1s1g1s2e1t1g1f2e1w2f1f2e1s2g1u2e1s3f1h2e1t2g1d2e1t2g1m2e1v2g152e1s3f1v2e1u2e1m2e1u2g1y2e1u2g142e1u1e1b2e1u2g1w2e1u2e1y2e1u1f1y2e1t3e1x2e1u2e1v2e1u2e1t2e1t2g1a2e1t3g1t2e1u3g1s2e1v2g1t2e1s2g162e1s3g1x2e1u1g1v2e1u3e1t2e1w1e102e1s3g1s2e1u2e112e1t1f1i2e1s2g1t2e1t2f1h2e1t1f1u2e1r2e1d2e1s1e1x2e1u1g1h2e1v2e1x2e1u1g1z2e1s2g122e1u1g1d2e1s3f182e1v1g1a2e1t1g1d2e1s1g1t2e1u1g1e2e1t2e182e1v2g1d2e1t3e192e1t3e1k2e1u1g1d2e1s2e1d2e1w2g1e2e1u2g162e1t3g1h2e1u3e152e1r2e1h2e1u1f1t2e1u2g1z2e1u3g122e1t3f1r2e1r2f142e1v3g1d2e1s3e1t2e1s3g1h2e1s3g142e1u2g1d2e1t1g152e1r3f1e2e1t2e1h2e1u1g1x2e1s1g162e1u1f102e1t3f1i2e1t3e1f2e1t1e1u2e1u3e102e1v2g172e1u2g1t2e1t1g1e2e1s1f1l2e1t1g1z2e1v2f1g2e1t3g1t2e1s2g1h2e1s1g192e1t2g1f2e1v2g1m2e1t3g152e1s3f1x2e1u2e1i2e1u2g102e1w2e1f2e1r2e152e1r2e1d2e1s3g1r2e1t1e1z2e1w2e1w2e1t3e1a2e1t2g1m2e1t1f1t2e1u3g1s2e1v3g1r2e1s2g192e1u2g1s2e1s2g1w2e1s2e1k2e1w2f152e1s3f1i2e1t2f1z1f1y3e1x2e1z3e1f341e1k1m2j1d1t1v1e1h2s1e161','73a7eo3q1v3q241c291u393x211d3q0z121o27212o1b3x3e1k193x111k1c2z193u3y112z1611153x392q1932361s3u2v323p1z3w263e153v3b2q19322411211o252c1i2e2b381w2x3u11121m380y111229233x313b361y2x3u11101o2e182v2z3p11323a231s27353e14212x253e163u29111138251s27352c1621381y1a3u291y3u27182u291u2s291q3e113u2811113w26113w263u2m3q011131293y141o272c2q111z231211121o272c3q2o37322o1121313b213x2238163o011e1e2v2c2b2q142u1z121f311q1z313a25373u273w273t133823111138391131161h111e1o3e162v212r3e29233x312q1g29333e3b3w141o141l1c1e1f1e1e1f1e122f1k1c1e2g1m1e183g181g151e1m1e1k1f1d2e1s1f1r2c1v2g1t2e1q2e1w2e1s2e1g2e1u1e1x2e1s3e1r2c1w2e142e1q2g1m2e1u1c1m2e1u3e1f2e1u3f1z2c1u3e1z2e1r1f1u2e1s1d1w2e1s2e1s2e1t3g1v2c1w2e1v2e1s2g192e1u1d102e1t2g1o2e1s2f1y2c1v2g1l2e1r1e1u2e1t2c1u2e1s2e1w2e1s3e192c1w2g102e1q3e172e1t3e1v2e1s2f152e1s3f1x2c1u3f172e1q3f1e2e1s2d1b2e1s3f182e1s1f192c1v3g162e1q3f182e1s3d1x2e1s1f152e1t3f1c2c1u3f182e1q3f142e1s3d1b2e1u3f182e1s3f182c1u3f1h2e1q3f192e1s3d1f2e1s3f152e1s3f1t2c1u2f192e1q3f162e1s3d192e1t3e1g2e1s2f172c1u3f192e1q3f172e1u2c1w2e1s2e1c1e1f1e1m1e1e1e1k2f1b3e1b2e141c141f143f1q3f1c1g1u1d1y2f1j2f163f121d1f3e1g3f1m1e193e1f3f1j3e153f1l1e1g1f1h1f1g2c1a1e1f1f141g1s1f1j3c1e1e1g3g121f1h3g193e1e3f1s1g1k3e1f1e1f3d1e3f1f3f1d3f1f3f1f1d1d2f1e3f1c3f1e2g1s3c1h1e141g1q1g1f3f1r3b1e2f1f3e1d3e181e1f2e1d2e1c1g193f1g2e1f2c1e1g1k1e1b3e1g1f1g2c1l1f1t2e1q1f1j3e1d3e1a1e1d3g1g3f1f1e1g2c1t2e1u2e1q3f102e1t1e1j2e1t2f1i2e1u3f1q2c1w2g1t2e1s2e1r2e1r2d122e1u1f1s2e1s1e1y2c1w2g1h2e1r1g1j2e1u2e162e1u2g1j2e1u3e1k2c1u2g1k2e1r1g1q2e1t2e102e1s2e1f2e1u3e1u2c1v1g1l2e1r1e1z2e1u1c1j2e1t2g1i2e1s2g102c1v2e152e1r3g1y2e1r1e1u2e1s1e1q2e1t2g1t2c1w2e1m2e1q1e1m2e1s2c1q2e1t2e1p2e1u3e1k2c1v2e1h2e1s1e1s2e1t1c1j2e1t1e1d2e1u1g1m2c1u1g1d2e1s1e1y2e1t2c1v2e1t2f1q2e1u3e1w2c1u2e1y2e1q2g172e1t3e1h2e1u1e152e1s3g1l2c1u2g1a2e1p2e1w2e1t2d1v2e1t1e1j2e1u2g1i2c1w2e1x2e1s3g1j2e1s2e162e1t2g1s2e1t2f1y2c1w2g1l2e1q2g1d2e1u2c1x2e1u3e1y2e1u2g1t2c1t1e1z2e1s2g1d2e1t1c1u2e1u1g1o2e1t3g1j2c1t1g1v2e1q1g1v2e1u2e1v2e1s2g1c2e1s2e1s2c1u2g1j2e1s2e1g2e1t2e1x2e1r2e1q2e1u1g1y2c1w2g1k2e1s2e1r2e1s2e1w2e1s1f1j2e1t1e162c1u2g1v2e1r3f1s2e1s2d1z2e1s2g152e1s2e1u2c1u2g102e1s1e1k2e1r1d1u2e1t2f1y2e1t2f142c1u2f1h2e1p2e1l2e1r2c1v2e1s2e1r2e1u2g1l2c1w2g152e1r1g1y2e1t1e122e1u2g1w2e1u2g1j2c1w1e1r2e1s1e1k2e1t1e1u2e1u1g1y2e1u2e102c1v1g1u2e1s2e1t2e1u2e162e1t2g1r2e1t3f1z2c1u1g152e1s3e1t2e1t2e172e1s2g1d2e1u2g102c1w3g142e1s2g1j2e1s3c1v2e1s3e1j2e1s2e1s2c1v3e1r2e1s3g1m2e1t1d1a2e1t2g1w2e1s3e162c1u2f1s2e1r1e1g2e1t2e172e1u1e1x2e1s3g1f2c1v1e102e1r1g1s2e1t3c1a2e1t2e1c2e1t1g1f2c1w3g102e1r3e1h2e1s2c1j2e1s2g1a2e1u1g1z2c1w2g1x2e1q2g1f2e1t1e172e1s2g122e1s2g1s2c1u2e102e1q1e1z2e1u2c1u2e1t1e132e1r1e1z2c1u1e1h2e1q2g1j2e1s1d122e1u1f1b2e1u3g1t2c1t2e1z2e1s2f1d2e1u1c1u2e1u1e1x2e1u2e1e2c1v2g1h2e1r1g1x2e1r1c112e1s2g1q2e1s3e1t2c1v1f142e1q1g1m2e1t2e1j2e1s2g1r2e1u2g1l2c1u2g1z2e1s3e1y2e1u1c1y2e1u1f1o2e1s2g1s2c1v3e1t2e1s2e1y2e1t3e1u2e1u2e1h2e1s2e1m2c1v3g1c2e1r1f1s2e1u2e1h2e1u2g1t2e1t3e1x2c1w2e1m2e1p1e1t2e1u2e162e1u2e1h2e1u2g1f2c1v2e1u2e1s2e1m2e1t2e192e1t1e122e1u2g1x2c1w2g1m2e1r3g1u2e1s2e1v2e1u3e1q2e1u2f1u2c1v2g1t2e1r2e102e1u3e112e1s1g162e1s2e1q2c1v2g1t2e1r2e1t2e1s2e1v2e1s1g1r2e1s1e1h2c1v2g102e1r3e1y2e1t1e1m2e1t2g1b2e1t1g1h2c1v2e1y2e1q1f1y2e1s2c1f2e1u2g1d2e1s2g142c1v2e1z2e1s3e1j2e1s1c112e1u3f1b2e1s3f1f2c1u2f1t2e1r2e1k2e1s3e1f2e1u3g172e1r2g1z2c1t2f1t2e1s2g1d2e1s2e1q2e1t1g1a2e1t2f1t2c1v2f1s2e1s1e1y2e1s2c1f2e1t3g1d2e1t2e1s2c1v3f1k2e1r2g182e1r2e1w2e1u1g1t2e1u2g1t2c1v3f1t2e1p2f1a2e1t1e1f2e1s1e152e1u2f1z2c1v3g1q2e1q1g152e1t2d162e1s2e1o2e1s1g1z2c1v3g1x2e1r2g1r2e1s3e1q2e1u1e152e1r1e192c1t1g1d2e1p3g1c2e1r2e112e1t2g1b2e1u2f1f2c1v1e1e2e1r3e1d2e1t3e192e1t2e1c2e1s2g142c1w1g1z2e1r2g1e2e1t3e1i2e1s2g1h2e1u2g1h2c1v3g1t2e1r2e1m2e1t1e182e1s3e1r2e1t2f1s2c1w1g1l2e1p3g1m2e1s2d1v2e1s1g1q2e1t1e162c1w2e1h2e1q1e1x2e1u2d1i2e1t1e1p2e1r1g1f2c1v1g1j2e1r2f1r2e1s1e1v2e1t3f1y2e1s2f1s2c1t1e1s2e1q2e1s2e1t1c1f2e1t2g1r2e1t1g1w2c1v1g1a2e1s1g1h2e1t1d1u2e1u3g1f2e1s3e1m2c1u3e1y2e1r2g1f2e1r2d1h2e1t1e1h2e1t1g1t2c1v1e1s2e1q2g1f2e1u3d1x2e1t3e1u2e1s2f172c1v3g1h2e1s3f1w2e1t1c1e2e1t3g1r2e1t1e1z2c1u3e1t2e1r1g1r2e1s2c1l2e1r3g1u2e1u3e1z2c1v1e1t2e1r1g1w2e1t2e102e1t2g1s2e1u2f1r2c1u1e1c2e1q3g1d2e1u2e102e1t2g1v2e1s3f1t2c1v1e1w2e1r3g1f2e1u1e1u2e1t1g1k2e1s3f1m2c1t3g1h2e1q1e1c2e1r2c1h2e1u3g1q2e1r1g1c2c1v2e1f2e1r2g1z2e1r2d1d2e1s2e1p2e1t1e1t2c1v2e1s2e1r3g1w2e1t1d1h2e1s1g1f2e1t1e1f2c1v2g1s2e1p2e1t2e1t3c1q2e1r3g182e1t3f142c1v1f142e1r2e1r2e1t3e1f2e1u2f1d2e1t1e1e2c1v3e1f2e1r3g1e2e1s3e1e2e1s2g1p2e1r2e1t2c1w1g1y2e1s1e1i2e1t3e1v2e1s2f1q2e1s1g102c1u2f1s2e1p1e1q2e1s2c1w2e1t1e1b2e1t2g1t2c1v1g1a2e1q2f1s2e1t2e1q2e1u2g1j2e1s2e1z2c1v2g1z2e1s2e1y2e1t2c1m2e1u1g1p2e1u2g1t2c1t2e1v2e1q1g1f2e1s2e102e1s1e1q2e1u2g1j2c1u1e1i2e1r3e1s2e1s3c1t2e1s3e1s3g1r2e1t3c1y2e1u3g1w2e1u3g1j2c1u1f1f2e1s2e1h2e1u2c1u2e1s2g1h2e1u1e1r2c1w1g1y2e1s2e1w2e1t1e1z2e1u1e1s2e1t1e1j2c1u1f1y2e1r3f1s2e1t2e1v2e1u2g1p2e1u3g1s2c1w1e1r2e1q2g1d2e1s1e102e1u2e1d2e1s2g1r2c1u1e1s2e1s2g1g2e1u1e1m2e1t3g1c2e1u1e1j2c1w1g1y2e1s2f1c2e1s1d102e1t1e1r2e1u2f102c1v2f1t2e1q1g1t2e1u2c112e1u2g1w2e1t2g1y2c1w2e1e2e1s2e1x2e1s3c1h2e1u2g122e1t1g1h2c1v2e1q2e1q1e1t2e1u2c1j2e1u3g1v2e1t3e1f2c1u1e1s2e1r3e1f2e1s1e1t2e1s2g142e1t3g1r2c1w1e1i2e1r2e1s2e1t1c102e1u2e1o2e1t1g102c1v3g1j2e1q1e1w2e1u2e1y2e1u1e1h2e1u1e1t2c1w1e1x2e1r1g1f2e1t2c122e1t1g1h2e1r1e1r2c1u2f1d2e1s2g1g2e1r2e1r2e1u2e1y2e1u3e1h2c1u2e1t2e1s2e1m2e1t1d1m2e1s1g1t2e1t2g1m2c1w3e1x2e1r2f182e1s1c1z2e1u2e1p2e1s3g1d2c1w1g1h2e1s2g1a2e1u2e1x2e1u1e1e2e1u3e1t2c1t2e1k2e1s2e102e1t2c1s2e1t1g1r2e1s2g1g2c1w2g1r2e1r2e182e1r1e1w2e1u3g122e1t1g1t2c1w2e1r2e1s1e1w2e1r2e1r2e1u1g1k2e1t2f1g2c1w2e1m2e1s3e1z2e1t2c1l2e1r1g1y2e1t3e1k2c1w1e1w2e1s2g1d2e1u2d1r2e1s2e1w2e1t2g1m2c1w2g1r2e1r1g1t2e1t2c1y2e1s2f1h2e1u1e1x2c1v2e1r2e1r2e1j2e1s1c1t2e1r2f1j2e1t3f172c1u3g1y2e1s2g1x2e1u2c122e1u2g1h2e1u1g1j2c1u1g152e1q1e1f2e1u2e1u2e1t3g1v2e1s3e102c1u1e1y2e1s3f1l2e1t2e1f2e1s2g1h2e1t2f1j2c1w2g1y2e1r2e1f2e1u2e1v2e1s1g1i2e1u2g1s2c1w2e1j2e1s1e1u2e1s1c1j2e1s2g1b2e1s2e1g2c1w2f1t2e1q2e1j2e1u1c1t2e1t2f1d2e1t2g162c1u2g1k2e1r2e1t2e1s2e1w2e1u1f1d2e1u3e1f2c1t2e1w2e1s1g1h2e1s1c1z2e1u2e1d2e1u1e1m2c1v1e1x2e1s2g1r2e1t1e1w2e1u2g1r2e1r1e1c2c1u3f1x2e1q2g1t2e1s1e1i2e1r1g1h2e1u2g1t2c1w3e1u2e1s2e1m2e1s1c1w2e1t1e1y2e1t1e1h2c1v3e1y2e1r2e1d2e1t2c1w2e1s2g1u2e1u2e1t2c1v2e1j2e1q2g1l2e1u2e1m2e1r2e122e1s2e1f2c1w2g1t2e1q1e102e1u2e1h2e1u2e1w2e1u2e1h2c1u2e1k2e1r3g1a2e1t1c1u2e1u2g1b2e1u2g1t2c1v2e1v2e1r3f1u2e1u2e1a2e1u2e1w2e1t1f1y2c1u2f1m2e1q2g1l2e1t2e102e1t2e1g2e1u3f1j2c1v3f1q2e1r1f1y2e1s2e112e1r1e1w2e1u1f1d2c1t3f1d2e1p2g1v2e1s1e1i2e1s1g1y2e1r3g1l2c1v3g1t2e1r3g1t2e1r3c162e1r2g1r2e1t2e1r2c1v2g1j2e1p2g1h2e1s2d1d2e1t1e1v2e1s1e1v2c1u3f1d2e1q2e162e1s1e1u2e1r3f1r2e1u2e152c1w2g1m2e1r3g1e2e1s2c1a2e1u3f1h2e1u1g1a2c1u1f1r2e1q2g172e1t2c1t2e1s3f1q2e1t2g1r2c1w2g1m2e1q3g1d2e1u2e1t2e1r1g1s2e1t3f1c2c1v2f1q2e1s3f1d2e1u2e1l2e1s1g122e1r1f1l2c1v1e1d2e1s2g1r2e1s1c1d2e1t2g1s2e1s3e1q2c1v2g1c2e1q2g142e1t2e1k2e1s2g1p2e1s2e1e2c1v2g1r2e1s1g152e1t2e1h2e1u3g1d2e1s3f1t2c1v1e1u2e1p2g152e1u2e1e2e1u2g1t2e1t1f1j2c1v3g1t2e1r1e1d2e1t3d1m2e1u1g1e2e1t2f1g2c1t2f1d2e1r3g1g2e1r2d112e1r3f1g2e1s1g1h2c1v1f1d2e1s1f172e1t3e1t2e1u1g1w2e1u1g1r2c1v1g1w2e1q1e1x2e1u2d1z2e1t3f1b2e1u1g1m2c1u2g1m2e1p2g1r2e1s1e192e1u1g1e2e1s1g1d2c1w1e1d2e1r3g1q2e1t2c1l2e1s2f1q2e1t2g1j2c1w2g1j2e1s3g1w2e1t2c1w2e1u3g1p2e1u3e1v2c1w2f182e1s2f1a2e1u2e1h2e1s2g1x2e1u1g1e2c1u1g1t2e1s2g1s2e1t3d1h2e1u3e152e1t3g1t2c1v1g142e1q3g1u2e1u2d1f2e1s2g1q2e1r1g1u2c1w2f1q2e1r2e1g2e1s1d102e1u2f1g2e1t2g1r2c1v2e1z2e1r2f1t2e1s1e1z2e1s3e1w2e1u2g1f2c1w2e172e1q1e192e1s3d1h2e1t3e1b2e1t3g1r2c1v3f1d2e1r2g172e1t2e1e2e1u1f1a2e1s2g1w2c1t3f1d2e1r2g1c2e1t2d1t2e1u3g1k2e1t2e1a2c1w2g1e2e1s1g1q2e1u1e1l2e1r2g1h2e1u1e1j2c1u1f1h2e1r2g1r2e1s1e1e2e1u1g1p2e1s3e182c1v3f1l2e1s1f1x2e1t3e182e1s3g1p2e1t3g1a2c1v1f1c2e1s3e1q2e1t1e1s2e1s3g1r2e1t1e1u2c1t2g152e1s2g1c2e1u2e1x2e1t2f1k2e1u3e1r2c1v1g1m2e1p2e1x2e1u1c162e1u2g1e2e1s1g1d2c1u3g1u2e1s1e1d2e1t3e1s2e1t2e1h2e1s2f1s2c1v2g1j2e1s2g1j2e1u2c172e1t1g1q2e1r2e1r2c1w2f1t2e1p1g1r2e1s2d1k2e1u2g1r2e1u2e1m2c1w3f1l2e1q1g1t2e1t1e1g2e1s1e1y2e1t2g1j2c1v1e102e1s2e1q2e1t1e1v2e1s2f1r2e1u3f1f2c102e1u2g192e1u3f1y2c1v2e1k2e1r2g1b2e1t1c1j2e1u2e1r2e1r3e1d2c1w2e1h2e1s1f162e1u2c1t2e1s2g1h2e1t2e1f2c1w3g142e1r2g1b2e1t1e1e2e1t1g1s2e1t2e1u2c1w2e1s2e1q2e1t2e1u1d172e1t1e1p2e1u3e1m2c1v1g1h2e1r2f1r2e1u2c1v2e1u1e1o2e1u2g1w2c1w3e1z2e1r2e1h2e1u2c102e1t1e1f2e1t2g1x2c1v3f1h2e1r3g1y2e1t1c1u2e1s2e1y2e1u3e1d2c1u2g1z2e1r1e1s2e1t2c102e1s2g122e1u2e1u2c1t2g162e1s2g1l2e1s3d1a2e1u3e1w2e1s3e1y2c1u2g1r2e1s2f1t2e1s1e1r2e1u2g1f2e1u3f1h2c1t2g192e1r2e1h2e1t1e1u2e1s3g1f2e1t2e1w2c1w2g1l2e1q2g192e1u2e1u2e1t3e1w2e1s2e1f2c1w1e1y2e1s2e1j2e1r2e1v2e1s2g1f2e1t2f1y2c1v1g1h2e1r3e1y2e1t1c1j2e1u2g1s2e1t2f1j2c1w3e1w2e1r2e1t2e1r2c1a2e1t2g1i2e1t2e1w2c1w1g1f2e1s1e1v2e1u2e1h2e1t2g1h2e1r2e162c1w2e1s2e1r2e142e1u1c112e1u3e1f2e1u2e1e2c1u2e1z2e1q3g1d2e1u2d122e1s3g1s2e1s2g1c2c1v1f1y2e1s2f1u2e1u2e1q2e1s3g1g2e1t3e1x2c1t1f1v2e1p2e1s2e1t2c1x2e1u1g1q2e1u2f1w2c1w3g1h2e1s1e1y2e1t1c1q2e1r1g1q2e1t3g1e2c1w2g1h2e1s1e1e2e1u1c172e1u1e1v2e1t2e1s2c1w1g1h2e1s1e1t2e1u1e1q2e1s1g1f2e1t3g1s2c1v2e1k2e1q2g142e1u1e162e1u1f1q2e1t2g142c1w3f1f2e1q1g1r2e1t1c122e1u3e1p2e1s2e102c1w1e1y2e1s2g1r2e1u2c102e1u1e1v2e1t2g102c1u2f1s2e1q1f1r2e1s1c1q2e1u3g1s2e1u3g1c2c1u2g182e1r2e102e1s2e1q2e1u2e1u2e1t1f1m2c1u1e1l2e1s1e1u2e1u3c1u2e1s2g1f2e1s3e102c1u2g1m2e1s3e102e1t1c172e1u1e1g2e1u2g1v2c1w2g1s2e1q1e1y2e1u2e182e1s1g1r2e1t2e172c1w2f142e1r2g1v2e1r2c1j2e1u3g1h2e1s1e1x2c1w3e1l2e1q2g1s2e1t2c1x2e1s2g1r2e1u1f1l2c1w2g1v2e1s2f1j2e1r2e1l2e1s2g1g2e1r3g1j2c1u3e1t2e1p1e1s2e1t1c112e1s2g1a2e1s3g1d2c1u2g1q2e1r2g1k2e1t2e192e1u2g122e1u2e1j2c1u2f102e1r1g1l2e1t2e112e1u2e1w2e1u3g1q2c1u3f1u2e1q2f152e1s2c1l2e1t3e1w2e1t2f1s2c1w2e1v2e1r2e1l2e1s3e1s2e1u2g1k2e1r2e142c1u2f1e2e1s2g1v2e1s2e1x2e1t3e132e1t3f1a2c1t2e1s2e1r3e1y2e1u2e122e1r1g1q2e1s1g1h2c1w2f1t2e1s2f182e1t2e1g2e1r2g1v2e1t2g1r2c1t2e1l2e1p1g1f2e1s1e122e1u1g1q2e1u1g1z2c1v1g1t2e1r3g1w2e1s2e1v2e1u1g1r2e1u2g1e2c1v3g1z2e1r2e1h2e1s1e1v2e1u2e1f2e1t1g1i2c1w2e1s2e1q3f1f2e1t1c1e2e1r3f1j2e1t3g1d2c1v2f1h2e1q3e1e2e1s2e1d2e1r2g1w2e1t2e162c1v3e1r2e1q3e1d2e1r2e1u2e1u2g162e1u2f1d2c1v2g1w2e1q1f1t2e1u2d1c2e1t3e1r2e1u1g1s2c1w2g1x2e1s2g1d2e1u2c1a2e1r2f1y2e1u3f1t2c1v2g1f2e1q2g1q2e1u2c122e1t2f1k2e1s1g1u2c1u3f1t2e1r3g1x2e1t2c172e1s1g1f2e1r2g1u2c1v3g1l2e1q2g1z2e1u2c1j2e1t2g1y2e1t3e1c2c1w1f182e1r2f102e1t1e102e1s3f1s2e1t3e1r2c1u2g1t2e1q2g1t2e1u2e1t2e1s2g1p2e1s2e1t2c1u2g1f2e1r2g1h2e1t3e1y2e1r2g1f2e1r2g1r2c1u1f1s2e1p1g102e1t2c1w2e1t2g1g2e1t3e1x2c1t2e1z2e1s1g1j2e1s2d112e1t3e1d2e1u2g1i2c1u2e1r2e1p1f1r2e1t2e1l2e1t1f142e1u3e1m2c1t2f162e1q3e1d2e1t2e1v2e1t3g1r2e1u2e152c1v1g1u2e1p2e1t2e1u2c1j2e1s2g1t2e1t1e1k2c1v2e1z2e1r3e1d2e1t1c1w2e1u3e1u2e1t1e1u2c1u1e1s2e1r2f1r2e1r3c1m2e1t2g1c2e1s3e1m2c1w2g1t2e1r1e1l2e1u1d1x2e1s2e1u2e1u1e1i2c1u2g1w2e1p1e172e1u1d1f2e1r1g142e1r3e142c1v2g102e1r2g1w2e1s3e1v2e1r2f1w2e1u2g1r2c1w1e1r2e1s2e1j2e1r1c192e1s3f1d2e1t2g1j2c1w1g1t2e1q2g1h2e1r2d122e1s1g1r2e1s2e1v2c1v1f1y2e1r3g1f2e1t3e1t2e1s1g1d2e1t1f1f2c1v1g1s2e1s3e1w2e1u1c122e1t3f1c2e1u1g1t2c1v2e1m2e1p1e192e1r2e1c2e1t3f1f2e1u1e1x2c1v3g1d2e1r3f1d2e1t2c1q2e1t3g1k2e1u2e182c1v2g102e1q3g1t2e1s2c1v2e1s1g1c2e1r1f162c1v2f102e1r1g1y2e1s3c1w2e1t2e1r2e1s2g1d2c1v2e1t2e1p2f1f2e1r2e1j2e1u3e142e1t1e1j2c1t2g1i2e1s2f1s2e1s3c1f2e1t2g1r2e1t3g1r2c1w2e172e1r1g1u2e1r2c1v2e1u3e1u2e1u2g1s2c1v2g1v2e1r3f1f2e1u1e1w2e1u2e1w2e1u2f1y2c1v2e1l2e1r1e162e1u1d1j2e1u2g1f2e1s3f1j2c1w2g1t2e1s2g1l2e1t2d1y2e1t2g142e1u2e142c1v1e1a2e143e1v2f103c1y3e191g1r163g1f2f163g1t3e1a3c1w3g1a1g1g3e1l1e1l1c1j2e181d1e3f162e1u2e1v2e1u2f1p2e1u3g1x2c1u2g142e1s2g102e1t2e112e1s2e1q2e1u2g1v2c1v2e1v2e1r2e1x2e1s3d1y2e1u3e1o2e1u3g1h2c1u2e1z2e1q2e1g2e1s1c1k2e1s3e1x2e1w2e1v2c1w1f1r2e1r1e1i2e1s1d1z2e1t2e1k2e1w1g1v2c1v2e152e1s2e102e1s3c1g2e1u2e1p2e1u1f162c1w3e1g2e1q3f1b2e1u3d182e1s3f152e1u3f1e2c1u1f192e1q3f1x2e1s3d1b2e1s3e162e1u3f192c1w3g1b2e1q3f1a2e1s3d1a2e1s3f172e1w3f1v2c1u3f182e1q3e1e2e1s3d1b2e1t3g1b2e1u3f192c1u3f1k2e1q1f192e1u3e1e2e1s1f172e1w3e1q2c1u1f172e1r3e1k2e1s3d192e1s3f1c2e1u3f172c1u2e1z2e1q1e1m1e183d1m1g1j1g1d3e1k1f1m3d1t3d1f3g1d1f1d3g1h3d153f1l1e1g1f1j1f1g3c1a1e1f2f141g1e1f1j3c1f1e1g3f121f1j3g193d1e3f1s1g1k3e1e1e1d3d1u2f1m1e193e1e3f1c1c1r1g1f2g1h3g1f1e1s1d1r1g1m1g1k1g1r1g1f3d1m3f181e161e162f1d3d1f1e1m3e1d1f1i1f141e1e2e1g1e1b3f1e3f1f3c1k3e121e141g1m1f1h2c1u1g1q3f1d3g1a3g1k1d171f1k1e1d1e1f3f1s3c1e3f1s2g1j3e1f1e1w2c1j2e1s2e172e1v1g172c1v1e102e1q1e102e1s3e182e1s2e1d2e1w2g1v2c1u1g152e1r2e1x2e1u2e1r2e1s3g1p2e1w2e152c1w1e1t2e1s2g102e1t2e1d2e1t2e1d2e1w2g102c1v2g1t2e1r3g1e2e1s2e1y2e1t3e1u2e1v2g102c1w2e1h2e1r2f122e1u1e1v2e1u2e1q2e1w1g1h2c1u2g1s2e1r3e1v2e1u2e122e1t3e1d2e1w3e1z2c1u2g1e2e1s1e122e1t2e1e2e1r2g1q2e1v2e1z2c1u1e1t2e1p2e112e1t3c1j2e1s3g1d2e1w3g1l2c1u3e1y2e1r2e102e1t2d162e1t3e1d2e1u2f1h2c1u2g102e1r2e182e1u2d112e1s3e1u2e1w1e1h2c1u2f1s2e1s1e172e1r2c182e1r3f1i2e1v2g1h2c1v2f1k2e1p2e1u2e1u1c162e1u3e1d2e1w2g102c1w1g102e1r2e1e2e1s2e1e2e1u2e1v2e1t1g142c1w1g102e1r1g1j2e1u2c112e1t1e1d2e1v2e102c1w1g1x2e1q1g1v2e1u2e1m2e1t3f1r2e1w3g1h2c1u2e1w2e1r2e1l2e1u2c1v2e1u1e182e1u1g1k2c1v2e1s2e1s2e182e1s2e122e1t3g132e1w1g1t2c1t2g1f2e1q3f1v2e1u2e122e1u3g1h2e1w1e1s2c1u3f1v2e1s2e1w2e1t1c1y2e1t3e1s2e1v2f1x2c1v2e1h2e1q2e1m2e1t2e1l2e1s2g1w2e1u2e142c1u1e1y2e1q3e112e1s2c1t2e1u2g1x2e1w2e1i2c1u1g152e1s3g112e1s2c1y2e1t2g1v2e1v2g1l2c1v1e102e1s3g1v2e1t2c1u2e1t2g1q2e1w3g1u2c1v2g1h2e1s2g1t2e1s2c102e1t2e1h2e1v3g1e2c1w2f1b2e1q1g1v2e1s2c1u2e1t3f1q2e1v2g1a2c1v2g1y2e1q3e182e1t2d1x2e1u2g1v2e1u3f1i2c1v2g1y2e1r1g122e1t2e1h2e1s2g1h2e1v2g1i2c1u3e142e1s3g1u2e1t3e1v2e1t2e1v2e1t1g102c1u2f142e1r2g1u2e1t2e172e1r2g1d2e1w2g1w2c1w2g1s2e1s2e1k2e1t2d1q2e1s2e1s2e1v3g182c1v2e152e1r2e1j2e1t1c1m2e1s1e1e2e1v2g1g2c1v3e1x2e1r1f1l2e1u2e1f2e1u2g1k2e1t3g1h2c1v2g102e1q2g122e1u2e1w2e1u2e1x2e1v2g1t2c1v3g1t2e1s1f162e1r2e1t2e1u2g1q2e1v1g102c1v2e1v2e1q1f1m2e1t2e1l2e1s3g1p2e1u2e1x2c1v2e1u2e1q2e1v2e1u1d1u2e1u3e1i2e1t1e1s2c1u2e1w2e1r3e1y2e1t2c172e1s2g1y2e1w3e162c1u2f1l2e1s3e1x2e1s3d1x2e1s1e1d2e1w3g1l2c1w1e152e1s2g102e1s2c1x2e1t3e1s2e1w2g152c1u2e1v2e1s1e1y2e1u3c1t2e1s1e162e1v2g1e2c1t2e162e1r1f1j2e1t1e1q2e1s1e1i2e1u3e152c1v3e172e1q2f112e1u2c112e1s3g1p2e1w2g1w2c1u1e1t2e1r3g122e1s2d1w2e1t2g1f2e1w3g162c1v2e1e2e1p1g1y2e1t2d1d2e1u2e122e1v2f1t2c1t2g1v2e1q2g1f2e1s2d1j2e1t3g1t2e1v3f1l2c1u2g102e1r3g122e1s2d1h2e1s1g1h2e1u2e1f2c1t3e152e1r3g1f2e1s3c1f2e1t2g1h2e1v1g1f2c1w3g1y2e1r2g1a2e1t2e1u2e1r2g1w2e1v2g1e2c1u2e1z2e1r1f1v2e1t2e1z2e1t2f1r2e1v1f1u2c1v1g1d2e1r1g1v2e1u3e1h2e1t2e1r2e1t1g1w2c1u3g1w2e1r3e1w2e1r2e192e1u2f1o2e1v3g1l2c1u2g1z2e1r2g1v2e1u1e1s2e1s3f1r2e1w3f1g2c1w1f1y2e1r1e182e1t1d1d2e1s3e1r2e1v3e1d2c1t2g1f2e1p2f112e1s1d122e1s3e1o2e1u2g1q2c1v2e1z2e1q3f1j2e1r2c1j2e1s2e1p2e1v1g1j2c1u1e1z2e1p2f1u2e1u1c112e1s1g1v2e1t2f1z2c1u2f1s2e1r2e1w2e1t1c1q2e1u1e1p2e1u1g1z2c1v1g1z2e1r2g162e1s2e182e1t1g1v2e1u2e1t2c1t1e1h2e1q2g1k2e1s2d1t2e1s2e1c2e1w2f1r2c1u3g1g2e1p2g1v2e1r2e112e1t2g1e2e1w2e1f2c1t2e152e1p2e1d2e1u3c1r2e1s3e1o2e1v3e1t2c1v1e1t2e1s2f162e1s2e1x2e1r2g1c2e1v2f1u2c1w2g152e1s2g102e1r1c1u2e1s3g1h2e1v3g1t2c1v2f152e1s2f1q2e1u2c1w2e1s1f1c2e1v1f1s2c1v1e1z2e1r1g1h2e1u2d1v2e1t1g1r2e1v2g1t2c1w2g1z2e1r2f182e1r3c1q2e1s3g1j2e1u3e1e2c1w2g1z2e1r1e1w2e1u2d1b2e1s3g1w2e1u1g1t2c1v3g1e2e1q2e1b2e1t2e1s2e1t1g1q2e1v1g1t2c1v2g1r2e1q2e1h2e1t3d1w2e1t3e1q2e1v1e1h2c1w1f1s2e1s1e1f2e1t2e1u2e1r1e152e1v2e1y2c1u1e1s2e1s3f1h2e1u2e1q2e1r1g192e1v1e1s2c1u1g172e1r2f162e1s2c1s2e1s1g1v2e1v3g1x2c1v2g1t2e1r3e1q2e1t2d1d2e1r2g152e1v2g1f2c1t2g1z2e1q1f122e1s3c1u2e1s2g1j2e1t3e1z2c1u3g1t2e1s1g192e1r3d1y2e1t3g1c2e1u2g102c1u1g1u2e1q2f1u2e1r2e1v2e1r2g1v2e1v2g1i2c1w2e1f2e1p2e172e1r2c1d2e1s3f1q2e1w2g1s2c1v1g102e1s2e1h2e1u2d1u2e1t2f1h2e1w3g1j2c1v2g1r2e1p1g182e1t3c1u2e1t2g122e1v3g1t2c1t1e162e1s1f112e1u2c1u2e1t2e1t2e1w3g1e2c1w1g102e1s2e1w2g1r2c1v3g142e1r2g1l2e1u2e1v2e1u3e1w2e1u2e1q2c1w3f1j2e1s2g1m2e1s1e102e1u2e1q2e1w2g1i2c1u3e1y2e1s1e1h2e1u1c1u2e1t3g132e1v2g1t2c1w2e1x2e1s2g1t2e1t2e1r2e1t2g1r2e1u2g1q2c1w2g1w2e1s1e1z2e1u2e1y2e1t2e1e2e1w1f1s2c1u1e1e2e1s2e1v2e1s2e1d2e1t2e1r2e1w3g1t2c1w2e1j2e1r1g122e1t1c1h2e1t1g1j2e1v1g1s2c1w2g1s2e1s2e1r2e1u2e1j2e1r1g1k2e1w2f1v2c1w2e102e1p3f1t2e1s2e1m2e1s1g152e1v3g1m2c1v2f1r2e1r1e1l2e1u2e162e1s3e1u2e1w2e1t2c1u2e1f2e1q1e1h2e1s3c1h2e1u2g1r2e1v2g1v2c1v2g1r2e1q3g1l2e1s1e1h2e1u3e1d2e1v3e1m2c1w1e1x2e1s2e122e1t3e1h2e1u2g1k2e1w2e1x2c1u1g1y2e1s3f1f2e1s1e1t2e1r1f1q2e1w1g1j2c1w2f1y2e1q1e1h2e1t3c1x2e1t1f1q2e1w2g1v2c1w3e1s2e1s2g1t2e1u2e1h2e1u2e1q2e1v2e1r2c1w2g1x2e1q2g1t2e1r1c102e1u1e1s2e1u2g1w2c1w1e1w2e1q2g1v2e1u1c1x2e1u1e1w2e1w2e1t2c1w2e1e2e1s2g1s2e1s2c1x2e1t2f142e1v1g1f2c1v2g1x2e1q2f1y2e1t1e1l2e1s2g1p2e1v2g142c1w2g1x2e1s2g1h2e1u1e1j2e1u2g1q2e1v3e1y2c1v2f1f2e1r2e1r2e1s1c1d2e1u1e1y2e1u1g1s2c1w2g1m2e1r2e122e1r2c1l2e1u2g1d2e1u2f1f2c1w3e1r2e1s2g1v2e1t1c1t2e1t2e1a2e1w1g1q2c1w2g1e2e1r2e1f2e1t1d1l2e1t3e1y2e1w1g1k2c1v1g1h2e1s1g1j2e1s1e172e1s2g1d2e1v1e1s2c1w2e1x2e1r1g102e1t2e1e2e1t2g1q2e1w3g1c2c1u1g162e1s2g122e1u2c1y2e1s1g1e2e1w1g1h2c1v2g1e2e1r3g102e1u1e102e1u1g1y2e1v2g162c1v3e1r2e1q2e102e1t1d1z2e1u3g1w2e1v3g102c1w2e1t2e1r2g1w2e1s2e1v2e1t2g1j2e1v3e142c1v2g1s2e1s1g1m2e1t2e1h2e1t2e1p2e1u2e1h2c1w3g1t2e1s1g1r2e1r1c1e2e1s3e1p2e1w2e1f2c1w1g1j2e1p2g1v2e1t2c162e1r3g122e1t2f1r2c1w1g1x2e1s1g1y2e1u3c1g2e1t3g1q2e1v3e1f2c1w1f102e1s2g102e1u1c1l2e1t3e1t2e1w1e102c1w2g1f2e1r1g1l2e1s2e112e1u2g1s2e1w1g142c1u1e1f2e1q2e1i2e1s1c1l2e1s3e1b2e1u1e1q2c1v2e1v2e1q1e1w2e1t2c1w2e1t2e1y2e1u2g102c1w3e142e1q2f1l2e1u3c1v2e1s3f1f2e1u1e1q2c1u2e1v2e1s2g1z2e1s1d172e1u3g1h2e1w1f1q2c1v3f1t2e1q3g102e1s1d1z2e1u2e1q2e1t1e1y2c1v2e1z2e1p2e1d2e1u1d1u2e1s2f132e1v3g1u2c1t2e1r2e1r2g1z2e1u1e1e2e1t3g1f2e1v1e1t2c1w2g1e2e1r3g1m2e1u3c1h2e1u2f132e1t3g1f2c1t2g1u2e1r2e102e1s1e102e1s1e142e1v1g1f2c1v3g1f2e1p1g1z2e1s3e1e2e1u1f1i2e1t3f1e2c1u1f1t2e1s3e1f2e1t3e1s2e1t1f1c2e1v3g1e2c1u3g182e1r3f102e1s2d1u2e1u1g1k2e1v3g1m2c1w1g152e1r2g1u2e1s3e102e1u2e1k2e1u1f1f2c1w3g1f2e1q3g102e1u2e1t2e1u1g1u2e1w3e1r2c1u1f182e1r3f112e1s2e1l2e1s2f1p2e1v2f1d2c1t1e1v2e1q2f1f2e1r3d1f2e1r2g1p2e1u3f1y2c1u3f1m2e1s2g1f2e1t1e1t2e1t3g182e1u2f1r2c1u1g1z2e1q3g1u2e1u2d112e1t2g1x2e1u2f1h2c1v2g1g2e1p3g1z2e1s2e1h2e1u1e1v2e1v1g1e2c1v2g1f2e1r2g1f2e1r2d1y2e1s2g1d2e1v1e1r2c1u1f1u2e1s1f1w2e1t1e1f2e1t3g1v2e1u2g1r2c1u2g1h2e1q2g1h2e1u2c1r2e1u1g1w2e1v2e1s2c1v2e1e2e1s1g1t2e1s2e1t2e1s1g1w2e1v3g1z2c1w3e1s2e1s2g1s2e1t1e102e1u2e162e1w2f1a2c1u3g1q2e1q1g1j2e1s1c1w2e1s1g1w2e1u1g1j2c1w2g1v2e1r2f102e1s2c1w2e1t3g1w2e1v2g1r2c1w3g1u2e1q2g102e1t3c192e1t3e122e1v3f1j2c1u2g1d2e1r3g1t2e1u1d1v2e1t2e1b2e1t2e1r2c1v2f1t2e1s3e1u2e1t2c1t2e1u1g1p2e1v1f1x2c1u2e1y2e1s2e182e1u2e1s2e1t3e142e1u3f1y2c1u2g1k2e1r2g172e1t1c1w2e1s1f1p2e1u2g162c1v1f1y2e1q3g1e2e1t2e1h2e1s2g1b2e1v1f1u2c1v2f1r2e1q2f192e1t2c1t2e1s2g1s2e1v2g1e2c1w1g1q2e1s3f1h2e1u2c182e1r3e1w2e1w2g1c2c1v2g1r2e1p1e1d2e1t2e1w2e1s3e1o2e1v2g1c2c1u2g142e1r2g1k2e1s2e1t2e1u1f1p2e1v2g1a2c1w1f1d2e1r1g1t2e1t3e1c2e1s2f1p2e1u1g1z2c1u3g1y2e1p1g1r2e1t2c1z2e1t1g1p2e1w2g1q2c1u1g1t2e1p1e122e1s2e1f2e1s2g1p2e1u1g1y2c1v2g1z2e1s3e1u2e1u2e1s2e1t1g1w2e1w2e1k2c1v2e1y2e1q2g1u2e1t2c1c2e1u2e132e1w3g1v2c1u2e1f2e1s2g122e1t1e1t2e1u2g1r2e1w2g1y2c1t1g1u2e1s2g1k2e1t2c1g2e1u2e1s2e1v3g102c1u1e1k2e1r1e122e1s1c1v3e1z2e1s3g1h2e1s1e1l2e1s1e1w2e1w2e162c1u2f1t2e1q1e1b2e1u2d102e1u2g1k2e1w1e1x2c1v2e1r2e1p2g1v2e1u2d102e1r1e1w2e1w1g1l2c1w1g1h2e1r1e1j2e1u2c172e1u2g1r2e1v2g1t2c1u2f172e1s2e102e1u1c1j2e1s2e1j2e1w1g1w2c1w2f1f2e1s2f1l2e1t1c1a2e1u3e132e1t2g1j2c1w2e1y2e1r1e112e1s1e1q2e1t2g122e1w1g152c1w1g1l2e1s1e1t2e1s2c1u2e1r2e1x2e1w2g1f2c1v2f1z2e1r2f1h2e1t1e192e1u1f1a2e1w3e1z2c1u1g102e1r1g1z2e1t3e1v2e1u1e1i2e1u1e1v2c1v2e172e1s3g1r2e1t2d1v2e1t2f1q2e1w3e1w2c1u3g1m2e1r3g1u2e1t2c1c2e1t3g1x2e1v3e1r2c1w3g1s2e1r3e1h2e1u1d1y2e1u2g132e1w2e1z2c1v1e1z2e1q2g1z2e1u2c1t2e1u2e1j2e1v3g1f2c1u2e102e1r1e1v2e1u3e1x2e1t1g1e2e1t2g1k2c1v1e1y2e1s1e1z2e1t2c1v2e1u2e1w2e1v2f1t2c1t1g1m2e1s2e1z2e1t1e1v2e1u3g1r2e1u2e102c1w2g102e1r2e112e1r1e1v2e1t2e1b2e1t2f1s2c1u2f1h2e1r2e1u2e1u2c1f2e1u2f1j2e1w2e102c1u1g1r2e1s2g172e1s3e1u2e1s1g1y2e1v1g1i2c1v1f1t2e1s1f182e1u1d1a2e1u3e1p2e1w1f182c1t1g1v2e1s1g1x2e1t1e1a2e1u1f1j2e1w3e1k2c1u2f1s2e1q1e102e1t2d112e1u2g1t2e1w3e1s2c1w1f1h2e1s2f1s2e1u1c1v2e1s3g1q2e1v2g1k2c1v1e102e1r2f102e1s2e1l2e1t1e1r2e1v2f1v2c1v2e1l2e1s2g1l2e1u2c102e1u2g1p2e1w3e1u2c1w1g142e1q2e1z2e1t2e1d2e1u1g1y2e1w1g1h2c1u3e1d2e1r2f1v2e1t1c112e1s1e122e1v3g1h2c1w2e1u2e1s1g1y2e1u2e1f2e1u1e1x2e1v2e1l2c1u1g172e1q1g1j2e1s2d1u2e1t2g1v2e1v1e1w2c1v2g1x2e1q2e1z2e1s1e172e1s2f1y2e1v1g1s2c1v2g162e1q2g102e1s2c162e1s2g1c2e1v2f1l2c1v3e1u2e1p2e1t2e1t2c1s2e1u1g1r2e1w2e1l2c1w2f1z2e1s2e1v2e1u2e1u2e1r2g1j2e1u2g1z2c1t2g1h2e1s2e1g2e1u2c1q2e1s2e1b2e1v2g102c1v1g1i2e1p2e1w2e1s2c1l2e1u2e1y2e1v3g1y2c1v1f1j2e1r3e1y2e1u2e162e1s1f1q2e1u2e1r2c1u1e1x2e1q2e1s2e1u2d1y2e1t2e1j2e1w3e1l2c1w1e182e1r2g1k2e1t2d1q2e1s2g122e1w2g1w2c1w1g162e1q1e1h2e1s2c1k2e1s1e1j2e1u3e1f2c1v2f1a2e1s2g182e1s1c1g2e1t1f1j2e1v2e102c1v1e1z2e1q2g162e1s3e1x2e1u1g1v2e1w3e1t2c1w2g1t2e1p2e1u2e1u2e1v2e1u2f192e1u1e1f2c1w2g1t2e1r2g1v2e1s1e1v2e1t1e1x2e1u1g1t2c1v1g1t2e1q2e1j2e1r3e1y2e1u3e1x2e1v2e1t2c1v1g1y2e1r2g1y2e1t2e1w2e1u2f1p2e1u1e1c2c1v3g1a2e1r1g1d2e1s1e1t2e1u1g1e2e1v2e182c1v2g1d2e1r3e192e1t3c1k2e1u1g1d2e1u2g1d2c1w2g1e2e1s2g162e1t3e1h2e1u3e152e1t2e1h2c1u1f1t2e1r2e1z2e1u3e122e1t3f1r2e1t2f142c1v3g1d2e1p3e1t2e1u1c1g2e1s2e1g2e1w2f1e2c1u3e1l2e1r3f192e1t1e1d2e1u3g1r2e1t2f1l2c1v2g142e1r2g1v2e1s2c1v2e1u1g1x2e1u1g162c1u3f1f2e1p1f182e1t1c1d2e1t2g1i2e1w2f1x2c1w2e1f2e1r1e182e1t3d1j2e1u2e1d2e1u2g1f2c1v2g182e1p2g1z2e1t2e1v2e1s2f1s2e1w2e1z2c1w1g152e1s2g1f2e1s1e1q2e1u1g1f2e1w2e1g2c1v2g1r2e1p1e1g2e1u2c1j2e1u2g1p2e1u2g1i2c1u2g1j2e1q2f1r2e1r2c1t2e1t3e1p2e1u3e1z2c1t2f1h2e1q2g1j2e1r2c172e1s1g1q2e1t3g1e2c1u2g1j2e1r2f1m2e1t2c122e1s2g1s2e1v2e102c1v1f1u2e1r2f1s2e1r1c112e1r2e1q2e1u3e1l2c1w3e1e2e1r3e1q2e1u3e1z2e1u2f122e1w1g1e2c1v2g102e1r3e192e1r2d1k2e1t2e1q2e1u2e1w2c1w2g1f2e1r3e122e1t2e1h2e1u1e1v2e1v2g1h2c1t1g152e1s2g1d2e1r2c1u2e1u1g162e1u3e182c1v1g1t2e1r1e172e1t3c1w2e1u2e122e1w2g1h2c1u3f1f2e1q3f192e1r2e172e1t2g1x2e1u1g1d2c1v1f1s2e1r1g1t2e1r1d1v2e1t2g1a2e1u1g1a2c1w3g1t2e1q1f1t2e1s1d1z2e1u2g1q2e1v2f1h2c1u2g1u2e1q1e102e1u3c1h2e1t1e1q2e1v3g1u2c1v2f1t2e1q3g1t2e1u1e1r2e1s1g1u2e1u1f1t2c1v3g1x2e1r2f122e1s1d1j2e1r2g182e1v3e1z2c1v1f1z2e1q1e1d2e1t2e1m2e1u2g1v2e1w2e1f2c1v1e182e1r3f1h2e1s2e112e1r1g1f2e1w1g1f2c1w1e152e1q1g1i2e1u2e192e1u1g1r2e1w3f1u2c1t3g1e2e1q2g1j2e1t2d1r2e1t2e1y2e1u3g1u2c1v2e1c2e1s1g1j2e1t1d1u2e1u1g1f2e1u2e1h2c1v2e1t2e1r3e1l2e1t2d102e1s2g1f2e1u3e1r2c1w2e1m2e1q1g1l2e1u2d1v2e1u2g1r2e1w2e142c1u1g1z2e1q1f1s2e1s3e102e1s3e1q2e1z2e192c182e141e1j1r1g1c1e1i2g141g1e3e1j1f1e3g121f1i1g1j1e1v2e1i1g1u2e1r1g1g2c1w1e1u2e1r2e1k2e1u2c182e1s2g1k2e1s1f192c1w2g1m2e1s1g1x2e1s2e102e1s3f1y2e1s3e1w2c1u1f1k2e1p2g1v2e1t3e1i2e1s2e1s2e1s1f1r2c1v2g1t2e1q2e1w2e1s2e1g2e1u1e1x2e1s3e1r2c1w2e142e1q2g1m2e1u1c1m2e1u3e1f2e1u3f1z2c1u3e1z2e1r1f1u2e1s1d192e1t3e142e1s1f182c1w3f182e1q3f172e1s3c1d2e1s3f152e1u3g1t2c1u1f192e1q3f1e2e1s3d192e1s3g142e1s1f192c1u3f1g2e1q3f172e1u3d162e1s2f172e1s3f1z2c1u3f192e1q3f1w2e1s3d1b2e1t3f1c2e1s3f172c1u3e1e2e1q3f182e1t3d1b2e1s1f152e1t3e192c1u3f172e1q3f192e1s2c1w2e1s2e1u1e1f1e123c181e1k3g193e141e121d161g1s2e193e1q1e183c1e1e1g3g121f1h3g191d1e3f1s1g1k3e1d1e1f3d1u2f1m1e193e1d3g1c3c1r1g1f1g1a3g1f1e1s1d1e3e1d1f141g1s1f1b1d1l3f1f3g1e3f1g2e1f1c1s3f1c3f1h3f183f142c1c1e1f3f1d3f183g1f3d1r3e121f123e1e1e1d3d1u3f1i1f1d3f1m1g1d1c163e1s3f1k3e181e1t3c1e3g1g1g1g3f171g1e3c1q1e1f1e1d2e1s1f1f3d1r1g1f3e1i1f1m3e121c1w2g1y2e1s1e1l2e1s1e1j2e1s1g1f2e1t2e162c1w1e1r2e1s2g102e1u2c1j2e1s1g1j2e1t3g162c1w2e1s2e1r1g1x2e1s1c1t2e1s1g1y2e1t2e1m2c1w2e1l2e1r2g1u2e1u1e1c2e1u1e1y2e1s2f1i2c1w2g1f2e1r2g1r2e1u2e172e1t1g1k2e1t3g1m2c1w2e1s2e1r2e152e1u2e102e1s2g162e1s3e1a2c1w3e1m2e1p1g1h2e1t3c1v2e1u3e1f2e1u3e1d2c1u2e1r2e1q3g1t2e1s2e1v2e1r2g1p2e1u2g1t2c1w2g142e1s2g1h2e1u1c192e1t3g1d2e1u1e172c1u3e1f2e1s2e162e1u2d182e1u2g1s2e1t2f1r2c1w2e1f2e1r2e102e1t2c182e1t2g1j2e1s1g1m2c1w2e1q2e1r2f1s2e1u1e1z2e1s1e1w2e1t1e102c1v1e1j2e1s1g102e1t1c1r2e1s1f1f2e1s2e1s2c1u2g1f2e1p3e1y2e1t2e1v2e1t3g1p2e1u2e1t2c1v1g1z2e1s2g1t2e1u2c1l2e1t2g1u2e1s1e1v2c1w2g1f2e1q1e152e1t1c1v2e1t1e1t2e1u2g1z2c1t3e1r2e1q2e1s2e1u2c1v2e1s1g1t2e1s1g1u2c1w2e1h2e1r2e102e1t3c122e1s3g1r2e1u2e102c1w2e1s2e1s3g1l2e1s2e1v2e1u3e1y2e1t3e1l2c1v3e1w2e1q2e1s2e1u2e1h2e1t3e1s2e1u1g1h2c1u2e1t2e1r2g1h2e1s2e1j2e1u1e142e1u2g1h2c1w2g1q2e1s2g1j2e1s2e102e1u2g132e1t2g1h2c1w2g102e1q2g1v2e1u2c1q2e1u3e1h2e1u2e102c1v2g1c2e1s1f102e1t1e1u2e1t2g132e1u1g1r2c1w1f1t2e1q1g1s2e1u2d172e1s3f1x2e1s2e1u2c1w1f1w2e1s1f102e1s2e102e1s3e142e1t3f1h2c1v3g1e2e1q1g1u2e1u1c1k2e1u3g1o2e1t3e1e2c1u1g162e1r3g152e1u3d1t2e1t1e1w2e1u2g152c1w2f1z2e1s3f1h2e1t1c1l2e1u2e1q2e1u3g1i2c1v1e1f2e1r2e1f2e1u2e102e1s3e1f2e1s2g1z2c1w2g162e1r3g102e1s2e1t2e1u2g1f2e1u1g102c1u1g1i2e1r3e1s2e1t2e112e1s2g1x2e1s2e182c1v2g1j2e1r2e1h2e1t1e1h2e1t2g1f2e1r2g1s2c1t2e1f2e1r2g1j2e1t1e122e1s3e1w2e1t3e1l2c1w1g1t2e1r3g1i2e1t2c102e1s2g1h2e1s1g1s2c1u1e1d2e1q2f1l2e1t2e1u2e1t2g1s2e1u2e1h2c1w2f1t2e1q1e1h2e1u2d1w2e1r3e1h2e1u3e102c1w2f1u2e1q2g102e1s1c1t2e1u3e1i2e1u2e1s2c1v2e1i2e1s3g1r2e1u1c1v2e1s2g1k2e1u2g102c1v2e1u2e1r2g152e1s1c182e1s2g1r2e1u3g1x2c1v2e1v2e1q2f1q2e1u2c122e1t1f1o2e1u2g172c1w2g1x2e1s2g162e1u2d1e2e1t1g1u2e1s3e152c1v2e1g2e1q3g1t2e1t2c172e1t3g1d2e1u3g1r2c1w2g1c2e1p2f1j2e1s1e1d2e1s2g1x2e1t3g1w2c1w2e1c2e1q3g1v2e1u1e172e1u2e1r2e1r1e1e2c1v2e1z2e1p3e1v2e1t1e1u2e1t2f1w2e1s3f182c1u1e162e1r2g1t2e1s1d122e1s2f172e1r2g1f2c1u2e172e1s1g1f2e1t3e1h2e1t3g172e1t2e1c2c1w2e1e2e1p1g102e1s3c1d2e1r2f1c2e1s1e1u2c1v3f1r2e1r3e1s2e1t3e1w2e1s1g1c2e1u2g1z2c1v2f162e1p1e1h2e1t1e1d2e1t3g1b2e1t2e1d2c1u3f1t2e1q1g1f2e1u1e112e1s1g1r2e1u2g1k2c1w2f1f2e1s1e142e1r2d1k2e1r2g142e1r3g1l2c1v2g1c2e1p1f1f2e1s1e1f2e1t3e1j2e1t2g172c1w2g1d2e1s2f182e1u2d1f2e1t3e1u2e1s1g1h2c1u2g1d2e1r2e1t2e1r2d1e2e1r2g1f2e1u3e162c1u2f1q2e1s2e1r2e1s2e102e1s1e1x2e1t2g1t2c1v3g1m2e1r2f1i2e1t3c122e1t3g1q2e1t2g1t2c1u1g1m2e1p3g1i2e1t3e1v2e1t1g1g2e1u1g1z2c1v1g1k2e1q1e1r2e1s3e1u2e1s2f122e1t1e172c1v2g1z2e1s3e1w2e1s2e1w2e1r1g1t2e1s2g1a2c1u2g1t2e1s2g1t2e1t2e1h2e1t2f1s2e1r2f142c1v3f1d2e1p3e1q2e1u2c1a2e1t1g1k2e1t3g1w2c1u2g1r2e1s3e1s2e1s2d172e1s2f162e1s2e1u2c1u2f1d2e1p3f1f2e1r2e1z2e1s2f1r2e1s2g1s2c1w2f162e1r2g1t2e1s2e1v2e1u1f1o2e1u3f1y2c1w1g1r2e1r2g1h2e1s1c1v2e1t1g1s2e1u2e152c1v1g1y2e1q3f1f2e1t2e1y2e1s1e162e1s1f182c1w2g182e1s3f1s2e1t1e1d2e1r1g1a2e1s1f1x2c1v1f1t2e1q3g1r2e1t2c1v2e1r2f1y2e1r2g1l2c1v3e1q2e1r3g1s2e1u3c1j2e1s2e1p2e1s1g1l2c1w1e162e1r3f1t2e1t3e1u2e1t3g1j2e1s3g1z2c1v2g1r2e1s1g1q2e1s3d1u2e1u3f1j2e1t2f1d2c1u2g1e2e1r3g1t2e1t3d1q2e1t2g152e1u2g1f2c1w2f162e1s2f1b2e1r3d112e1t1g1u2e1t1e1h2c1w2g1t2e1q2g1u2e1r2d1a2e1t3g1f2e1s2g1h2c1v1e152e1r2g142e1u3c1y2e1s2g1s2e1r1g1v2c1u2g182e1s3e1k2e1t2e1u2e1u2e1r2e1s1g1s2c1v2e1y2e1s2e1t2e1u2c1l2e1s2g1e2e1s3e102c1v1e1g2e1q2g1y2e1t1c182e1u1g1j2e1s2g1m2c1t2g1q2e1r2f102e1u3d1q2e1u3f123e1r2e1u2d1h2e1u1f1u2e1u3f1z2c1w2g1y2e1r3e1f2e1t2c1w2e1u2e1k2e1u2g1f2c1u1g1y2e1s3e142e1u2e1z2e1u2g1d2e1u2g1k2c1w2g1t2e1r1f1i2e1s3c1z2e1u1e1j2e1u3e1r2c1v1g1x2e1r1e1q2e1s2e1t2e1u1e1y2e1t2g1l2c1w2g1w2e1s2e1x2e1t3e1l2e1t2e132e1s2g1q2c1v1g1w2e1s2e1q2e1t2e1g2e1u2g1x2e1u3e1f2c1w2e1z2e1r2g1z2e1t2c1v2e1u2e1p2e1r1g1r2c1u2e1x2e1s1e1i2e1r2d1y2e1s1e1h2e1u3g1x2c1v2e1f2e1q2g1z2e1u1c1w2e1s2e1o2e1u1e102c1t3g1z2e1r2f1y2e1t2e102e1u2g122e1s3f1z2c1u1g102e1r3e1g2e1s1e1l2e1s1e1p2e1u3g1t2c1u2f1j2e1s1g1f2e1u1c102e1s3g1w2e1s1g182c1v1g1j2e1r1g102e1r1e1v2e1u2g1u2e1s2g172c1v1e1j2e1r2g1u2e1u1c122e1u3e1r2e1u2f1u2c1u3e1k2e1q2e1s2e1u2e1v2e1t3g1h2e1s1g1k2c1u2f1t2e1s3g1t2e1u2e1l2e1r2e122e1u1f1f2c1u2g1d2e1r2e1t2e1u2e1l2e1r2g1y2e1u2f1c2c1u2e1r2e1s2e1q2e1s2c1q2e1r2g1q2e1s3e1w2c1w2g152e1s2e1t2e1u2e102e1s2f1y2e1t2g1a2c1w2e1t2e1s2g1s2e1t2e1u2e1t2g1q2e1t3e1m2c1u2e1s2e1r1f162e1t1c1v2e1u1g1h2e1u2f1f2c1v2g1t2e1r1e1f2e1t1c1w2e1u1e1x2e1t2e1y2c1u1e1x2e1r2g1u2e1s2c1x2e1u1g1y2e1u2g1g2c1t2e1f2e1r2e1i2e1t2e102e1u1e162e1t1f1m2c1u1f1l2e1r1e1w2e1u1c1v2e1t1e1e2e1s1g152c1u1g1f2e1s3g1w2e1t1c1s2e1u3f1j2e1t3e1e2c1v2g1f2e1r1f1t2e1t1e1z2e1s2e1j2e1t2g1t2c1w1e1f2e1s1e1w2e1r2c1x2e1t2g1v2e1t2e1y2c1v2e1t2e1s1g152e1s2e1w2e1s1e1e2e1t1e1t2c1u2e1y2e1r1e1t2e1t2e1f2e1u1e1u2e1s3e1y2c1v2e152e1s1e1s2e1t2e1s2e1t1g1e2e1t2f1c2c1w1e1s2e1s2g1m2e1t1e1l2e1s2g1u2e1u3g1e2c1w2g1f2e1q1g1t2e1u1e1i2e1t2g1w2e1s2g1z2c1u2f142e1p2e1x2e1u3e1w2e1u2g1o2e1u3e1y2c1u2f1d2e1r1e1t2e1s3e1z2e1u2g1r2e1t2g1d2c1v2f1j2e1p2e1i2e1s1c1s2e1t2e1b2e1u2g1m2c1v2e102e1s2e1j2e1s1c192e1u3e122e1u3e1x2c1w2e1y2e1q1g1s2e1u2c112e1s1e1s2e1s3e1h2c1w3e1y2e1s2f1u2e1s2e102e1s1e1k2e1u3e1i2c1w1e1t2e1s2f1x2e1u2c1f2e1s2e1f2e1u2g182c1u3e1s2e1s1e1i2e1t3c1e2e1t2e1x2e1t2f1j2c1w3f142e1s2g1f2e1r2c102e1s2g1f2e1r1g1z2c1v3f162e1r2e1y2e1t1e1h2e1t2g122e1t1f1i2c1u1f1r2e1p2f1f2e1t3d1u2e1r1e1a2e1s1e1x2c1w1g1f2e1r2e1v2e1u1e1z2e1s2g1w2e1u1g1d2c1u2f162e1r1e172e1s3e1e2e1u1f152e1s1e162c1v2g1s2e1r3f1s2e1r2c1l2e1r2f1p2e1u2g152c1w1g1q2e1p2e1s2e1r3e1d2e1s3f1p2e1t2g1r2c1v1e1f2e1s3f1d2e1u1e112e1t2g1b2e1t3f1f2c1w3e1x2e1p1f1d2e1u2e1l2e1s3g1p2e1t2g1t2c1w2g1e2e1s1e142e1s2e1e2e1t3e1h2e1t2f1c2c1w2e1u2e1q3e142e1s2c1d2e1r1g1b2e1u1g1h2c1u3g152e1q2g1d2e1t2e1f2e1u2f1r2e1t1f1u2c1w2g1l2e1r2e1r2e1t1c1w2e1u2e1w2e1u2g1f2c1u1f102e1r3g1t2e1r2d1r2e1r2g1d2e1r1g1d2c1w2e1h2e1q2f1e2e1r1c1v2e1t2f1y2e1s2g1q2c1v2g1g2e1s1g1g2e1r3d182e1u1g1s2e1u2g1i2c1u1g1s2e1p3g1g2e1t3e1t2e1r2f1e2e1u1g1i2c1u2e1u2e1s1g1x2e1t2e1t2e1u2g1s2e1s1g1r2c1v2g182e1s2f1q2e1s2c1r2e1u3e1g2e1t2g1t2c1w2e1r2e1q1f1y2e1s2c1a2e1t2f1p2e1t2f1r2c1v2g1r2e1r2g152e1u1e1t2e1t2e1t2e1t2g1u2c1w2g182e1s2e1y2e1t1d102e1s1f1d2e1u2e182c1v3g1m2e1r3f1x2e1r1e1f2e1s1g1w2e1u1g1e2c1u2e1t2e1q2e152e1s3e1v2e1u2e122e1u3e1d2c1u1e1x2e1r1e1f2e1r3e1t2e1u2f1w2e1t3g1f2c1w2e1s2e1r1g1y2e1s3d1f2e1r1f142e1s3f1l2c1w2f162e1s2e1d2e1t2c182e1u2g1d2e1t3g1e2c1w1f162e1r3g1d2e1t1c182e1t2f132e1t3g1e2c1v2g1v2e1r1g1g2e1s1e1e2e1t3e1h2e1u2g1t2c1v3g1e2e1q3e1r2e1s3e1f2e1t2g192e1s1f182c1v3f1z2e1q2g1j2e1s2d1t2e1t2f1b2e1r1e1v2c1v2g1d2e1q2f1l2e1s3e1e2e1t1f1s2e1u2g1l2c1v2e1r2e1r1e1u2e1u2c102e1t1g1p2e1r1f1x2c1w2g1q2e1q3e1t2e1s2e1u2e1t2g1o2e1t3g1g2c1u2f1d2e1r2g182e1u2d1s2e1s2e1k2e1u3e1i2c1v2g1t2e1s2e1r2e1s1c1b2e1u2g1s2e1u2e1u2c1w3e1w2e1r2g1f2e1r2c1f2e1t2e1s2e1s2e1s2c1u2f1g2e1r2g1k2e1u2e1u2e1u3g1o2e1r2e1t2c1w1g1y2e1s2g1w2e1s2e1v2e1t1e122e1s2f1v1c1a2e1u3e1v2e1t1e1b2c1u2e1b2e1r1e102e1u2e1x2e1u2e132e1u2e1x2c1v3e162e1r1g1z2e1u1c1q2e1u1e1h2e1t2e1k2c1t2f1h2e1s1e102e1t2e112e1t2g1r2e1u2e1l2c1w1e1s2e1s2g1z2e1s2e1x2e1t1g1y2e1u3e1h2c1w2g1w2e1r3e1u2e1t2c1s2e1t1g1q2e1s3g1w2c1w2f1r2e1s2g1h2e1u2c1q2e1t1g1u2e1t2e1f2c1w2f1v2e1r2e1l2e1t2e1l2e1u1g1q2e1u3f1s2c1w2g1f2e1s2g1u2e1r2c1j2e1s3g1t2e1s2g152c1u2e102e1q2g1r2e1u2d1u2e1t1e1d2e1s3e1h2c1u3e1h2e1s2g142e1t3e1q2e1s1g1w2e1u2e1w2c1u3e1y2e1r2e1y2e1t2e1x2e1t2f1g2e1t3e1h2c1u2e1y2e1s2e1y2e1u1c1r2e1t3e1d2e1u3e152c1v2g1h2e1r1g1t2e1u1e112e1t2g1p2e1u2e1z2c1t1g152e1r2f1h2e1r2e1v2e1u2e1v2e1u2e1v2c1v1f1s2e1q1e1s2e1u1c1r2e1t3e1p2e1s3g1j2c1w1g1s2e1s2g1x2e1s1c112e1u3e142e1u1g1m2c1w2e1g2e1s2g1t2e1u2e1q2e1t2e1p2e1u2g1j2c1u3e1w2e1p3f1s2e1u2c122e1u2e1x2e1t3g1t2c1t1g1y2e1s2e1t2e1t2c1c2e1u2f1p2e1u3e1y2c1u2g1t2e1s1e1f2e1t2c1v2e1u1g1w2e1t2g172c1v2f1l2e1s2g1u2e1t2e1q2e1t2g1h2e1t2f172c1w1e1x2e1q2g1s2e1s2e1x2e1s2g1d2e1u2e1t2c1v2g102e1r1g1j2e1u2e1j2e1t2g1h2e1u2f1s2c1v3e1t2e1q2g1s2e1r2e1q2e1r2g1r2e1t3e102c1u3f1d2e1s1g1l2e1u2e1h2e1u3f1o2e1u3g1w2c1w2g1r2e1s2e1u2e1s2c1h2e1s2g1d2e1u3e1x2c1v2g1h2e1r1g1u2e1t1e1j2e1s2f1y2e1s2f142c1v1g102e1r1e1f2e1t2c1x2e1u2g1o2e1t1g1u2c1v1g102e1s1g1w2e1t2d1j2e1s1e1t2e1t3e1v2c1w2g1z2e1r2e1l2e1u1e1u2e1s2g1f2e1u2e1i2c1v2e1l2e1r2g1f2e1u3c192e1t2g1x2e1t3g1u2c1w2g142e1s2e1m2e1u2c1d2e1t2f1v2e1s1g1j2c1v2f1l2e1q3e1t2e1u1c1j2e1t2e1w2e1t3g1g2c1w3e1j2e1s1e192e1t2e1j2e1t2e1s2e1s1e1s2c1w2f1d2e1r1g1g2e1t2e1a2e1s3e1r2e1t3e102c1v3g1s2e1s1g1m2e1t1e1q2e1u1e142e1t2g1k2c1w2e1f2e1r2g1v2e1u1c1w2e1s2e122e1u2f1s2c1v2f1u2e1r2e1l2e1u1c1y2e1t3e162e1s2e1r2c1w2e1r2e1r3e152e1u2d1q2e1s1e152e1u3e162c1w3e1z2e1s3e102e1s1c1t2e1s3e172e1t1e1z2c1w2e1q2e1r3f1t2e1s2c1u2e1u2g1w2e1s1g1v2c1u1g1j2e1s3e1j2e1s2c1v2e1t2g1p2e1r2g162c1w1g1y2e1r1g1a2e1r1e1l2e1t2g1y2e1t2g1i2c1v1g1f2e1s2f1t2e1t1e1x2e1t2g1p2e1u2g1z2c1v2f162e1p3e1l2e1s3e1s2e1s3e1a2e1u3g1z2c1v1e1u2e1s3f192e1s3e1f2e1s2f1p2e1r2f1h2c1w1e1y2e1q3f1r2e1t2e1h2e1s2g1r2e1t3g1d2c1u1f152e1q2f1e2e1s2e1q2e1t2g1a2e1u2e1f2c1v3g1e2e1r1g1m2e1u2c1a2e1r2e1d2e1u1g1s2c1w2g1f2e1r2e1s2e1u1e1b2e1s2e1a2e1s3f1y2c1v2g1s2e1r3e1s2e1s3c1f2e1t3e182e1t1g1t2c1w3f1t2e1r1f142e1t1c1u2e1s3g1h2e1u3g1h2c1u2f1e2e1q3e102e1t1c1h2e1t3g1a2e1t2e1e2c1v2g192e1r3e142e1s3e1k2e1s1f1w2e1s3e1s2c1u3e1t2e1q3e182e1s2e1k2e1t2g1d2e1r3g1u2c1v2g1t2e1r2e1l2e1s2d1i2e1t1g1d2e1u2g1f2c1w1g1t2e1s2g102e1r3c1v2e1r1g1p2e1s3e1s2c1w1e1s2e1r1g1m2e1r2e1v2e1r2f1e2e1s2g1h2c1t2e1t2e1q1g1h2e1u2c1i2e1t2g1p2e1r2e1u2c1v2e152e1s1f1u2e1s1c1v2e1s2f1x2e1s1e1b2c1w2g1w2e1s2e1w2e1u1c1q2e1u3e1f2e1r2g1x2c1v1g1x2e1s3f1e2e1u1e122e1s1f1v2e1t3g1z2c1w1g1y2e1r3e152e1t2d1e2e1r2e1o2e1t3e1r2c1u1e162e1r3g1l2e1u3e192e1s1g1g2e1s2g1e2c1u3e1t2e1p1g1d2e1u2e1q2e1t1g1q2e1r2e1d2c1t1e1r2e1r2e1k2e1u2d1j2e1r3g1w2e1t2e1f2c1t1g1s2e1s3e1m2e1u1e122e1s3f1b2e1t3g1d2c1u1g1f2e1q3e1f2e1s2c1q2e1u1g1o2e1u1e102c1v2g1e2e1s2e1h2e1s2d1u2e1t1g1p2e1u1g1t2c1t3g1e2e1s1f102e1t3e1u2e1t3f1d2e1s2g1t2c1u2e1c2e1p1g1d2e1t1c1u2e1u2f162e1u3g1c2c1v3f192e1r1f1e2e1u3e1v2e1r1f1h2e1t2g142c1w2g1s2e1r1f1h2e1t1c1h2e1t2g1d2e1r2g192c1v3e142e1q3g1i2e1s1d122e1s3e1o2e1s1g1t2c1w2g1h2e1s1e1l2e1s2c1i2e1u2f1p2e1u2g1f2c1u1g1w2e1q2e1g2e1t1d1w2e1s1e1p2e1s2f142c1u1e1b2e1s2g1w2e1u2c1y2e1u3e1o2e1t3e1t2c1w1e1t2e1s2f1c2e1u2e1j2e1s2g1x2e1u2g142c1v2e1w2e1q2g1e2e1u1e102e1s2e1c2e1u2e1r2c1u1g1s2e1r1e1x2e1t2c1y2e1t2e1w2e1u3g102c1v1g1v2e1d2f143e1u2d182f12142h2k1q1l1j2e1d2l1s1g221o','77d162b35313y331y391e27303q1b3v3e1b3q021z1o25313q2m273c2q2o2w25381g252z1i3c2b381a2x3s11311m380w113139233v313b361c2v3u113z1o2z182v3z2p1z323a231s25353e14212v253e1w3u27111138251q27353c163z281y10111411153v3b2o1921341u3s2v213n113u263e133x392q192z3610111o23113u28113u281z3w281z3w2o313b213x3c2b233v2b213x272y3b3v2e111z2433163q00323c2b3y121o3c1d3q0z312k24113z1o2z11113s291z311f393x3c1a1y10322v3w2u333e10111e1m11133x29211v302q14232720352e162833211f1e1a3c1631261y1z1211303u2711121m3u350131223514351k1d3f1j1g1k1d1f1c1s3f1h2g1o3f1f3e183e1m1g1g1e1f2f1e3c1s3d1m2e1r3e1x2e1u3e1y2c1v2e1w2e1q3f1k2c1s2c1a2e1q3e1p2e1u2c1q2c1v1e1e2e1s2e142c1u2c112e1q2e192e1u2e1e2c1v3g1h2e1q2e1u2c1s1e162e1s2g1p2e1s2c1z2c1w2e1e2e1s3e1t2c1u2e1y2e1r2e1r2e1u2e1g2c1v2e1v2e1s2f1y2c1u2c1a2e1q2g1v2e1u2e1b2c1u1f142e1s3g1v2c1s3d1b2e1q3f172e1s1d182c1u3f1x2e1q3f192c1s3c1k2e1q2f152e1u3d142c1u2f152e1r3f1l2c1s2d1b2e1s3f122e1s3d192c1w3e1a2e1q2f172c1u3d1f2e1q3f152e1t3d1f2c1u3f152e1q3g1b2c1s2d192e1r3f1x2e1s3d162c1w3g182e1q2f182c1u3e1x2e1q3f152e1s3d192c1u3f1s2e1q2e1u2c1f1c1j3f1e1g1e3g1u1d141e1u2g1b3e1g3f121d143d1i1e1e3e1q1g1q3e1f3c1l3e1d1f193f1j2d183e143e173f1d1g1g3d1g2c1e3f1q3g1i3e1l1c1i1e1j3f1a1e1f3e1b2d1k3e1a3f1d3e181f1g3e141d1j1e101e181e1a1c1a1c1c3f1k1g1q1f1b2d1b1d1r3f1d3f1e1g1d1d1m3c142e123g1y1e1f3d1f3e1m3f1r1g1q1e1d1d1a3e1u1e1q3e1e3f1e3e141d1k1g1q1f1e3e1u2d1h3d1e3e1d1g1i3e123e1f3d1i1g1p3g1o2e1u3d102c1v3f1f2e1r3e1t2c1t1c122e1s1f1w2e1t2e1s2c1v1e1t2e1r2f1f2c1u1c1j2e1r2g1v2e1t2e1l2c1u2f1y2e1r1g1q2c1u1c112e1s1f1r2e1t3e1l2c1w1e1q2e1s2e1r2c1r2e162e1r1e1f2e1t3c1l2c1v3e1f2e1s1g1q2c1u1c1q2e1q2e1v2e1u1c102c1v2g1d2e1r3e1k2c1t2e1w2e1r1e1s2e1u1e1l2c1v2e1y2e1q2f1r2c1t1c122e1r2f1y2e1u2c1g2c1w1e1j2e1r1g1j2c1t1c1j2e1r3g1j2e1s3e1l2c1w2g1u2e1p1e1r2c1t3c102e1q2f1y2e1t3e1s2c1t2g172e1r2e1f2c1s3d1a2e1s1e1y2e1u1c1w2c1v1g1x2e1r1g1h2c1t2d1u2e1r1f1q2e1s2e152c1t3g1r2e1q1g1y2c1t1e1u2e1r1f1y2e1t3e1r2c1w1e1w2e1s2e1a2c1t2d1w2e1p2g1f2e1u1c1y2c1w2f1f2e1r1e1j2c1r3e112e1s2e1f2e1t3e1h2c1w1e1y2e1q2e1t2c1s2e1y2e1q2g1o2e1s2c1t2c1w3g1w2e1p2e1u2c1s1e1m2e1r2g1x2e1u1d1u2c1u2g1u2e1s2e1g2c1u1d1m2e1q2e1v2e1u3d102c1w1g1w2e1r1f1r2c1s2e1z2e1s1e1v2e1t1e1l2c1v3e1j2e1p2e1z2c1s3c1z2e1s1e1x2e1t1c1y2c1w1e1p2e1s2g1w2c1t2e1q2e1s2g1y2e1u1c1l2c1w1f1j2e1q2e1z2c1t1c1q2e1s2g1d2e1u3c1h2c1v1g1j2e1r2f1h2c1t3c1q2e1q1e1f2e1u1c1t2c1t2g1r2e1q2e1x2c1t2c102e1q2e1i2e1s3c1a2c1w3e1p2e1r3g1t2c1u1e1u2e1r2e132e1t3e1r2c1v3g132e1q3f152c1s1e1y2e1q2g122e1t3c152c1v2f1f2e1r3e1v2c1s1d1a2e1r2e1p2e1u1c1j2c1w2g1y2e1s1e1d2c1t1c122e1s2g1j2e1t2e1h2c1u2g132e1q2f1r2c1u1e1l2e1r1e122e1t1c1a2c1u1e1v2e1s2f1z2c1u2e1j2e1s3f1x2e1u3e1s2c1t1e1f2e1s2g1x2c1u1e1u2e1q2g1q2e1s2c1j2c1v2f1p2e1q2f1m2c1u2e1h2e1r1g1d2e1u1e1s2c1w2g1e2e1r1e1h2c1s2e122e1s2g1r2e1t2e1u2c1u2g1j2e1p2e1f2c1t2c1v2e1p2e1t2e1t3c1g2c1v1e1f2e1q2g1r2c1s3d112e1q2g1f2e1r3c1h2c1w1e1y2e1s1e1q2c1s1e1u2e1s2g1x2e1s3e152c1u2e1j2e1s3e1i2c1t3c1u2e1q2e142e1s1e1v2c1u2e132e1r2e1v2c1u2c1y2e1q1f152e1u2c1l2c1v1f1v2e1q2g1u2c1t2c102e1q2e1y2e1t2e1j2c1u2g1t2e1q1f1t2c1s1c1t2e1q1e1v2e1s2c1s2c1w2f1u2e1r2e1j2c1u3c1q2e1r2g1y2e1t1d172c1v2g1t2e1s1f152c1s3e1s2e1r1g1q2e1t2e1t2c1v2f132e1s2f1j2c1u2c1w2e1s1e1s2e1s3e1t2c1w2e1y2e1r2e1j2c1u2c1f2e1q1e1r2e1s2e1f2c1t2f1i2e1s2f1q2c1t3c1k2e1q1g1y2e1u3d1k2c1v2g1r2e1r2e1z2c1t2e1u2e1q1g1x2e1s3c102c1w2g1f2e1s3e172c1s1c1d2e1q3g1y2e1s1e1t2c1v3g1c2e1q2f172c1t2e1s2e1r3g1p2e1t1e1t2c1v2g1p2e1q2e1d2c1t3d1w2e1r2e1s2e1t1c1h2c1w1f1q2e1s1e1e2c1t2e1u2e1p1e172e1t2e1y2c1u1e1q2e1s3g1d2c1u2e1q2e1p1g1b2e1t1e1s2c1u2e1b2e1q1e1j2c1u3c1z2e1s2f122e1r2e1f2c1u3g1r2e1q3e1r2c1t2e1h2e1p2g132e1t3e1w2c1u3g1b2e1r3e1j2c1t2d1d2e1p2g1d2e1u1e182c1v1g1q2e1q1g1z2c1r2c1v2e1q2e1b2e1r3e1c2c1w2g162e1s1e1w2c1s1e1t2e1s2g1j2e1t3e1y2c1u1g1d2e1s3e1r2c1s3c1x2e1s1e142e1s2c1y2c1u2e1j2e1r1e102c1u2c1v2e1r3g1e2e1r3e172c1w1e1t2e1s1e1i2c1t2d1m2e1q2f1p2e1r2c1g2c1v2g1r2e1r3g1f2c1r2e1j2e1s1g1f2e1u1e1z2c1u1g1f2e1p2g1a2c1r1e1z2e1s2e1c2e1u2e1v2c1w1g1h2e1r1f1q2c1u1e1j2e1s2g1i2e1u2e1f2c1v1g1b2e1r2g1e2c1s2d1e2e1q1e1a2e1t3d1s2c1u2e1u2e1s2f1d2c1s3c1k2e1r3g1f2e1u3e1t2c1w2g142e1s2f1a2c1t1e1y2e1q3e132e1t2d172c1v3g1f2e1s2e142c1t2e1j2e1r1g1c2e1r2c1j2c1w2g1q2e1s2e152c1r1d182e1p2g1k2e1s2e1d2c1w2f1t2e1s1e1t2c1t3c1y2e1q3f1d2e1s3c182c1v2g1r2e1q1f1y2c1s2d1b2e1p2g1d2e1s2e192c1w1g1d2e1r1g1d2c1t3e1b2e1r2e1a2e1u3c1d2c1t1g1y2e1q1e1c2c1r2e1d2e1q1e1s2e1t3d1t2c1v3e1q2e1r1g1s2c1s1e1d2e1s1g1x2e1t2d182c1t1e1f2e1r1f1f2c1s2d1l2e1r2g1r2e1t1c1s2c1u1e182e1r3g1a2c1r2e182e1p2g1j2e1u3d1t2c1u1g122e1p2e1r2c1s3c1f2e1p2g1a2e1u3e182c1w3e1d2e1p1g1r2c1u1d1v2e1p1e1f2e1t1e1i2c1v1e1d2e1s2e1r2c1t2c1h2e1p1g1v2e1u3c1e2c1w2g1t2e1s1g1h2c1t1d1u2e1s3g1f2e1t3c1w2c1w3g1r2e1s3e1v2c1u2e1q2e1q2g1x2e1s2e1s2c1v1g1v2e1q2g1j2c1r2d1u2e1s1e1t2e1u2d1k2c1w3e1p2e1r2f1l2c1s2c1q2e1q1e1j2e1s2c162c1v3g132e1q3e1a1c102c1w2e172e1q2f1b2c1t1e172e1s1g1d2e1u1c1r2c1t2g1w2e1s2g1z2c1u2e1l2e1r1e1k2e1t2e1t2c1w2g1g2e1s2e1j2c1u1e1h2e1s2e1d2e1t1d192c1u2g1r2e1r2e1s2c1u1c102e1s1g1d2e1r2e1w2c1w1g1d2e1q1e1z2c1t1c1s2e1r1e1j2e1s3e1t2c1u2e1d2e1r3f102c1u2e1f2e1q2g1d2e1t1e1s2c1w3e1k2e1s2g1f2c1t2c1y2e1s2g1q2e1s2e1d2c1v1e1q2e1s2e1x2c1u1e1t2e1q1g1w2e1s1e1y2c1w3e162e1r2e1w2c1s2e1h2e1s1g1r2e1t3d1f2c1w1g1w2e1s3g102c1r1e112e1r1f1f2e1u1c152c1u2e1d2e1r3g1t2c1r2e162e1s2g1h2e1s2e1r2c1v1e1h2e1s2g1y2c1u1e1h2e1q1g122e1t3e1f2c1w1g1w2e1r2e1f2c1s2c1h2e1s2g1b2e1s2e1f2c1w3e1p2e1q1e1f2c1r2d1h2e1r2g1w2e1s2c1t2c1w2g1s2e1q1e1s2c1u2e172e1q1e1w2e1t2c1t2c1w1e1i2e1s2e1m2c1u3e1s2e1s2g162e1u2e1r2c1u1e1b2e1q2e1t2c1u2c162e1s2e1c2e1u2c1s2c1w1e1r2e1s1e1j2c1r2e162e1r2e1q2e1t1c1w2c1u1g1p2e1s2f1f2c1t2e1t2e1r3e1o2e1u2d1y2c1t2g1c2e1r2e162c1u2c1d2e1s2g1u2e1t1c1d2c1t2f1o2e1s2e1d2c1u2e1y2e1p1g1w2e1u2c142c1w1e1v2e1q2g1d2c1u2e1a2e1r3g1h2e1t3c1w2c1w3e1v2e1s1g1r2c1u3c1v2e1s2g1r2e1u3e1g2c1v1g1u2e1r2e1q2c1u2e1d2e1q1e1w2e1t3d1x2c1w1g1b2e1s2f1u2c1t2d1b2e1r1g122e1u1c1y2c1v3g1r2e1r2g1v2c1u3e1l2e1p1f1h2e1u1e1k2c1w3e1v2e1s2e182c1t1c112e1s3f1j2e1t3c162c1v2f1r2e1r2f1r2c1s1c1r2e1s3e1w2e1s2e1r2c1w2g1q2e1s3g1l2c1t2c1y2e1s2e1u2e1t1c1f2c1u2f1d2e1q3g1w2c1u1c1x2e1q2e1s2e1u1c1r2c1u2e1h2e1s3g1y2c1s2c1z2e1s1e1y2e1u2e1v2c1w3f1r2e1s3e1g2c1u2e182e1r2g1s2e1t1c1h2c1w2g1h2e1p3e1t2c1t1e1m2e1p2f1k2e1t1e1r2c1w2g1k2e1r1g1q2c1u1c1h2e1r1f1b2e1s2d1s2c1v1g1d2e1q2e1f2c1t2c1z2e1r3g122e1u3c1v2c1v1g1e2e1q2e1m2c1t2c1l2e1s2g142e1u2c1w2c1v2e1s2e1s2g1z2c1u2e1v2e1s2e1q2e1s3c1z2c1u1f1t2e1r2g1u2c1s1e1t2e1r2g1p2e1t3e1i2c1w2g1y2e1r1e1r2c1t2c1x2e1s2e1s2e1s1c152c1w2e1h2e1r1f1v2c1s2e1w2e1r2e1u2e1s1e142c1w2g1t2e1r2e1y2c1s2c1l2e1r1f1p2e1s2e1x2c1w2g1s2e1q2g1y2c1t3c192e1r3e122e1t3c1j2c1t1e1w2e1r2e1j2c1r1e1h2e1q3e182e1t3d1t2c1t2e1k2e1s2g1e2c1r1c172e1s1f1c2e1r1e142c1t2e122e1r2f1y2c1t2e1w2e1q3g1p2e1r2d1w2c1w2g1p2e1s1e1m2c1u2c1j2e1p1e132e1s3d1y2c1u2g1i2e1r2g152c1t1c1w2e1q1f1p2e1s2e162c1v1f1w2e1q3g1c2c1t2e1h2e1q2g1b2e1t1d1u2c1v2f1p2e1q2f172c1t2c1t2e1q2g1s2e1t2e1e2c1w1g1o2e1s3f1f2c1u2c182e1p2e1w2e1u2e1c2c1v2g1p2e1p1g1j2c1t1c1m2e1q2e1h2e1t1c1u2c1v1g1b2e1q2f1w2c1t3c162e1s3g1s2e1t2e1r2c1u1g1s2e1r2e1r2c1r2e1t2e1s3f1p2e1t2e1d2c1v2e1p2e1q1g152c1t1e1e2e1r2g1e2e1s3d1x2c1v1g1u2e1q3e1s2c1s2c1l2e1r3e172e1t1c1e2c1u3g1b2e1q2g1m2c1r2c1t2e1s1g1u2e1u1c142c1w2g1v2e1r2g1e2c1t1e1g2e1q2e1h2e1s2e1i2c1v1g1b2e1q1e1f2c1t1c1h2e1p2f1d2e1s1c1e2c1v2g1p2e1p1g1d2c1r1e1m2e1p3g1q2e1u1c1q2c1v2e1e2e1r1g1g2c1u1e1i2e1s3g1g2e1t1c1e2c1v1e1p2e1r2e1u2c1u3e1t2e1s3e1t2e1u3d1f2c1w3f1w2e1r2g1c2c1u1e1e2e1r1e1p2e1t2c1q2c1v2g1p2e1q2e1t2c1s2c1h2e1s2e1d2e1s2c1y2c1u2e152e1s3e1f2c1t2c112e1r2f1h2e1u3d142c1v3g1p2e1s1g1r2c1s2c1g2e1q1g1s2e1t1e1y2c1v1g1g2e1r2e1x2c1u2c1v2e1r3g1v2e1u1e1r2c1t2e1d2e1s2e152c1s1d1s2e1q2g1x2e1t1d1d2c1v1e182e1q3g1c2c1u1d192e1q1e142e1t2e1s2c1v3f1q2e1p2e1j2c1r2d1t2e1s2g132e1u1e1q2c1t2e1q2e1p3g1e2c1s3d1t2e1r2g1p2e1t1c1f2c1w3f1b2e1s1g1z2c1t2e1f2e1r3f1d2e1u3c1x2c1t1f1b2e1s2g1j2c1t3e1e2e1s1e132e1r3e1f2c1u2f132e1q3f162c1t3e102e1s1g1f2e1s3e152c1u2f1b2e1r2g1c2c1t2e1i2e1q3f1v2e1t1e1w2c1u3e1q2e1q1e1r2c1u1e1f2e1r2e1h2e1t1e1x2c1w1g1e2e1q3g1r2c1s3c1h2e1p1g122e1u3e1i2c1v1e1c2e1r1e1r2c1t2c1w2e1s3g1p2e1u3c1v2c1w2g1r2e1r1e1k2c1t2c1z2e1r3f1t2e1t1d1i2c1t2e1x2e1r3g1s2c1u2c1v2e1r1g122e1t1c1j2c1u1e1c2e1r1e1j2c1r2e1v2e1s2g1b2e1u2c1q2c1w1e1k2e1r1g1u2c1u2c1c2e1y2e1q1e1v2c1u2e102e1r2g1y2e1t1c1z2c1w3f1f2e1s1g1w2c1t1d102e1s1e1t2e1s2e1h2c1v2e1s2e1r2e1u2c1t2c1t2e1s2e132e1t2c1z2c1w1g1f2e1s2g1m2c1t1e1v2e1r3f1r2e1u3c1t2c1u3g1f2e1q1f1f2c1t2c102e1r3g1f2e1t3e1y2c1v3e1q2e1q1g1l2c1u1e1u2e1q2f132e1t3d1t2c1w2g1y2e1s3e1m2c1t3c1u2e1s2g162e1u3d102c1w3f1f2e1s2g1s2c1s2c1c2e1r2e1p2e1t2c1d2c1u2g1y2e1r2e1t2c1s1e1q2e1q3f1x2e1r2d1q2c1w1e172e1s1e102c1u2c122e1s3g1x2e1t3e1r2c1u3e1f2e1s2f1r2c1u1e122e1s3g1x2e1t1c1u2c1v3e1g2e1s3g182c1u2c1y2e1p3f1w2e1u3c1x2c1w1g1y2e1s3e102c1t3e1y2e1s3e1j2e1u2d1t2c1w3e1o2e1r1e1r2c1u3c1u2e1r2g1f2e1t2e1d2c1u3g1j2e1r2e1t2c1t2e1w2e1s2e162e1t2e1x2c1u2g1s2e1r1e1z2c1u1c1u2e1s1e1f2e1s3c1f2c1v2e1s2e1s2g1v2c1u3c1v2e1s1e1y2e1s3c1t2c1v2e1j2e1q2e102c1s2c1v2e1q2g1u2e1r1e162c1u2g1s2e1q2g102c1t1c1v2e1r2g1e2e1s1e1r2c1v1e1w2e1s3g152c1u3d122e1p1e1j2e1u2c1r2c1v2g1r2e1s2g1k2c1t2d1q2e1r2f132e1u2e1d2c1v2f1j2e1q1e1h2c1t2c172e1r2f1y2e1t2e1g2c1v2g1j2e1q1e1l2c1r2c1w2e1s3e1i2e1s3c1d2c1v3e1b2e1r2g1h2c1u2e162e1r1e1y2e1t2c1r2c1v2g1g2e1q2e1h2c1t3c1v2e1q2g1b2e1u2c1j2c1w3e1j2e1s1g1c2c1u2e1u2e1q2e1d2e1s2e1u2c1w1e1w2e1p1f1l2c1t1c1u2e1s3g1o2e1s2c1h2c1w1g1j2e1r1g152c1s3e162e1q2e1o2e1u3d1z2c1v2g1r2e1s3e1r2c1u2c1l2e1q1g1j2e1u2c1h2c1v2g182e1r1f1w2c1u2e122e1q1e1o2e1u1c102c1v2e1g2e1r1e1i2c1t1c1y2e1p1f1u2e1t3c1i2c1u3e1s2e1q1f1k2c1u1c1q2e1q2f1q2e1t3d1r2c1w1g1r2e1p2e1e2c1u1e1j2e1r1g162e1t2e1x2c1t2g1t2e1s1e1s2c1s2e1k2e1q3e1x2e1u1e1u2c1w2e1r2e1q1g1u2c1t3e112e1s2g122e1t3e1g2c1v1e1j2e1s1g1z2c1s2c112e1r2g1q2e1t2c1t2c1w1e1r2e1s2g1x2c1u3c1t2e1s2f1r2e1s2c1k2c1w1g1y2e1r2e1w2c1t2e172e1q1e142e1s2e1r2c1w3g1v2e1s1f102c1t2e1x2e1q2g1q2e1t2d1s2c1u3e122e1q1f1x2c1t2e1y2e1q1g1r2e1t2e1r2c1v3g1s2e1s3f102c1s2d122e1s2g1w2e1s2e182c1v3e1y2e1r2e1k2c1r2d1k2e1r2e1q2e1s2c1u2c1w2g1t2e1s2g1t2c1r2c1q2e1s2g1r2e1t3d1j2c1u1g1d2e1p1g1d2c1t3c1e2e1r2g1f2e1t2c192c1v3g1r2e1s2g1j2c1t2e1v2e1p2e142e1u3c1y2c1w2g1d2e1q1e1z2c1u2c1j2e1q2e1u2e1s3e152c1u3f1d2e1q2f192c1r2e172e1r2g1x2e1s1e1e2c1v1f1q2e1s1g1t2c1r1d1v2e1r2g1a2e1s1e182c1w3g1r2e1q1f1t2c1s1d1z2e1s2g1q2e1t2d1f2c1u2g1s2e1q3e102c1u3c1h2e1r1e1q2e1t3e1s2c1v2f1r2e1q3g1t2c1u1e1f2e1r3g1o2e1t2e1z2c1u1f1y2e1s2g1z2c1t1d1h2e1p3g1d2e1r3c172c1v2g1u2e1s2f1h2c1s1e1v2e1q3g182e1t3c1x2c1v1f1x2e1r1g1s2c1s3d122e1r1g1b2e1u3e1y2c1t3e1d2e1r3g1e2c1s1d112e1q1g1t2e1u2e1v2c1t2f1p2e1r2f1r2c1u3c1v2e1r1g1p2e1r3c1x2c1w1e142e1q3f1t2c1u2d1r2e1r2g1d2e1u1e1j2c1t3g1q2e1q1g1t2c1s3e112e1s2g1x2e1t2e1f2c1v2g1r2e1p1g1f2c1s1e1t2e1p3g1q2e1t1e1g2c1v2e1r2e1q1g1l2c1s2e122e1r3f1x2e1u2c1c2c1u2f1s2e1q2g152c1u2e1x2e1r1e1k2e1t2c1x2c1v1e1y2e1r2e1x2c1t3e1j2e1r2e1q2e1t2e1e2c1w3g1j2e1s1f152c1u2e1f2e1q1e1h2e1t3d1s2c1v3g152e1r3e1t2c1t1d122e1q1g1t2e1s1e1h2c1w3e1h2e1q2g1t2c1s1c1j2e1r2g1y2e1s2c1l2c1v2g1d2e1r2f1h2c1t2e122e1r3e1t2e1s2d1x2c1u2f1c2e1r1g1t2c1t1d1u2e1s1e1g2e1t3d1w2c1u2g1d2e1r1g1e2c1s2d1v2e1p2f1f2e1u1c1w2c1u3g1p2e1r2g1f2c1s2e1u2e1r3g1b2e1s1d102c1u2f1c2e1q2g1l2c1t2e1d2e1s2e1d2e1t1e1c2c1v1g1k2e1s2e182c1r2c1j2e1s1g1q2e1u3e1d2c1v2e1q2e1s1g192c1s2c1d2e1q3g162e1s2c1e2c1v2g1r2e1p2e1a2c1t2c1u2e1q1g1r2e1u2d1c2c1u3e1y2e1r1e1f2c1r2e1f2e1s2g1y2e1r3c1d2c1v3g1c2e1q1f1z2c1s1e1u2e1r2e1r2e1r1e1x2c1w2f1x2e1r3f142c1s2e1l2e1r2f1q2e1r3e1x2c1v2e1c2e1q2f1u2c1s2e172e1s2g1t2e1t1c1k2c1v2e1x2e1r3f102c1s2e1w2e1p1g1t2e1s2e182c1v1g1d2e1s2g1t2c1s1e1q2e1q2e1v2e1t3e1f2c1w1g1h2e1s3g1y2c1t2e122e1s2g1r2e1t2c1x2c1v2f1s2e1r3e1x2c1u1e1q2e1q2e1b2e1u1c182c1u3f173f17141f1d3g173f1s1c191c153g103e121g1k3d171e1g2g1i1e1v3g1k3e152c1v3g1t2e1s2e1x2c1u2e1b2e1s1f1w2e1v2e1q2c1u2f1w2e1r2g1q2c1t1c1w2e1r2e1q2e1u3c1y2c1u3e172e1s2g122c1s3c192e1r3g1x2e1u3c1w2c1w1e1j2e1r2e172c1s1c1q2e1q3g1d2e1w2c1e2c1u3g1e2e1s1f1z2c1t2e1l2e1s3g1r2e1w3e1z2c1u2e1a2e1s1e1z2c1u2c1j2e1q1f162e1w3d1a2c1u3f172e1q3f1c2c1s3d1b2e1s3f1j2e1u3d192c1v3e1b2e1q1f1a2c1u3d172e1q3f152e1v3d1d2c1u3f162e1s3g122c1s3d1a2e1q3f172e1u3d182c1u3e152e1q3f192c1s3c1f2e1q3f152e1u3d1l2c1u3f172e1s3f1e2c1s3d192e1q3f1h2e1u2d182c1w3f1c2e1q3f192c1s3d1d2e1q3e1x2e1u2c1k1c1j3e1d2f1c1e1j3b1f3d1e3e192e123e123b1d3e1a1f171g1d1g1i3d1g3c1e3f1d2g1i3e1q1c1i1d1j1f1a1e1f3e1d2d1k3d1a3f1d3e181f1i3d141d1j3e101g1u2f1l1d181c141d1b1g1c3f1r1c1b3c1e3f1h3g1c3f1g3e1e3d1g3e1d3f1d1f1m3d1k3d1y1f122e1c1e1d1c1d1e1j3f1k3e1w3g1e2d132c1c3f122f1d3e1i1c1i3c1e1e1q2g1k1e1e2e1b3d163g1b2g1g1f1m1d1h3c141f121e181f1t1e1b3c1g1e1t2e1s2e1s2c1t3e1j2e1s2g1f2e1w3e1h2c1w3f132e1r1e1q2c1t3c1x2e1r3g1h2e1u3e1t2c1w2f1q2e1s1e162c1u2c1w2e1q2g1h2e1v1c1v2c1v2g1r2e1r1g1w2c1u1c1t2e1r2f1r2e1w3c142c1w2g1y2e1r2g112c1u2c1x2e1s3f1r2e1v2e1u2c1w1g1f2e1s2g1t2c1t1d1d2e1q2e1q2e1v2d1e2c1w1f1s2e1r2g1e2c1s2e172e1s3e1u2e1v2e1l2c1w2g1r2e1s2e1v2c1t2c1z2e1s3e1d2e1w2c1t2c1u2g122e1r1f182c1u3e102e1r3f122e1u3e1r2c1v2f1x2e1s2g162c1u1d1v2e1r2f1r2e1w3c1w2c1u1g1y2e1s2g122c1u2c1j2e1q3f1p2e1u2e1m2c1u1g1o2e1r2g162c1s1e1r2e1s1e1r2e1v1c1t2c1v3e1f2e1r1g162c1u1c1r2e1s2g1g2e1w3e1q2c1v2e1r2e1s2g1v2c1u1c1j2e1r3g1k2e1w1e1h2c1v2g1r2e1s2e1j2c1u1c1q2e1p1g1g2e1w2c1d2c1v2e1r2e1s1g102c1u2d102e1r1e1v2e1v2c1r2c1w1e1q2e1r1e1l2c1t2c1k2e1q1e1r2e1v3c1z2c1u2e1y2e1r1g112c1t3c1d2e1q3e1v2e1v2e142c1t2e1q2e1r1e102c1t2e1m2e1s3g122e1u3c1w2c1v3g1f2e1r3e1e2c1u2c1v2e1q2g1q2e1w2c1t2c1v1g1t2e1s1e1t2c1u1e1u2e1s2g1h2e1v1d182c1w1g1r2e1s2g1u2c1t2e1y2e1r2e1j2e1u2d1e2c1v2g1q2e1r1e1u2c1s2c1u2e1s2g1d2e1w2e102c1w3e1r2e1q2f1u2c1s2c102e1q2g1o2e1v2d1w2c1v1g1r2e1r1g1w2c1u1e162e1q2f1x2e1u2c1l2c1u3e1o2e1r2e1e2c1u1c1u2e1r3e1t2e1u1d182c1v2g1w2e1s3g1u2c1r3c102e1r1g1q2e1v2e1f2c1u2f1q2e1r3f1q2c1s1d1t2e1r2g1a2e1w2c1c2c1u2f122e1r2e1w2c1s2e1h2e1q2g1u2e1w2c1u2c1v1g1v2e1s2g1r2c1u1d1s2e1r1e1q2e1v1e1z2c1w1e1u2e1r2f1v2c1s2c112e1s2g1u2e1w2e1u2c1u2e1j2e1s2g1h2c1t1e1u2e1r3e162e1v3c1j2c1w1f1t2e1p2g1v2c1t3e112e1s3g1u2e1u3e1s2c1u2e1x2e1r2g1q2c1s1e1v2e1s3e1c2e1w1c1l2c1u2g1t2e1s3g1x2c1u1e1j2e1r2e1v2e1w2e1h2c1u1g1q2e1r1g182c1u2e1u2e1r3g1w2e1u3c1s2c1v1g1j2e1r2e122c1t2e1l2e1q2e1y2e1v2e102c1u3e1q2e1r2e1u2c1u3c1c2e1s2g1s2e1w2e1a2c1w2e1a2e1s2g1l2c1u2c1a2e1q1e1b2e1v2e1v2c1w1e1s2e1q2e182c1u2d1u2e1r2f1q2e1v2c1l2c1v1e122e1s1e1l2c1t1e1v2e1r1e1o2e1u2e1e2c1w3f1f2e1r2e1j2c1s3d172e1q2f142e1u2c1u2c1u2f1v2e1r2g102c1s2e1v2e1r2f1f2e1w1e102c1u3g1u2e1s1f1v2c1s2e122e1q1g1r2e1v2c1f2c1t1e1r2e1r2f1x2c1u3c1w2e1r2f1p2e1w1e1t2c1v1g1x2e1q2e122c1u2c1a2e1s2g1o2e1v3c182c1u3f1y2e1q3f1h2c1t3e1y2e1q2e142e1u1d182c1w2g182e1s3f1u2c1t1e1d2e1p2g182e1u1d1x2c1v3f1q2e1q3f1t2c1t3c1v2e1p2g1w2e1t2d1l2c1v2e1q2e1r3g1u2c1u1c1j2e1q2e1k2e1u1d1l2c1w1e162e1r3f1v2c1t3e1h2e1p1g122e1v3e162c1v3f1x2e1r1g1z2c1t1e1c2e1r3e1v2e1v3c1s2c1u2g1b2e1q2g1c2c1t1d192e1r1g1h2e1v2d1d2c1u2g1b2e1q1f122c1t1e162e1p2g1p2e1w2e1s2c1v3f1f2e1p3g1e2c1s2d1v2e1q1f1t2e1v2c172c1w1g1y2e1r2g1v2c1t1e1e2e1q2g1j2e1v1e1z2c1v2f1e2e1q1g1j2c1u2c1q2e1r2e1p2e1v2c1u2c1u3g1h2e1q1g1e2c1s1e1i2e1s3e1c2e1v1e1z2c1w2g1p2e1q2g1j2c1r2e1w2e1q3g1f2e1v2e1s2c1w1e1t2e1s1g1v2c1r3e1w2e1s1g1a2e1t3d1x2c1u3f1t2e1r2e1t2c1t2c1u2e1r3e1p2e1v1c1t2c1w2f1a2e1q1e1e2c1u1e122e1p3g1b2e1t1c1t2c1t2f1x2e1q2f1x2c1r1e1v2e1q3f1q2e1u2e1v2c1w1e1f2e1s3g122c1s2e192e1q3f1s2e1v3d1x2c1u3e1w2e1s2g1d2c1t3e1e2e1s3e1k2e1u1e1k2c1w2e1v2e1q2f1j2c1u2e1x2e1s2g1o2e1v1e1x2c1w2e152e1q2g182c1r2e162e1r2g1u2e1v2c1j2c1w3f1y2e1q3e1a2c1t2e1d2e1s2e142e1v1d1v2c1u3f1s2e1q2f1d2c1s2c1j2e1q1g1p2e1v2d1w2c1u3e172e1r2g102c1s2c1f2e1s3g1d2e1v1c1d2c1u1g1q2e1r2g1h2c1t1c1w2e1r3g1i2e1w2e1e2c1v2g1r2e1p2f1h2c1t2c1f2e1q3g1b2e1u1e1t2c1u2e1r2e1r2g1h2c1r3e172e1r3e1s2e1u2e1a2c1v3g1o2e1r3f1z2c1t3e1v2e1s2g1r2e1v3d1h2c1t2g1a2e1q2f1v2c1s1d122e1p1e1b2e1u1c1h2c1v2g182e1r1e1a2c1u2c1t2e1r2f1g2e1u3e1t2c1u2g1v2e1q3f1x2c1t2d1t2e1r3e1o2e1v3c1t2c1v1e1r2e1s2f1e2c1s3e1u2e1q1e1f2e1u1c1w2c1w3e1u2e1r1e1y2c1s2c102e1q2g1r2e1w1e1m2c1v1e132e1r2g1q2c1u1c122e1r1f1d2e1w3e1l2c1w1g1t2e1s3g1x2c1u2c102e1s2g1h2e1u1d1t1c1u2e1s3g152e1w1c1x2c1u1e1w2e1s3e162c1u3e1t2e1s2e132e1w2e1y2c1w2g1g2e1s1e1v2c1t2d1s2e1r1e122e1v3e1k2c1u2g1f2e1s3g172c1u3e1v2e1q2e1x2e1v2e1v2c1v1e1r2e1s2e1t2c1u1e1t2e1s1e1q2e1v2c1f2c1u2g1y2e1s2e1s2c1s1c1h2e1r2g1g2e1u2d1y2c1v2g1u2e1q2e1x2c1t3e122e1s3g1y2e1u2c1f2c1w3g1b2e1r3e1h2c1t1c1h2e1q2g1r2e1w1c1y2c1v1e1q2e1s2e1i2c1t3e1t2e1q3e1u2e1u2e1b2c1w2e1t2e1r3g1l2c1r2c122e1r3e1p2e1v1e1h2c1v2e1o2e1q2e102c1t2c1s2e1s2e1x2e1w1d1h2c1w1e182e1s2e1z2c1u2e1q2e1r3g1y2e1v3c162c1w1g1d2e1s1g112c1t2e1c2e1r1e1d2e1w2c1q2c1u2f162e1p2g1t2c1u2c1v2e1p3e1d2e1u2c1d2c1w2f1k2e1r3g1i2c1u2c1h2e1s1e1p2e1w2e1m2c1v3e122e1r2g1m2c1s3c1r2e1s3e142e1v1e1t2c1w2g1t2e1q2e1t2c1s3e1t2e1s2g1p2e1u2d1t2c1u1g1f2e1p2g1l2c1t2e1u2e1s2g1h2e1v2c1q2c1u2f1h2e1r2g1j2c1s2e1r2e1s3g1p2e1w2c1u2c1u1e1p2e1p1f1q2c1t2e1h2e1p2e1p2e1w2c1r2c1t1f1h2e1q2g1z2c1r2c1u2e1s1e1u2e1u2c1w2c1u3g1h2e1s2e1y2c1t2d102e1r3g1s2e1u1e1y2c1u2g1g2e1s2g1d2c1u1e1k2e1r3e1w2e1w3c1t2c1w2e1u2e1r1e1s2c1t1c1u2e1r3e1a2e1w3c1y2c1w3g1g2e1q2g1u2c1t2e1h2e1r2e1w2e1w3d1y2c1v3g1b2e1q1g162c1s2c1i2e1r2e1d2e1u1e1j2c1t1f1h2e1s1g1q2c1s2c1h2e1r2g1o2e1u2e1d2c1u2f1q2e1s2g1z2c1s3e112e1q2e1i2e1w1e1y2c1w3e1v2e1q2g1l2c1u2c1m2e1r1e1y2e1w1c1c2c1w1e1d2e1s2g1h2c1s2d1t2e1q3e122e1w1e1z2c1u2g1d2e1r3e122c1t3e102e1r3g1q2e1v3c1y2c1v1e1t2e1q1f1s2c1s2c1a2e1s1g1w2e1u3e1j2c1u2f1r2e1r2e1t2c1t2e1t2e1s2g1c2e1v2c1i2c1v2g1i2e1p2g102c1s1e1v2e1s1g1k2e1u2c1q2c1v2e1y2e1q3f192c1t2c1y2e1s1e1d2e1w1e1m2c1v1e1a2e1q3g102c1s2e172e1r3e1f2e1w3e1t2c1w2g1h2e1q2g112c1t2e1k2e1s2g1y2e1v1e1j2c1u2g1r2e1s2e1u2c1u2e1l2e1s1f1f2e1u2d1y2c1u2e1g2e1r1e182c1s2c1h2e1s2e1r2e1t3c1j2c1v2g1w2e1q3e1v2c1t1c1v2e1s3e162e1w2e1u2c1w1g162e1s2g1c2c1r3c1d2e1q1g1r2e1w3e1s2c1v3f1d2e1s3e182c1u2e1h2e1q1g1d2e1w2c182c1v3g1k2e1r3f1z2c1u3e1l2e1p1e1w2e1v3e1t2c1v3e1d2e1s3f1y2c1t1c1f2e1s1g1x2e1u2d1v2c1v2g1d2e1p1g122c1u2e1d2e1p2e1r2e1w1d162c1u2e142e1r1g1t2c1t1c172e1r3e1q2e1w2c1z2c1w2g1d2e1q3f1f2c1s2d1f2e1p1f142e1u3d1l2c1w2f142e1s2e1f2c1t2c182e1r2g1d2e1v3e1e2c1w1f142e1r3g1f2c1t1c182e1r2g132e1v3e1e2c1v2g1t2e1r1g1i2c1s1e1e2e1r1e1h2e1w2e1t2c1v3g1c2e1q3e1t2c1s3e1f2e1r2g192e1w1e142c1v3g1p2e1s2f1f2c1t1d182e1s2f1d2e1t2e142c1t2f1w2e1q1e1u2c1t1d1s2e1r1g1d2e1u1e1u2c1v2g1b2e1q2f1q2c1s2e192e1r2g1a2e1v2e1r2c1u3e1k2e1s2g182c1t2e1x2e1s2e1b2e1v1c162c1w3g1w2e1q1e1z2c1s2e1z2e1q3g1p2e1w1e152c1t3f1s2e1r3g1g2c1s1e1k2e1r3e1q2e1v3c1t2c1t1g1v2e1s3g1z2c1r3e1h2e1p2f1d2e1w1c1j2c1w1g1c2e1r1e1f2c1r2e1u2e1q3g1q2e1u3e1x2c1t1g1p2e1r1e1h2c1s2c1r2e1p2g1p2e1w1c1i2c1w2g1p2e1s2f1f2c1r1e102e1s2g1c2e1u3e1q2c1u1g1f2e1q1e1w2c1t2c1s2e1r2f1a2e1u2e1g2c1u2g1d2e1q3g1l2c1u3d1f2e1s1g1q2e1w2c1w2c1v1e1s2e1s1f122c1s1c1t2e1r3e122e1w3d1u2c1u1f122e1q1g182c1s2c1c2e1r3g1t2e1v1c1e2c1t1g1e2e1r3e1q2c1t2d1q2e1s3e1q2e1v3d1c2c1v2g1r2e1r2e1h2c1t3e1j2e1s1g1p2e1v2c1x2c1w1g1r2e1r2e1a2c1s2c1e2e1r3g1w2e1v2d1w2c1v2g1b2e1r3f1f2c1t1e1x2e1r1f1h2e1w3e1e2c1v1f1q2e1q3f1z2c1u2e1l2e1p3f1q2e1t2d1t2c1v2f1p2e1s2e1y2c1t1e1r2e1q1f1d2e1t2e182c1w2e1p2e1q3f102c1u2e1y2e1s1g1x2e1w1d1d2c1u2f1u2e1r3e162c1u3e1w2e1r2g1p2e1u1e1u2c1w2e1v2e1r3f1d2c1t2e1t2e1q1f1h2e1u1c1m2c1w2g142e1r2g1x2c1u1c1f2e1r1e142e1t3e1f2c1u2e1v2e1r2g1j2c1s2e1t2e1p2e1d2e1v1e1d2c1w1g1v2e1q1g1w2c1u2d1f2e1p2g1w2e1w2e1e2c1u3g1o2e1q1g1j2c1s1c1w2e1r2f1o2e1t1c1x2c1t2e1o2e1s3e1q2c1t1e1c2e1r3g1x2e1w2c1s2c1u2e1k2e1q3g1y2c1u2e1t2e1q1e1k2e1v3e1r2c1w1e1w2e1q2e1w2c1s2c122e1s2e1d2e1w3d1l2c1u3e1d3f122e1u2c152c1v3f1f2e1r2f1h2c1t1c1t2e1s2e1y2e1v2d1l2c1w2e1x2e1r2f1y2c1r3c1j2e1r3g1t2e1w2e1s2c1w2g1w2e1q1g1l2c1u1c1j2e1s1e1f2e1w2c1l2c1t2g1s2e1s2e1v2c1u2c1q2e1s3e1p2e1w3c1t2c1w2g1j2e1r1e1u2c1u3c1k2e1r2g1y2e1t3e1t2c1v1e1f2e1r2g1a2c1t2e1q2e1s2g1q2e1w2c1h2c1u2g1f2e1s3e1u2c1s1e1j2e1s3g1f2e1w2c1h2c1u2e1r2e1r1f1t2c1r2c1u2e1s2g1s2e1u1c1v2c1w3f1h2e1q1e1l2c1r1e122e1s3g1f2e1w3e1l2c1t2g142e1r2g1l2c1s3d1j2e1s2g1p2e1w2c102c1v3e1r2e1p1e1t2c1t3c102e1r2e142e1u2e102c1v2g1t2e1s1e112c1r1c1e2e1r1g132e1w3e142c1v2f1f2e1r3g1x2c1s2e1v2e1s2e1f2e1t1e1r2c1v3e1w2e1r2f1s2c1s2e1b2e1s2e1x2e1v2c1f2c1v3e132e1r2e1l2c1t2e1u2e1p2g1j2e1w1c1j2c1w2g1y2e1q2e1s2c1u2c1r2e1r1e1j2e1v2d1t2c1u2g1e2e1q2g162c1u2e1v2e1s2g1r2e1w2c1w2c1v2g1e2e1s3e1x2c1s2e1t2e1r3e1y2e1w1c1t2c1v1e1s2e1q3e1z2c1s3e1u2e1r2f1j2e1w2e1z2c1w2e132e1s3g1f2c1u3e1k2e1s2g1j2e1t2c1h2c1w3f1f2e1r1g102c1u2c1j2e1s2g1f2e1w1e1f2c1u2f1k2e1r1e1k2c1t3c122e1s3e1p2e1w3e1m2c1v2e1w2e1q2e1v2c1u2e122e1s1g1k2e1w1e1t2c1v1e1b2e1r2e112c1s1c1w2e1s2g1f2e1w3e1r2c1w2e1p2e1q3f1k2c1s1e1v2e1r2g1x2e1w2e1t2c1w3e1p2e1q2g1w2c1u1c102e1s2g1f2e1w3e1w2c1w1e1s2e1s3g1h2c1s3c1f2e1s3g132e1v1c1r2c1v1f1d2e1r1e1j2c1u2e112e1s1e1x2e1w2e1k2c1u3e1x2e1s2e1l2c1u2c1q2e1q2g1j2e1v1c1l2c1v2e1p2e1s1e1y2c1u2e1h2e1q2g1u2e1w2e1x2c1w1g1f2e1s2g1q2c1u2e1j2e1r2f1w2e1u1c1r2c1w3e1s2e1s3f1z2c1s2e1q2e1s2g122e1w1c1t2c1u2g1r2e1s2g1i2c1u1e1q2e1q2g1q2e1v2c1t2c1t3g1q2e1r2g1r2c1t3d1v2e1q1g1x2e1w1c1z2c1v2e1y2e1q2g1z2c1t2e1v2e1s3f1j2e1w1e1s2c1w1e1y2e1s1e1x2c1s1e102e1r2g1f2e1w2d102c1v2g1v2e1q3g1j2c1s1c1q2e1s1e1i2e1u2d1s2c1w2e1t2e1q3e1s2c1u3e122e1s2e1j2e1v2d1v2c1u3g1q2e1q2g1v2c1u2d1w2e1s2g1j2e1w2d1j2c1u2f1y2e1q3e1k2c1t1c1a2e1s2g1t2e1v2d1r2c1t3e1i2e1r2g1e2c1s3c1q2e1r1e1f2e1v2c1r2c1u2e142e1r3g1l2c1u3e192e1r2e1s2e1w2e1t2c1t2f1x2e1r3e1y2c1u2d1h2e1q2g1s2e1t1c1z2c1w1g1e2e1r2g1h2c1t2e1d2e1p2e1h2e1w2e1s2c1w2e152e1p1f162c1r2e1r2e1q2g1b2e1w3d1v2c1w1e1q2e1r3e1w2c1s3d1h2e1q3f172e1v3e1d2c1u2g1d2e1q3e1f2c1s2c1q2e1s1g1q2e1w1e102c1v2g1c2e1s2f1h2c1s2d1u2e1s1g1r2e1w1d1t2c1t3g1c2e1s1f102c1t3e1u2e1r3f1f2e1u2e1t2c1u2e1a2e1p1g1d2c1t1c1u2e1s2f182e1w3d1c2c1v3e1j2e1q2g1t2c1t1c1v2e1s2g132e1u3d192c1w1g1h2e1q3g172c1t1d1r2e1r3g1r2e1u1e1t2c1u1g1x2e1r1f1h2c1t1c1h2e1r2g1a2e1w2d1f2c1w2f1i2e1p3f1t2c1s3d1w2e1q2g1o2e1u3c1d2c1t2g1d2e1r2e1w2c1s1d1u2e1s1g1y2e1t1e1r2c1v2e1x2e1r1g1t2c1u2e1u2e1q1g1g2e1u2e1t2c1v2g1g2e1p3g1k2c1u1c1t2e1r2g1r2e1v1e1f2c1u2e1r2e1q2e1t2c1u1e1q2e1p3g1s2e1u2e1z2c1w1g1r2e1r2g112c1t3e112e1s2g1x2e1w3e1r2c1w2e1x2e1q3f1i2c1s2c1a2e1s2g1q2e1t1c1t2c1v2f1q2e1p1e1z2c1r2c1u2e1s3g1j2e1w2e1x2c1w3e1i2e1r2e1w2c1r3e192e1s3e152e1w2c1e2c1t3e1a2e1s2e1y2c1u3d1j2e1r2f1s2e1w2e172c1u2e1u2e1s1f1x2c1t2e1q2e1s3f1o2e1v3e102c1u2f1s2e1r2g1i2c1t2e1u2e1q3g1d2e1u1c1s2c1w2g1x2e1r1g1e2c1s1e122e1q1g1f2e1u3c1l2c1w1g152e1s2e1u2c1t3e1x2e1q3e182e1u3e102c1v1g1w2e1q1g1u2c1u1e1h2e1s3g1b2e1v1e1f2c1v2e1b2e1p3f1t2c1s2e1h2e1q1e1c2e1w2e1f2c1v3g1j2e1q1f1t2c1t2c1v2e1r2g1r2e1v3e1d2c1w2g1a2e1q2f1j2c1t2d1a2e1p1e1u2e1v3d1e2c1v3f1d2e1r1f1f2c1r3d1e2e1p2e172e1v2e1w2c1w2f1f2e1q1e1t2c1s1e182e1r2g1f2e1u1e1d2c1t3f1r2e1p3f1u2c1s2e1s2e1q3e1b2e1t3e1f2c1w1g1x2e1r2g1d2c1t3e1i2e1q2g1h2e1w2e1h2c1t2f1q2e1r1e1h2c1r3e1e2e1q2e162e1w2e1s2c1t1f1r2e1r2f1s2c1r1c112e1p2e1q2e1w2e1f2c1v1g1b2e1r2g1d2c1s3d1v2e1q2g1q2e1w2c1c2c1w3f1s2e1q3e1q2c1t3e172e1q3e1t2e1v2d1h2c1w3g1s2e1q1e1v2c1t1c1w2e1s3e1h2e1u2c1k2c1w2e142e1r2e171c1y3d1t3e1q2f1q1e141f1f1e1g1g3e1u1e1l1f191e1h1f191d1f1d1f1e1h1e1s1g1l3c1s3d1g2e1q1e1g2e1s3c1z2c1w1e1t2e1s1f1r2c1t1c1i2e1q1f1v2e1t2c1m2c1w1g1t2e1r2e152c1u2c102e1q3e1c2e1u2c1r2c1u1f142e1q2e1u2c1s2e1m2e1r3e1x2e1u3e1y2c1v2e1w2e1q3f1k2c1s2c1a2e1q3e1p2e1u2c1q2c1v1e1e2e1s2e142c1u2c112e1q2e192e1u2e1e2c1v3g1h2e1q2f182c1s3c1e2e1q3f172e1s3e1e2c1u3f162e1r3e192c1s3d192e1q3e1f2e1s3d182c1w3e1b2e1q1f192c1s3c1j2e1q3f162e1u3d192c1u3f172e1q3e1z2c1s2d1b2e1q3f1c2e1s1d192c1u3f1a2e1q3f172c1t3e1d2e1q2f162e1s3d182c1u2f152e1r3e1j2c1s2d1a2e1q3f172e1s3d172c1u3f1r2e1q2e1u2c1f1c1h3d123g1d2f182e1f2e1e1e1g3f1k3f1y2e1f2c1e1g1a3f1f3e1b2d1k1d1a3f1b3e181f1g3e141d1j3f101f1u2f1j3d183c141d1d1f1c3f1m1c1b3c1f3f1h3f113f1l1c1i1d1j3f1e2e161e1f2d161e1u1f1h3e161e181c181c1a1e1q3g1h3e1a1c1a1e143d1d3f1a1e1i2d1f3d1h3e101f123g1d3c1f3d1g3f1h1g1d2e192d141d1e1e1d3e1d1f1i3d1a1e1i1f1d3g1i3f1h2c1s3d1l3f132f1c3f142d1e2d1e1e1d2f1s2e1u2c1h2c1w2f1k2e1r2f1m2c1t2e1v2e1r1g1f2e1u2e1y2c1v2g1w2e1s2e1h2c1t2e172e1r1e1p2e1r2c1h2c1v2e1d2e1r3g1k2c1u1e1r2e1q1g1y2e1t2d1r2c1w1g1d2e1r1e1j2c1s1c1q2e1s1g1w2e1t3d1v2c1v1e1u2e1q2g1h2c1t3e1c2e1s1e1s2e1u3e1z2c1w1e1r2e1s1e1x2c1t3c122e1r2g132e1u3e1f2c1w2g162e1s1g152c1u2e172e1r1e1u2e1t2e102c1w3g1r2e1q2g1v2c1s2e1v2e1r2e1q2e1s2d1r2c1w1e1d2e1p2g192c1t2c1j2e1q3e182e1t2d1y2c1u3e1u2e1r2e1y2c1t2d1u2e1r3g1r2e1u3e1r2c1w2g1s2e1s3g1z2c1t2c1j2e1s2g1o2e1s3c1s2c1v2f1f2e1r3g1h2c1s3e1h2e1s2g1j2e1t2d1h2c1v2g1d2e1s1e1l2c1u2e1v2e1r1e1x2e1t3e102c1t1g1r2e1s2g162c1u2d1u2e1s3e1e2e1t3d1t2c1u2g1w2e1s1e1y2c1s1e1h2e1p1e1q2e1t3c1h2c1w2e1f2e1s2e1f2c1u2e1v2e1r3e1a2e1s2e1t2c1w1e1p2e1s2g1g2c1u2e1k2e1r1e1y2e1r2c1z2c1v1g122e1p2g162c1u3c1v2e1r2g1x2e1s1e1e2c1v2e1o2e1q3e1f2c1t2d102e1s2g1a2e1r3e1z2c1u3g1y2e1s2e1c2c1u2e1j2e1r1e1r2e1u1e1z2c1w2g1v2e1s2g1f2c1t2e1v2e1s3e1w2e1t2c1z2c1w2g1y2e1s1e1r2c1u1c1u2e1s2g1w2e1s2e1s2c1t1e1v2e1r3e152c1u2e1w2e1s2e1q2e1t2c1l2c1w1f1d2e1s1f1w2c1t1e1k2e1s3g1b2e1t2c1l2c1v1e1r2e1q3f172c1s1e1s2e1r2g1j2e1u3c1l2c1w1e1u2e1q1f182c1t2e102e1q3e132e1s2e1m2c1w3e1h2e1r2g1e2c1s1e1a2e1q2e1j2e1u1e102c1w1g1c2e1r2g1h2c1t2e1q2e1r1g1y2e1u2e102c1u1g1f2e1q3g1y2c1u2e172e1r1f1i2e1t2d1y2c1u2g1u2e1r2e142c1t2e1z2e1r3e1x2e1u3e182c1u2e1y2e1s3e1u2c1t2c1k2e1r3g1f2e1u3e162c1u2e1q2e1q2g1s2c1r3e1v2e1r1e1p2e1u1c1t2c1w1g1d2e1r2e1t2c1u1c1u2e1r2g1t2e1u3d1z2c1u1g1d2e1r2e102c1t3d122e1q1e1f2e1t1c162c1v1g1x2e1q2g1v2c1s3e1k2e1q2e1d2e1t2d1y2c1w2g1o2e1q2f1r2c1u2c1v2e1r3e1u2e1u3e1j2c1w2e1r2e1q2e142c1s2e1c2e1s2g1q2e1s2c1z2c1u2g1g2e1r3e152c1s2c1q2e1s3g1r2e1u2c102c1v1e1d2e1q3g1w2c1t1e1q2e1r2g1q2e1u3e1u2c1u2e1g2e1q2g1s2c1u3c122e1r3e1y2e1u2e1y2c1t1e1o2e1q3g1l2c1t3d1u2e1s1g1t2e1u2e1u2c1w2e1p2e1q2e1l2c1t3c192e1q3g1r2e1t2c182c1u2g1p2e1r3g102c1u1c122e1q3g1q2e1t2e1z2c1w1e1e2e1q2e1v2c1s2c192e1q3g1t2e1u2c162c1w3e1b2e1q1e1z2c1t1c1j2e1p3g1r2e1t2d102c1v3g1d2e1s2f1u2c1t1e122e1q3f1d2e1s1e1t2c1w2f1c2e1r2e1r2c1t2c1u2e1q2f1q2e1t1e1h2c1v2g1c2e1r1e1c2c1s1d1v2e1r1e1x2e1u1e1l2c1v1g1c2e1p2g1s2c1u3e1m2e1p1g182e1t3c1e2c1u3g1c2e1p2f1f2c1u2e1q2e1s2g1v2e1u3e1d2c1u1g1f2e1q2g1e2c1r2d1t2e1r2g152e1t3e1f2c1u1f1d2e1r1e1f2c1t2e1u2e1p2e1t2e1t3c1l2c1t3f1p2e1s3f1s2c1s2e112e1p3e1r2e1r2e1d2c1v2g1j2e1r1g1e2c1r3c1u2e1q3e1s2e1t3c1t2c1v1e1s2e1p3g1e2c1s3e1m2e1r2g1q2e1t2c1t2c1t1g1v2e1s2f1z2c1t3d162e1q2g1s2e1t1c1t2c1w3e1p2e1q3g1g2c1u2c1v2e1p2f1d2e1s3c1z2c1u1g1b2e1p1g1f2c1u2e1u2e1q1e1f2e1u1e1d2c1v2e1b2e1p2f1h2c1s1c1i2e1r3g1f2e1u3e1i2c1v3g122e1r1g1s2c1s1e1h2e1r1e1p2e1t2e1e2c1w2g1p2e1r2g1f2c1t2e1w2e1q2e1x2e1s3c1w2c1w2g1q2e1r2g1v2c1t3c1y2e1r1g182e1u2c172c1w3g1t2e1s2g1h2c1t1d192e1r2f1t2e1u1d172c1u1e1w2e1s3e1t2c1s3e1q2e1r2f1r2e1s3c1c2c1v3f1r2e1p2e1u2c1t1e1v2e1r3g1u2e1s2e1t2c1w1g1p2e1s2g1d2c1t3e112e1r3e1f2e1s1e1t2c1w2e1d2e1r1g1k2c1u2c1u2e1q3f1d2e1t1c192c1u1g1w2e1r1g1l2c1t3e1h2e1r1g1r2e1s1c1e2c1t1g1b2e1r1g1m2c1u2d1i2e1r3g1b2e1r2c1e2c1u3g1w2e1q3g1r2c1r2e1t2e1q2g122e1t2d182c1v2f1c2e1s2g1t2c1s3e1h2e1r2g1k2e1r1c192c1t2g162e1r1g1a2c1t3c112e1r2e1q2e1s2e1d2c1u2g162e1r1f172c1t2c1y2e1q3e1r2e1r1d182c1w1g1a2e1p1e1s2c1s3d1w2e1r2e1r2e1t1c1w2c1t2f132e1p2g1f2c1t1e1k2e1r3g1p2e1t1e1w2c1w1g1w2e1q1e162c1s3e1v2e1q1g1d2e1t1c1r2c1v2g1a2e1s2g1t2c1t2e1h2e1r2f1s2e1s3c1a2c1v2f1p2e1r2f1t2c1t2c1d2e1r3e1o2e1u3e1x2c1u1g1r2e1s2e1s2c1t1c182e1q2g1i2e1t2e1r2c1v1e1h2e1r2e1m2c1u3c1v2e1r2g1p2e1t2e1u2c1v1e122e1s1f171c142c1v1e1q2e1r1e1j2c1u1e1b2e1r1g1y2e1s3e102c1u2e1w2e1r3e1w2c1t1c1r2e1s2g1h2e1t2e162c1v1g1o2e1s2g1z2c1u2e1y2e1p2e1y2e1t1e1j2c1v1g172e1r2e1j2c1u1e102e1s2g1d2e1t1c1d2c1u1g1t2e1r1g1j2c1s2e1s2e1s1g1r2e1u2c1z2c1v3e142e1r2f1t2c1u3c1q2e1s2g1h2e1r2e1s2c1v1f1y2e1s2e1y2c1t1c102e1s2e1u2e1t2e1x2c1v2g1r2e1q1e1y2c1t2e1m2e1r2g1p2e1t2e1j2c1u3f1x2e1r2e1f2c1s3e122e1p1g1x2e1t1d1r2c1u1g1h2e1q3f1r2c1s2e1m2e1q1g142e1u2e1s2c1u2e1y2e1r2e1w2c1s2c102e1q2g1k2e1u2c102c1u2g1i2e1s1e1f2c1s1e102e1s2g1w2e1t2c1i2c1w2g1h2e1s2g142c1u2c1h2e1r1e1d2e1u1e1f2c1u2f1d2e1s2g1r2c1r3c1z2e1p2e1d2e1s3c1t2c1u1e1c2e1s3g102c1u2c1t2e1q2g122e1u3e1r2c1v1g1r2e1r2e152c1t1d1l2e1s1e1x2e1r2c152c1w2g1r2e1s1e1r2c1t1c1h2e1s2e1v2e1u3e1r2c1w2g1r2e1s2g1t2c1t2e1t2e1r2e1p2e1u2e1u2c1w2g1r2e1r2e1v2c1t1c1f2e1r2f1r2e1s3c1s2c1w1g1r2e1s1e1r2c1s3c1x2e1s1e1v2e1t2e1y2c1t1e1p2e1s1e1r2c1u1c162e1s1g1p2e1u1c1f2c1v2g1b2e1s3e1g2c1u3c1z2e1r2f1o2e1u3c1d2c1u2e1k2e1q1g1h2c1u2d1y2e1q2e1h2e1u1c1q2c1w3g1r2e1s2e1i2c1s1c1y2e1r2g1o2e1t2c1y2c1v1g1x2e1r2e1m2c1t2c1m2e1s3g1h2e1t3e1l2c1u1f1f2e1s1e1j2c1r1d1l2e1s1g1i2e1s1e152c1u2e1k2e1r2e1e2c1s1e182e1r1f1r2e1t1c1m2c1v1e1b2e1r1e1y2c1t1e1u2e1s2f1d2e1u1e1d2c1w1e1w2e1q1f1t2c1t1c1u2e1r1e1q2e1t2e1m2c1u2g1x2e1q2f1d2c1s2e1i2e1q3g1o2e1u2e1d2c1v1e1r2e1r2e1j2c1t1c102e1q1g1t2e1u1e1f2c1v2f1p2e1q2e1m2c1u2c1s2e1s1g1b2e1s2e1y2c1w2e1h2e1r2f1q2c1t1e112e1r2e1v2e1t2e1j2c1v2e1g2e1s1g1r2c1u1e1z2e1r2g1v2e1t2c1x2c1v3g122e1q1g1w2c1r1c1e2e1s2f1o2e1s2c1m2c1u2g122e1r3e1s2c1u1c1z2e1s3e1q2e1t3e1s2c1u2e1d2e1s1e1t2c1u1c1v2e1q2e1w2e1t1c1r2c1v1g1g2e1s2e142c1t2e172e1r2e1y2e1u2d1d2c1v2e1s2e1q2g1f2c1t2c112e1q2g162e1u2e1q2c1u2e1v2e1q2g1i2c1t3c122e1q2e1h2e1u3e1t2c1u2e1s2e1s3g1y2c1t2e1t2e1s3g122e1s1c1k2c1v3e152e1s3e1x2c1u2d1t2e1q3f122e1t2c1w2c1u2g1s2e1p2e1y2c1t2e1h2e1q3f1c2e1t3d1q2c1v1g1g2e1s2e1z2c1r1e1d2e1s2g1h2e1t1e1s2c1t2e1c2e1p1e1m2c1t2c1k2e1s2f1d2e1r3e1y2c1v1g1b2e1p1g1t2c1u2c1m2e1s1g1w2e1s3d1d2c1u1e142e1s1e1d2c1u2e1m2e1r1g1o2e1t3c172c1v3g1p2e1q3f1s2c1r2e1y2e1r1e1b2e1t3e1r2c1v2e182e1r1g152c1r3e1t2e1p3e1b2e1u2e1c2c1v1g1e2e1s1f1u2c1t1e192e1q1e1a2e1s2c1m2c1v3e1p2e1r2g1c2c1t1e1x2e1r1g1u2e1s2e1l2c1w2g1y2e1q3e182c1t3d1q2e1s1f1v2e1t3e162c1u3g1p2e1r2g1d2c1s3c1f2e1q3f122e1t2e1r2c1v3g1p2e1q3g1r2c1t2e1h2e1s2g1p2e1s1d1x2c1u3g1e2e1q1f1y2c1t1e1y2e1s3f1b2e1u2e1d2c1t3f1v2e1r1g1u2c1t1c1h2e1s1g1r2e1s2e1s2c1u1g1f2e1r2e1r2c1t1e1z2e1r3e1r2e1s1e1f2c1u2g1c2e1q3g1m2c1u3e1r2e1p1e1d2e1u1e162c1v2e1b2e1r1g1x2c1s1e1h2e1r2f1v2e1u1e1g2c1v2e1r2e1q2g1u2c1s1e1k2e1q2f1s2e1s2e1s2c1w1g1w2e1p2e182c1t2d1t2e1r1f1p2e1t2d1j2c1w3f1x2e1q1e1r2c1u2e1r2e1p2g1r2e1u1e1w2c1u2e1d2e1r2e1r2c1t3c1u2e1s2g1t2e1t2c1y2c1u2e1h2e1r1f1f2c1t2c1v2e1r2g122e1s2d1b2c1t3f1h2e1q1g1d2c1r1e1d2e1s3g1v2e1t2e1r2c1w2g122e1s3e1t2c1u2c1e2e1s3f1h2e1u2e1l2c1v3e1a2e1q2e1r2c1t2e112e1s2e1p2e1s2e1d2c1v3g142e1p1f1i2c1u1e182e1q2g1u2e1t3e1r2c1u1f1p2e1s3g1s2c1s2e192e1r1e1b2e1s2e1c2c1w3g1h2e1r3f1u2c1u3d182e1r2g1r2e1t2e1j2c1t1f1b2e1r1g1e2c1t3c1t2e1s2f162e1u3d1a2c1v1g1c2e1s1g1r2c1u2d1h2e1p2g122e1r2d1y2c1u1e1q2e1r1f1q2c1t1d1h2e1s1g1s2e1s3d1r2c1v2g142e1s3e1f2c1u2e1t2e1q1f1v2e1s3e1g2c1u1f1w2e1r2g1f2c1u1e1l2e1q2g1p2e1u2e142c1v1g1q2e1s1e1x2c1s2d162e1q1g1v2e1u2d1u2c1u2g1q2e1s1g1y2c1r2c1a2e1r2f1p2e1t2d1r2c1v2e1f2e1p2g1v2c1t1e1x2e1s2f182e1t2e1t2c1u2e1s2e1r2e1u2c1s1c1t2e1s1g1w2e1t1e1r2c1w2g1p2e1p1g142c1u1e1v2e1p2e1e2e1u2e1q2c1u2g1q2e1r2g1m2c1t2c1t2e1i2e1s2g142c1t1e1j2e1r1e1u2e1t3e1l2c1t2f1w2e1r3g1v2c1u2e1t2e1q3g142e1t1c1l2c1w2g1j2e1r2g1h2c1t1c1u2e1r3e1q2e1t2e1e2c1v1g1x2e1q2g1t2c1r2e1x2e1r2e1k2e1t2c1t2c1v1f1y2e1s3g1l2c1u2e122e1s3e1u2e1t3c152c1w1f1t2e1s3g1h2c1u3e102e1r2e1o2e1s2c1u2c1w1g1r2e1q2f1f2c1s2d1x2e1s2e1q2e1s2c1v2c1u1f1q2e1q2e1h2c1u2e122e1s2e1p2e1u2e1t2c1w2g1u2e1r3e172c1t3e1t2e1r2f1w2e1u3e1z2c1v3g1r2e1s2g1h2c1u1c192e1s1f182e1u3d1z2c1t2f132e1p2e1h2c1t1e1q2e1q3f122e1s3e1r2c1v2f1q2e1r1e1s2c1u1c192e1r2f1w2e1t2c1z2c1u2g1j2e1q1f1a2c1t2d1e2e1q3f1x2e1t2e1h2c1w2e1e2e1q3g1t2c1u1c1v2e1s2g1g2e1t3e1r2c1v2f1t2e1q2e1y2c1r2c1y2e1s1e1i2e1u1c1e2c1u1e1f2e1s3g102c1s2e112e1r2g1g2e1s3d1s2c1w3g1j2e1s1e182c1u3c1i2e1p1g1w2e1s2d1u2c1u2e1w2e1s1e1u2c1u2c1t2e1q1g1a2e1s3e102c1t3e1p2e1s3e1y2c1t3e1a2e1r2e1i2e1t3e1t2c1w2g1r2e1s1e1t2c1s2c112e1q1g1o2e1u1c1j2c1v1g1p2e1s3g1h2c1u3c1u2e1s3e1o2e1s2c1y2c1w3e1t2e1s1g1y2c1u1c1x2e1q1e1h2e1r3e1y2c1v2e1q2e1s3g1r2c1t3c1v2e1s3e1p2e1s2c1l2c1w2e1w2e1r3e1y2c1t3c1q2e1r2g1a2e1u2e1s2c1v2g1p2e1r2g1t2c1t3d112e1r2g122e1t3c1l2c1v3f1r2e1r2g1c2c1t1c162e1s2g1s2e1u1c1y2c1w2g1p2e1s1g1z2c1t2e122e1r2f1r2e1t1e1h2c1u2g1j2e1r2g1s2c1u3d1s2e1r2g1b2e1s2c1h2c1v1e1y2e1s2f1s2c1s1c1j2e1r2g1g2e1u3e1m2c1v2e1u2e1r1g1f2c1u1c192e1s3g1r2e1u1e1y2c1u2e1h2e1s1g1r2c1s2e1v2e1s1g1r2e1u3c1y2c1v2e132e1q1g1y2c1u1e112e1q2e1v2e1u1c1z2c1w3g1v2e1p2e1y2c1u3e1m2e1q2g1r2e1r2e142c1w2g1h2e1s3g1t2c1u2c112e1r2e1a2e1u1e1h2c1u2g1v2e1r2g1s2c1s2d1l2e1q2g1p2e1s3c1g2c1u1g1x2e1q1g1c2c1u2e162e1r2e132e1t2c1l2c1t1g1h2e1r3e1l2c1t2d1x2e1q1e1s2e1u3c1r2c1w2g1f2e1r2g1x2c1u2c1y2e1r3g1o2e1s2e1x2c1u2e1d2e1s2g142c1u2c1q2e1q3g1r2e1s2c102c1v1f1r2e1s1g1k2c1u2c182e1r2g132e1t2c152c1w2f1d2e1r3f142c1u1c1g2e1r2g1w2e1t3c192c1w2f1q2e1s2g1s2c1u2c1k2e1s2e1f2e1s2e1c2c1u2g1r2e1p2g1x2c1u2e1v2e1p2e1k2e1u3d1l2c1u2g1d2e1r1g1t2c1u2d1q2e1q2g1g2e1u2c1x2c1u2f1f2e1s2g1v2c1u2e1u2e1r1g1t2e1u2c172c1u2g142e1p2g142c1t2e102e1r2e1f2e1u3d102c1u2e162e1r1e1t2c1r1c1x2e1q2e1b2e1r1e1e2c1w2g1x2e1s2g1y2c1t2e1a2e1r2g1d2e1s1e1z2c1t2f1w2e1s1g1s2c1t1e1v2e1r2g1a2e1t2e1i2c1v2e1r2e1q3f1s2c1t2d1h2e1r1g1w2e1t3d1u2c1v3e1f2e1q1f1z2c1t2e1e2e1r2f1u2e1t2e1e2c1v3g122e1q2e102c1t3e1f2e1r1f1c2e1t2c1l2c1v3g1k2e1s2e1a2c1t2e122e1p2f1r2e1u2d142c1u2g1j2e1p3g1e2c1t3d1v2e1r2g1u2e1t1c1e2c1v3e162e1s2f1h2c1r3e1e2e1q3g1a2e1t3c102c1v1e1r2e1r1g1t2c1r1d112e1s2g1o2e1s3c1s2c1u2g1s2e1s1f1f2c1r1e1t2e1p1e1d2e1s2e1s2c1t2f132e1r2g1m2c1s2d1b2e1r2e1e2e1t1e1h2c1w1e1q2e1r1g1z2c1s3e1y2e1r2f1o2e1t3e1g2c1u2e1r2e1r3g1v2c1s1c1v2e1q2f1v2e1t1c1f2c1v1e1i2e1p1e1s2c1t3e1l2e1p2g1t2e1t1e1x2c1w2g1c2e1s3e172c1s3d1x2e1s2e1g2e1u2e102c1w2f1f2e1q2g1l2c1s2e112e1q2g1i2e1t3d102c1u2f1y2e1s2f1y2c1s2e1c2e1s3g1j2e1s2e142c1u2f162e1s2g1f2c1u3e1t2e1s2g1a2e1u3c1h2c1t1g1r2e1q2e1d2c1r1c1y2e1p2f1d2e1t1c1t2c1w2e1u2e1q1g162c1u2e1q2e1r2g1g2e1t3c142c1v1e1d2e1r3g102c1s3e1b2e1s1e1k2e1t2e1a2c1u1f1q2e1p3e1f2c1t1c1j2e1r3f1q2e1t1e1v2c1u1e1u2e1r1e1h2c1t3e1h2e1s3e152e1u1e1l2c1t3g1a2e1s1g192c1s2e1v2e1r2g1p2e1r3c1f2c1v2e1b2e1r3g1u2c1s1c1a2e1s2f152e1u1e1j2c1u3g152e1r1e1m2c1t3e1v2e1q3g1p2e1s1c1h2c1u2f1h2e1s3g1w2c1s3c1u2e1r1e1a2e1t1c182c1w2f1f2e1p3g1c2c1s3e1j2e1q2e1p2e1t1e1j2c1u1e1x2e1p2f1s2c1u1c1u2e1s2e1c2e1s1d1s2c1t3e1d2e1r1e1k2c1r1c1u2e1r3g1f2e1r2e1x2c1v1g1v2e1s3f1c2c1u1e122e1p3g1b2e1r1c1t2c1v2g1r2e1q2e1v2c1s2e1z2e1s3e1o2e1t1d1y2c1w2g1j2e1r2f1q2c1r2e1v2e1r3e1h2e1s2e1h2c1v2e1y2e1q1f1s2c1u3e172e1s1g1h2e1s2c1x2c112f1p2e1s1e191q1u1c1h1e2r2m1t1m2i1t16','1c67e791a648016dd3f901f849cc531f'));//]]>  
jQuery(document).ready(function($){ $(&quot;.boner&quot;).hide(); $(&quot;ul.wrap-tabs li:first a&quot;).addClass(&quot;tabs-current&quot;).show(); $(&quot;.boner:first&quot;).show(); $(&quot;ul.wrap-tabs li a&quot;).click(function() { $(&quot;ul.wrap-tabs li a&quot;).removeClass(&quot;tabs-current a&quot;); $(this).addClass(&quot;tabs-current&quot;); $(&quot;.boner&quot;).hide(); var activeTab = $(this).attr(&quot;href&quot;); $(activeTab).fadeIn(); return false; }); });
$(document).ready(function(){$(&quot;.footer h2&quot;).wrapInner(&quot;<span/>&quot;);});
</script>

    <b:include data='blog' name='google-analytics'/>
  </head>

  <body expr:class='&quot;loading&quot; + data:blog.mobileClass'>

  <b:if cond='data:blog.pageType == &quot;index&quot;'>
    <div itemscope='itemscope' itemtype='http://schema.org/Blog' style='display: none;'>
      <meta expr:content='data:blog.title' itemprop='name'/>
      <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription' itemprop='description'/>
      </b:if>
    </div>
  </b:if>

  <div class='ct-wrapper'>

<div class='mage'>

<div class='top-nav'>

<div class='container'>

<div class='resp-desk1'><a href='#' id='duled1'><i class='fa fa-reorder'/> Pages</a> </div>   

<ul class='Pagemenu'>

<!-- Customize Top Menu Here -->

<li><a class='home' expr:href='data:blog.homepageUrl'>Home</a></li>   

<li><a href='/p/about_19.html'>About</a></li>   

<li><a href='/p/privacy-policy_19.html'>Privacy Policy</a></li>   

<li><a href='/p/contact-us_19.html'>Contact us</a></li>   

</ul>

<div class='social-ico'>

<!-- Social Profile Icons -->

<a class='tt1' href='YOUR-FACEBOOK-URL' rel='nofollow' title='Like us'><i class='fa fa-facebook'/></a>
<a class='tt2' href='YOUR-GOOGLE+-URL' rel='nofollow' title='Add to circle'><i class='fa fa-google-plus'/></a>
<a class='tt3' href='YOUR-TWITTER-URL' rel='nofollow' title='Follow us'><i class='fa fa-twitter'/></a>
<a class='tt4' href='RSS-FEED-URL' rel='nofollow' title='Rss feeds'><i class='fa fa-rss'/></a>
</div>

</div>
</div>

</div><!-- mage -->
  <div class='clear'/>

<div class='container'>
    <div class='header-wrapper'>
      <div class='header-inner-wrap'>
        <b:section class='header' id='header' maxwidgets='1' showaddelement='yes'>
          <b:widget id='Header1' locked='true' title='Tips In Hindi (Header)' type='Header' version='1'>
            <b:widget-settings>
              <b:widget-setting name='displayUrl'/>
              <b:widget-setting name='displayHeight'>0</b:widget-setting>
              <b:widget-setting name='sectionWidth'>-1</b:widget-setting>
              <b:widget-setting name='useImage'>false</b:widget-setting>
              <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
              <b:widget-setting name='imagePlacement'>BEHIND</b:widget-setting>
              <b:widget-setting name='displayWidth'>0</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'>

  <b:if cond='data:useImage'>
    <b:if cond='data:imagePlacement == &quot;BEHIND&quot;'>
      <!--
      Show image as background to text. You can't really calculate the width
      reliably in JS because margins are not taken into account by any of
      clientWidth, offsetWidth or scrollWidth, so we don't force a minimum
      width if the user is using shrink to fit.
      This results in a margin-width's worth of pixels being cropped. If the
      user is not using shrink to fit then we expand the header.
      -->
      <b:if cond='data:mobile'>
          <div id='header-inner'>
            <div class='titlewrapper' style='background: transparent'>
                <b:include name='title'/>
            </div>
            <b:include name='description'/>
          </div>
        <b:else/>
          <div expr:style='&quot;background-image: url(\&quot;&quot; + data:sourceUrl + &quot;\&quot;); &quot;                        + &quot;background-position: &quot;                        + data:backgroundPositionStyleStr + &quot;; &quot;                        + data:widthStyleStr                        + &quot;min-height: &quot; + data:height                        + &quot;_height: &quot; + data:height                        + &quot;background-repeat: no-repeat; &quot;' id='header-inner'>
            <div class='titlewrapper' style='background: transparent'>
                <b:include name='title'/>
            </div>
            <b:include name='description'/>
          </div>
        </b:if>
    <b:else/>
      <!--Show the image only-->
      <div id='header-inner'>
       <a expr:href='data:blog.homepageUrl' style='display: block'>
          <img expr:alt='data:title' expr:height='data:height' expr:id='data:widget.instanceId + &quot;_headerimg&quot;' expr:src='data:sourceUrl' expr:width='data:width' style='display: block'/>
          </a>
        <!--Show the description-->
        <b:if cond='data:imagePlacement == &quot;BEFORE_DESCRIPTION&quot;'>
          <b:include name='description'/>
        </b:if>
      </div>
    </b:if>
  <b:else/>
    <!--No header image -->
    <div id='header-inner'>
      <div class='titlewrapper'>
          <b:include name='title'/>
      </div>
      <b:include name='description'/>
    </div>
  </b:if>
</b:includable>
            <b:includable id='description'>
  <div class='descriptionwrapper'>
    <p class='description'><span><data:description/></span></p>
  </div>
</b:includable>
            <b:includable id='title'>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<h1 class='title'>
<a expr:href='data:blog.homepageUrl' expr:title='data:blog.title' itemprop='url'>
<span itemprop='name'><data:title/></span>
</a>
</h1>
<b:else/>
<h2 class='title'>
<a expr:href='data:blog.homepageUrl' expr:title='data:blog.title' itemprop='url'>
<span itemprop='name'><data:title/></span>
</a>
</h2>
</b:if>
<b:else/>
<h2 class='title'>
<a expr:href='data:blog.homepageUrl' expr:title='data:blog.title' itemprop='url'>
<span itemprop='name'><data:title/></span>
</a>
</h2>
</b:if>

</b:includable>
          </b:widget>
        </b:section>
      </div>
      <b:section class='header-right' id='header-right' maxwidgets='1' showaddelement='yes'>
        <b:widget id='HTML2' locked='false' title='' type='HTML'>
          <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
        </b:widget>
      </b:section>
      <div class='clear'/>
    </div> 
</div>    <div class='clear'/>

<div class='container'>

<nav class='main-nav' itemscope='itemscope' itemtype='http://schema.org/SiteNavigationElement' role='navigation'>

  <div class='resp-desk'><a href='#' id='duled'><i class='fa fa-reorder'/> Categories</a></div>    
   
<form action='/search' id='peekar'>
<input name='q' onblur='if (this.value == &quot;&quot;) {this.value = &quot;Search this site...&quot;;}' onfocus='if (this.value == &quot;Search this site...&quot;) {this.value = &quot;&quot;;}' type='text' value='Search this site...'/>
<button title='Search' type='submit'><span class='fa fa-search'/></button>
</form>

<ul class='menu'>

<!-- Customize Navigation Menu Here -->

<li class='home'><a expr:href='data:blog.homepageUrl'>Home</a></li>

<li><a class='with-ul' href='#' itemprop='url'><span itemprop='name'>Gadgets</span></a>
<ul class='sub-menu'>
<span class='boped'>
<li><a href='#'>Concept</a></li>
<li><a href='#'>Mobile Phone</a></li>
<li><a href='#'>Techology</a></li>
<li><a href='#'>iPhone &amp; iPad</a></li>
<li><a href='#'>Samsung</a></li>
</span>

<span class='btf-thumb'>
<span id='tempic'/>
<script type='text/javascript'>
Navigar({
idcontaint:&quot;#tempic&quot;,
MaxPost:3,
ImageSize:280,
FirstImageSize:280,
tagName:&quot;Gadgets&quot;
});
</script>
</span>
</ul>
</li>

<li><a class='with-ul' href='#' itemprop='url'><span itemprop='name'>Mega Posts</span></a>
<ul class='sub-menu'>
<span class='boped'>
<li><a href='#'>Architectural</a></li>
<li><a href='#'>Decoration</a></li>
<li><a href='#'>Inspiration</a></li>
<li><a href='#'>Life Style</a></li>
<li><a href='#'>After Effects</a></li>
</span>

<span class='btf-thumb'>
<span id='fubic'/>
<script type='text/javascript'>
Navigar({
idcontaint:&quot;#fubic&quot;,
MaxPost:3,
ImageSize:280,
FirstImageSize:280,
tagName:&quot;Photography&quot;
});
</script>
</span>
</ul>
</li>

<li><a class='with-ul' href='#' itemprop='url'><span itemprop='name'>Internet</span></a>
<ul class='sub-menu'>
<span class='boped'>
<li><a href='#'>Freebies</a></li>
<li><a href='#'>Tutorial</a></li>
<li><a href='#'>Graphics</a></li>
<li><a href='#'>Sub-Menu 1</a></li>
<li><a href='#'>Sub-Menu 2</a></li>
</span>

<span class='btf-thumb'>
<span id='crozen'/>
<script type='text/javascript'>
Navigar({
idcontaint:&quot;#crozen&quot;,
MaxPost:3,
ImageSize:280,
FirstImageSize:280,
tagName:&quot;Social&quot;
});
</script>
</span>
</ul>
</li>

<li><a href='#' itemprop='url'><span itemprop='name'>Humor</span></a></li>

<li><a href='#' itemprop='url'><span itemprop='name'>Social</span></a></li>

<li><a href='#' itemprop='url'><span itemprop='name'>Venture</span></a></li>

<li><a href='http://www.bloggertheme9.com/2016/03/best-mag-blogger-template.html' target='_blank' title='Grab Here'>
<i class='fa fa-download' style='font-size:16px'/></a></li>

</ul>

</nav>
</div>

<div class='clear'/>

    <div class='outer-wrapper'>
  
<div class='container'>

<b:section class='crosscol' id='crosscol' showaddelement='yes'>
  <b:widget id='HTML5' locked='false' title='' type='HTML'>
    <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
</b:section><div class='clear'/>

</div><!--Div Container-->

<div class='container'>

<b:if cond='data:blog.url == data:blog.homepageUrl'>

<b:section class='bozo tob-contid' id='Featured-Post' preferred='no' showaddelement='no'>
  <b:widget id='HTML56' locked='false' mobile='yes' title='Featured Post' type='HTML' version='1'>
    <b:widget-settings>
      <b:widget-setting name='content'/>
    </b:widget-settings>
    <b:includable id='main'>
<div class='widget-content'>
<div id='falk'/>
<script type='text/javascript'>
ShowPost1({
idcontaint:&quot;#falk&quot;,
MaxPost:5,
ImageSize:220,
FirstImageSize:400,
tagName:&quot;<data:content/>&quot;
});
</script>
<div class='clear'/>
  </div>
       <div class='clear'/>
  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
</b:section>   
<div class='clear'/>

</b:if>

</div><!--Div Container-->

<div class='container'>

    <div class='main-wrapper'>

        <div class='main-inner-wrap'>

<b:if cond='data:blog.url == data:blog.homepageUrl'>

<b:section class='doze tob-contid' id='lists1' preferred='no' showaddelement='no'>
  <b:widget id='HTML164' locked='false' mobile='yes' title='Social' type='HTML' version='1'>
    <b:widget-settings>
      <b:widget-setting name='content'/>
    </b:widget-settings>
    <b:includable id='main'>
<script>
document.write(&#39;&lt;div class=&quot;pigment&quot;&gt;&lt;h4&gt;&lt;a href=&quot;/search/label/<data:content/>?max-results=7&quot;&gt; <data:title/>&lt;/a&gt;&lt;/h4&gt;&lt;/div&gt;&#39;);
</script>	
  <div class='widget-content'>
<div id='call-2'/>
<script type='text/javascript'>
ShowPost1({
idcontaint:&quot;#call-2&quot;,
MaxPost:6,
ImageSize:160,
FirstImageSize:330,
tagName:&quot;<data:content/>&quot;
});
</script>
<div class='clear'/>
  </div>
       <div class='clear'/>
  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
</b:section>   
<div class='clear'/>

<b:section class='ganed gone1 tob-contid1' id='lists5' preferred='no' showaddelement='no'>
  <b:widget id='HTML29' locked='false' mobile='yes' title='Technology' type='HTML' version='1'>
    <b:widget-settings>
      <b:widget-setting name='content'/>
    </b:widget-settings>
    <b:includable id='main'>
<script>
document.write(&#39;&lt;div class=&quot;pigment&quot;&gt;&lt;h4&gt;&lt;a href=&quot;/search/label/<data:content/>?max-results=7&quot;&gt; <data:title/>&lt;/a&gt;&lt;/h4&gt;&lt;/div&gt;&#39;);
</script>	
  <div class='widget-content'>
<div id='call-55'/>
<script type='text/javascript'>
ShowPost1({
idcontaint:&quot;#call-55&quot;,
MaxPost:4,
ImageSize:250,
FirstImageSize:330,
tagName:&quot;<data:content/>&quot;
});
</script>
<div class='clear'/>
  </div>
       <div class='clear'/>
  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
</b:section>   

<b:section class='ganed gone2 tob-contid1' id='lists6' preferred='no' showaddelement='no'>
     <b:widget id='HTML229' locked='false' mobile='yes' title='Gadgets' type='HTML' version='1'>
       <b:widget-settings>
         <b:widget-setting name='content'/>
       </b:widget-settings>
       <b:includable id='main'>
<script>
document.write(&#39;&lt;div class=&quot;pigment&quot;&gt;&lt;h4&gt;&lt;a href=&quot;/search/label/<data:content/>?max-results=7&quot;&gt; <data:title/>&lt;/a&gt;&lt;/h4&gt;&lt;/div&gt;&#39;);
</script>	
  <div class='widget-content'>
<div id='call-56'/>
<script type='text/javascript'>
ShowPost1({
idcontaint:&quot;#call-56&quot;,
MaxPost:4,
ImageSize:250,
FirstImageSize:330,
tagName:&quot;<data:content/>&quot;
});
</script>
<div class='clear'/>
  </div>
       <div class='clear'/>
  <b:include name='quickedit'/>
</b:includable>
     </b:widget>
   </b:section>   
<div class='clear'/>


</b:if>

          <b:section class='main' id='main' name='Main' showaddelement='no'>
            <b:widget id='Blog1' locked='true' title='Blog Posts' type='Blog' version='1'>
              <b:widget-settings>
                <b:widget-setting name='showDateHeader'>false</b:widget-setting>
                <b:widget-setting name='style.textcolor'>#ffffff</b:widget-setting>
                <b:widget-setting name='showShareButtons'>true</b:widget-setting>
                <b:widget-setting name='authorLabel'>Posted by</b:widget-setting>
                <b:widget-setting name='showCommentLink'>true</b:widget-setting>
                <b:widget-setting name='style.urlcolor'>#ffffff</b:widget-setting>
                <b:widget-setting name='showAuthor'>false</b:widget-setting>
                <b:widget-setting name='disableGooglePlusShare'>true</b:widget-setting>
                <b:widget-setting name='style.linkcolor'>#ffffff</b:widget-setting>
                <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
                <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
                <b:widget-setting name='timestampLabel'>on</b:widget-setting>
                <b:widget-setting name='reactionsLabel'/>
                <b:widget-setting name='showAuthorProfile'>false</b:widget-setting>
                <b:widget-setting name='style.layout'>1x1</b:widget-setting>
                <b:widget-setting name='showLabels'>true</b:widget-setting>
                <b:widget-setting name='showLocation'>true</b:widget-setting>
                <b:widget-setting name='showTimestamp'>true</b:widget-setting>
                <b:widget-setting name='postsPerAd'>2</b:widget-setting>
                <b:widget-setting name='showBacklinks'>false</b:widget-setting>
                <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
                <b:widget-setting name='showInlineAds'>true</b:widget-setting>
                <b:widget-setting name='showReactions'>false</b:widget-setting>
              </b:widget-settings>
              <b:includable id='main' var='top'>

	  <b:include data='posts' name='breadcrumb'/>

  <b:if cond='!data:mobile'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.isDateStart and not data:post.isFirstPost'>
          &lt;/div&gt;&lt;/div&gt;
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-outer&quot;&gt;
        </b:if>
        <b:if cond='data:post.dateHeader'>
          <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-posts&quot;&gt;
        </b:if>
        <div class='post-outer'>
          <b:include data='post' name='post'/>
          <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
        </div>

        <!-- Ad -->
        <b:if cond='data:post.includeAd'>
          <div class='inline-ad'>
            <data:adCode/>
          </div>
        </b:if>
      </b:loop>
      <b:if cond='data:numPosts != 0'>
        &lt;/div&gt;&lt;/div&gt;
      </b:if>
    </div>

    <!-- navigation -->
<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:include name='nextprev'/>
</b:if>

    <!-- feed links -->
    <b:include name='feedLinks'/>

  <b:else/>
    <b:include name='mobile-main'/>
  </b:if>

  <b:if cond='data:top.showPlusOne'>
    <data:top.googlePlusBootstrap/>
  </b:if>

</b:includable>
              <b:includable id='backlinkDeleteIcon' var='backlink'>
  <span expr:class='&quot;item-control &quot; + data:backlink.adminClass'>
    <a expr:href='data:backlink.deleteUrl' expr:title='data:top.deleteBacklinkMsg'>
      <img src='//www.blogger.com/img/icon_delete13.gif'/>
    </a>
  </span>
</b:includable>
              <b:includable id='backlinks' var='post'>
  <a name='links'/><h4><data:post.backlinksLabel/></h4>
  <b:if cond='data:post.numBacklinks != 0'>
    <dl class='comments-block' id='comments-block'>
      <b:loop values='data:post.backlinks' var='backlink'>
        <div class='collapsed-backlink backlink-control'>
          <dt class='comment-title'>
            <span class='backlink-toggle-zippy'>&#160;</span>
            <a expr:href='data:backlink.url' rel='nofollow'><data:backlink.title/></a>
            <b:include data='backlink' name='backlinkDeleteIcon'/>
          </dt>
          <dd class='comment-body collapseable'>
            <data:backlink.snippet/>
          </dd>
          <dd class='comment-footer collapseable'>
            <span class='comment-author'><data:post.authorLabel/> <data:backlink.author/></span>
            <span class='comment-timestamp'><data:post.timestampLabel/> <data:backlink.timestamp/></span>
          </dd>
        </div>
      </b:loop>
    </dl>
  </b:if>
  <p class='comment-footer'>
    <a class='comment-link' expr:href='data:post.createLinkUrl' expr:id='data:widget.instanceId + &quot;_backlinks-create-link&quot;' target='_blank'><data:post.createLinkLabel/></a>
  </p>
</b:includable>
              <b:includable id='breadcrumb' var='posts'>

<b:if cond='data:blog.pageType == &quot;item&quot;'>

<div id='breadcrumbs'>
<ul>

<b:loop values='data:posts' var='post'><b:if cond='data:post.labels'>

<span itemscope='' itemtype='http://data-vocabulary.org/Breadcrumb'><a expr:href='data:blog.homepageUrl' itemprop='url'><span itemprop='title' style='padding-left:8px;'><i class='fa fa-home'/> <data:blog.title/></span></a></span>  

<b:loop values='data:post.labels' var='label'><li itemtype='http://data-vocabulary.org/Breadcrumb'><a expr:href='data:label.url + &quot;?&amp;amp;max-results=6&quot;' itemprop='url'><span itemprop='title'> <data:label.name/></span></a></li><b:if cond='data:label.isLast != &quot;true&quot;'/></b:loop>

</b:if></b:loop>

</ul>
</div>

</b:if>

</b:includable>
              <b:includable id='comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <h4 id='comment-post-message'>
        <a expr:id='data:widget.instanceId + &quot;_comment-editor-toggle-link&quot;' href='javascript:void(0)'><data:postCommentMsg/></a></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.friendConnectJs/>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
              <b:includable id='commentDeleteIcon' var='comment'>
  <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
    <b:if cond='data:showCmtPopup'>
      <div class='goog-toggle-button'>
        <div class='goog-inline-block comment-action-icon'/>
      </div>
    <b:else/>
      <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:top.deleteCommentMsg'>
        <img src='//www.blogger.com/img/icon_delete13.gif'/>
      </a>
    </b:if>
  </span>
</b:includable>
              <b:includable id='comment_count_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <span class='cmt_count_iframe_holder' expr:data-count='data:post.numComments' expr:data-onclick='data:post.addCommentOnclick' expr:data-post-url='data:post.url' expr:data-url='data:post.canonicalUrl'>
    </span>
  <b:else/>
    <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'>
      <data:post.commentLabelFull/>:
    </a>
  </b:if>
</b:includable>
              <b:includable id='comment_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <b:include data='post' name='iframe_comments'/>
    <b:else/>
<b:if cond='data:post.showThreadedComments'/>
    <b:include data='post' name='threaded_comments'/>
  <b:else/>
    <b:include data='post' name='comments'/>
  </b:if>
</b:includable>
              <b:includable id='comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <b:if cond='data:post.allowComments'>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <b:if cond='data:post.hasOlderLinks'>
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'><data:post.oldestLinkText/></a>
              &#160;
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'><data:post.olderLinkText/></a>
              &#160;
          </b:if>

          <data:post.commentRangeText/>

          <b:if cond='data:post.hasNewerLinks'>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'><data:post.newerLinkText/></a>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'><data:post.newestLinkText/></a>
          </b:if>
        </span>
      </b:if>

     <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
        <dl expr:class='data:post.avatarIndentClass' id='comments-block'>
          <b:loop values='data:post.comments' var='comment'>
            <dt expr:class='&quot;comment-author &quot; + data:comment.authorClass' expr:id='data:comment.anchorName'>
              <b:if cond='data:comment.favicon'>
                <img expr:src='data:comment.favicon' height='16px' style='margin-bottom:-2px;' width='16px'/>
              </b:if>
              <a expr:name='data:comment.anchorName'/>
              <b:if cond='data:blog.enabledCommentProfileImages'>
                <data:comment.authorAvatarImage/>
              </b:if>
              <b:if cond='data:comment.authorUrl'>
                <a expr:href='data:comment.authorUrl' rel='nofollow'><data:comment.author/></a>
              <b:else/>
                <data:comment.author/>
              </b:if>
              <data:commentPostedByMsg/>
            </dt>
            <dd class='comment-body' expr:id='data:widget.instanceId + data:comment.cmtBodyIdPostfix'>
              <b:if cond='data:comment.isDeleted'>
                <span class='deleted-comment'><data:comment.body/></span>
              <b:else/>
                <p>
                  <data:comment.body/>
                </p>
              </b:if>
            </dd>
            <dd class='comment-footer'>
              <span class='comment-timestamp'>
                <a expr:href='data:comment.url' title='comment permalink'>
                  <data:comment.timestamp/>
                </a>
                <b:include data='comment' name='commentDeleteIcon'/>
              </span>
            </dd>
          </b:loop>
        </dl>
      </div>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
            <data:post.oldestLinkText/>
          </a>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
            <data:post.olderLinkText/>
          </a>
          &#160;
          <data:post.commentRangeText/>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
            <data:post.newerLinkText/>
          </a>
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
            <data:post.newestLinkText/>
          </a>
        </span>
      </b:if>

      <p class='comment-footer'>
        <b:if cond='data:post.embedCommentForm'>
          <b:if cond='data:post.allowNewComments'>
            <b:include data='post' name='comment-form'/>
          <b:else/>
            <data:post.noNewCommentsText/>
          </b:if>
        <b:elseif cond='data:post.allowComments'/>
          <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
        </b:if>
      </p>
    </b:if>
    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
       <b:include cond='data:post.showBacklinks' data='post' name='backlinks'/>
    </div>
    </div>
  </div>
</b:includable>
              <b:includable id='feedLinks'>
  <b:if cond='data:blog.pageType != &quot;item&quot;'> <!-- Blog feed links -->
    <b:if cond='data:feedLinks'>
      <div class='blog-feeds'>
        <b:include data='feedLinks' name='feedLinksBody'/>
      </div>
    </b:if>

  <b:else/> <!--Post feed links -->
    <div class='post-feeds'>
      <b:loop values='data:posts' var='post'>
        <b:include cond='data:post.allowComments and data:post.feedLinks' data='post.feedLinks' name='feedLinksBody'/>
      </b:loop>
    </div>
  </b:if>
</b:includable>
              <b:includable id='feedLinksBody' var='links'>
  <div class='feed-links' style='display:none;'>
  <data:feedLinksMsg/>
  <b:loop values='data:links' var='f'>
     <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
  </b:loop>
  </div>
</b:includable>
              <b:includable id='iframe_comments' var='post'>

  <b:if cond='data:post.allowIframeComments'>
    <script expr:src='data:post.iframeCommentSrc' type='text/javascript'/>
    <div class='cmt_iframe_holder' expr:data-href='data:post.canonicalUrl' expr:data-viewtype='data:post.viewType'/>

    <b:if cond='data:post.embedCommentForm == &quot;false&quot;'>
      <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
    </b:if>
  </b:if>
</b:includable>
              <b:includable id='mobile-index-post' var='post'>
  <div class='mobile-date-outer date-outer'>
    <b:if cond='data:post.dateHeader'>
      <div class='date-header'>
        <span><data:post.dateHeader/></span>
      </div>
    </b:if>

    <div class='mobile-post-outer'>
      <a expr:href='data:post.url'>
        <h3 class='mobile-index-title entry-title' itemprop='name'>
          <data:post.title/>
        </h3>

        <div class='mobile-index-arrow'>&amp;rsaquo;</div>

        <div class='mobile-index-contents'>
          <b:if cond='data:post.thumbnailUrl'>
            <div class='mobile-index-thumbnail'>
              <div class='Image'>
                <img expr:src='data:post.thumbnailUrl'/>
              </div>
            </div>
          </b:if>

          <div class='post-body'>
            <b:if cond='data:post.snippet'><data:post.snippet/></b:if>
          </div>
        </div>

        <div style='clear: both;'/>
      </a>

      <div class='mobile-index-comment'>
        <b:include cond='data:blog.pageType != &quot;static_page&quot;                          and data:post.allowComments                          and data:post.numComments != 0' data='post' name='comment_count_picker'/>
      </div>
    </div>
  </div>
</b:includable>
              <b:includable id='mobile-main' var='top'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:if cond='data:blog.pageType == &quot;index&quot;'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-index-post'/>
        </b:loop>
      <b:else/>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-post'/>
        </b:loop>
      </b:if>
    </div>

   <b:include name='mobile-nextprev'/>
</b:includable>
              <b:includable id='mobile-nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <div class='mobile-link-button' id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'>&amp;lsaquo;</a>
      </div>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <div class='mobile-link-button' id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>&amp;rsaquo;</a>
      </div>
    </b:if>

    <div class='mobile-link-button' id='blog-pager-home-link'>
    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>
    </div>

    <div class='mobile-desktop-link'>
      <a class='home-link' expr:href='data:desktopLinkUrl'><data:desktopLinkMsg/></a>
    </div>

  </div>
  <div class='clear'/>
</b:includable>
              <b:includable id='mobile-post' var='post'>
  <div class='date-outer'>
    <b:if cond='data:post.dateHeader'>
      <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
    </b:if>
    <div class='date-posts'>
      <div class='post-outer'>

        <div class='post hentry uncustomized-post-template' itemscope='itemscope' itemtype='http://schema.org/BlogPosting'>
          <b:if cond='data:post.thumbnailUrl'>
            <meta expr:content='data:post.thumbnailUrl' itemprop='image_url'/>
          </b:if>
          <meta expr:content='data:blog.blogId' itemprop='blogId'/>
          <meta expr:content='data:post.id' itemprop='postId'/>

          <a expr:name='data:post.id'/>
          <b:if cond='data:post.title'>
            <h3 class='post-title entry-title' itemprop='name'>
              <b:if cond='data:post.link'>
                <a expr:href='data:post.link'><data:post.title/></a>
              <b:elseif cond='data:post.url and data:blog.url != data:post.url'/>
                <a expr:href='data:post.url'><data:post.title/></a>
              <b:else/>
                <data:post.title/>
              </b:if>
            </h3>
          </b:if>

          <div class='post-header'>
            <div class='post-header-line-1'/>
          </div>

          <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' itemprop='articleBody'>
            <data:post.body/>
            <div style='clear: both;'/> <!-- clear for photos floats -->
          </div>

          <div class='post-footer'>
            <div class='post-footer-line post-footer-line-1'>
              <span class='post-author vcard'>
                <b:if cond='data:top.showAuthor'>
                  <b:if cond='data:post.authorProfileUrl'>
                    <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                      <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                      <a expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                        <span itemprop='name'><data:post.author/></span>
                      </a>
                    </span>
                  <b:else/>
                    <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                      <span itemprop='name'><data:post.author/></span>
                    </span>
                  </b:if>
                </b:if>
              </span>

              <span class='post-timestamp'>
                <b:if cond='data:top.showTimestamp'>
                  <data:top.timestampLabel/>
                  <b:if cond='data:post.url'>
                    <meta expr:content='data:post.canonicalUrl' itemprop='url'/>
                    <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><abbr class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></abbr></a>
                  </b:if>
                </b:if>
              </span>

              <span class='post-comment-link'>
                <b:include cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                                  and data:post.allowComments' data='post' name='comment_count_picker'/>
              </span>
            </div>

            <div class='post-footer-line post-footer-line-2'>
              <b:if cond='data:top.showMobileShare'>
                <div class='mobile-link-button goog-inline-block' id='mobile-share-button'>
                  <a href='javascript:void(0);'><data:shareMsg/></a>
                </div>
              </b:if>
              <b:if cond='data:top.showDummy'>
                <div class='goog-inline-block dummy-container'><data:post.dummyTag/></div>
              </b:if>
            </div>

          </div>
        </div>

        <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
      </div>
    </div>
  </div>
</b:includable>
              <b:includable id='nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <span id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'><data:newerPageTitle/></a>
      </span>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <span id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'><data:olderPageTitle/></a>
      </span>
    </b:if>

    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>

    <b:if cond='data:mobileLinkUrl'>
      <div class='blog-mobile-link'>
        <a expr:href='data:mobileLinkUrl'><data:mobileLinkMsg/></a>
      </div>
    </b:if>

  </div>
  <div class='clear'/>
</b:includable>
              <b:includable id='post' var='post'>
  <div class='post hentry uncustomized-post-template' itemprop='blogPost' itemtype='http://schema.org/BlogPosting'>
    <b:if cond='data:post.firstImageUrl'>
      <meta expr:content='data:post.firstImageUrl' itemprop='image_url'/>
    </b:if>
    <meta expr:content='data:blog.blogId' itemprop='blogId'/>
    <meta expr:content='data:post.id' itemprop='postId'/>

    <a expr:name='data:post.id'/>


<b:if cond='data:blog.pageType == &quot;static_page&quot;'>

    <b:if cond='data:post.title'>
      <h2 class='post-title entry-title' itemprop='name'>
      <b:if cond='data:post.link or (data:post.url and data:blog.url != data:post.url)'>
        <a expr:href='data:post.link ? data:post.link : data:post.url'><data:post.title/></a>
      <b:else/>
        <data:post.title/>
      </b:if>
      </h2>
    </b:if>

</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>

    <b:if cond='data:post.title'>
      <h1 class='post-title entry-title' itemprop='name'>
      <b:if cond='data:post.link or (data:post.url and data:blog.url != data:post.url)'>
        <a expr:href='data:post.link ? data:post.link : data:post.url'><data:post.title/></a>
      <b:else/>
        <data:post.title/>
      </b:if>
      </h1>
    </b:if>

<div class='nread'>
<div class='title-secondary'>

<span class='fa fa-pencil-square-o'/>

      <span class='post-author vcard'>
        <b:if cond='data:top.showAuthor'>
            <b:if cond='data:post.authorProfileUrl'>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                <a class='g-profile' expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                  <span itemprop='name'><data:post.author/></span>
                </a>
              </span>
            <b:else/>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <span itemprop='name'><data:post.author/></span>
              </span>
            </b:if>
        </b:if>
      </span>

&amp;nbsp;
<i class='fa fa-calendar-o'/>

      <span class='post-timestamp'>
        <b:if cond='data:top.showTimestamp'>
          <b:if cond='data:post.url'>
            <meta expr:content='data:post.canonicalUrl' itemprop='url'/>
            <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><span class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></span></a>
          </b:if>
        </b:if>
      </span>


        <!-- quickedit pencil -->
        <b:include data='post' name='postQuickEdit'/>

</div>

<div class='feet-icons'>
<a class='facebook-ico' expr:href='data:post.sharePostUrl + &quot;&amp;target=facebook&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' expr:title='data:top.shareToFacebookMsg' target='_blank'><i class='fa fa-facebook'/></a>

<a class='twitter-ico' expr:href='data:post.sharePostUrl + &quot;&amp;target=twitter&quot;' expr:title='data:top.shareToTwitterMsg' target='_blank'><i class='fa fa-twitter'/></a>


<a class='plus-ico' expr:href='&quot;https://plus.google.com/share?url=&quot; + data:post.url' target='_blank' title='Share on Google+'><i class='fa fa-google-plus'/></a>

<a class='email-ico' expr:href='data:post.sharePostUrl + &quot;&amp;target=email&quot;' expr:title='data:top.emailThisMsg' target='_blank'><i class='fa fa-envelope-o'/></a>

<a class='pinterest-ico' expr:href='data:post.sharePostUrl + &quot;&amp;target=pinterest&quot;' expr:title='data:top.shareToPinterestMsg' target='_blank'><i class='fa fa-pinterest'/></a>

</div>
</div>

<!-- Show Ads Below Post Title -->

    </b:if>

    <div class='post-header'>
    <div class='post-header-line-1'/>
    </div>

    <!-- Then use the post body as the schema.org description, for good G+/FB snippeting. -->
    <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' expr:itemprop='(data:blog.metaDescription ? &quot;&quot; : &quot;description &quot;) + &quot;articleBody&quot;'>
     
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<p><data:post.body/></p>
<b:else/>
<b:if cond='data:blog.pageType == &quot;static_page&quot;'>
<data:post.body/>
<b:else/>

<b:if cond='data:post.firstImageUrl'>
<a expr:href='data:post.url' expr:title='data:post.title'><div class='bukshan'><img expr:src='data:post.firstImageUrl'/><span class='overlay-icon'/></div>
</a><b:else/>
<a expr:href='data:post.url' expr:title='data:post.title'><div class='bukshan'><img src='http://1.bp.blogspot.com/-Nit_LiUtMHE/VflsSxNxENI/AAAAAAAADiM/CuVVm4SVl8E/s320/No-image-bt9.jpg'/></div>
</a>
</b:if> 
 
<b:if cond='data:post.title'>
<h2 class='post-title entry-title' itemprop='name headline'>
<b:if cond='data:post.link'>
<a expr:href='data:post.link'><data:post.title/></a>  
<b:else/>
<b:if cond='data:post.url'>
<b:if cond='data:blog.url != data:post.url'>
<a expr:href='data:post.url'><data:post.title/></a>
<b:else/>
<data:post.title/>
</b:if>
<b:else/>
<data:post.title/>
</b:if>
</b:if>
</h2>
</b:if>

<div class='title-secondary'>

<span class='post-meat'>
<b:loop values='data:post.labels' var='label'><a expr:href='data:label.url + &quot;?&amp;amp;max-results=6&quot;' itemprop='url'><b:if cond='data:label.isLast == &quot;true&quot;'><data:label.name/></b:if></a>
</b:loop>
</span>

<span class='fa fa-pencil-square-o'/>

      <span class='post-author vcard'>
        <b:if cond='data:top.showAuthor'>
            <b:if cond='data:post.authorProfileUrl'>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                <a class='g-profile' expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                  <span itemprop='name'><data:post.author/></span>
                </a>
              </span>
            <b:else/>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <span itemprop='name'><data:post.author/></span>
              </span>
            </b:if>
        </b:if>
      </span>

&amp;nbsp;
      <span class='post-timestamp'><i class='fa fa-calendar-o'/>
        <b:if cond='data:top.showTimestamp'>
          <b:if cond='data:post.url'>
            <meta expr:content='data:post.canonicalUrl' itemprop='url'/>
            <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><span class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></span></a>
          </b:if>
        </b:if>
      </span>

</div>

<div expr:id='&quot;summary&quot; + data:post.id'><div itemprop='description articleBody'><data:post.body/></div></div>
<script type='text/javascript'>bintiz(&quot;summary<data:post.id/>&quot;,&quot;<data:post.title/>&quot;,&quot;<data:post.url/>&quot;,&quot;&quot;);</script>

</b:if>
</b:if>

      <div style='clear: both;'/> <!-- clear for photos floats -->
    </div>

    <b:if cond='data:post.hasJumpLink'>
      <div class='jump-link'>
        <a expr:href='data:post.url + &quot;#more&quot;' expr:title='data:post.title'><data:post.jumpText/></a>
      </div>
    </b:if>


<b:if cond='data:blog.pageType == &quot;item&quot;'>
    <div class='post-footer'>
    <div class='post-footer-line post-footer-line-1'>

       <!-- backlinks -->
       <span class='post-backlinks post-comment-link'>
         <b:if cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                      and data:post.showBacklinks'>
           <a class='comment-link' expr:href='data:post.url + &quot;#links&quot;'><data:top.backlinkLabel/></a>
         </b:if>
       </span>

      <span class='post-icons'>

      </span>

      <!-- share buttons -->
      </div>

      <div class='post-footer-line post-footer-line-2'>

<span class='post-labels'>
<span class='fa-stack fa-lg'>
<i class='fa fa-circle fa-stack-2x'/>
<i class='fa fa-tags fa-stack-1x fa-inverse'/>
</span>
        <b:if cond='data:top.showPostLabels and data:post.labels'>
          <b:loop values='data:post.labels' var='label'>
            <a expr:href='data:label.url' rel='tag'><data:label.name/></a><b:if cond='not data:label.isLast'>,</b:if>
          </b:loop>
        </b:if>
      </span>
      </div>

      <div class='post-footer-line post-footer-line-3'>

<b:if cond='data:blog.pageType == &quot;item&quot;'>

<div id='related-article'>
<b:loop values='data:post.labels' var='label'>
<script expr:src='&quot;/feeds/posts/default/-/&quot; + data:label.name + &quot;?alt=json-in-script&amp;callback=related_results_labels&quot;' type='text/javascript'/>
</b:loop>
<script type='text/javascript'>
var maxresults=3;
var size = 350;
removeRelatedDuplicates();
printRelatedLabels(&#39;<data:post.url/>&#39;);</script>
</div>
<div class='clear'/> 

<div class='greden'>
<div class='reg-bent'>
<div class='reg-bent2'>
    <b:if cond='data:newerPageUrl'>
      <span id='blog-pager-newer-link'>
        <span class='two-left'>Next</span><br/>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'><i class='fa fa-chevron-left'/> Prev Post</a>
      </span>
<b:else/>
      <span class='one-left'><span class='two-left'>Latest</span></span>
    </b:if>
</div>
</div>
<div class='fed-bent'>
<div class='fed-bent2'>
    <b:if cond='data:olderPageUrl'>
      <span id='blog-pager-older-link'>
        <span class='two-left'>Previous</span><br/>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>Next Post <i class='fa fa-chevron-right'/></a>
      </span>
<b:else/>
<span class='one-right'><span class='two-left'>First</span></span>
    </b:if>
</div>
</div>
</div>
</b:if>
<div style='clear: both;'/>

      </div>

<div class='auth-panel'>
<img class='author_avatar' expr:alt='data:post.author' expr:src='data:post.authorPhoto.url' height='96' width='96'/>
<h4>About <data:post.author/></h4>
<p>
<!-- Change Author Info Here -->

Author Description here.. Nulla sagittis convallis. Curabitur consequat. Quisque metus enim, venenatis fermentum, mollis in, porta et, nibh. Duis vulputate elit in elit. Mauris dictum libero id justo.
</p>
</div>

      <b:if cond='data:post.authorAboutMe'>
        <div class='author-profile' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
          <b:if cond='data:post.authorPhoto.url'>
            <img expr:src='data:post.authorPhoto.url' itemprop='image' width='50px'/>
          </b:if>
          <div>
            <a class='g-profile' expr:href='data:post.authorProfileUrl' itemprop='url' rel='author' title='author profile'>
              <span itemprop='name'><data:post.author/></span>
            </a>
          </div>
          <span itemprop='description'><data:post.authorAboutMe/></span>
        </div>
      </b:if>

    </div>
</b:if>

  </div>
</b:includable>
              <b:includable id='postQuickEdit' var='post'>
  <b:if cond='data:post.editUrl'>
    <span expr:class='&quot;item-control &quot; + data:post.adminClass'>
      <a expr:href='data:post.editUrl' expr:title='data:top.editPostMsg'>
        <img alt='' class='icon-action' height='18' src='//img2.blogblog.com/img/icon18_edit_allbkg.gif' width='18'/>
      </a>
    </span>
  </b:if>
</b:includable>
              <b:includable id='shareButtons' var='post'>
  <b:if cond='data:top.showEmailButton'><a class='goog-inline-block share-button sb-email' expr:href='data:post.sharePostUrl + &quot;&amp;target=email&quot;' expr:title='data:top.emailThisMsg' target='_blank'><span class='share-button-link-text'><data:top.emailThisMsg/></span></a></b:if><b:if cond='data:top.showBlogThisButton'><a class='goog-inline-block share-button sb-blog' expr:href='data:post.sharePostUrl + &quot;&amp;target=blog&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' expr:title='data:top.blogThisMsg' target='_blank'><span class='share-button-link-text'><data:top.blogThisMsg/></span></a></b:if><b:if cond='data:top.showTwitterButton'><a class='goog-inline-block share-button sb-twitter' expr:href='data:post.sharePostUrl + &quot;&amp;target=twitter&quot;' expr:title='data:top.shareToTwitterMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToTwitterMsg/></span></a></b:if><b:if cond='data:top.showFacebookButton'><a class='goog-inline-block share-button sb-facebook' expr:href='data:post.sharePostUrl + &quot;&amp;target=facebook&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' expr:title='data:top.shareToFacebookMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToFacebookMsg/></span></a></b:if><b:if cond='data:top.showPinterestButton'><a class='goog-inline-block share-button sb-pinterest' expr:href='data:post.sharePostUrl + &quot;&amp;target=pinterest&quot;' expr:title='data:top.shareToPinterestMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToPinterestMsg/></span></a></b:if><b:if cond='data:top.showPlusOne'><div class='goog-inline-block google-plus-share-container'><data:post.googlePlusShareTag/></div></b:if>
</b:includable>
              <b:includable id='status-message'>
  <b:if cond='data:navMessage'>
  <div class='status-msg-wrap'>
    <div class='status-msg-body'>
      <data:navMessage/>
    </div>
    <div class='status-msg-border'>
      <div class='status-msg-bg'>
        <div class='status-msg-hidden'><data:navMessage/></div>
      </div>
    </div>
  </div>
  <div style='clear: both;'/>
  </b:if>
</b:includable>
              <b:includable id='threaded-comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.friendConnectJs/>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
              <b:includable id='threaded_comment_js' var='post'>
  <script async='async' expr:src='data:post.commentSrc' type='text/javascript'/>

  <script type='text/javascript'>
    (function() {
      var items = <data:post.commentJso/>;
      var msgs = <data:post.commentMsgs/>;
      var config = <data:post.commentConfig/>;

// <![CDATA[
      var cursor = null;
      if (items && items.length > 0) {
        cursor = parseInt(items[items.length - 1].timestamp) + 1;
      }

      var bodyFromEntry = function(entry) {
        if (entry.gd$extendedProperty) {
          for (var k in entry.gd$extendedProperty) {
            if (entry.gd$extendedProperty[k].name == 'blogger.contentRemoved') {
              return '<span class="deleted-comment">' + entry.content.$t + '</span>';
            }
          }
        }
        return entry.content.$t;
      }

      var parse = function(data) {
        cursor = null;
        var comments = [];
        if (data && data.feed && data.feed.entry) {
          for (var i = 0, entry; entry = data.feed.entry[i]; i++) {
            var comment = {};
            // comment ID, parsed out of the original id format
            var id = /blog-(\d+).post-(\d+)/.exec(entry.id.$t);
            comment.id = id ? id[2] : null;
            comment.body = bodyFromEntry(entry);
            comment.timestamp = Date.parse(entry.published.$t) + '';
            if (entry.author && entry.author.constructor === Array) {
              var auth = entry.author[0];
              if (auth) {
                comment.author = {
                  name: (auth.name ? auth.name.$t : undefined),
                  profileUrl: (auth.uri ? auth.uri.$t : undefined),
                  avatarUrl: (auth.gd$image ? auth.gd$image.src : undefined)
                };
              }
            }
            if (entry.link) {
              if (entry.link[2]) {
                comment.link = comment.permalink = entry.link[2].href;
              }
              if (entry.link[3]) {
                var pid = /.*comments\/default\/(\d+)\?.*/.exec(entry.link[3].href);
                if (pid && pid[1]) {
                  comment.parentId = pid[1];
                }
              }
            }
            comment.deleteclass = 'item-control blog-admin';
            if (entry.gd$extendedProperty) {
              for (var k in entry.gd$extendedProperty) {
                if (entry.gd$extendedProperty[k].name == 'blogger.itemClass') {
                  comment.deleteclass += ' ' + entry.gd$extendedProperty[k].value;
                } else if (entry.gd$extendedProperty[k].name == 'blogger.displayTime') {
                  comment.displayTime = entry.gd$extendedProperty[k].value;
                }
              }
            }
            comments.push(comment);
          }
        }
        return comments;
      };

      var paginator = function(callback) {
        if (hasMore()) {
          var url = config.feed + '?alt=json&v=2&orderby=published&reverse=false&max-results=50';
          if (cursor) {
            url += '&published-min=' + new Date(cursor).toISOString();
          }
          window.bloggercomments = function(data) {
            var parsed = parse(data);
            cursor = parsed.length < 50 ? null
                : parseInt(parsed[parsed.length - 1].timestamp) + 1
            callback(parsed);
            window.bloggercomments = null;
          }
          url += '&callback=bloggercomments';
          var script = document.createElement('script');
          script.type = 'text/javascript';
          script.src = url;
          document.getElementsByTagName('head')[0].appendChild(script);
        }
      };
      var hasMore = function() {
        return !!cursor;
      };
      var getMeta = function(key, comment) {
        if ('iswriter' == key) {
          var matches = !!comment.author
              && comment.author.name == config.authorName
              && comment.author.profileUrl == config.authorUrl;
          return matches ? 'true' : '';
        } else if ('deletelink' == key) {
          return config.baseUri + '/delete-comment.g?blogID='
               + config.blogId + '&postID=' + comment.id;
        } else if ('deleteclass' == key) {
          return comment.deleteclass;
        }
        return '';
      };

      var replybox = null;
      var replyUrlParts = null;
      var replyParent = undefined;

      var onReply = function(commentId, domId) {
        if (replybox == null) {
          // lazily cache replybox, and adjust to suit this style:
          replybox = document.getElementById('comment-editor');
          if (replybox != null) {
            replybox.height = '250px';
            replybox.style.display = 'block';
            replyUrlParts = replybox.src.split('#');
          }
        }
        if (replybox && (commentId !== replyParent)) {
          replybox.src = '';
          document.getElementById(domId).insertBefore(replybox, null);
          replybox.src = replyUrlParts[0]
              + (commentId ? '&parentID=' + commentId : '')
              + '#' + replyUrlParts[1];
          replyParent = commentId;
        }
      };

      var hash = (window.location.hash || '#').substring(1);
      var startThread, targetComment;
      if (/^comment-form_/.test(hash)) {
        startThread = hash.substring('comment-form_'.length);
      } else if (/^c[0-9]+$/.test(hash)) {
        targetComment = hash.substring(1);
      }

      // Configure commenting API:
      var configJso = {
        'maxDepth': config.maxThreadDepth
      };
      var provider = {
        'id': config.postId,
        'data': items,
        'loadNext': paginator,
        'hasMore': hasMore,
        'getMeta': getMeta,
        'onReply': onReply,
        'rendered': true,
        'initComment': targetComment,
        'initReplyThread': startThread,
        'config': configJso,
        'messages': msgs
      };

      var render = function() {
        if (window.goog && window.goog.comments) {
          var holder = document.getElementById('comment-holder');
          window.goog.comments.render(holder, provider);
        }
      };

      // render now, or queue to render when library loads:
      if (window.goog && window.goog.comments) {
        render();
      } else {
        window.goog = window.goog || {};
        window.goog.comments = window.goog.comments || {};
        window.goog.comments.loadQueue = window.goog.comments.loadQueue || [];
        window.goog.comments.loadQueue.push(render);
      }
    })();
// ]]>
  </script>
</b:includable>
              <b:includable id='threaded_comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>

<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<h5><i class='fa fa-comments-o' style='font-size:18px;'/> <data:post.commentLabelFull/>:</h5>

  <a class='buffer' href='#comment-editor'>Write <data:commentLabelPlural/></a></b:if>

    <div class='comments-content'>
      <b:include cond='data:post.embedCommentForm' data='post' name='threaded_comment_js'/>
      <div id='comment-holder'>
         <data:post.commentHtml/>
      </div>
    </div>

    <p class='comment-footer'>
      <b:if cond='data:post.allowNewComments'>
        <b:include data='post' name='threaded-comment-form'/>
      <b:else/>
        <data:post.noNewCommentsText/>
      </b:if>
    </p>

    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
      <b:include cond='data:post.showBacklinks' data='post' name='backlinks'/>
    </div>
    </div>
  </div>

</b:includable>
            </b:widget>
          </b:section>


          <aside>

          </aside>

        <div style='clear: both'/>

    <footer>

    </footer>

<b:if cond='data:blog.url == data:blog.homepageUrl'>

<b:section class='proof tob-contid1' id='lists7' preferred='no' showaddelement='no'>
  <b:widget id='HTML24' locked='false' mobile='yes' title='Photography' type='HTML' version='1'>
    <b:widget-settings>
      <b:widget-setting name='content'/>
    </b:widget-settings>
    <b:includable id='main'>
<script>
document.write(&#39;&lt;div class=&quot;pigment&quot;&gt;&lt;h4&gt;&lt;a href=&quot;/search/label/<data:content/>?max-results=7&quot;&gt; <data:title/>&lt;/a&gt;&lt;/h4&gt;&lt;/div&gt;&#39;);
</script>	
  <div class='widget-content'>
<div id='call-57'/>
<script type='text/javascript'>
ShowPost1({
idcontaint:&quot;#call-57&quot;,
MaxPost:10,
ImageSize:270,
FirstImageSize:270,
tagName:&quot;<data:content/>&quot;
});
</script>
<div class='clear'/>
  </div>
       <div class='clear'/>
  <b:include name='quickedit'/>
</b:includable>
  </b:widget>
</b:section>   
<div class='clear'/>


</b:if>


        </div><!-- main-inner-wrap -->
      </div><!-- /main-wrapper -->


      <div class='sidebar-wrapper'>

<b:section class='sidebar' id='sidebar1' showaddelement='yes'/>

<div class='threetabs'>
<ul class='tabber wrap-tabs'>
<li class='keez'><a href='#id2'>Popular Posts</a></li>
<li class='keez'><a href='#id3'>Comments</a></li>
<li class='keez'><a href='#id4'>Category</a></li>
</ul>
<div class='clear'/>

<div class='boner' id='id2'>

<b:section class='sidebar' id='popular-post' preferred='no' showaddelement='no'>
  <b:widget id='PopularPosts2' locked='true' title='Popular Posts' type='PopularPosts' version='1'>
    <b:widget-settings>
      <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
      <b:widget-setting name='showThumbnails'>true</b:widget-setting>
      <b:widget-setting name='showSnippets'>true</b:widget-setting>
      <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title'><h2><data:title/></h2></b:if>
  <div class='widget-content popular-posts'>
    <ul>
      <b:loop values='data:posts' var='post'>
      <li>
        <b:if cond='data:showThumbnails == &quot;false&quot;'>
          <b:if cond='data:showSnippets == &quot;false&quot;'>
            <!-- (1) No snippet/thumbnail -->
            <a expr:href='data:post.href'><data:post.title/></a>
          <b:else/>
            <!-- (2) Show only snippets -->
            <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            <div class='item-snippet'><data:post.snippet/></div>
          </b:if>
        <b:else/>
          <b:if cond='data:showSnippets == &quot;false&quot;'>
            <!-- (3) Show only thumbnails -->
            <div class='item-thumbnail-only'>
              <b:if cond='data:post.thumbnail'>
                <div class='item-thumbnail'>
                  <a expr:href='data:post.href'>
                    <img alt='' border='0' expr:height='data:thumbnailSize' expr:src='data:post.thumbnail' expr:width='data:thumbnailSize'/>
                  </a>
                </div>
              </b:if>
              <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            </div>
            <div style='clear: both;'/>
          <b:else/>
            <!-- (4) Show snippets and thumbnails -->
            <div class='item-content'>
              <b:if cond='data:post.thumbnail'>
                <div class='item-thumbnail'>
                  <a expr:href='data:post.href'>
                    <img alt='' border='0' expr:height='data:thumbnailSize' expr:src='data:post.thumbnail' expr:width='data:thumbnailSize'/>
                  </a>
                </div>
              </b:if>
              <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
              <div class='item-snippet'><data:post.snippet/></div>
            </div>
            <div style='clear: both;'/>
          </b:if>
        </b:if>
      </li>
      </b:loop>
    </ul>
    <b:include name='quickedit'/>
  </div>
</b:includable>
  </b:widget>
</b:section>

</div>

<div class='boner' id='id3'>

<script src='/feeds/comments/default?alt=json&amp;callback=ms_recent&amp;&amp;max-results=50' type='text/javascript'/>

</div>

<div class='boner' id='id4'>

<b:section class='sidebar' id='Category' preferred='no' showaddelement='no'>
  <b:widget id='Label3' locked='true' title='Labels' type='Label' version='1'>
    <b:widget-settings>
      <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
      <b:widget-setting name='display'>LIST</b:widget-setting>
      <b:widget-setting name='selectedLabelsList'/>
      <b:widget-setting name='showType'>ALL</b:widget-setting>
      <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'>
    <h2><data:title/></h2>
  </b:if>
    <div expr:class='&quot;widget-content &quot; + data:display + &quot;-label-widget-content&quot;'>
                <b:if cond='data:display == &quot;list&quot;'>
                  <ul>
                    <b:loop values='data:labels' var='label'>
                      <li>
                        <b:if cond='data:blog.url == data:label.url'>
                          <span expr:dir='data:blog.languageDirection'>
                            <data:label.name/>
                          </span>
                          <b:else/>
                          <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'>
                            <data:label.name/>
                          </a>
                        </b:if>
                        <b:if cond='data:showFreqNumbers'>
                          <span dir='ltr'>
                            (
                            <data:label.count/>
                            )
                          </span>
                        </b:if>
                      </li>
                    </b:loop>
                  </ul>
                  <b:else/>
                  <b:loop values='data:labels' var='label'>
                    <span expr:class='&quot;label-size label-size-&quot; + data:label.cssSize'>
                      <b:if cond='data:blog.url == data:label.url'>
                        <span expr:dir='data:blog.languageDirection'>
                          <data:label.name/>
                        </span>
                        <b:else/>
                        <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'>
                          <data:label.name/>
                        </a>
                      </b:if>
                      <b:if cond='data:showFreqNumbers'>
                        <span class='label-count' dir='ltr'>
                          (
                          <data:label.count/>
                          )
                        </span>
                      </b:if>
                    </span>
                  </b:loop>
                </b:if>
                <b:include name='quickedit'/>
              </div>
</b:includable>
  </b:widget>
</b:section>

</div>

</div>
<div class='clear'/>

        <b:section class='sidebar' id='sidebar' showaddelement='yes'>
          <b:widget id='HTML1' locked='false' title='Advertisement' type='HTML'>
            <b:widget-settings>
              <b:widget-setting name='content'/>
            </b:widget-settings>
            <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
          </b:widget>
          <b:widget id='HTML3' locked='false' title='Featured Video' type='HTML'>
            <b:widget-settings>
              <b:widget-setting name='content'/>
            </b:widget-settings>
            <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
          </b:widget>
          <b:widget id='HTML10' locked='false' title='Elegant Themes' type='HTML'>
            <b:widget-settings>
              <b:widget-setting name='content'/>
            </b:widget-settings>
            <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
          </b:widget>
          <b:widget id='ContactForm1' locked='false' title='Contact Form' type='ContactForm' version='1'>
            <b:includable id='main'>
</b:includable>
          </b:widget>
        </b:section>
      </div><!-- sidebar-wrapper -->

      <div class='clear'/>

</div><!--Div Container-->

    </div><!-- outer-wrapper -->

  <div id='footer'>
<div class='mage1'>

<div class='container'>

      <b:section class='footer boxer lefter' id='footer1' preferred='yes'>
        <b:widget id='HTML13' locked='false' title='Instagram posts' type='HTML' version='1'>
          <b:widget-settings>
            <b:widget-setting name='content'/>
          </b:widget-settings>
          <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
<div class='clear'/>

  </div>

  <b:include name='quickedit'/>
</b:includable>
        </b:widget>
      </b:section>
      <b:section class='footer boxer lefter tagcloud1' id='footer2' preferred='yes'>
        <b:widget id='Label51' locked='false' title='Category' type='Label' version='1'>
          <b:widget-settings>
            <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
            <b:widget-setting name='display'>LIST</b:widget-setting>
            <b:widget-setting name='selectedLabelsList'/>
            <b:widget-setting name='showType'>ALL</b:widget-setting>
            <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
          </b:widget-settings>
          <b:includable id='main'>
              <b:if cond='data:title'>
                <h2>
                  <data:title/>
                </h2>
              </b:if>
              <div expr:class='&quot;widget-content &quot; + data:display + &quot;-label-widget-content&quot;'>
                <b:if cond='data:display == &quot;list&quot;'>
                  <ul>
                    <b:loop values='data:labels' var='label'>
                      <li>
                        <b:if cond='data:blog.url == data:label.url'>
                          <span expr:dir='data:blog.languageDirection'>
                            <data:label.name/>
                          </span>
                          <b:else/>
                          <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'>
                            <data:label.name/>
                          </a>
                        </b:if>
                        <b:if cond='data:showFreqNumbers'>
                          <span dir='ltr'>
                            (
                            <data:label.count/>
                            )
                          </span>
                        </b:if>
                      </li>
                    </b:loop>
                  </ul>
                  <b:else/>
                  <b:loop values='data:labels' var='label'>
                    <span expr:class='&quot;label-size label-size-&quot; + data:label.cssSize'>
                      <b:if cond='data:blog.url == data:label.url'>
                        <span expr:dir='data:blog.languageDirection'>
                          <data:label.name/>
                        </span>
                        <b:else/>
                        <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'>
                          <data:label.name/>
                        </a>
                      </b:if>
                      <b:if cond='data:showFreqNumbers'>
                        <span class='label-count' dir='ltr'>
                          (
                          <data:label.count/>
                          )
                        </span>
                      </b:if>
                    </span>
                  </b:loop>
                </b:if>
                <b:include name='quickedit'/>
              </div>
            </b:includable>
        </b:widget>
      </b:section>
      <b:section class='footer boxer lefter' id='footer3' preferred='yes'>
        <b:widget id='HTML4' locked='false' title='About Us' type='HTML'>
          <b:widget-settings>
            <b:widget-setting name='content'/>
          </b:widget-settings>
          <b:includable id='main'>
  <!-- only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <div class='widget-content'>
    <data:content/>
  </div>

  <b:include name='quickedit'/>
</b:includable>
        </b:widget>
      </b:section>
  <div class='clear'/>

      </div><!--Div Container-->
      </div><!-- mage1 -->

  </div><!-- footer -->
  <div class='footer-credits'>
  <div class='mage2'>
<div class='container'>
      <div class='attribution'>&#169; Copyright 2015 <a expr:href='data:blog.homepageUrl'><data:blog.title/></a>. <span id='credit'/>. <span class='deen'>Powered by <a href='https:blogger.com/'>Blogger</a>.</span>

</div>
</div>
</div><!-- mage2 -->

</div><!-- footer-credits -->

  </div><!-- ct-wrapper -->

<div class='tibber'>

<!-- Change contact button url -->

<a href='/p/contact-us_5.html'><span class='fa fa-comments-o'/></a>

</div>

<div id='fb-root'/>
<script type='text/javascript'>
//<![CDATA[

//Facebook Script
(function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(d.getElementById(id))return;js=d.createElement(s);js.id=id;js.src="//connect.facebook.net/en_US/all.js#xfbml=1";fjs.parentNode.insertBefore(js,fjs)}(document,'script','facebook-jssdk'));

//]]>
</script>

<!-- Page Counter - Edit Number Of Post To Show On Each Page -->

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<script type='text/javascript'>

var home_page=&quot;/&quot;;
var urlactivepage=location.href;
var postperpage=7;
var numshowpage=2;
var upPageWord =&#39;&#171;&#39;;
var downPageWord =&#39;&#187;&#39;;

</script>

<script type='text/javascript'>
//<![CDATA[

eval(function(p,a,c,k,e,r){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--)r[e(c)]=k[c]||e(c);k=[function(e){return r[e]}];e=function(){return'\\w+'};c=1};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('5 G;5 i;5 b;5 n;1f();x 1g(15){5 6=\'\';H=I(K/2);3(H==K-H){K=H*2+1}J=b-H;3(J<1)J=1;o=I(15/j)+1;3(o-1==15/j)o=o-1;L=J+K-1;3(L>o)L=o;6+="<4 e=\'1y\'>1z "+b+\' 1A \'+o+"</4>";5 16=I(b)-1;3(b>1){3(b==2){3(i=="w"){6+=\'<4 e="1B"><a f="\'+y+\'">\'+M+\'</a></4>\'}c{6+=\'<4 e="k"><a f="/r/s/\'+n+\'?&7-l=\'+j+\'">\'+M+\'</a></4>\'}}c{3(i=="w"){6+=\'<4 e="k"><a f="#" z="N(\'+16+\');A B">\'+M+\'</a></4>\'}c{6+=\'<4 e="k"><a f="#" z="O(\'+16+\');A B">\'+M+\'</a></4>\'}}}1h(5 g=J;g<=L;g++){3(b==g){6+=\'<4 e="1C">\'+g+\'</4>\'}c 3(g==1){3(i=="w"){6+=\'<4 e="k"><a f="\'+y+\'">1</a></4>\'}c{6+=\'<4 e="k"><a f="/r/s/\'+n+\'?&7-l=\'+j+\'">1</a></4>\'}}c{3(i=="w"){6+=\'<4 e="k"><a f="#" z="N(\'+g+\');A B">\'+g+\'</a></4>\'}c{6+=\'<4 e="k"><a f="#" z="O(\'+g+\');A B">\'+g+\'</a></4>\'}}}5 17=I(b)+1;3(b<o){3(i=="w"){6+=\'<4 e="k"><a f="#" z="N(\'+17+\');A B">\'+1i+\'</a></4>\'}c{6+=\'<4 e="k"><a f="#" z="O(\'+17+\');A B">\'+1i+\'</a></4>\'}}5 C=u.1D("C");5 18=u.1E("1F-1G");1h(5 p=0;p<C.P;p++){C[p].1j=6}3(C&&C.P>0){6=\'\'}3(18){18.1j=6}}x 1a(Q){5 R=Q.R;5 1k=I(R.1H$1I.$t,10);1g(1k)}x 1f(){5 d=m;3(d.9("/r/s/")!=-1){3(d.9("?S-7")!=-1){n=d.D(d.9("/r/s/")+14,d.9("?S-7"))}c{n=d.D(d.9("/r/s/")+14,d.9("?&7"))}}3(d.9("?q=")==-1&&d.9(".6")==-1){3(d.9("/r/s/")==-1){i="w";3(m.9("#E=")!=-1){b=m.D(m.9("#E=")+8,m.P)}c{b=1}u.1l("<h T=\\""+y+"U/V/W?7-l=1&X=Y-Z-h&11=1a\\"><\\/h>")}c{i="s";3(d.9("&7-l=")==-1){j=1J}3(m.9("#E=")!=-1){b=m.D(m.9("#E=")+8,m.P)}c{b=1}u.1l(\'<h T="\'+y+\'U/V/W/-/\'+n+\'?X=Y-Z-h&11=1a&7-l=1" ><\\/h>\')}}}x N(F){12=(F-1)*j;G=F;5 13=u.1m(\'1n\')[0];5 v=u.1o(\'h\');v.1p=\'1q/1r\';v.1s("T",y+"U/V/W?1t-1u="+12+"&7-l=1&X=Y-Z-h&11=1b");13.1v(v)}x O(F){12=(F-1)*j;G=F;5 13=u.1m(\'1n\')[0];5 v=u.1o(\'h\');v.1p=\'1q/1r\';v.1s("T",y+"U/V/W/-/"+n+"?1t-1u="+12+"&7-l=1&X=Y-Z-h&11=1b");13.1v(v)}x 1b(Q){1c=Q.R.1K[0];5 1w=1c.1x.$t.D(0,19)+1c.1x.$t.D(1L,1M);5 1d=1N(1w);3(i=="w"){5 1e="/r?S-7="+1d+"&7-l="+j+"#E="+G}c{5 1e="/r/s/"+n+"?S-7="+1d+"&7-l="+j+"#E="+G}1O.f=1e}',62,113,'|||if|span|var|html|max||indexOf||nomerhal|else|thisUrl|class|href|jj|script|jenis|postperpage|showpageNum|results|urlactivepage|lblname1|maksimal|||search|label||document|newInclude|page|function|home_page|onclick|return|false|pageArea|substring|PageNo|numberpage|nopage|nomerkiri|parseInt|mulai|numshowpage|akhir|upPageWord|redirectpage|redirectlabel|length|root|feed|updated|src|feeds|posts|summary|alt|json|in||callback|jsonstart|nBody||banyakdata|prevnomer|nextnomer|blogPager||hitungtotaldata|finddatepost|post|timestamp|alamat|halamanblogger|loophalaman|for|downPageWord|innerHTML|totaldata|write|getElementsByTagName|head|createElement|type|text|javascript|setAttribute|start|index|appendChild|timestamp1|published|showpageOf|Page|of|showpage|showpagePoint|getElementsByName|getElementById|blog|pager|openSearch|totalResults|20|entry|23|29|encodeURIComponent|location'.split('|'),0,{}))

//]]>
</script> 
</b:if>
</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
<script type='text/javascript'>
$(document).ready(function(){
var olderLink = $(&quot;a.blog-pager-older-link&quot;).attr(&quot;href&quot;);
$(&quot;a.blog-pager-older-link&quot;).load(olderLink+&quot; .post-title:first&quot;, function() {
var olderLinkTitle = $(&quot;a.blog-pager-older-link:first&quot;).text();
$(&quot;a.blog-pager-older-link&quot;).text(olderLinkTitle);//rgt
});
var newerLink = $(&quot;a.blog-pager-newer-link&quot;).attr(&quot;href&quot;);
$(&quot;a.blog-pager-newer-link&quot;).load(newerLink+&quot; .post-title:first&quot;, function() {
var newerLinkTitle = $(&quot;a.blog-pager-newer-link:first&quot;).text();
$(&quot;a.blog-pager-newer-link&quot;).text(newerLinkTitle);
});
});

</script>
</b:if>


</body>

</html>
