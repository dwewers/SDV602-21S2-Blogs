# SDV601 - Week 13 Blog

------

#### <u>Threading</u>

------

This week I focused on finalizing my project and further improving the code where I could. The main focus was improving my chat thread. The problem I was having was that it would crash from time to time when I would close one DES, then open up another. I took a look at my code and read up on some documentation on Python threading. 

The main change I made was creating an if statement containing a global variable that would be checked every time the thread would loop through the function. By default, this would be set to false. This method is as follows:

```python
def chat_thread(self, session_id, window,):
        while True:
            Data.RetrieveMessages(self, app=App, session=session_id, window=window)
            global thread_status
            
            if thread_status:
                print('Chat thread has stopped')
                break
            
            print ('Chat has updated\n')
            time.sleep(2)
```

The value of `thread_status` is set prior to the chat thread running. In the case that `thread_status` is set to True, we break from the loop.

I set up a method that waits for the window event shown below. If this is detected, `thread_status` is set to True, causing it to be read as True the next time the thread method loops. We then use the `join()` method to terminate the thread.

```python
            if event in (sg.WIN_CLOSED, '_EXIT_'):
                thread_status = True
                t2.join()
                window.close()
                break
```

This subtle difference greatly improved the reliability of the application. In saying this, I cant guarantee that it will run as smoothly on my laptop as it has far less specs than my home PC. 

Another issue I was having was that there would be a delay from clicking the close button before the form would close. The reason this was happening is because the `time.sleep(2)` every time the loop was running. This meant that even if the thread was terminated, It would still run through the loop one last time. By adding `time.sleep(2)` at the end of the loop after the `if` statement, this removed the delay. If I were to have the sleep at the start of the loop, it would pause before checking the value of `thread_status.`

