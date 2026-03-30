# tft180-stm32f103c8t6-flash-UI-
感谢 WwuSama大佬
https://www.bilibili.com/video/BV1LCh9zrEMp?t=1.8 这是原作者的视频教程
我也使用到了江协科技的flash库和长按按键，添加了一些功能
MyProblem.docx是我对原代码的底层驱动的一些更改的说明
##不过这里有一个问题，每次动态添加文件时直接烧录会造成初始数据对应不上的问题，由于flash_index 先后顺序的问题，
比如 目前已经有 aaa bbb ccc 三个文件 ， 若添加文件为 aaa bbb eee ccc 则eee显示的数据为 ccc 的 ， 若 添加文件后顺序为 aaa bbb ccc eee 则 eee 对应数据为0 ，其余数据不变
解决方法：每次添加文件后将对应flash擦除即可 ， 可以使用stlink utility


