# Setting Up an SBT Project in IntelliJ IDEA

## **Step 1: Install Required Tools**
Before starting, ensure you have the following installed:

1. **Java Development Kit (JDK 8 or later)**
   - Recommended: **JDK 11 or JDK 17**.
   - To check if Java is installed, run:
     ```sh
     java -version
     ```
   - If not installed, download and install it from [AdoptOpenJDK](https://adoptopenjdk.net/).

2. **Scala SDK** (IntelliJ can install it automatically)

3. **SBT (Scala Build Tool)**
   - Check if it's installed:
     ```sh
     sbt --version
     ```
   - If not installed, download from [SBT Official Site](https://www.scala-sbt.org/).

4. **IntelliJ IDEA (Community or Ultimate)**
   - Download from [JetBrains](https://www.jetbrains.com/idea/download/).

---

## **Step 2: Install IntelliJ Scala Plugin**
1. Open **IntelliJ IDEA**.
2. Go to **File → Settings** (on macOS: **IntelliJ IDEA → Preferences**).
3. Navigate to **Plugins**.
4. Search for **Scala** and install the **"Scala" plugin**.
5. Restart IntelliJ IDEA.

---

## **Step 3: Create a New SBT Project**
1. Open **IntelliJ IDEA**.
2. Click **"New Project"**.
3. Select **Scala** (on the left).
4. Choose **SBT** as the build system.
5. Set the **Project SDK** to JDK 11 or JDK 17.
6. Select **Scala version**
7. Choose a **Project Name** (e.g., `MyScalaProject`).
8. Set the **Project Location** (e.g., `C:\Users\YourName\IdeaProjects\MyScalaProject`).
9. Click **Finish**.

---

## **Step 4: Project Structure**
After project creation, IntelliJ will generate the following structure:
```
MyScalaProject/
├── .idea/               # IntelliJ project files
├── project/             # SBT configuration files
│   ├── build.properties # Defines the SBT version
├── src/
│   ├── main/            # Application code
│   │   ├── scala/       # Scala source files
│   ├── test/            # Test files
├── target/              # Compiled classes
├── build.sbt            # SBT configuration file
```

---

## **Step 5: Edit `build.sbt`**
Modify `build.sbt` to include:
```scala
ThisBuild / scalaVersion := "3.6.3"

lazy val root = (project in file("."))
  .settings(
    name := "MyScalaProject",
    version := "0.1.0",
    libraryDependencies += "org.scalactic" %% "scalactic" % "3.2.16"
  )
```

---

## **Step 6: Create and Run a Scala Program**
1. **Go to `src/main/scala`**.
2. **Create a new file**: `HelloWorld.scala`
3. **Add the following code**:
   ```scala
   object HelloWorld {
     def main(args: Array[String]): Unit = {
       println("Hello, Scala with SBT!")
     }
   }
   ```
4. **Run the program**:
   - Right-click the `HelloWorld.scala` file and choose **Run**.
   - Or use **Shift + F10**.

---

## **Step 7: Run SBT Commands**
Open the **terminal in IntelliJ** or command prompt (`cmd`/`bash`) and navigate to the project folder.

### **Compile the project**:
```sh
sbt compile
```

### **Run the application**:
```sh
sbt run
```

### **Test the project** (if tests are added):
```sh
sbt test
```

### **Clean compiled files**:
```sh
sbt clean
```

### **Reload SBT after modifying `build.sbt`**:
```sh
sbt reload
```

---

## **Step 8: Enable Auto-Import (Optional)**
To avoid manually reloading SBT:
1. Open `build.sbt`.
2. Click **Enable Auto-Import** at the top.

---

## **Step 9: Enable Git Version Control (Recommended)**
1. Open **VCS** → **Enable Version Control Integration**.
2. Select **Git**.
3. Run the following commands in the terminal:
   ```sh
   git init
   git add .
   git commit -m "Initial Scala SBT project"
   ```

---

## **Step 10: (Optional) Add Dependencies**
To add libraries:
1. Find dependencies at [Maven Repository](https://mvnrepository.com/).
2. Add them to `build.sbt`. Example for Akka:
   ```scala
   libraryDependencies += "com.typesafe.akka" %% "akka-actor-typed" % "2.8.0"
   ```
3. Run:
   ```sh
   sbt update
   ```

---

## **Conclusion**
You have now successfully:
✅ Installed Scala, SBT, and IntelliJ  
✅ Created an SBT project in IntelliJ  
✅ Configured and ran a basic Scala program  

Let me know if you have any questions! 🚀
