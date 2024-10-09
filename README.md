Family Tree Generator
Problem Statement
Develop a C++ program for building and visualizing a hierarchical family tree. The program should allow users to interactively add family members, specify their parent-child relationships, and visualize the family tree's structure. The program must handle scenarios where users attempt to add a family member to a specified parent who may or may not exist within the tree.

Constraints:
Each individual in the family tree is represented by their name, birthdate, and a list of their children.
The family tree begins with a single root individual.
The program should support adding and visualizing multiple generations in the family tree.
Visualization should use ASCII-based hierarchy representation for clarity.
The program should provide user-friendly input validation and error messages for invalid operations.
Motivation
The motivation behind creating a family tree generator in C++ stems from several factors:

Educational Purposes: Developing a family tree generator serves as a valuable learning exercise, giving understanding of data structures and their practical implementations. It provides an opportunity to apply concepts of tree data structures in a real-world context, thereby enhancing the understanding of data organization and management.

Problem-Solving and Algorithmic Thinking: Tackling the challenges involved in designing a family tree generator encourages the development of problem-solving skills and the cultivation of algorithmic thinking. It necessitates the consideration of various scenarios, such as handling user input, managing data relationships, and effectively visualizing hierarchical structures.

User-Friendly Interface: Emphasizing a user-friendly interface allows individuals with limited technical knowledge to easily utilize the program. By providing clear instructions and feedback, the program becomes accessible to a wider audience, including those with minimal programming experience or familiarity with complex data structures.

Personal and Cultural Significance: Family trees hold great significance for many individuals and communities, as they provide a means to preserve and document familial relationships across generations. Creating a program to generate and visualize family trees can help individuals understand their ancestry better and appreciate the importance of preserving family history.

Practical Application in Genealogy: The program has practical applications in genealogy and historical research. By facilitating the creation and visualization of family trees, the program can aid genealogists and historians in organizing and analyzing complex familial relationships, thus contributing to the preservation of historical records and the study of family histories.

Solution Description
Algorithm:
Define the Individual class with private attributes for name, birthdate, and a vector of children. Include methods for adding a child, getting the name, birthdate, and children.
Define the FamilyTree class with a private attribute for the root individual. Include methods for adding a child, visualizing the family tree, and getting the root.
In the main function, create an instance of the FamilyTree class with a root name and birthdate.
Create a vector of Individual* called individuals and add the root individual to it.
Enter a loop to display the main menu and handle user input. Repeat until the user chooses to exit.
Inside the loop, display the main menu options:
Add Family Member
Visualize Family Tree
Exit
Prompt the user to enter their choice.
If the user selects "Add Family Member":
Prompt the user for the parent's name, child's name, and child's birthdate.
Search for the parent in the individuals vector to find the individual to whom the child will be added.
Create a new Individual for the child and add it as a child of the parent.
Add the child to the individuals vector.
Display a success message.
If the user selects "Visualize Family Tree":
Call the visualizeTree method on the root individual to display the family tree hierarchy.
If the user selects "Exit":
Display a goodbye message.
Break out of the loop to exit the program.
If the user enters an invalid choice, display an an error message and prompt the user to choose a valid option.
