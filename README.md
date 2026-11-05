# Servo_Serial

作业。通过串口uart2向两个舵机发送信号，使其进行增量移动。其中信号格式为：0xAA （舵机号） （增/减角度） 0xFF，支持一条指令同时控制两台舵机。其中0xAA，0xFF分别是包头和包尾，两个舵机号为0x01，0x02，分别对应TIM1的CHANNEL_3和CHANNEL_4。两电机初始化为90度，电机的可旋转角为0~180度，发送时注意用16进制，例：0xAA 0x01 0x1E 0x02 0x1E 0xFF。

Homework. Send signals to two servos via UART2 to make them move incrementally. The signal format is: 0xAA (servo ID) (increment/decrement angle) 0xFF, and a single command can control both servos simultaneously. 0xAA and 0xFF are the packet header and footer respectively; the two servo IDs are 0x01 and 0x02, corresponding to CHANNEL_3 and CHANNEL_4 of TIM1 respectively. Both motors are initialized to 90 degrees, and the rotatable angle range of the motors is 0~180 degrees. Remember to use hexadecimal when sending, for example: 0xAA 0x01 0x1E 0x02 0x1E 0xFF.
