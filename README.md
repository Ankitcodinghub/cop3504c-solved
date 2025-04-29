# cop3504c-solved
**TO GET THIS SOLUTION VISIT:** [COP3504C Solved](https://www.ankitcodinghub.com/product/cop3504c-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;109881&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COP3504C Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Lab 06: Image Scaling

Overview

Requirements

The program should be driven classless main function and Image class.

Standalone Functions (scaler.cpp)

int main()

When the program is run via the main() method, the program should:

1) Fetch ConsoleGfx singleton via ConsoleGfx.getInstance()

2) Display the welcome message

3) Display color test (ConsoleGfx.testRainbow)

4) Display the menu

5) Prompt for input

Load File

Load file via unsigned char *ConsoleGfx.loadFile(string file). Note that loadFile() allocates an array for the file data, but the caller is responsible to deallocation.

Success (File was Loaded) Failure (File wasn’t Loaded)

Select a Menu Option: 1

Enter name of file to load: logos/uga.gfx File loaded.

Scaler Menu

———–

Select a Menu Option: 1 Enter name of file to load: foo.png Error: could not load file.

Scaler Menu

———–

Load Test Image Show Image Properties

Loads ConsoleGfx.testImage: Displays the length and width of the current image.

Select a Menu Option: 2 Test image data loaded.

Scaler Menu

———–

Select a Menu Option: 6 Image Dimensions: (14, 6)

Scaler Menu

———–

Display Image

Displays current image by invoking ConsoleGfx.displayImage(unsigned char *imageData) method.

Success (Previously Loaded) Failure (No Image Loaded)

Enlarge / Shrink Image

Prompts the user for orders of magnitude to change (powers of two), then enlarges the image.

Select a Menu Option: 4 Select a Menu Option: 5

Enter orders of magnitude for enlargement: 3 Enter orders of magnitude for reduction: 3

Image enlarged! Image reduced!

Scaler Menu _

Scaler Menu

———– ———–

unsigned char *scaledImage(unsigned char *imageData, int orders)

Returns a scaled version of the image data based on the orders of magnitude (i.e., powers of two to scale).

The number of orders of magnitude should be in the range [-4, 4] (inclusive), which allows scaling down to 1/16 or up by a factor of 16 in each dimension. Do no implement this via recursive or iterative doubling; this takes twice as long as creating a new image one time, and it causes memory fragmentation.

This function should never scale any image above 256 in width or height; instead, it should limit scaling such that the image is scaled up by a power of two but remains less than or equal to 256 in each dimension. Likewise, no image should be scaled below a height or width of one. To determine the color for reduced images, the number of colors of each pixel should be counted, and the most common color should be used. If there is a tie, the earliest pixel (by row, then by column) should be used. This function should allocate memory and return it to the caller; the caller is responsible for deallocation.

Image Class

The Image class will the image data and should be constructed from the raw data.

The class must also have the following methods and behaviors (this is mandatory):

public Image(unsigned char *imageData)

This method should be the only constructor for this class. There should not be a default constructor! Its sole argument is a pointer to an array of raw image data as loaded from the file. The data is formatted as follows:

public unsigned char *getImageData()

Returns a pointer to the raw image data (not a copy).

public unsigned char *getPixelData()

Returns a pointer to the raw pixel data (excluding the image property information). Should not be a copy.

public unsigned char getWidth()

Returns the width of the image.

public unsigned char getHeight()

Returns the height of the image.

public void setImageData(unsigned char *newData) Changes the image data to the new pointer.

Building and Testing

For this project, students will begin to learn more details about the practical building and testing of C++ programs, including accessing executables built by the compiler from outside of the IDE.

Building

CLion uses the standardized CMake build system, which is supported across multiple platforms and IDEs (including CLion and Visual Studio) and supports many compilers (GCC, Clang, and MS Visual C.) When you create a CLion project, it will create CMakeLists.txt. The CMakeLists.txt file for this lab might look like this:

cmake_minimum_required(VERSION 3.20)

project(scaler) C++ version

set(CMAKE_CXX_STANDARD 14)

Executable name add_executable(scaler ConsoleGfx.cpp scaler.cpp) Source files

You should make sure that the CMakelists.txt file correctly lists your source files and the executable. Then, click on the “Build” button (), which is on the toolbar to the left of the “Run” ( ) and “Debug” () buttons.

Testing

To open Explorer , open the build folder (e.g, cmake-build-debug), right-click on scaler.exe, and select Open In  Explorer. Then, right click in Explorer and select “Open in Windows Terminal”. Once the terminal window is open, you can run your program by typing the executable’s name (e.g., scaler):

Submissions

NOTE: Your output must match the example output *exactly*. If it does not, you will not receive full credit for your submission!

Files: scaler.cpp, Image.cpp, Image.h

Method: Submit on ZyLabs
