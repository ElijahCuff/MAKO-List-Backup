# MAKO List Backup
This project plans to make an Offline Accessible version of the MAKO list in fear it may be taken down soon, again.
This is a backup of all the offenders on MAKO.org.au from A-Z in a Flat File database.    
   
It has taken me about 2 days and about 18 hours to build software and extract the government backup of MAKO.org.au from the Trove WayBack Machine and the Website Archive WayBack Machine.  
     
• This file is a single database of all the offenders names, ages (if known), sentences & offences with a small description of the offence committed.   
• It took me hours of time and hours to build software for this extraction to be as successful as it was.    
       
## How do i use this database ?    
This database uses the following structure,    
Each line in the file is a record found on MAKO, the Seperating Character for the information on each line is (|) without the brackets.    
   
Here's an example of the first line,   
```
FIRSTNAME MIDDLENAME LASTNAME ( OTHERNAME ) ( LOCATION ) | AGE | SENTENCE | OFFENCE | IMAGE OF OFFENDER
```
The line is Split into 5 sections,    
1 Name & Location    
2 Age    
3 Sentence    
4 Offence    
5 Image    
    
Each section is split by the | character.   
     
To read this file, you'll need a script that reads the file Line-By-Line until it hits the record you want, each record is split by the Next Line Character "\n".
     
    
EXAMPLE FILE,
```
ADAM LAME CITIZEN (VIC) | 20 yrs old | Charged with Assault | Assault Details
JOHN DOE CITIZEN (NT) | 24 yrs old | Charged with Assault | Assault Details | /images/john_citizen.jpg
JIM HOE CITIZEN (ACT) | 60 yrs old | Charged with Assault | Assault Details
```     
Notice how only records with Found images have the Images link attached, this means that only records with images are 5 sections long, others are 4 sections long,
this can make putting the details into an array difficult so be warned that the section count varies between 4 and 5 sections of information.
     
PLEASE NOTE THAT THE IMAGES TOOK UP 130 MB OF SPACE, FAR TOO BIG FOR GITHUB EXTRA DATA, SO I'VE FOUND A LIVE VERSION OF THE FOLDER HERE,
```
https://web.archive.org.au/awa/20180314133944im_/http://www.mako.org.au/images/
```
     
This was the latest backup on the WayBack Machine, so please use that link to make your live photo links work, example

```
https://web.archive.org.au/awa/20180314133944im_/http://www.mako.org.au/images/john_citizen.jpg
```
   
Other Resources,      
Search Offenders on Trove,   
```
https://trove.nla.gov.au/search/advanced/category/websites?l-site=mako.org.au&keyword=First+Last
```
   
Search Other Offenders on AussieOffenders,   
```
https://aussiesexoffenders.wordpress.com/?s=First+Last
```

Please Be Sensible and Safe with this information.
 
I'd like to give special thanks to the government WayBack machine and the Australian National Library for providing this information in 2020.

