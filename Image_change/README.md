将彩色图片转换为用字符显示（hen简单的无聊之举）
   --简单的图片应用
   
   
将彩色图片的RGB的值转换为相应的灰度值
        gray = int(0.2126 * r + 0.7152 * g + 0.0722 * b)


再进行图片和字符之间的映射，遍历图片的两个通道用txt显示        