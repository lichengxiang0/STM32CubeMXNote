# STM32CubeMX learn  


## 移植原子例程中的TFTLCD  
以前只是直接用原子中固件库，现在尝试用STM32CubeMX来驱动TFTLCD，也就是移植到Cube上。发现的问题:原子的函数，对TFTLCD有5个引脚未用到，应为初始化并没有看到，所以  
```
T_MISO  
T_MOSI
T_PEN  
T_CS  
T_SCK  
```
都没有用到。发现Cube不能直接配置复用推挽和复用开漏模式  
