# sherpath-postman-APIautomation (work in progress)
Currently due to the limited features subscription of postman which Elsevier is using, we dont have integration between Github and postman. As such, this repository has to be manually updated and maintained. The following are the steps and guidelines suggested for doing that : 

### Contents
- Exporting a new API test to github
- Importing from github and executing a test/collection in postman
- Writing a new test
- Creating a new collection (needs approval)
- Global variables in postman
- Environment variables in postman, aka local variables
- Security concerns and guidelines
- Test maintenance

### Exporting a new API test to github - 
1. Using postman, write the API test
2. Once the test passes, insert the test in the appropriate Postman collection, while following the folder structure. 
3. Did you make any changes to any environment variable ? if yes, verify that it didnt cause any regression in the collection
4. Did you make any changes to any global variable ? if yes, verify that it didnt cause any regression in the collection
5. Once Steps 3 and 4 have passed and its verified that there is no regression in the collection, use the export option in the Postman collection to export the collection as a .json file. Postman does not provide the ability to export folders or individual tests.
6. Using the Add FIle - Upload Files option in github, upload the exported json files to github
7. Add a description of the changes.
8. Choose the option : Commit directly to the main branch - Commit changes

### Importing from github and executing a test/collection in postman
Since postman does not provide the ability to export folders or individual tests, each test will reside as a part of the collection, and each postman collection will exist in the github repo as a .json file.  
1. Go to the Github project and click-open the collection file you want to import into postman.
2. Click the Copy Raw contents button
3. Inside Postman, click the Import button
4. Choose the raw text tab, and paste the code you had copied from github 
5. Click continue 




### to-do : 
1. will each collection have its own environment variable file ? 
2. insert screenshots from postman 
3. approval/review process ? 
