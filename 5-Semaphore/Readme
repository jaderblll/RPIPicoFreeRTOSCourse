LimitWorkers :

1. In mainTask, we add one worker :

	BlinkWorker worker4(LED4_PAD);

2. In mainTask we also change the semaphore to have 2 jetons and we add the semaphore to the last worker :

SemaphoreHandle_t sem = xSemaphoreCreateCounting(2, 2);
	worker1.setSemaphore(sem);
	worker2.setSemaphore(sem);
	worker3.setSemaphore(sem);
	worker4.setSemaphore(sem);

3. Now we start the 4th worker with the task on it :

worker4.start("Worker 4", TASK_PRIORITY);

4. In the loop I put my name with my student ID :

while (true) { // Loop forever
		runTimeStats();
		vTaskDelay(3000);
    printf("Jade REBEYROLLE F14128807");
	}

