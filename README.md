# Django
this is the django trainee assignment for the second round of my Selection.....
 QUESTION 1 - By default, Django signals are executed synchronously. This means that when a signal is sent, the code that triggered the signal will wait for all connected receivers to finish executing before continuing.


def receiver(sender):
    print("Receiver started")
    time.sleep(5)  # Simulate some long-running task
    print("Receiver finished")


def sender_function():
    print("Sender started")
    my_signal.send(sender=None)
    print("Sender finished")

sender_function()



When we run the sender_function, the output will be:

Sender started
Receiver started
Receiver finished
Sender finished


the sender_function waits for the receiver to finish executing before continuing. This demonstrates that Django signals are executed synchronously by default.
