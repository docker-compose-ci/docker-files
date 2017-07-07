# PHP在gitlab上持续集成的示例项目

## phplint

phplint用于检查PHP语法错误

## phpmd

PHP Mess Detector用于检查PHP的代码风格，主要包括命名规范、函数复杂度、超级静态变量使用等，具体规则参考 https://phpmd.org/rules/index.html

本项目中对规则进行了部分定制，参考文件 [phpmd.xml](./phpmd.xml)