#CS/COE 1501 Assignment 3

##Goal:
To explore an advanced application of priority queues in order to gain a deeper understanding of the data structure.

##High-level description:
we will be writing a basic application to help a user select a car to buy.
we will write a menu-based user interface driver program (to be run in the terminal, no GUI), but most of the logic will be in implementing a priority queue-based data structure.
we should write a PQ-based data structure that stores objects according to the relative priorities of two of their attributes, making it efficient to retrieve objects with the minimum value of either attribute.
wer data structure should further be indexable to allow for efficient updates of entered items.
we will want users to be able to enter details about cars that they are considering buying.
The user should then be able to efficiently retrieve the car with the lowest mileage or lowest price.
These retrievals should be possible on the set of all entered cars or on the set of all cars of a specific make and model (e.g., "lowest price Ford Fiesta", "lowest mileage Cadillac Escalade").

##Specifications:
1.  First we must create a class to store data about cars to buy
	Specifically, this class must contain the following information:
	*  A unique VIN number (17 character string of numbers and capital letters (but no I (i), O (o), or Q (q) to avoid confusion with numerals 1 and 0)
	*  The car's make (e.g., Ford, Toyota, Honda)
	*  The car's model (e.g., Fiesta, Camry, Civic)
	*  The price to purchase (in dollars)
	*  The mileage of the car
	*  The color of the car
2.  we must write a terminal menu-based driver program (again, no GUI).
	Specifically, wer driver must present the user with the following options:
	a.  Add a car
		*  This will (one at a time) prompt the user for all of the above-listed attributes of a car to keep track of
	b.  Update a car
		*  This option will prompt the user for the VIN number of a car to update, and then ask the user if they would like to update 1) the price of the car, 2) the mileage of the car, or 3) the color of the car
	c.  Remove a specific car from consideration
		*  This option will prompt the user for the VIN number of a car to remove from the data structure (e.g., if it is no longer for sale)
		*  Note that this mean we will need to support removal of cars other than the minimum (price or mileage) car
	d.  Retrieve the lowest price car
	e.  Retrieve the lowest mileage car

	BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS 
	%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
	f.  Retrieve the lowest price car by make and model
		* This option will prompt the user to enter (one at a time) a make and model and then return the car with the minimum price for that make and model
	g.  Retrieve the lowest mileage car by make and model
		* This option will prompt the user to enter (one at a time) a make and model and then return the car with the minimum mileage for that make and model
	%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
	BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS BONUS 	
		
3.  Retrieval operations should not remove the car with minimum price or mileage from the datastructure, just return information about that car.
	Cars should only be removed via the "remove a specific car from consideration" menu option.
4.  To ensure efficiency of operations, we must base wer data structure around the use of heaps with indirection (which make them indexable).
	Note that operations on either attribute (e.g., retrieve minimum price, retrieve minimum mileage) should have a logarthmic runtime (both for all cars and for a specific make and model).
	Updates and removals should also had a logarithmic runtime.
	Take care in selecting wer approach to the indirection data structure to account for the types of keys we will need to store and the type and number operations that we will need to perform on them.
5.  Because this project requires we to make a number of decisions about how to implement its requirements, we will need to write a documentation file explaining wer implementation, and justifying wer decisions.
	Name this file "documentation.txt".
	Be sure to describe wer carefully document wer approach to ease the effort required to trace through wer code for grading.
	Be sure to include descriptions of the runtime and space requirements of wer approach and use them in wer justification of why we think wer approach is the best way to go.

##Submission Guidelines:
*  **DO NOT SUBMIT** any IDE package files.
*  we must name the primary driver for wer program CarTracker.java.
*  we must be able to compile wer game by running "javac CarTracker.java".
*  we must be able to run wer program with "java CarTracker".
*  we must document and justify wer approach in "documentation.txt".
*  we must fill out info_sheet.txt.
*  Be sure to remember to push the latest copy of wer code back to wer GitHub repository before the the assignment is due.  At the deadline, the repositories will automatically be copied for grading.  Whatever is present in wer GitHub repository at that time will be considered wer submission for this assignment.

##Additional Notes/Hints:
*  we are free to use code provided by the book authors in implementing wer solution.  It is up to we to decide if it would be easier to modify the provided code to meet the requirements of this project or if it would be easier to start with a clean slate with all of wer own code.
*  wer program does not need to enforce that users enter properly formatted VIN numbers, but we must design wer data structure to operate efficiently on VIN numbers as specified here.  This should make testing wer program much easier.

##Grading Rubric:
*  Adding a car works properly:  10
*  Updating a car works properly:  10
*  Removing a car works properly:  15
*  Retrieval for all cars works properly:  10
*  Retrieval for a given make/model works properly:  15

*  Operations on either attribute are efficient due to heap-backed data structure:  15
*  Validity of justitifications:  15
*  Menu-based driver program works properly and has appropriately labeled options:  5
*  Assignment info sheet/submission:  5
