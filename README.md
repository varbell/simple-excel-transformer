# simple-excel-transformer
View the internals of a simple transformer that can add single digits between 0 and 9. This simple model was trained in python, then copied the weights over. Everything should be organized and color coded appropriately to help you follow the logic of the inside of a transformer step by step.

vocab size: 12 (one, two, three, four, five, six, seven, eight, nine, ten, plus, equals)

model dim: 8

sequence length: 4 :)

layers: 1

heads 4

PE: RoPE

To Start:
  - Clone the repo and open the excel sheet.
  - Change the text to add two numbers that will result in a single digit. "one plus one equals", "three plus four equals".
    
    <img width="1108" height="383" alt="image" src="https://github.com/user-attachments/assets/2339513c-05dc-4bf1-be43-4f0f79e6eabc" />

  - I highly recommend for you to open a "New Window" and scroll one of the windows to see how the various matrices change in real time as you change the values.
    
    <img width="672" height="219" alt="image" src="https://github.com/user-attachments/assets/1577e393-3dd3-4287-b271-fb184c4871aa" />

    
