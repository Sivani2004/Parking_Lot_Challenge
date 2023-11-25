# Parking_Lot_Challenge

Create a parking lot class that takes in a square footage size as input and creates an array of empty values based on the input square footage size. Assume every parking spot is 8x12 (96 ft2) for this program, but have the algorithm that calculates the array size be able to account for different parking spot sizes. For example, a parking lot of size 2000ft2 can fit 20 cars, but if the parking spots were 10x12 (120 ft2), it could only fit 16 cars. The size of the array will determine how many cars can fit in the parking lot.

Create a car class that takes in a 7 digit license plate and sets it as a property. The car will have 2 methods:

   1) A magic method to output the license plate when converting the class instance to a string.
   2) A "park" method that will take a parking lot and spot # as input and fill in the selected spot in the parking lot. If another car is parked in that spot,           return a status indicating the car was not parked successfully. If no car is parked in that spot, return a status indicating the car was successfully parked.

Have a main method take an array of cars with random license plates and have them park in a random spot in the parking lot array until the input array is empty or the parking lot is full. If a car tries to park in an occupied spot, have it try to park in a different spot instead until it successfully parks. Once the parking lot is full, exit the program.

Output when a car does or does not park successfully to the terminal (Ex. "Car with license plate [LICENSE_PLATE] parked successfully in spot [SPOT #]").

Description upon Code Implementation:
  
  1) ParkingLot Class:
  >>__init__(self, square_footage, spot_size=(8, 12)): Initializes a ParkingLot object with the given square footage and spot size. It calculates the initial           number of available spots based on the spot size and square footage.
  >> park_car(self, car, spot): Parks a car at the specified spot if the spot is available. Updates the parking map and decreases the available spots.
  >> generate_parking_map(self): Returns the parking map as a dictionary.
  >> max_cars(self): Calculates and returns the maximum number of cars that can be parked in the parking lot based on its square footage and spot size.

  2) Car Class:
  >> __init__(self, license_plate): Initializes a Car object with a given license plate.
  >> __str__(self): Returns a string representation of the car object.
  >> park(self, parking_lot): Attempts to park the car in a randomly chosen spot in the parking lot. Returns a status message indicating whether the car was parked      successfully.

  3) Main Method (main function):
 * Takes input for the square footage of the parking lot.
 * Creates a ParkingLot object based on the provided square footage.
 * Calculates and prints the maximum number of cars that can be parked in the given square footage.
 * Takes input for the number of cars and their license plates.
 * Creates Car objects using the provided license plates.
 * Attempts to park each car in the parking lot until the parking lot is full or there are no more cars.
 * Prints the parking status for each car.
 * Prints the final parking map.
 * Optionally writes the parking map to a JSON file named "parking_map.json".
 * Optionally, you can upload the file to an S3 bucket (this part is commented out and needs to be implemented based on your S3 setup).

    The program is designed to simulate a parking lot scenario, where cars are randomly assigned parking spots until the parking lot is full or there are no more       cars to park. The parking map is printed at the end, showing which cars are parked in which spots.






