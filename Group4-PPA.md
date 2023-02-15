
# Importance of Version Control Systems while coding


## What is Version Control?
Version control is a system and practice for managing changes in a file or digital content. By using a set of version control practices and tools, one can revert to a previous state of a project and view or manipulate its content. In fast-paced development environments, these systems make it easier for teams to work efficiently. Most often, these systems are designed to record every modification to the contents of the project. When there is an issue, those working on the project can compare previous versions to fix issues, errors, or inconsistencies with minimal disruption.

## Source Code Version Control
Source-code version control is a tool that is specifically used to manage code files. Like any other version control system, it is built to provide important features such as tracking the history of code, creating multiple versions of code, and merging changes made in separate branches, all while allowing for an easier way to resolve conflicts.

Today, there are multiple source-code version control tools available on the market. Some of the most popular ones are Git, Subversion, and Mercurial. Each of these has its own unique operations, rules, and advantages.

The nature of the project one is working on really defines which version control system is best for that specific project's needs. However, in this article, we will be focusing on the GitHub environment.

## Advantages of using a Version Control System 

Using a source code version control system is essential in modern-day software development practices. These tools offer powerful features and advantages to teams working on a code project.
Here's a list of a few features that a version control system can offer for your project:
- It provides the ability to supervise and protect the codebase.
- As already mentioned, it gives developers the ability to record all changes made to the code and save the code in those particular states.
- By using a version control tool, a developer can analyze version history, giving them the power to revisit a code in any of the previous saved states.
- Not only does it provide a feature to revisit code, but it also allows developers to roll back the code to a previous state.
- All these features give the developers an environment to experiment and make errors without affecting the final working code.
- All these updates and experiments can easily be reviewed when using a version control tool.

A version control tool provides many more advantages and powerful features to the developer, but one of the biggest advantages of using this tool is that multiple team members can collaborate on a single project and utilize all these features simultaneously.

Now that we've talked about what a version control system is and its advantages, let's look at how to use Git for version control activities.
- Step 1 - Create a repository.
You can create a repository for the code on the GitHub platform by following the simple prompts for creating the repository.
- Step 2 - Clone the repository.
Once a repository is created, you need to replicate it to your local machine. You can create files and folders in the repository and start writing your code.
- Step 3 - Save and commit.
As you write your code, save your files with every small code block change and commit those changes. This is an important step, as each commit becomes a new state of the code that can later be revisited. It's important to create commits with short but descriptive commit titles and descriptions.
- Step 4 - View commit history.
As you develop your project, you can keep track of the history of your commits to ensure the changes you've made to the code.
- Step 5 - Make any required changes.
If you identify that your code requires changes, revisit those parts, make the changes, and recommit your code.
- Step 6 - Push changes.
Finally, all these commits need to be pushed to the remote repository. Once in the cloud, you can access your project from any other device.

## Code Example for incremental commits

Here's a simple example of what it means to save your code with small blocks of code. For instance, let's say you're writing a simple Java program for a calculator that performs tasks such as addition, subtraction, multiplication, and division.

### Commit 1
```
// Create Program Structure

import java.util.Scanner;

public class Calculator {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    // Ask the user to input the type of operation they want to perform

    // Read the user's choice

    // Ask the user to input the two numbers

    // Perform the requested operation
  }
```

### Commit 2
```
// Ask the user to input the type of operation they want to perform
    System.out.println("Please select the type of operation you want to perform:");
    System.out.println("1. Addition");
    System.out.println("2. Subtraction");
    System.out.println("3. Multiplication");
    System.out.println("4. Division");

    // Read the user's choice
    int choice = input.nextInt();
```

### Commit 3
```
// Ask the user to input the two numbers
    System.out.println("Please enter the first number:");
    double num1 = input.nextDouble();

    System.out.println("Please enter the second number:");
    double num2 = input.nextDouble();
```

### Commit 4
```
// Perform the requested operation
    switch (choice) {
      case 1:
        System.out.println("Result: " + (num1 + num2));
        break;
      case 2:
        System.out.println("Result: " + (num1 - num2));
        break;
      case 3:
        System.out.println("Result: " + (num1 * num2));
        break;
      case 4:
        System.out.println("Result: " + (num1 / num2));
        break;
      default:
        System.out.println("Invalid choice");
    }
```

With each commit, a new state is created. Using GitHub's commit history, the developer can go back to any previous state, make changes, and continue from there.
For example, if the developer wants to allow operations for three numbers instead of two, they can go back to commit 3 where the code would look something like this:

```
import java.util.Scanner;

public class Calculator {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    // Ask the user to input the type of operation they want to perform
    System.out.println("Please select the type of operation you want to perform:");
    System.out.println("1. Addition");
    System.out.println("2. Subtraction");
    System.out.println("3. Multiplication");
    System.out.println("4. Division");

    // Read the user's choice
    int choice = input.nextInt();

    // Ask the user to input the two numbers
    System.out.println("Please enter the first number:");
    double num1 = input.nextDouble();

    System.out.println("Please enter the second number:");
    double num2 = input.nextDouble();

    // Perform the requested operation

  }
}
```

He can add additional statments to input a third number

```
System.out.println("Please enter the third number:");
    double num3 = input.nextDouble();
```

He can then save this as a new commit, add the next set of statements, and save them in commit 4. This would make the program look like the following:

```
import java.util.Scanner;

public class Calculator {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    // Ask the user to input the type of operation they want to perform
    System.out.println("Please select the type of operation you want to perform:");
    System.out.println("1. Addition");
    System.out.println("2. Subtraction");
    System.out.println("3. Multiplication");
    System.out.println("4. Division");

    // Read the user's choice
    int choice = input.nextInt();

    // Ask the user to input the two numbers
    System.out.println("Please enter the first number:");
    double num1 = input.nextDouble();

    System.out.println("Please enter the second number:");
    double num2 = input.nextDouble();

    // Perform the requested operation
    switch (choice) {
      case 1:
        System.out.println("Result: " + (num1 + num2 + num3));
        break;
      case 2:
        System.out.println("Result: " + (num1 - num2 - num3));
        break;
      case 3:
        System.out.println("Result: " + (num1 * num2 * num3));
        break;
      case 4:
        System.out.println("Result: " + (num1 / num2 / num3));
        break;
      default:
        System.out.println("Invalid choice");
    }
  }
}
```

## Version Control Best Practices

Now that we've looked at how to create commits in GitHub for better version control, let's look at the best practices.

- Commit relatively When you commit, make sure it's understandable what you've really changed through those commits.
- Commit small but often Always commit in small increments. This would reduce the risk of integration conflicts and make it easier to revert when a conflict does occur. Infrequent, large commits would create challenges in resolving disputes and understanding those changes.
- Do not commit incomplete work Only commit your code to the repository when it's fully functional.
- Use branches Using branches is an important feature of Git, which helps to keep different lines of development separate and reduces confusion.

In conclusion , A version control system like Git can greatly enhance software development processes by allowing for efficient tracking of code changes, enabling collaboration, and providing greater control over project history.
