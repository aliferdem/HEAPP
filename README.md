![HEAPP Preview](https://github.com/user-attachments/assets/ea4d4e68-d7d8-4ce7-97d7-a3fc58c883dc)

HEA Phase Predictor
====================

HEA Phase Predictor (HEAPP) is a free software tool designed to 
predict solid solution formation in high-entropy alloys (HEAs) 
using semi-empirical parameters. This tool enables researchers to 
input alloy compositions and obtain tabulated data and predictions 
regarding solid solution formation based on phase formation rules 
available in the literature. The tool helps accelerate the 
experimentation and research process. HEAPP is developed within 
**Metals Development Laboratory** (MDL) at **Middle East Technical 
University** (METU).

Phase formation rules
---------------
HEAPP currently uses six phase formation rules to predict whether 
a solid solution or intermetallic phase will form in high-entropy 
alloys. These rules are based on studies from the literature, and 
are named as R1, R2, ..., R6.

>**R1**: The solid solution forms when Ω ≥ 1.1 and 𝛿 ≤ 6.6%, where 
Ω is the ratio of entropy and enthalpy of mixing, and 𝛿 is the 
atomic size difference[^1].
[^1]: X. Yang, Y. Zhang, Prediction of high-entropy stabilized 
solid-solution in multi-component alloys, Materials Chemistry and 
Physics 132 (2012) 233–238. 
https://doi.org/10.1016/j.matchemphys.2011.11.021.

>**R2**: Solid solutions tend to form when 𝛿 is less than 6.6% 
(𝛿 < 0.066) and the mixing enthalpy (Δ𝐻𝑚𝑖𝑥) is between − 11.6 
kJ/mol and 3.2 kJ/mol[^2].
[^2]: S. Guo, Q. Hu, C. Ng, C.T. Liu, More than entropy in 
high-entropy alloys: Forming solid solutions or amorphous phase, 
Intermetallics 41 (2013) 96–103. 
https://doi.org/10.1016/j.intermet.2013.05.002.

>**R3**: The phase selection between solid solution and 
intermetallic phases is influenced by atomic packing misfit. 
Solid solutions tend to form when the atomic packing parameter 
(𝛾) is less than 1.175[^3].
[^3]: Z. Wang, Y. Huang, Y. Yang, J. Wang, C.T. Liu, Atomic-size 
effect and solid solubility of multicomponent alloys, Scripta 
Materialia 94 (2015) 28–31. 
https://doi.org/10.1016/j.scriptamat.2014.09.010.

>**R4**: The geometrical parameter Λ predicts the formation of 
disordered solid solutions (DSS) in multi-component alloys. The 
values of Λ greater than 0.96 favor the formation of DSS, while 
values below 0.24 lead to compound formation[^4].
[^4]: A.K. Singh, N. Kumar, A. Dwivedi, A. Subramaniam, A 
geometrical parameter for the formation of disordered solid 
solutions in multi-component alloys, Intermetallics 53 (2014) 
112–119. https://doi.org/10.1016/j.intermet.2014.04.019.

>**R5**: High-throughput density-functional-theory (DFT) 
calculations show that for solid solution formation in 
high-entropy alloys, the enthalpy of formation for all binary 
compounds must lie between **− 138 meV/atom** and **37 meV/atom**[^5].
[^5]: M.C. Troparevsky, J.R. Morris, P.R.C. Kent, A.R. Lupini, 
G.M. Stocks, Criteria for Predicting the Formation of Single-Phase 
High-Entropy Alloys, Phys. Rev. X 5 (2015) 011041. 
https://doi.org/10.1103/PhysRevX.5.011041.

>**R6**: A solid solution is stable when the ratio between the 
enthalpy of mixing and the enthalpy of intermetallic phase 
formation is lower than a critical threshold at a given 
temperature[^6].
[^6]: O.N. Senkov, D.B. Miracle, A new thermodynamic parameter 
to predict formation of solid solution or intermetallic phases 
in high entropy alloys, Journal of Alloys and Compounds 658 (2016) 
603–607. https://doi.org/10.1016/j.jallcom.2015.10.279.





Getting started
---------------

Follow the instructions below to get started with HEAPP, whether 
you're using the Windows installer or running from source.

### 1\. **Using the Windows Installer**

If you prefer the ready-to-use version of HEAPP, download the 
Windows installer from the official website:

[Download HEAPP Windows Installer](https://metumdl.framer.website/)

After downloading, follow the steps in the installer to set up 
HEAPP on your machine. Once installed, you can launch HEAPP 
directly from your desktop.

> [!WARNING]
> You may encounter warnings from antivirus softwares after 
> downloading the Windows installer of HEAPP, as some antivirus 
> programs may flag compiled binaries as potential malware. 
> [This is a known issue with binaries compiled using Nuitka on 
> Windows](https://nuitka.net/user-documentation/common-issue-solutions.html#windows-virus-scanners),
> and may occur even though the software is safe to use.

### 2\. **From Source**

**Prerequisites**

If you are installing from source, you will need:
- **Python 3**. The software is compatible with Python versions 
  between **3.9** and **3.12**. The development and testing were 
  done using Python **3.11.8**, and no issues were encountered.
- **pip** (Python package installer) to manage dependencies.

1.  **Clone the Repository:**

    Download the source code by cloning the GitHub repository:

    ```source-shell
    git clone https://github.com/aliferdem/heapp.git
    ```

2.  **Navigate to the Project Directory:**

    ```source-shell
    cd heapp
    ```

3.  **Install Dependencies:**

    HEAPP uses several dependencies, all listed in the 
    `requirements.txt` file. Install them using the following 
    command:

    ```source-shell
    pip install -r requirements.txt
    ```

4.  **Run the Application:**

    Once the dependencies are installed, you can launch the HEAPP 
    application by running:

    ```source-shell
    python main.py
    ```

### 3\. **How to Use HEAPP**

Once HEAPP is running:

1. Use the interactive periodic table to select elements for your 
   alloy composition. The details of the element hovered on will be 
   displayed right below the periodic table.
2. You can input the proportions of each element in **atomic ratio**, 
   **at%**, **wt%**, and **mass** (if you enter total mass for your 
   batch). The entered proportions will immediately be converted to 
   the others. 
3. Once you are done with the composition, hit the **Calculate** 
   button and HEAPP will perform calculations and provide 
   tabulated data and predictions on solid solution formation.
4. You can also calculate over a range of compositions by setting 
   the inital and final values of the range in at%, and setting the 
   step size.
5. You can export the results to an Excel file using the 
   **Save to Excel** feature for further analysis.

That's it! You're now ready.

## Contributing to HEAPP

Any modifications or contributions to HEA Phase Predictor must
be made under the terms of the GNU General Public License,
Version 3 (GPLv3). Modifications must include appropriate
notices stating the changes made, the relevant date, and that
the program is released under GPLv3.

## Components

HEAPP incorporates several third-party components, each
licensed under its respective terms. These components include:

1. **Carbon Design System v10** – A design system developed by
    IBM, used for the application’s user interface components.
    Carbon Design System is licensed under the Apache License,
    Version 2.0. More information can be found at: 
    https://carbondesignsystem.com/.
3. **PySide6 6.7.3** – A set of Python bindings for the Qt
    application framework, used for creating HEAPP’s graphical
    user interface (GUI). PySide6 is licensed under the GNU
    Lesser General Public License (LGPL). More information
    can be found at: https://wiki.qt.io/Qt_for_Python.
4. **Nuitka 2.4.8** – A Python compiler used to convert the
    HEAPP source code into executable format. Nuitka is
    licensed under the Apache License, Version 2.0. More
    information can be found at: https://nuitka.net/.
5. **Inno Setup 6.3.3** – A free installer used to package HEAPP
    for distribution on Windows platforms. Inno Setup is
    licensed under its proprietary Inno Setup License. More
    information can be found at: 
    https://jrsoftware.org/isinfo.php.

The full text of the licenses governing these third-party
components is provided in the `License` folder. Their use in HEAPP
complies with the terms of the GNU General Public License,
Version 3, under which HEAPP itself is distributed.

> [!NOTE]  
> Due to limitations in Qt's ability to fully replicate all aspects
  of the Carbon Design System, some UI components in HEAPP may not
  perfectly align with the design integrity of Carbon. Nevertheless,
  we have made every effort to maintain a consistent user experience.

## License

HEA Phase Predictor (HEAPP) is distributed under the **GNU General 
Public License, Version 3** (GPLv3). For more information, see the 
`LICENSE.txt` file.

> [!NOTE]  
> HEA Phase Predictor is a derivative work based on 
> **HEACalculator**, originally authored and copyrighted by 
> **Doğuhan Sarıtürk**, and licensed under the GNU General Public 
> License, Version 3.
> 
> For more information about HEACalculator, you can visit the 
> [**GitHub repository**](https://github.com/dogusariturk/HEACalculator).

## Attribution

If you use **HEA Phase Predictor** in academic research, 
publications, presentations, or any other form of work, please 
provide appropriate acknowledgment by citing the software. 
Additionally, if you reference **HEACalculator**, ensure proper 
attribution to its author and original work.

## Contact

If you have any questions or concerns regarding the usage of HEAPP,
please feel free to contact:

Ali Fethi Erdem – **Email:** erdem.ali@metu.edu.tr
