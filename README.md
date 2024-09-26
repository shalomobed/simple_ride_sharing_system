# A Simple Ride-Sharing System
Let's consider a two-dimensional city where positions are defined using x and y coordinates.
Within this city, multiple cars and passengers are situated at various locations. As illustrated in the
image above, you can see the positions of two cars and two passengers. The cars, passengers, and
their respective positions can be represented by the 'Car,' 'Passenger,' and 'Location' classes
respectively. The UML diagrams depicting these classes are provided below. This city operates a
straightforward ride-sharing system, which is represented by the ‘RideSharingApp' class in the
UML diagram below.

Implement these four classes using Python. Below is a brief description of those classes:
## 1. Location
This class has 2 data attributes and 2 methods.
### Data attributes
x - An integer value representing the x-coordinate
y - An integer value representing the y-coordinate
### Methods
__init__(self, x, y): It is the constructor of the class. It should assign the given
parameters to the corresponding data attributes.
__str__(self): This method should return a string representation of the
location object. The format of the string should be similar to - ‘(x,y)’
## 2. Car
This class has 3 data attributes and 3 methods.
### Data attributes
car_name - A string representing the name of the car.
location – An object of the ‘Location’ class representing the position
of the car within the 2-dimensional space.
cost_per_mile – A floating point number representing the car’s fare per mile.
### Methods
__init__(self, name, location, cost): It is the constructor of the class. It should assign
the given parameters to the corresponding data attributes.
__str__(self): This method should return a string representation of a car object. The
format of the string should be similar to - ‘[car_name, location, cost_per_mile]’
move_to(self, new_x, new_y): this method should update the x and y coordinates
of the ‘location’ attribute to new_x and new_y
CSC 1302 / DSCI 1302 Homework 1 Due date: Fri, 13-Sep-2024 11:59PM
## 3. Passenger
This class has 2 data attributes and 3 methods.
### Data attributes
passenger_name - A string representing the name of the passenger.
location – An object of the ‘Location’ class representing the position
of the passenger within the 2-dimensional space.
### Methods
__init__(self, name, location): It is the constructor of the class. It should assign the
given parameters to the corresponding data attributes.
__str__(self): This method should return a string representation of a passenger
object. The format of the string should be similar to – ‘[passenger_name, location]’
move_to(self, new_x, new_y): this method should update the x and y coordinates
of the ‘location’ attribute to new_x and new_y.
## 4. RideSharingApp
This class has 2 data attributes and 7 instance methods.
### Data attributes
cars – A list of ‘Car’ objects
passengers – A list of ‘Passenger’ objects
### Methods
__init__(self): It is the constructor of the class. It should set the ‘cars’ and
‘passengers’ attributes to empty lists.
add_car(self, car) - adds the given car object to the ‘cars’ attribute
add_passenger(self, passenger) – adds the given passenger object to the
‘passengers’ attribute
remove_car(self, car) – removes the given car object from the ‘cars’ attribute
remove_passenger(self, passenger) - removes the given passenger object from the
‘passengers’ attribute
find_cheapest_car(self) – This method finds the cheapest car and prints the string
representation of that car. The cheapest car is determined based on the
‘cost_per_mile’ attribute of the car objects.
find_nearest_car(self, passenger) – This method finds the nearest car for the given
‘passenger’ object and prints the string representation of that car. The nearest car is determined based on the distance between the passenger and the available cars.
For example, if a passenger’s location is (x1, y1) and a car’s location is (x2, y2), their
distance can be calculated according to: d= sqrt((x2 - x1)^2 +(y2-y1)^2)
