# PierresV2

### By Brandon Spear

Created for Epicodus Code Review #12

### Technologies Used
  * C#
  * .NET6 SDK
  * MSTest
  * Powershell
  * ASP.NET Core MVC
  * EF Core
  * MySQL Server
  * MySQL Workbench
  * HTML
  * CSS
  * Identity

### Description
* This application allows the user to Make a unique account with a valid email and password, and save ingredients to account.
* Within the app, the user can:
  - Sign in with authentication for securitry.
  - Add, edit, combine, and delete flavors, ingredienmts, and items.

### Application Instructions
* NOTE: In order to run this application, you will need to ensure the following software packages are installed locally:
  - .NET6
  - MySQL and MySQL workbench
  - A code editor of your choice (VSCode, Sublime Text, etc.)

#### Installing .NET and MySQL
1. Install .NET6 if you have not done so. Visit [this link](https://dotnet.microsoft.com/en-us/download/dotnet/6.0) to download the recommended versions of both .NET and MySQL software packages.
2. Follow the installer prompts to install the software. Use the default settings.
3. In a terminal, install `dotnet-script` by entering the following command: `$ dotnet tool install -g dotnet-script`. You will also need to configure your environment to access this tool. See [this link](https://www.learnhowtoprogram.com/c-and-net/getting-started-with-c/installing-dotnet-script).
4. Install MySQL.  Follow the instructions at [this link](https://www.learnhowtoprogram.com/c-and-net/getting-started-with-c/installing-and-configuring-mysql).

#### Initial Setup 
5. Clone this repository.
6. Open the terminal and navigate to this project's production directory, named "Bakery".
7. If you have not previously added the following packages globally, Add the following packages within the production directory ("Bakery"):
```bash
$ dotnet add package Microsoft.EntityFrameworkCore -v 6.0.0 
$ dotnet add package Pomelo.EntityFarmeworkCore.MySql -v 6.0.0
```
8. Within the production directory, create a new file called appsettings.json.
9. Open your code editor and navigate to appsetings.json.
10. Within appsettings.json, add the following code, replacing the `uid` and `pwd` values with your own username and password for MySQL.

```json
{
  "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Port=3306;database=brandon_spear_pierre_v2;uid=[uid];pwd=[pwd];"
  }
}
```

11. Use database migration to construct a shiny new database locally:
* In a terminal window, navigate to the project's root directory, named "PierreBakery2-SOlution-Main".
* Run the following commands:
```bash
$ dotnet ef migrations add Initial
$ dotnet ef database update
```
* These two commands will instantiate a local database conforming to the program requirements.

#### Running the Program
17. Open a terminal and navigate to this project's production directory ("Bakery") if you have not already done so.
18. Type `dotnet restore` in the command line to ensure all required dependencies are loaded.
18. Type `dotnet watch run` in the command line to start the project in development mode with a watcher.
* If the build fails, revisit steps 1 - 3 above to ensure that .NET6 has been properly installed.
19. Open the browser to _https:localhost:5001_. 

### Known Bugs
  * No known bugs yet.
  
### License
MIT License

Copyright (c) [2023] [Brandon Spear]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.