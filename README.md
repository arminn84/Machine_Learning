# Algorithms and models have been developed using the TensorFlow and PyTorch frameworks.
<img width="355" alt="Screenshot 2023-12-03 at 12 25 31 PM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/69dbcce9-fd44-4a72-9a23-fe4a1368a460">

### Detailed information is available on my website https://www.arminnabaei.com/

## The proposed optimizer and SoftMax loss functions are implemented in TensorFlow.

###
To invoke the custom Adaptive Soft Margin SoftMax function:
```ruby
from ASoftMax import my_forward
```

Next, simply replace the last layer with the corresponding command:

<img width="729" alt="Screenshot 2023-12-01 at 4 08 25 AM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/f49d2f6c-9150-455c-adb6-f96254254ba9">

```ruby
x_1 = Dense(num_classes,kernel_initializer="he_normal")(prev_input)
out =Activation(my_forward,dynamic=True, name='MyProposed_SoftMax')(x_1)
```

<img width="467" alt="Screenshot 2023-11-30 at 1 05 20 PM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/c831a9c2-c351-420a-b7a2-7f679dd00be8">
<img width="475" alt="Screenshot 2023-11-30 at 1 05 38 PM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/ba8af3ad-f92e-422f-b1eb-b8c906d553d8">


###


To call My proposed First-Order Optimizer, Use These lines of Codes to Call it:

```ruby
from AADAM import ArminAdam
optimizer= ArminAdam(lr=0.001)
```

###
<img width="437" alt="Screen Shot 2023-09-28 at 12 29 05 AM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/d085d97c-d1b7-4309-908c-8dc1736cb86e">


<img width="674" alt="Screenshot 2023-11-26 at 3 42 01 PM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/3fa85f23-193e-4ffc-83a4-a08d48b0a59c">


################

To call My Proposed Classification Loss and Class-Weight Functions, Use the  comment Line:
```ruby
loss=MyLoss()
```
<img width="360" alt="Screenshot 2023-11-30 at 1 00 13 PM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/c3554520-362f-4473-b642-926b682ee8a1">
<img width="358" alt="Screenshot 2023-11-30 at 1 00 23 PM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/3a5bd62e-0450-429f-82a8-07af765b1c4c">

#####
To call Loss Class-Weight Functions, Use the below comment Lines:
``` ruby
class_weights = create_class_weight(labels_dict)
```
<img width="466" alt="Screenshot 2023-12-01 at 4 02 15 AM" src="https://github.com/arminn84/Machine-Learning/assets/150948007/c03f9cc6-dafe-41f2-8b90-5e371da0c3ef">
______________________________________________

# CALL MY PROPOSED FUNCTIONS
### download functions, run the below lines in your model 
``` ruby
from ASoftMax import my_forward
from AADAM import ArminAdam
from ALoss import MyLoss
from AClass_Weight import create_class_weight


optimizer= ArminAdam(lr=0.001)
loss=MyLoss()
class_weights = create_class_weight(labels_dict)
```
