# How to use

## Using with *canhw*

1. Clone *canhw*

```
git clone https://github.com/waterloo-rocketry/canhw.git
```

2. This repository is already included as a submodule, so no need to clone it as well

```
git submodule update --init
```

3. Add library 

    a. Open/Create a KiCAD project inside of canhw

    b. At the top menu: *Preferences*->*Manage Symbol Libraries...*

    c. Switch to the *Project Specific Libraries* tab
    
    d. Add an empty row to the table by pressing the *+* sign at the bottom
    
    e. Set the nickname to whatever you like (ie. *canhw* or *Rocketry*)
    
    f. Set the library path to `${KIPRJMOD}\..\kicad-footprints\canhw.kicad_sym`

    <img width="1171" height="813" alt="image" src="https://github.com/user-attachments/assets/b9bf31a5-f0b7-443a-a3d9-615e50fd8648" />

    NOTE: this library path assumes your project is structured as `canhw\my_board\my_board.kicad_pro` . If you're project is structured elsewise, modify the library path apropriatly (ie. `canhw\my_boards\my_board1\my_board1.kicad_pro` would use `${KIPRJMOD}\..\..\kicad-footprints\canhw.kicad_sym`)
    
    g. Repeat the process for footprints by going to *Preferences*->*Manage Footprint Libraries...*
    
    h. Now you will need to set two paths
      - For footprints `${KIPRJMOD}\..\kicad-footprints\canhw_footprints.pretty`
      - For silkscreens `${KIPRJMOD}\..\kicad-footprints\Team_Logo.pretty`

    <img width="1290" height="855" alt="image" src="https://github.com/user-attachments/assets/a1afd283-6c57-4674-b082-ddd847ca6a93" />

## Using outside *canhw*
1. Clone this repository where you deem apropriate inside your project 
```
git submodule add https://github.com/waterloo-rocketry/kicad-footprints.git
```
Recomended way to structure your project

```
My_Project
├── .git/
├── my_board
|    └── my_board.kicad_pro
├── kicad-footprints/
```

2. Same as step 3b and onwards above
