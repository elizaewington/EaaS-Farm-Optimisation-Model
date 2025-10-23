# EAAS AGRI FOOD DECARBONISATION

## Name
Agrifood Decarbonisation through EaaS Renewable Systems

## Description
This project contains an optimistaion tool that helps users determine an ideal number of solar panels and batteries to be installed on a farm for either emissions reduction or reduced expenditure. Users are required to supply their own demand loads as data inputs, as well as define site specific variables. Site specific variables include:
- Grid connection rating
- Available roof space and roof pitch
- Panel types and ratings (if unknown, the program will use a defualt)

Results of this program are idealised and are to only be used as an indicator. No financial advise should be placed entirely on the results of this project.

## Installation
This project is developed in Jupyter notebooks running python. To be able to run files in this project, users will need to install python and have the ability to run Jupyter notebooks. Alternatively, the files can be run on a Jupyter server if the user has access to one.

Please see the 'requirements.txt' file for a list of required external packages.

Please note that the optimisation model also requires a valid GUROBI license to solve. Please see https://www.gurobi.com/academia/academic-program-and-licenses/ for information on how to obtain an academic license (academic staff and students only. Alternatively, you can use pulp’s default solver but note that this will significantly increase the run time. To use the default solver in pulp, replace the line:
model.solve(pulp.GUROBI(Method=2, Crossover=0, Threads=8, Presolve=2, msg=1))
in the Final_Combined_System.ipynb file with the line
model.solve()

## Usage
To run this program, start by cloning or downloading the repository locally onto your computer and open it in VSCode or other IDE that runs Jupyter notebooks. The required external packages are listed in the ‘requirements.txt’ file. 
1. Please start by filling in the excel file ‘Farm Constraints Data Import Template - V1.0.xlsx’ with the farm specifications, energy bill and any technical specs. The file currently contains data specific to the East Kerang Piggery site. The emissions and costs savings priorities are set to 3 and 4 respectively by default. This can be changed as desired. The first tab on the excel file contains descriptions of each field to fill out. Please do not modify anything in the ‘Drop Down’ tab. This will cause errors in the program. Don’t forget to save the excel file when you’re done!
2. Upload one years worth of demand data to the ‘Upload Demand Files Here’. They must be an excel file. IMPORTANT NOTE: the first column of the demand file MUST contain the date and time. Any subsequent columns must contain only electricity in kW. Do not include any total demand columns. You can upload multiple files, just ensure that they ALL follow this same format. There is a demand electricity file already uploaded in this folder for East Kerang. This can be replaced or used for reference as an example of accepted format. 
3. Once you have modified the excel file and uploaded your demand data, you are ready to run the program. Simply open up the file ‘Final_Combined_System.ipynb’ in your preferred Jupyter notebook IDE and hit run all. The outputs are displayed at the bottom of the file under the ‘Output Graphs’ section. The full results from the linear program optimisation is also saved in three csv files. They output with the emissions priority and cost priority in the title so if you run the program again with different priorities you can easily compare results. The results printed in the notebook will need to be saved separately. 

## Error checking
If you run into errors please ensure that you have not input alphabetical values into numerical only fields in the excel file. It will not run. 
Ensure that you have a working gurobi license. 
Ensure that the columns in your demand file are correct as per the specifications in step 2. 
Sometimes pandas throws an error with the date time format. You may have to manually modify this in the data processing file. 

## Support
Post handover, the development team will have limited ability to provide support. This project is considered to be in a completed state, including all bugs (known and unknown) at the time of handover.

## Roadmap
This project is limited in its functionality, however can be extended by users. Some example extensions that users may find useful to explore are:
- Inclusion of FCAS (Frequency Controlled Ancillary Services) market participation. This project will not be updated with FCAS participation modelling, but can be used as a base for FCAS to be included.
- Market forecasting would extend the model to be able to explore future expected results. Due to large number of unknowns, this was out of scope for the project.

## Contributing
This project repository will not continue to be updated, and as a result will not accept contributions. Users are welcome to take a copy of the repository and edit/extend/improve upon the work completed in this project.

## Authors and acknowledgment
Developers:
- Anglea Jordan
- Asteria Li
- Charles Crowley
- Eliza Ewington
- Louise Jones
- Luella Phillips

## License
This project is solely owned by the project client, Tesseract ESS.

## Project status
This project is completed and is in the process of being handed over to the project client.

Initially, this project was going to include FCAS market participation. Due to delays and other roadblocks, FCAS was removed from the scope of the project and was not implemented in any form.



