# Arduino


## 1. Arduino简介  

Arduino是一种开源电子原型平台，由硬件和软件组成，旨在让用户能够快速、轻松地创建互动项目。Arduino开发板通常使用微控制器作为核心，用户可以通过Arduino IDE编写代码，并将其上传到开发板上，以控制各种传感器、LED、马达等设备。Arduino的设计思想强调易学易用，使得无论是刚入门的初学者，还是经验丰富的开发者，都能在其基础上快速实现创意。凭借丰富的社区资源和众多可用的库，Arduino在教育、艺术、科学和DIY项目中得到了广泛的应用。  

## 2. 连接图  

![](media/fbde4632bc0bf86f147e1c9dd6aa8664.png)  

## 3. 测试代码  

```cpp  
// 定义数字口13  
int ledPin = 13; // 定义数字口13  
int inputPin = 3; // 定义数字口3  

void setup() {  
    pinMode(ledPin, OUTPUT); // 将ledPin设置为输出  
    pinMode(inputPin, INPUT); // 将inputPin设置为输入  
}  

void loop() {  
    int val = digitalRead(inputPin); // 设置数字变量val，读取到数字口3的数值，并赋值给 val  
    if (val == LOW) { // 当val为低电平时，LED亮起  
        digitalWrite(ledPin, HIGH); // LED亮起  
    } else {  
        digitalWrite(ledPin, LOW); // LED变暗  
    }  
}  
```  

## 4. 测试结果  

按照上图接好线，烧录好代码后，上电后，传感器在检测到黑色或没有检测到东西时，板上的D13指示灯不亮，传感器上D1指示灯不亮；传感器在检测到其他颜色时，信号端输出高电平，板上的D13指示灯亮，传感器上D1指示灯亮起。旋转电位器可调节灵敏度，将D1调节至亮与不亮的临界点时，灵敏度最高。




