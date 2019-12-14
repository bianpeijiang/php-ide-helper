# php-ide-helper

php framework and php extension Auto Compelete for phpstorm

Yaf、Yar、Yac、Yaconf、Redis、Swoole等框架或C扩展之PhpStrom代码自动补全（屏蔽IDE undefined，全命名空间，中文详细文档，比手册更详细）
这个想法fork自phpboy（https://github.com/xudianyang/yaf.auto.complete)

## 原理

项目中先包含写好的相关的框架的PHP类文件(相当于本地类，因为ya*系列都是使用C语言写的PHP扩展，通过PHP将其定义出来引用)，编辑器即可在使用这些类的时候自动定位其定义的用法

## 目前支持的框架或扩展

1、Yaf(3.0.7)

2、Yac(2.0.3-dev)

3、Yaconf(1.0.8-dev)

4、Yar(2.0.4)

5、phpRedis(包括RedisCluster,支持phpredis 5.1.1)

6、swoole扩展(支持swoole 4.2.9)

7、SeasLog(1.8.5)

8、MsgPack(beta)

9、Xhprof

10、FastDFS(FastDFS 1.00)

## 使用说明

#### 一.支持composer的项目通过composer安装

##### 1.在项目的composer配置文件composer.json中的require-dev段添加以下内容
```
"require-dev": {
    "shixinke/php-ide-helper":"dev-master"
}
```

##### 2.通过composer install安装包

```
composer install
```

#### 二.不支持composer的项目安装

1、下载源文件并解压，将src文件夹下面的内容放到任意一个位置(我习惯将它放到我的phpstorm安装路径下的plugins\php\lib下面，然后建立一个vendor文件夹，如C:\Program Files (x86)\JetBrains\PhpStorm 9.0.2\plugins\php\lib\vendor)

2、打开phpstorm,选择File->Settings，打开setting控制面板

![phpstorm设置第一步](https://github.com/shixinke/phpstorm-for-php-framework/blob/master/static/images/step1.png)


3、在setting控制面板中，选择Languages & Frameworks->PHP,点击PHP面板右侧的加号按钮，将第1步放置的类文件包含进来即可

![phpstorm设置第二步](https://github.com/shixinke/phpstorm-for-php-framework/blob/master/static/images/step2.png)


## 示例

![phpstorm自动补全效果](https://github.com/shixinke/phpstorm-for-php-framework/blob/master/static/images/yaf.auto.complete.png)

## 其他说明

此次php源码文档由[php-document-creator](http://github.com/shixinke/php-document-creator) 生成，它可以生成任何PHP扩展的源码文档

## 作者

shixinke

邮箱：<ishixinke@qq.com>

博客：<http://www.shixinke.com>
