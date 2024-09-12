
# An introduction to programming ABM simulations with the Julia language

- Przemysław Szufel
- Bogumił Kamiński

**Dates:** September 16, 2024
Hours: 14:30 - 17:30

**Location**:
        Social Simulation Conference 2024, Cracow University of Economics, Poland
                                                                               

The Julia language was designed to address typical challenges faced when working with computationally intensive numerical models. With syntax similar to Python and Matlab, Julia supports an efficient and convenient development process. However, programs developed in Julia boast performance comparable to C++. This speed can be further increased by built-in mechanisms for parallel computing, making it an ideal tool for scientific computing and running large-scale simulations.

The goal of this 3-hour intensive workshop is to offer a quick hands-on introduction to the Julia language, enabling participants to begin using it for their research. 
The workshop assumes no prior knowledge of Julia. We will start with an introductory overview of the Julia language. 
Next, we will explore specific language features that are useful in numerical models. 
Following this, we will present a use-case scenario demonstrating how to build agent-based simulation models in Julia. 
Additionally, we will showcase how simulations can be executed in a spatial setting using real-world city maps from the OpenStreetMap project. 
Finally, we will briefly demonstrate how straightforward it is to run Julia models at scale using parallel and distributed computing. 



**Schedule**

<table>
<tr><td><a href="1_Basics/">1 Basics</a><br>
</td><td>&nbsp;</td></tr>
<tr><td><a href="2_Working_with_Data/">2 Working with Data</a><br>
</td><td>&nbsp;</td></tr>
<tr><td><a href="3_Simulation_Models/">3 Running simulation models in Julia</a><br>
</td><td>&nbsp;</td></tr>

</table>


**What is Julia**

Julia is a new Open Source language designed for science and data analysis. With the stable 1.0 version released in August 2018, an exponential growth of language popularity has been observed and the language is in the top-20 programming languages in IEEE Spectrum ranking and top-10 programming languages developed on GitHub. Julia takes “walks like Python, runs like C” approach and is a perfect replacement for Matlab, Python and R scientific data workflow, yet due to its speed it can be also used to implement computation intensive algorithms that are normally implemented in languages such as Java or C++. Nowadays, the most popular Julia applications include computations related to data science, machine learning, numerical simulation, quantitative economics, applied mathematics, physics, astronomy, chemistry, and bioinformatics.

**Installation instructions**

1. Please download Julia from [https://julialang.org/downloads/](https://julialang.org/downloads/) and follow the installation instructions presented at https://julialang.org/downloads/platform/. During the workshop we will be using the Stable Release **v1.10.5**. The 64-bit version is recommended.

2. Install Julia packages that will be used throughout the workshop. Once Julia is installed please follow the steps:

    1. Clone this repository by running the following git command:
        ```
        git clone https://github.com/pszufe/2024_Julia_Krakow.git
        ```
        or you can download the entire repository from GitHub by clicking the green button `Code => Download ZIP`. If you download the repository you need to unzip it.

    2. Change the directory to where `Project.toml` and `Manifest.toml` files are located
        ```
        cd "2024_Julia_Krakow"
        ```
    3. Run the Julia console or in the command line (run command **julia** in the project folder). Once Julia interpreter is running paste the following Julia code:
        ```
        using Pkg
        pkg"activate ."
        pkg"instantiate"   # installs all packages and dependecies.
        ```

       Additionally, you need to make Julia to work with Python. We recommend Python that comes with CondaPkg.jl Julia package.
       Python along with visualisation tools and Jupyter notebook can be configured by running the following Julia commands (directly after running the above mentioned installation)
       ```
        using CondaPkg, Pkg
        CondaPkg.add_channel("conda-forge")
        CondaPkg.add("jupyter")
        ENV["JUPYTER"] = CondaPkg.which("jupyter")
        Pkg.build("IJulia")
       ```

4. The recommended programming environment for the Julia language is Visual Studio Code (https://code.visualstudio.com/) with Julia extension. Please follow the steps below:

    a) Download and install VS Code (available at https://code.visualstudio.com/download/)

    b) Start VS Code, click View->Command Palette...  and type `View: Show Extensions` to go to the extension manager

    c) In the extension manager search box type “Julia”

    d) On the top of the extension list you should see “Julia Language Support” – click *Install* to install the extension.

    If you run into any installation problem, more detailed instructions can be found in https://github.com/julia-vscode/julia-vscode#getting-started


5. During the workshop will be mostly working with Julia within Jupyter notebook (this can be also used instead of VS Code)

    To run Julia inside a Jupyter notebook start the Julia console (this assumes that the console is run in the main folder of this repository) and run the two following commands:
    ```
    using Pkg
    Pkg.activate(".")
    using IJulia
    notebook(dir=".")
    ```
    After running the above commands a new web browser tab should open with Jupyter Notebook.



**Literature**

1. Julia Language Manual, https://docs.julialang.org/en/v1/

2. The Julia Express - A concise Julia language introductory manual for programmers, https://github.com/bkamins/The-Julia-Express/

3. B. Kaminski: Julia for Data Analysis, Manning, 2023, https://www.manning.com/books/julia-for-data-analysis
