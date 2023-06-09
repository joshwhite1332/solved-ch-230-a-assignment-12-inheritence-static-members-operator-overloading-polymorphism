Download Link: https://assignmentchef.com/product/solved-ch-230-a-assignment-12-inheritence-static-members-operator-overloading-polymorphism
<br>
<h1>Problem 12.1 <em>Hexagon class                                                                                        </em></h1>

Write a class called Hexagon which is derived from the RegularPolygon class. A hexagon has a side and a color. Provide methods for computing the perimeter and the area of a hexagon. For each property appropriate setter and getter methods need to be provided (i.e., it should not be possible to manipulate data directly). The class should also a parametric constructor, a copy constructor and a destructor.

Note, that the area of a hexagon of side t can be computed by using the formula.

Name the files Shapes.h and Shapes.cpp. Then write a testing program testHexagon.cpp that:

<ol>

 <li>creates a blue hexagon that has the side of 9,</li>

 <li>creates a green hexagon that has the side of 15,</li>

 <li>creates a copy for the second hexagon using the copy constructor, and</li>

 <li>computes the perimeter and area of all three hexagons and prints the results on the screen.</li>

</ol>

<table width="457">

 <tbody>

  <tr>

   <td width="457"><strong>Problem 12.2 </strong><em>TournamentMember class</em></td>

  </tr>

  <tr>

   <td width="457"> </td>

  </tr>

 </tbody>

</table>

<h2>Language: C++</h2>

Imagine that you are in the design stage of a software system for handling the data of the participants of a major soccer tournament. As different roles will be present (players, coaches, referees, etc.) you are required to develop a class handling the data of a generic league member. For each person the following data is at least needed

<ul>

 <li>first name as character array (36 characters characters including ’ ’)</li>

 <li>last name as character array (36 characters)</li>

 <li>date of birth as character array (11 characters, storage format is yyyy-mm-dd)</li>

</ul>

In addition the whole team is located somewhere, so location is an additional static property of the class.

Design and implement a class for holding these data. In addition add at least two other general properties to this class.

The class, which will be called TournamentMember, should provide constructors (empty and parametric), a destructor and also a copy constructor. The class should also provide inline setter and getter methods (either inside or outside of the class).

Moreover, in order to carry out the functionality of the application, the following methods are required:

<ul>

 <li>a method which prints the information of a tournament member on the screen,</li>

 <li>a method which changes the location.</li>

</ul>

Also all constructors and the destructor should print a short informational message on the screen, such that you can see which is being called when.

You should provide three files: a header file named TournamentMember.h with the declaration of the class, a file named TournamentMember.cpp with its definition, and an additional file called testTournamentMember.cpp with a main() function which tests the functionality of the class.

<em>The needed data can be initialized in the code from the main() function.</em>

<h1>Problem 12.3 <em>Player class                                                                                            </em></h1>

A Player class should be derived from the TournamentMember class. It holds additional properties such as number, position, number of goals scored, and whether the player is left-footed or right-footed. For each property appropriate setter (except the number of goals scored) and getter methods need to be provided as inline methods, and it should not be possible to manipulate data directly. An appropriate constructor to set all properties on creation should be provided as well as a copy constructor that creates a correct copy of a player, and a destructor. Also all constructors and the destructor should print a short informational message on the screen such that you can see which is being called when. Also the following methods are required:

<ul>

 <li>a method which prints all the information of a player on the screen,</li>

 <li>a method which increments the number of goals scored by a player.</li>

</ul>

Add code to the files TournamentMember.h, TournamentMember.cpp, and write a testing program named testPlayer.cpp that tests the functionality of the Player class. Create three players with different properties. Then move all players to the location “Hamburg”. <em>The needed data can be initialized in the code from the main() function.</em>

