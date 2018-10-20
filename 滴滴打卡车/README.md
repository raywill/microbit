# 滴滴打卡车

```
/*

microbit 小车自带超声波传感器、避障传感器，基于这两个传感器可以检测到 “刷卡行为”。

检测到刷卡行为后，通过车身蜂鸣器，车顶LED灯，开发板 LED 阵列来做出响应动作。

*/

let distance = 0
input.onButtonPressed(Button.A, () => {
    music.playTone(2110, 200)
    basic.pause(100)
    game.addScore(1)
})


let playtimes = 0
qbit.qbitInit()
basic.forever(() => {
    distance = qbit.Ultrasonic()
    qbit.clearLight()
    let obbstacleDetectorAlert: boolean = 
        qbit.obstacleSensor(qbit.ObstacleSensor.SENSOR1_OBSTACLE) ||
        qbit.obstacleSensor(qbit.ObstacleSensor.SENSOR2_OBSTACLE);
    let distanceDetectorAlert : boolean =  
        distance > 0 && distance < 10;

    let detectorAlter : boolean = (obbstacleDetectorAlert || distanceDetectorAlert);
    if (detectorAlter && playtimes < 2) {
        music.playTone(2110, 200)
        playtimes += 1
        game.addScore(1)
        qbit.setPixelRGB(0, playtimes);
        qbit.setPixelRGB(1, playtimes);
        qbit.setPixelRGB(2, playtimes);
        qbit.setPixelRGB(3, playtimes);
        qbit.showLight()
        basic.pause(100 * playtimes)
    } else {
        playtimes = 0
        basic.clearScreen()
        basic.pause(50)
    }
})

```
