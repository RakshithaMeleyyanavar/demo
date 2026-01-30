# demo
Maven Project Setup, Java Application, and Execution – Table Format
Step No.	Activity / Action	Command / Details	Expected Outcome / Notes
1	Verify Maven installation	mvn --version	Displays Maven version, Java version, and environment details

2	Generate Maven project	mvn archetype:generate	Creates project directory structure; connects to the internet to download dependencies/templates

3	Choose Archetype Number	2309 (press Enter)	Selects Maven archetype template

4	Choose Java Compiler Version	9 (press Enter)	Configures the Java version for the project

5	Set GroupId	com.bnmit	Unique company/university identifier

6	Set ArtifactId	sample-app	Unique project/application name

7	Set Version	1.0-SNAPSHOT (press Enter)	Project version identifier

8	Set Package Name	com.bnmit	Defines Java package structure

9	Confirm Configurations	Press y	Maven generates the project folder sample-app in current directory

10	Check Maven Local Repository	Open C:\Users\<username>\.m2	Maven downloads dependencies/plugins here to avoid repeated downloads

11	Compile & Package Project	mvn package	Creates target folder with compiled JAR: sample-app-1.0-SNAPSHOT.jar

12	Clean Build Artifacts	mvn clean	Deletes target folder and built classes

13	Generate Project Documentation	mvn site	Creates target/site/index.html containing project reports and documentation

14	Modify Java Code	Edit sample-app/src/main/java/com/bnmit/App.java
Paste Bank Application code:
```java
class BankAccount {
  private double balance;
  public BankAccount(double initialBalance) {
    if (initialBalance < 0) throw new IllegalArgumentException("Initial balance cannot be negative");
    this.balance = initialBalance;
  }
  public void deposit(double amount) {
    if (amount <= 0) throw new IllegalArgumentException("Deposit must be positive");
    balance += amount;
  }
  public void withdraw(double amount) {
    if (amount <= 0	

15	Rename File	App.java → BankService.java	File name matches the main class for compilation

16	Clean Project	mvn clean	Deletes previous build artifacts

17	Compile & Package	mvn package	Creates target/sample-app-1.0-SNAPSHOT.jar and target/classes/com/bnmit/BankService.class

18	Navigate to Target Folder	cd target	Ready to run JAR

19	Run Java Application	java -cp sample-app-1.0-SNAPSHOT.jar com.bnmit.BankService	Output on console: Final Balance:





















Sure 👍 Here are **simple Java programs** for each asked problem (very easy VTU style).

---

# ✅ 1. Java Program to Calculate Area of Square

```java
import java.util.Scanner;

class AreaSquare {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter side of square: ");
        int side = sc.nextInt();

        int area = side * side;

        System.out.println("Area of Square = " + area);
    }
}
```

---

# ✅ 2. Java Program to Calculate Simple Interest

Formula:
**SI = (P × R × T) / 100**

```java
import java.util.Scanner;

class SimpleInterest {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Principal: ");
        int p = sc.nextInt();

        System.out.print("Enter Rate: ");
        int r = sc.nextInt();

        System.out.print("Enter Time: ");
        int t = sc.nextInt();

        int si = (p * r * t) / 100;

        System.out.println("Simple Interest = " + si);
    }
}
```

---

# ✅ 3. Java Program to Check Whether a Number is Prime or Not

```java
import java.util.Scanner;

class PrimeCheck {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        int count = 0;

        for(int i = 1; i <= n; i++) {
            if(n % i == 0)
                count++;
        }

        if(count == 2)
            System.out.println(n + " is Prime Number");
        else
            System.out.println(n + " is Not Prime Number");
    }
}
```

---

# ✅ 4. Java Program to Print Alternate Prime Numbers (1 to N)

Example Output: 2, 5, 11, 17...

```java
import java.util.Scanner;

class AlternatePrime {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter limit: ");
        int n = sc.nextInt();

        int primeCount = 0;

        for(int num = 2; num <= n; num++) {
            int count = 0;

            for(int i = 1; i <= num; i++) {
                if(num % i == 0)
                    count++;
            }

            if(count == 2) {
                primeCount++;

                if(primeCount % 2 != 0)
                    System.out.print(num + " ");
            }
        }
    }
}
```

---

# ✅ 5. Java Program to Find Length of a String

```java
import java.util.Scanner;

class StringLength {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        System.out.println("Length of String = " + str.length());
    }
}
```

---

✅ Done:
✔ Area of Square
✔ Simple Interest
✔ Prime Check
✔ Alternate Prime Numbers
✔ Length of String

If you want, I can also give programs for **factorial, palindrome, Armstrong, Fibonacci** etc.



| **Command / Action**                                      | **One-Line Explanation**                                     |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| `git config --global user.name "Your Name"`               | Sets your Git username globally for commits.                 |
| `git config --global user.email "your_email@example.com"` | Sets your Git email globally for commits.                    |
| `git clone <repo-url>`                                    | Downloads a repository from GitHub to local machine.         |
| `cd <folder>`                                             | Changes directory to the specified folder.                   |
| `git init`                                                | Initializes a new local Git repository.                      |
| `git remote add origin <repo-url>`                        | Connects local repo to remote GitHub repository.             |
| `git pull origin main`                                    | Fetches and merges changes from remote `main` branch.        |
| `git fetch origin`                                        | Downloads updates from remote without merging.               |
| `git merge origin/main`                                   | Merges fetched changes from remote into local branch.        |
| `git add <file>`                                          | Stages file(s) to be committed.                              |
| `git add .`                                               | Stages all changes in the folder for commit.                 |
| `git commit -m "message"`                                 | Records staged changes to local repository with a message.   |
| `git push origin main`                                    | Uploads local commits to remote `main` branch.               |
| `git push -u origin main`                                 | First-time push: sets remote `main` as default upstream.     |
| `git branch <branch-name>`                                | Creates a new branch locally.                                |
| `git checkout <branch-name>`                              | Switches to the specified branch.                            |
| `git checkout master`                                     | Switches back to the `master` branch.                        |
| `git pull origin master`                                  | Updates local master branch after merge on GitHub.           |
| `git branch -d <branch-name>`                             | Deletes a local branch.                                      |
| `git push origin --delete <branch-name>`                  | Deletes a branch from remote repository.                     |
| `Click Fork`                                              | Copies someone else’s repository to your GitHub account.     |
| `Click Compare & Pull Request`                            | Starts a pull request to merge your branch into base branch. |
| `Click Create Pull Request`                               | Submits your changes for review.                             |
| `Review Changes → Approve`                                | Reviewer approves the pull request on GitHub UI.             |
| `Click Merge Pull Request → Confirm Merge`                | Merges the feature branch into base branch on GitHub.        |

