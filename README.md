HerpDock User Manual
1. Introduction
HerpDock is an open-source, GUI-based software designed to streamline molecular docking, high-throughput virtual screening, and ADME (Absorption, Distribution, Metabolism, and Excretion) studies. It primarily focuses on HSV-1 viral proteins and host proteins involved in HSV-1 infection.
This manual will guide you through the steps for setting up and using HerpDock, including how to perform docking studies, ADME analyses, and visualize results.

2. System Requirements
Operating System: Windows 10 or higher
Pre-installed Software:
Open Babel (for molecular format conversion and ligand optimization)
Installation Instructions:
Download HerpDock: Download the HerpDock package from the provided GitHub link: "https://github.com/Sudhk24/Herpdock"
Install Open Babel: Follow the installation guide for Open Babel, available on its GitHub page: "https://github.com/openbabel/openbabel/releases"
Ensure Internet Access: HerpDock uses Pubchem to download small molecules and ChEMBL for ADME calculations, so make sure you have an active internet connection for those features.

3. Workflow Overview

3.1 Launch the HerpDock executable on your system.
Project Name: Enter a name for your project to create a new working directory.

3.2 Ligand Selection
You can add ligands to the project by either:
Downloading from PubChem:
Enter the PubChem CID(s) or compound names in the text box (comma-separated for multiple ligands).
Click "Download 3D Conformer" button to retrieve the ligands.
The downloaded ligands will be stored in the "ligands" folder within the project directory.
Uploading Local Ligands:
Click Browse to select ligand files from your local system.
The selected ligands will be copied to the project’s "ligands" folder.

3.3 Target Protein Selection
Use the dropdown menu to select a target protein for docking from the list of pre-optimized HSV-1 viral proteins included in HerpDock.
For example, choose glycoprotein D (gD) if your goal is to study viral entry inhibition.

3.4 Molecular Docking
Once the ligands and target proteins are selected, click Dock to initiate molecular docking.
The ligands are optimized using Open Babel, converted to the pdbqt format, and stored in a "ligands_pdbqt" folder within the project directory.
Docking will be performed using AutoDock Vina, and the docked protein-ligand complexes will be saved in a "Results" folder present in the project file, including:
Ligand_Complex_PDB folder: Stores protein-ligand complexes for visualization.
Another file would be created in the main project folder named Docking_results.csv: Contains docking scores and binding affinities.

3.5 Visualization of Docking Results
After docking, click the Visualize button to open RasMol, a molecular visualization tool included with HerpDock.
RasMol allows you to explore the 3D structure of the protein-ligand complex.

3.6 ADME Studies
After docking, click ADME to perform ADME calculations on the ligands.
ChEMBL will provide basic ADME properties for the ligands, and the results will be saved as "ADME_results.csv" in the main project folder.

4. Detailed Step-by-Step Example
Here is a step-by-step guide using an example docking scenario with HSV-1 glycoprotein D (gD):

4.1 Creating a Project
Enter a project name: Example_Project_HSV1_gD.
Click "Create" to generate the project folder.

4.2 Ligand Selection
Enter the ligand name: Example: acyclovir,tenofovir,cidofovir
Click "Download 3D Conformer" to retrieve and store the ligand files in the "ligands" folder.

4.3 Protein Selection
From the dropdown menu, select gD (HVEM interaction site) as the target protein.

4.4 Docking
Click Dock to initiate the docking process between the selected ligands and the target protein.
The protein-ligand docked results will be stored in the "Ligand_Complex_PDB" folder present inside the "Results" folder present in the project file.
The summary file would be present in the project folder named Docking_results.csv

4.5 Visualization
After docking, click Visualize and select the small molecule and protein complex that you want to explore.

4.6 ADME Analysis
Click ADME to calculate the absorption, distribution, metabolism, and excretion properties of the top docking ligands using ChEMBL.
The results will be stored in the main project folder named as "ADME_results.csv".

5. Limitations of HerpDock
Operating System: HerpDock currently only supports Windows OS.
3D Structure Requirements: Small molecules without a 3D structure in PubChem cannot be directly used in HerpDock. Users must convert 2D structures to 3D using external software.
ADME Properties: HerpDock’s ADME functionality provides only basic properties, as it relies on ChEMBL.

6. Future Directions
In future versions, HerpDock may include:
Support for additional herpesvirus proteins (e.g., HSV-2).
AI integration for improved docking predictions and ligand scoring.
Expanded ADME features with more comprehensive property analysis.

7. Troubleshooting
Common Issues:

Issue: HerpDock does not load ligand files.
Solution: Ensure that ligand files are in the correct format (e.g., .mol, .sdf) and convert if necessary using Open Babel.

Issue: No ADME properties for certain ligands.
Solution: ADME calculations are dependent on ChEMBL, and properties may not be available for certain compounds.

Issue: Where can I find ligands for high-throughput virtual screening.
Solution: You can download a library of 5376 ligands that are ready for molecular docking from the link: "https://github.com/Sudhk24/Ligand_Database". 
You can download the ligands from the link then extract all the files. If you want, you can select all these ligands for virtual screening against protein of your choice. This can be done by clicking the "Browse" button in the HerpDock program.

8. Contact and Support
For additional support or to report issues, please visit our GitHub page "https://github.com/Sudhk24/Herpdock" or contact us at ssing73@uic.edu.
