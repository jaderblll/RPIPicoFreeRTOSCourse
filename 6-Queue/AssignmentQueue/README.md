main.cpp :

1- //LED PAD to use
#define LED_PAD				25
#define LED1_PAD			2
#define LED2_PAD			3
#define LED3_PAD			4
#define LED4_PAD			5

First I changed the value of the ledpad. It was 0 and I changed it into 25.

2- int main( void )
{
	//Setup serial over USB and give a few seconds to settle before we start
    stdio_init_all();
    sleep_ms(10000);
    printf("GO\n");
    printf("REBEYROLLE JADE F14128807 ");
    //Start tasks and scheduler
    const char *rtos_name = "FreeRTOS";
    printf("Starting %s on core 0:\n", rtos_name);
    vLaunch();


    return 0;
}

Then, in the main, I changed the value in sleep ms, I put 10000 and it was 2000.
And I also put my name with my student ID.
