# SS/SSR端口偏移
设置完单端口后，如果想指定某些SS/SSR节点使用不同与默认的端口, 则需要端口偏移.

## 面板设置
在SS/SSR节点地址后加入<br>
";port=1234#4321"(不含引号)<br>
此处1234为默认的单端口, 4321为该节点实际使用的端口号

## 配置文件设置
修改
>SSPanel根目录/config/.config.php

把以下变量修正为true

>$_ENV['mu_port_migration']          = true;    //为后端直接下发偏移后的端口

至此, SS/SSR后端即可获得偏移后的端口号