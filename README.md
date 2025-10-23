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

Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.

Please see the 'requirements.txt' file for a list of required external packages.

Please note that the optimisation model also requires a valid GUROBI license to solve. Please see https://www.gurobi.com/academia/academic-program-and-licenses/ for information on how to obtain an academic license (academic staff and students only. Alternatively, you can use pulp’s default solver but note that this will significantly increase the run time. To use the default solver in pulp, replace the line:
model.solve(pulp.GUROBI(Method=2, Crossover=0, Threads=8, Presolve=2, msg=1))
in the Final_Combined_System.ipynb file with the line
model.solve()

## Usage
Use examples liberally, and show the expected output if you can. It's helpful to have inline the smallest example of usage that you can demonstrate, while providing links to more sophisticated examples if they are too long to reasonably include in the README.

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