<h1>Problem 12.4 <em>Fractions I       </em>As a starting point, use the files fraction.h, fraction.cpp, testfraction.cpp (which you can download from:</h1>

<ul>

 <li>Replace the method print() by an overloaded operator &lt;&lt; such that you can use cout &lt;&lt; for printing a fraction on the screen.</li>

 <li>Overload the operator &gt;&gt; such that you can enter from the keyboard a fraction using cin &gt;&gt;. Check the validity of the input (you can assume that the numerator and denominator will be numbers).</li>

 <li>Overload the operators <sup>∗ </sup>and / for computing the multiplication and division of two fractions.</li>

 <li>In your testing program you should then be able to enter two fractional numbers (usingcin &gt;&gt;), then the product and quotient are printed on the screen (one per line using the overloaded operator and cout &lt;&lt;).</li>

</ul>

Use the suggestions from slide 10 (Tutorial 12) for choosing to write member methods or friend functions.

<em>You can assume that the input will be valid.</em>

<h1>Problem 12.5 <em>Fractions II                                                                                             </em></h1>

Continue with your program for <strong>Problem 12.4 </strong>in the following manner. Remember to check the mathematical validity of the parameters (you can assume that the nominator and the denominator are always numbers). Use the suggestions from slide 10 (Tutorial 12) for choosing to write member methods or friend functions.

Also consider the suggestions regarding the return types and parameter types.

<ul>

 <li>Overload the operators +, – for computing the sum and difference of two fractions.</li>

 <li>Overload the operator = for assigning.</li>

 <li>Overload the operators &lt; and &gt; to compare two fractions.</li>

 <li>In your testing program you should be able to enter two fractions from the keyboard usingcin &gt;&gt;. Determine the greater fraction and print it on the screen using cout &lt;&lt;. Also compute the sum and the difference of the two fractions (storing the result in other objects) and print them on the screen (one per line using the overloaded operator and cout &lt;&lt;).</li>

</ul>

In order to implement the addition and subtraction of two fractions you will have to calculate the lowest common multiple (LCM) of the denominators of the two fractions. The LCM can be com-

a · b

puted according to the formula: LCM(a,b) =                , where GCD is the greatest common

GCD(a,b)

divisor.

<h1>Operations with fractions</h1>

Addition:

<table width="414">

 <tbody>

  <tr>

   <td width="105">Subtraction:Multiplication:Division:</td>

   <td width="309">a c a · LCM(b,d)<em>/</em>b+c · LCM(b,d)<em>/</em>d+ = b d LCM(b,d)a c a · LCM(b,d)<em>/</em>b − c · LCM(b,d)<em>/</em>d− = b d LCM(b,d)a c a · c· = b d b · d</td>

  </tr>

 </tbody>

</table>

a c a · d

<em>/ </em>= b d b · c

<strong>Problem 12.6 </strong><em>Polymorphism I                                                    </em>from the terminal using g++.

<ul>

 <li>Draw (using ASCII characters) a diagram how these classes relate to each other and putthis into testvirtual.cpp as part of your comments.</li>

 <li>For each numbered point in the file testvirtual.cpp add a detailed comment about what is happening in the program.</li>

 <li>Like in Circle.cpp, output a message on the screen when the method calcArea() is being called in any of the classes.</li>

 <li>Add a method to calculate the perimeter for each class definition.</li>

 <li>Change the test program to additionally print the total perimeter of all objects.</li>

 <li>Also print a message on the screen when the method calcPerimeter() is being called.</li>

 <li>Add a Square class (consisting of a header file and a cpp file), and add a square object to your test program. Consider the relation of a square to the other classes.</li>

</ul>

Submit a <strong>zip </strong>file containing all your .h and .cpp files related to this problem.

<strong>Problem 12.7 </strong><em>Polymorphism II                                                                                     </em>

Change testvirtual.cpp such that 25 objects (circles, rings, rectangles, squares) are randomly created at runtime. Their colors (RED, BLACK, VIOLET and BLUE) and sizes (between 5 and 100) should also be randomly chosen.

Compute the area and the perimeter for each object and print them on the screen