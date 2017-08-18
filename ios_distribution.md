```

ios 企业应用分发
导出ipa和plist文件
Product-Archive --> Export --> Save for Enterprise Deployment --> Include manifest for over-the-air installation

方式一：进入下载页面之后点击安装APP按钮之后才能下载安装
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<htmlxmlns="http://www.w3.org/1999/xhtml">
    <head>
        <metahttp-equiv="Content-Type"content="text/html; charset=utf-8"/>
        <title>应用名字</title>
    </head>
    <body>
        <h1style="font-size:80pt">如果点击无法下载安装，请复制超链接到浏览器中打开<h1/>
        <h1style="font-size:100pt">
        <a title="iPhone" href="itms-services://?action=download-manifest&url=https://example.com/manifest.plist">安装APP</a><h1/>
    </body>
</html>

方式二：进入下载页面之后自动下载安装
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<htmlxmlns="http://www.w3.org/1999/xhtml">
    <head>
        <metahttp-equiv="Content-Type"content="text/html; charset=utf-8"/>
        <title>应用名字</title>
        <script>
            var url ="https://example.com/manifest.plist";
            window.location ="itms-services://?action=download-manifest&url="+ url;
        </script>
    </head>
    <body>
    </body>
</html>

方式三：通过iOS应用内安装
[[UIApplication sharedApplication] openURL:[NSURL URLWithString:@"itms-services://?action=download-manifest&url=https://example.com/manifest.plist"]];

4、方式四：直接使用第三方托管平台（推荐自己常用平台）
fir.im - 免费应用内测托管平台|iOS应用Beta测试分发|Android应用内测分发
蒲公英 - 免费的应用托管平台|App应用众测分发
TestFlight Beta Testing - App Store - Apple Developer

```
