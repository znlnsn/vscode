1.phpstudy-软件管理-php设置-开启xdebug调试组件
 
 
2.设置-php7.34配置文件，xdebug.remote-autostart和xdebug.remote-enable开启为1
![显示文本](/vscode/图片/php配置1.png)

 
一个修改，增加一个
xdebug.remote-autostart=1      加
xdebug.remote_enable=1        改
 
 
 
4.网站php文件物理路径，创建phpinfo.php，打开localhost/phpinfo.php，ctrl+f搜到xdebug说明xdebug配置成功
 
<?php
        phpinfo(); 
?>
要是php文件，txt文件不行，注意后缀
 
![显示文本](/vscode/图片/php配置2.png)

 
5.vscode-php debug插件的setting json，配上php.exe的路径，要带php.exe 双斜杠
D:/phpstudy_pro/Extensions/php/php7.3.4nts
 
 
 
{
    "explorer.confirmDelete": false,
    "php.executablePath": "",
    "php.files.exclude": [
   ],
    "php.docblock.packageSnippet": {},
    "workbench.editor.empty.hint": "hidden",
    "php.debug.executablePath": "D:/phpstudy_pro/Extensions/php/php7.3.4nts"
}
6.配环境变量 php-version 检验
在path上配置
D:/phpstudy_pro/Extensions/php/php7.3.4nts
C:\Users\15423>php-version
PHP 7.3.4 (cli)(built: Apr  2 2019 21:57:22) ( NTSMSVC15 (Visual C++ 2017) x64 )
Copyright (c)1997-2018 The PHP Group
Zend Engine v3.3.4,Copyright (c) 1998-2018 Zend Technologies
    with Xdebug v2.7.2, Copyright (c)2002-2019, by Derick Rethans
 
 
7.打开文件夹，test.php，启动调试要创建launch.json，要与设置里txt文件xdebug的端口号一致
 
 
<?php
echo "hello";
$a=$_POST['a'];
?>
