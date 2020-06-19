#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) If we were simply incrementing or decrementing from a the runtime would be O(n). But what I gather from looking into runtimes is that with the multiplication taking place the runtime ends up being O(logn). I'm not entirely sure why, though. 


b) With nested loops the runtime is O(n^2) because for each iteration of the outside loop, with runtime O(n), the inside loop also has a runtime of O(n).


c) Since this recursion is just being called once in the return it should have a runtime of O(n). After all, we're just adding the amount of bunnies until there aren't anymore to add.

## Exercise II

Runtime complexity: O(logn)

Given a height of n, I'd go to floor n/2 and drop an egg. If it broke I'd then go to floor (n/2)/2 = n/4 and drop an egg. If the first egg did not break then I would move up to floor 3n/4 and drop an egg. 

What is happening is that I am taking the whole interval of unknown and splitting it in half. Drop an egg from that floor. If the egg breaks then we're too high so the top of the next interval to search becomes the floor I just dropped an egg from and repeat the process. If the egg did not break then we can go higher and the floor I just dropped an egg from becomes the bottom of the next interval to be split in half. Each time an egg breaks that floor becomes the top. Each time an egg doesn't break that floor becomes the bottom. This repeats for logn times until we have found two adjacent floors where the bottom one is low enough that the egg doesn't break but the one above it the egg does break.
