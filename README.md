# Code
We modify the Arducam and VGA code and combine them, we give up using two cores as it's too difficult to debug. And now our bluetooth and APDS9960 can work well. The difficulty we met is how to change the image_buf(342 * 342) the camera output to fit the distinguishability the VGA transmit(640 * 480). And the code can be find [here](https://github.com/zgu74/Midpoint/tree/main/code).
# Media

## Materials

### HC-05 Bluetooth

![s-l500](https://user-images.githubusercontent.com/113784775/205466567-b379e764-0846-464e-8778-730bc205725e.jpg)

### Pico4ML

![微信图片_20221203194733](https://user-images.githubusercontent.com/113784775/205468396-f7646e87-75a1-4214-ab9a-8d6017183e20.jpg)


### VGA Cable

![s-l500 (2)](https://user-images.githubusercontent.com/113784775/205466681-2ccdc137-2668-424a-b9be-4e1992579cb4.jpg)

## Design

### Bluetooth Connection

![屏幕截图 2022-12-03 184500](https://user-images.githubusercontent.com/113784775/205467149-b96d1534-7d5f-4914-8015-6228fa00b566.png)

![屏幕截图 2022-12-03 185128](https://user-images.githubusercontent.com/113784775/205467151-843577f6-6d56-4efd-be85-ceb20e9fbcb4.png)

### VGA Connection

![屏幕截图 2022-12-03 185335](https://user-images.githubusercontent.com/113784775/205467206-fe48b1a6-c549-4ea1-abde-f6b091f83e84.png)

![微信图片_20221203185350](https://user-images.githubusercontent.com/113784775/205467209-7b4c89e7-08e7-4880-9561-0236a52191c1.jpg)

### Troubleshooting

We check the timing of Pico4ML output via the logic analyzer and change the output frequency to the timing supported by the screen. The first one is the correct frequency. The second one is half due to the clock of the camera.

![微信图片_20221203185523](https://user-images.githubusercontent.com/113784775/205467244-2c7dd666-0b06-4c3f-9c1d-4e05155bc394.jpg)

![微信图片_20221203185528](https://user-images.githubusercontent.com/113784775/205467245-752f47a9-20c3-4eb7-9f7f-05118b6eaa11.jpg)

## Demos

### Bluetooth

![微信图片_20221203191030](https://user-images.githubusercontent.com/113784775/205467584-b032c731-ce50-4dac-a9cc-8e1ce9742040.png)

![屏幕截图 2022-12-03 190815](https://user-images.githubusercontent.com/113784775/205467585-d6ccfc88-647e-4016-94cb-82a4b1cf98a6.png)


### VGA

![微信图片_20221203185357](https://user-images.githubusercontent.com/113784775/205467458-4bdabee5-d0f7-4fdd-b7a5-f152e3e446d3.jpg)

We are trying to improve the quality of pictures transmitted from the Pico4ML to the screen. Since it is a difficult and heavy task for us, we also have a backup plan that only send words to the screen through VGA and pictures are transmitted to the computer.

## Diagram

![屏幕截图 2022-12-03 181023](https://user-images.githubusercontent.com/113784775/205467300-d856ba9a-1267-4d9a-87d6-d1f615dab6c7.png)


