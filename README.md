Yii2 Mobile (Android, ios) push notifications extension
=======================================================

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist fgh151/yii2-push "*"
```

or add

```
"fgh151/yii2-push": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply add it in your config by  :

Basic ```config/web.php```

Advanced ```[backend|frontend|common]/config/main.php```

        'modules'    => [
            'push' => [
                'class' => 'fgh151\modules\push\Module',
            ],
            ...
            ...
        ],





<?php 
include_once 'class.push.php'; 
$push = new pushmessage(); 

$params = array("pushtype"=>"android", $idphone=>"android_smart_phone_id_here", $mst=>"Hello, an android user"); 
$rtn = $push->sendMessage($params); 
//print_r($rtn); 