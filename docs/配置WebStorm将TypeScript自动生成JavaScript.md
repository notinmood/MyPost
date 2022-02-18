---
title: 配置WebStorm将TypeScript自动生成JavaScript
updated: 2022-02-18T13:18:02.0000000+08:00
created: 2022-02-18T13:05:37.0000000+08:00
---

1.  安装和配置前提条件
    1.  安装node.js
    2.  安装TypeScript
| 1   | npm install typescript -g |
|-----|---------------------------|

3.  在 WebStorm 的 TypeScript 项目上，添加 tsconfig.json 配置文件
![tsconfig.json文件](https://gitee.com/xiedali/my-images/raw/master/image1-7.png)
**

2.  确保WebStorm的插件FileWatcher有效（缺省WebStorm的启用这个插件的）
![](https://gitee.com/xiedali/my-images/raw/master/image2-3.png)

5. 添加对TypeScript文件的监测

   ![image3](https://gitee.com/xiedali/my-images/raw/master/image3.png)

   ![image4](https://gitee.com/xiedali/my-images/raw/master/image4.png)
   其中各个设置如下：
   Program：
   Arguments：--sourcemap --target "ES5"
   Output paths to refresh：$FileNameWithoutExtension$.js:$FileNameWithoutExtension$.js.map
   Working directory：$FileDir$

4.  设置typescript自动编译，将发生改变时重新编译
![image5](https://gitee.com/xiedali/my-images/raw/master/image5.png)
当写完ts文件时会自动生成相应的js文件和映射文件map
![image6](https://gitee.com/xiedali/my-images/raw/master/image6.png)

*▌来自 \< [https://blog.csdn.net/u014641260/article/details/111410547](https://blog.csdn.net/u014641260/article/details/111410547?spm=1001.2101.3001.6650.1&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_default&utm_relevant_index=1)\>*

