This project will primarily investigate the average waiting times students will have to face during different times of the day, alongside an analysis of our model’s efficacy. 
We will model the coffee house as a queueing system, making assumptions as necessary.
Design of the simulation algorithm Rice’s coffeehouse operates as follows:
● There are one or two cashiers who take orders.
○ Number of cashiers depends on shift availability or number of customers.
● After getting their orders taken, the customers will wait until their name is called so they
can pick up their drink.
● The business opens at 7:00 AM and closes at 12:00 AM.
Our model can be seen as a tandem queue: i.e. two queues followed back to back, with some customers leaving after the first queue (Jackson network). The first queue is the cashier line, where a customer waits for his order to be taken. The second queue is where customers wait for their drinks to be made. For non-drink orders, the customers exit the system after leaving the first queue.
We will make the following assumptions in our model:
● 95% of orders are drink orders, 5% are non-drink orders (food items like croissants,
bagels, cinnamon rolls, etc).
● Service times are exponentially distributed.
● Each customer spends an average amount of $4.28 per visit.
● FIFO (“first in, first out”) queue.
● There are two types of drinks: fast drinks and slow drinks. Fast drinks, as the name
implies, are made fast, like ice chai or hot chocolates. Slow drinks use the sole espresso machine, and take longer to make.
○ Two types of drinks: Slow drinks are made at a rate of 70/hr and fast drinks are made at a rate of 150/hr.
○ Additionally, orders take around 45 seconds to complete, giving us a cashier
service rate of 80/hour.
● One person in the cashier line (the number of cashiers varies too much to take into
account). The queues are therefore both M/M/1 (although there is more than one person
making a drink, they serve as one drink-making “server”).
● There is no “capacity” to the queue(s):
○ Lines can sometimes go out of Chaüs and into the hallways of the RMC.
○ Although there isn’t unlimited space, the extrapolated arrival rates already take
into account people who get discouraged to go in the line.
○ Additionally, coffee can be seen as an inelastic good, where many customers
would be willing to stand in long lines to get it.
These assumptions will simplify our model and allow us to generalize the behaviors of workers and customers. We won’t be taking into account specific situations such as broken espresso machines or missing workers because (a) we don’t have the data to correctly simulate these situations and (b) we don’t want to take into account too many factors, as it could overly complicate our model, potentially losing accuracy.
