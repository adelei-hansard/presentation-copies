# presentation-copies

Automates the process of creating a presentation copy of a speech made in the commons.
An MP either asks the [Vote Office PET team](https://parlinet.parliament.uk/teams/house-of-commons/chamber-participation-team/vote-office/publications-enquiries-team/) or [Hansard](https://guidetoprocedure.parliament.uk/articles/v6wxttYz/how-to-make-a-maiden-speech) for a copy of their maiden speech. 
Or on occassion MPs or other external organisations/people request presentation copies of speeches for other reasons such as ceremonial or memorial reasons.

## What the project does
Creates an XML file of a MPs speech using a link either from the hansard website or using the commons library index.
The XML file can then be imported into an indesign template which will then create a front presentation page followed by a copy of the speech from Hansard.


### How it works - No GUI
* Insert Link into presentations-copies-script
* Link helps to find content from two Hansard APIs
* The end of the URL has FindDebateByContributionId
* [Hansard Search FindDebateByContributionId](https://hansard-api.parliament.uk/swagger/ui/index#!/Search/Search_FindDebateByContributionId)
* The data returned has a DebateSectionExtId, which the script uses to find the full details of the debate
* This is in the [Hansard Debate](https://hansard-api.parliament.uk/swagger/ui/index#!/Debates/Debates_GetDebate)
* The speech itself can then be found by using the contribution ID that is collected from the URL earlier

## Why the project is useful
There are currently 335 new MPs since the July 2024 general election. Between July and September over 230 MPs have made their maiden speeches and so far (Oct 24) the PET team have processed 70 requests.
The PET team were using word to create these which is not a print layout software and it is very time consuming.
This takes a 30+ min process into a process which takes a few minutes. 

## How users can get started with the project
### Users will need
* A code editor - Our team uses VSCode
* Indesign
* The [Hansard website](https://hansard.parliament.uk/) or the [library index spreadsheet](https://commonslibrary.parliament.uk/research-briefings/sn04588/)
* Member name, date of speech or debate 

### Create XML - With GUI
* Run the production-gui python file
* Opens a GUI, which asks for the website URL and for a folder location
* Saves the XML for the speech in the shared folder

### Create XML - Without GUI
* insert link into the presentation-copies-script python file
* Run the script
* the file will save in this project folder

## Where users can get help with your project
Nikki in the Tech team in PPU

## Who maintains and contributes to the project
The Tech team in PPU