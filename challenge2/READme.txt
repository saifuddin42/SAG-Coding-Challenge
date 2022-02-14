Details about implementing Statistic interface:

- I have assumed the input to be prices of arbitrary unnamed products.
- These prices are of type integers.
- I wanted to simulate continuous random input so I:
	- Wrote a for loop to send prices continuously
	- Implemented 2 threads to simulate random access
- My implementation runs locally in-memory assuming app is not orchestrated in cloud
	- So used ArrayList to work as db for prices
- Used class level synchronization to block computational calls and make transactions thread safe
- Added pauses between steps to give a chance for the threads to context switch
	