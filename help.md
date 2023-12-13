## 使用方法

    1、将源码检索到本地

        git clone git@github.com:faxhaidong/PHP_CodeSniffer.git php_codesniffer

    2、增加调整 CodeSniffer.conf 文件，default_standard 调整为 PSR12
    
        cp CodeSniffer.conf.dist CodeSniffer.conf

    2、在git项目中增加hooks,pre-commit 为主动 add，pre-commit-not-add 为不 add

        ln -s /work/server/php_codesniffer/bin/pre-commit ./pre-commit

    3、根据实际目录修改pre-commit中的变量配置
        
        PHPCS_BIN 格式检测命令
        PHPCBF_BIN 格式修正命令
        PHPCS_RULESET 格式校验规则自定义配置文件(该文件会和默认配置进行合并，相同的项会以自定义优先)
