Tractor Jack is a notorious pirate captain who sails the Saskatchewan River plundering farms for wheat, barley, and all the other grains. You may remember him from his exploits in CMPT 141 or CMPT 214. Jack wants to simulate the loading of cargo onto his ships so he can track how much of one type of grain is on a given ship, and to make sure that his ships are not overloaded.2
In this problem you will be given a list-of-lists data structure. It will be a list of Ship objects, each of which contains a list of Sack objects. Each Sack object represents one sack of a particular type of grain.
The type of grain in a sack is represented by a value of type Grain, where Grain is an enumeration. 

**Enumerations**
In this question use a data type in Java called an enumeration to represent the type of grain in a sack.
Enumerations define a fixed set of named constant values. The grains Jack most commonly plunders
are wheat, barley, oats and rye so he wants to count the amount of those four grains separately. Any
other types of grain he wants to count together. We can use an enumeration to define five constants
to denote what type of grain is in a sack:

enum Grain {
WHEAT , BARLEY , OATS , RYE , OTHER
}

This declaration defines a data type called Grain and five values which we can assign to variables of type Grain. You can find it at the top of Sack.java. Now we can then write in Java:
Grain g = Grain.WHEAT; // Assign value WHEAT to the variable g 
You’ll need to use one of the values from the Grain enumeration in task 3, below. 

**Description of Files Provided**
You are provided with three Java files:
Sack.java: Contains the class Sack which is an object that represents a sack of grain. A sack of grain has a grain type, and a weight (in pounds). This object is complete and you will not need to edit this file, but you should familiarize yourself with its data and methods. This file also contains the definition of the enumerated type Grain.
Ship.java: Contains the class Ship which represents a ship in Jack’s fleet. Each ship has a name, a capacity (weight in pounds), and contains a list of Sack objects which represent the ship’s cargo. This class contains two unfinished methods that you will write (see below). Familiarize yourself with the other methods and instance variables of this class.
CargoSimulator.java This file contains the CargoSimulator class. This class generates the data you’ll be working with for this question. Its constructor generates a list of ships and fills them with sacks of grain. You’ll be writing some code in the main() method of this class (see below).


**Your Tasks**
1. In Ship.java, complete the isOverloaded method. This method must return a boolean value true if the ship is overloaded, and false otherwise. The ship is overloaded if the total weight of all sacks of grain in its cargo exceeds the ship’s capacity.
2. In Ship.java, complete the sacksOfGrainType method. This method must return the number of sacks of grain of the grain type indicated by its parameter that are in the ship’s cargo. That is, if the parameter type is Grain.WHEAT and the ship’s cargo contains 42 sacks of wheat, the method should return 42.
3. In the main() method of CargoSimulator.java, there is an instance of a CargoSimulator object called sim. As described above, this object contains a list of ships, and each ship contains its list of cargo. At the location indicated, print out how many sacks of wheat each ship in sim is carrying.
4. Inthemain()methodofCargoSimulator.java,printoutamessageforeachshipintheCargoSimulator instance sim that is overloaded. If a ship is not overloaded, print nothing.
   
**Implementation Notes**
Upon inspection of the constructor for CargoSimulator, it may appear that the data is being randomly generated. The data is “randomly” generated, but a fixed random seed is used to ensure that the same random instance of the data is generated every time the program is run. Thus, you should expect that the data will always be the same, and that you will get the same answer every time. That said, it is possible that different computers and/or operating systems will generate different data. However, on the same machine within the same operating system, the same data will be generated every time.

**Sample Output**
Here is what the output might look like. This demonstrates the form of the output only, and not
the expected numbers. The exact numbers may depend on the random number generator for your
operating system.

The Icebreaker is carrying 37 sacks of wheat. The Salty Farmer is carrying 46 sacks of wheat. The Bunnyhug is carrying 40 sacks of wheat.
The Blackstrap is carrying 37 sacks of wheat. The Prairie Onion is carrying 40 sacks of wheat. The Icebreaker is overloaded!
The Salty Farmer is overloaded!
The Blackstrap is overloaded!
