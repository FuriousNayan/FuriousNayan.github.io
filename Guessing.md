# Guessing Game Flow Chart

```mermaid
flowchart TD
   Starting(Start)
   Starting-->random_comp_num[/Computer_generate_random_#/]
   Starting-->random_user_num[/User_input_#/]
   random_user_num-->nonnum{Is_user#_numerical}
   nonnum-->Yes
   nonnum-->No
   No-->Starting
   random_comp_num-->decision1{comp#  >  user#}
   Yes-->decision1{comp#  >  user#}
   random_comp_num-->decision2{comp#  <  user#>}
   Yes-->decision2{comp#  <  user#>}
   random_comp_num-->decision3{comp#  =  user#>}
   Yes-->decision3{comp#  =  user#>}
   decision1-->#_is_too_HIGH,_try_again
   decision3-->#_is_equal,_Great_Job!
   decision2-->#_is_too_LOW,_try_again
   #_is_too_LOW,_try_again-->Starting
   #_is_too_HIGH,_try_again-->Starting
   


```
## Documentation
First, it starts at the start node.

Then moves on to User Input and asks if it is numerical. If it is, it moves on, if its not, they have to start back. 

At the same time, the computer has already generated its number. 

After both the user input and computer input has finished, it moves on to each of the decisions. 

If our number is less than the computer number, it makes us restart.

If our number is higher than the computer number, it also makes us restart.

If it is spot on, you won.





