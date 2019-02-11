# UseML.NET
该项目将帮助您简单理解如何使用ML.NET进行图像分类识别

在打开解决方案之前,请确保您有以下工具

首先，确保已安装.NET Core 2.1或更高版本。ML.NET也适用于.NET Framework 4.6.1或更高版本，但建议使用4.7.2或更高版本。

1.Netron      作用:用于帮助打开.pb神经结构体,寻找输入输出参数
https://github.com/lutzroeder/netron

2.Visual Studio 2017或更高版本

当您已完成以上操作,您可以下载该项目然后尝试编译

Assets                  资源文件夹
****Inputs
******Images          用于存放图片的文件夹
*********xxx.jpg
*********xxx.tsv     简单的存储格式,每一行有两个字符串,第一个是图片完整名字包含后缀,空格后第二个名字是对应的标签
******Inception
*********xxx.txt     简单的存储格式,每一行是一个标签
*********xxx.pb      表示模型（神经网络）结构的二进制文件
ImageDataStructures
***ImageNetData.cs
***ImageNetPrediction.cs
ModelScorer
***TFModelScorer.cs    
Program.cs              入口

TFModelScorer.cs中的InceptionSettings结构体的输入/出 张量 名字对应着神经网络模型结构文件内的入口和出口,用Netron打开xxx.pb即可查看神经结构图

因为我经常爱搞类线性执行程序所以里面的内容光看注释应该也能看懂许多了.当然翻译肯定不规范.
有什么不懂的自己看看https://docs.microsoft.com/zh-cn/dotnet/machine-learning/
