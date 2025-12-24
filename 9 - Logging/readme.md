1- In main.cpp :

I put my name with my student ID

while (true) { // Loop forever
		runTimeStats();
		vTaskDelay(5000);
		printf("Jade REBEYROLLE F14128807");
	}


2- In Cmakelist :

I removed a part of this line : 

include(pico_sdk_import.cmake)
