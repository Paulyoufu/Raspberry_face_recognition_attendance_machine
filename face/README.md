之前的人脸识别考勤系统，已经依靠ｆａｃｅ＋＋和ｏｐｅｎｃｖ基本完成了功能初步测试。最后调试下的情况是：


管理员：使用python进行文件夹遍历，获取每个目录下的每个图片，以及name.txt文件获得名字。。。然后统一先行上传到服务进行识别训练。这时，我需要一份返回的识别组的ｉｄ。

摄像头监听：使用python调用建立新进程指令。从而反复进行拍摄命令，获取的每一张图片均调用ｏｐｅｎｃｖ进行人脸识别判定，如果有人脸则暂停进程，发出语音沟通，再次拍照进行二次识别。

活取到二次照片，进行文件沟通，首先移动到ｅｎｄ.jpg　然后将end.txt　设定为１。。在循环的主文件中，再将文件上传进行人脸准确识别。。返回的人脸名字，将当前时间记录下来，也存储到签到表中。

漏洞说明：使用文件沟通，可能引发读写故障，实用ｆａｃｅ＋＋考虑出ｔｒｙ的情况，可能返回错误信息，那时候的处理比较复杂。

现在重新整理文件情况。


程序文件的结构：
admin.py　　　管理员


