BlinkASSIGNMENT

1. I changed the LED here
//LED PAD to use
#define LED_PAD				1
#define LED1_PAD			2
#define LED2_PAD			3

2. Here I put my name and my ＩＤ　ａｎｄ　Ｉ　ｐｕｔ　２０００　（ｉｔ　ｗａｓ　３０００）
while (true) { // Loop forever
		runTimeStats();
		vTaskDelay(2000);
		printf("Jade REBEYROLLE F14128807");
	}


MultyBlink (Midterm chapter 4) 

1. First I added in the LED Pad and I defined all the other LEDS :

#define LED3_PAD 5
#define LED4_PAD 6
#define LED5_PAD 7
#define LED6_PAD 8
#define LED7_PAD 9


2. Now in the function MainTask I added the workers for all the LEDs

	BlinkAgent worker4(LED4_PAD);
    BlinkAgent worker5(LED5_PAD);
	BlinkAgent worker6(LED6_PAD);
	BlinkAgent worker7(LED7_PAD);

And also this : 

    worker5.start("Worker 5", TASK_PRIORITY + 4);
    worker6.start("Worker 6", TASK_PRIORITY + 5);
    worker7.start("Worker 7", TASK_PRIORITY + 6);

3. Then, in the loop I added my name and my student ID : 

	while (true) { // Loop forever
		runTimeStats();
		vTaskDelay(3000);
        printf("Jade REBEYROLLE F14128807");
	}


How many tasks you could create via RP2040 now?

After experimenting with the Chapter 4 program and increasing the number of tasks,
the RP2040 was able to handle around 80–100 FreeRTOS tasks running simultaneously (depending on stack size and code complexity).

Each task consumes memory for its stack and control block, and once the 264 KB RAM of the RP2040 is full, new tasks can no longer be created.

Beyond this limit, the scheduler fails to start new tasks or the board resets due to memory exhaustion.

