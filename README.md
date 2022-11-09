```c#
Naming Conventions and Standards

# 1 Use Pascal casing for Class names.

Example
public class BusinessCase  
{  
//.........  
}  
# 2 Use Pascal casing for Method names.

Example
void AutoComplete(string name)  
{  
// ......  
}  

# 3 Use Camel casing for variables and method parameters.

Example
int totalCount = 0;  
void AutoComplete(string name)  
{  
   string fullMessage = "Hello " + name;  
}  
# 4 Use Meaningful, descriptive words to name variables. Do not use abbreviations.

Example
Good:  
string address;  
int salary;  
Bad:  
string nam;  
string addr;  
int sal;  

# 5 Do not use single character variable names like i, n, s etc. Use names like index, temp

//One exception, in this case, would be variables used for iterations in loops.

Example
for (int i = 0; i < count; i++)  
{  
   //...........  
}  

# 6 Do not use underscores (_) for local variable names.

//Prefix boolean variables, properties, and methods with "is" or similar prefixes.
Ex: private bool _isFinished  
//Use appropriate prefix for the UI elements so that you can identify them from the rest of the variables.

# 7 Use appropriate prefix for each of the UI elements. A brief list is given below.
 
Example

Control	Prefix
Label	lbl
TextBox	txt
DataGrid	dtg
Button	btn
ImageButton	imb

# 8 Use Pascal Case for file names.
Indentation and Spacing

# 9 Use TAB for indentation. Do not use SPACES. Define the Tab size as 4.

//Comments should be in the same level as the code (use the same level of indentation).

Example

Good
// Format a message and display  
string fullMessage = "Hello my name is " + name;  
DateTime currentTime = DateTime.Now;  
string message = fullMessage + ", the time is : " + currentTime.ToShortTimeString();  
MessageBox.Show( message );  
Bad
// Format a message and display  
string fullMessage = " Hello my name is " + name;  
DateTime currentTime = DateTime.Now;  
string message = fullMessage + ", the time is : " + currentTime.ToShortTimeString();  
MessageBox.Show ( message ); 
//Curly braces ( {} ) should be in the same level as the code outside the braces.

# 10 Use one blank line to separate logical groups of code.

Example

Good
bool ShowMessage(string name) {  
    string fullName = "Hello " + name;  
    DateTime currentTime = DateTime.Now;  
    string message = fullName + ", the time is : " + currentTime.ToShortTimeString();  
    MessageBox.Show(message);  
    if (...) {  
        // Write your code here  
        // ...  
        return false;  
    }  
    return true;  
}  
Bad
bool ShowMessage(string name) {  
        string fullName = "Hello " + name;  
        DateTime currentTime = DateTime.Now;  
        string message = fullName + ", the time is : " + currentTime.ToShortTimeString();  
        MessageBox.Show(message);  
        if (...) {  
            // Write your code here  
            // ...  
            return false;  
        }  
        return true;  
//There should be one and only one single blank line between each method inside the class.

# 11 The curly braces should be on a separate line and not in the same line as if, for, etc.

Example

Good
if ( ... )  
{  
   // write your code here  
} 
Bad
if ( ... ) {  
// Write your code here }  
# 12 Use a single space before and after each operator and brackets.

Example

Good
if(showResult)  
{  
for ( int i = 0; i < 10; i++ )  
{  
//  
}  
}  
Bad
if(showResult==true)  
{  
for(int i= 0;i<10;i++)  
{  
//  
}  
}  
Superb Programming Practices

# 13 Method name should clarify the meaning. Do not use misleading names. If the method name is clear then there is no need of documentation.

Example

Good
void SaveStudentDetails (string studentDetails )  
{  
   // Save the student details.  
}  
Bad
// This method will save the student details.  
void SaveDetails (string student )  
{  
   // Save the student details.  
}  
# 14 A method should do only one job at a time. Do not use it for more than one job.

Example

Good
//Save student details  
SaveStudentDetails();  
//Send email to user that student details is added successfully.  
SendEmail();  
Bad
//Save student details  
Public void SaveStudentDetails()  
{  
   // First task  
   //Save student details  
   //Second task  
   // Send emails  
}  
# 15 Make sure string comparisons convert string to uppercase or lowercase for comparison.

Example

Good
If(UserName.ToLower()=="tom")  
{  
   // write yor logic here  
}  
Bad
If(UseName=="TOm")  
{  
//  
}  
