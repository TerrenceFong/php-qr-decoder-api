#php qr decoder api
> 本项目可以帮你快速搭建一个基于 PHP 的二维码解析接口api,并且不需要安装其他扩展。核心库lib是在[码云](http://git.oschina.net/capitalist/php-qr-decoder)里找的


#如何使用

##说明
> 直接把整个包放入到工程文件内即可



##运行
####环境
```
PHP >= 5.3
php.ini里面开启: extension=php_exif.dll
```

####参数
接收 get 或者 post 参数
* imgurl ` String `

返回值示例

`{"status":1, "msg":"解析成功", "qrtext":"解析结果"}`

如果没有传入参数, `status`则为0。只有解析成功了才会返回 `qrtext`

####使用
get方式则访问 http://localhost/index.php?imgurl=url


####其他
只引入核心库lib的使用方法
```
include_once('./lib/QrReader.php');
$qrcode = new QrReader('path/to_image');  //图片路径
$text = $qrcode->text(); //返回识别后的文本
```

