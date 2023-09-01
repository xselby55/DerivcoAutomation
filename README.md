Cocktail Exercise
Introduction
The Cocktail DB is a public database of cocktails and drinks from around the world https://www.thecocktaildb.com/. The Cocktail DB has a public API to retrieve data about ingredients and drinks. See the documentation here https://www.thecocktaildb.com/api.php.

We have proposed some requirements for the cocktail API (this list is not exhaustive!).

Your task is to:
Write a minimum set of test cases to test the requirements below
Write two additional test cases that are not covered by the requirements below.
Automate the test cases using a language/framework of your choice.
I have created a Framework with RestAssured,TestNG,Maven,ExtentReport for Reporting Purposes in Java Language.
I have also implemented POJO classes using jackson for serialization purposes to handle long api response in an efficient way.
Suggest two non-functional tests that you would design
a. Load Testing: To test the cocktail API performance under heavy traffic or concurrent user requests.
b. Security Testing: To test the cocktail API security against threats such as injection attacks and other security vulnerabilities.
Suggest a framework that could be used to automate the non-functional test above.
a. For Load Testing we can you Jmeter as it is an open source tool and been widely used and have a huge community of users, It provides a GUI based interface and also we can do scripting on it in Java.
b. For Security Testing against Injection Attacks we can OWASP ZAP.
Send your tests with instructions on how to execute the automated tests within 3 days.
a. Tests can be executed by doing right on runner.xml and click on run. Before this IntelliJ or Eclipse should be installed.
b. Execution report is generated in target/executionReports folder
Always explain yourself clearly and let us know if any assumptions were made.
Functional Requirements
Search Ingredients By Name: www.thecocktaildb.com/api/json/v1/1/search.php?i=vodka

The system shall include a method to search by ingredient name and return the following fields:
Ingredient ID (string),
Ingredient (string),
Description (string),
Type (string),
Alcohol (string) and
ABV (string).
If an ingredient is non-alcoholic, Alcohol is null and ABV is null
If an ingredient is alcoholic, Alcohol is yes and ABV is not null.
Search Cocktails By Name: www.thecocktaildb.com/api/json/v1/1/search.php?s=margarita

The system shall include a method to search by cocktail name.
If the cocktail does not exist in the cocktail DB, the API shall return drinks as null.
Searching for a cocktail by name is case-insensitive
API response must contain the following Schema properties:
Element Name	Type	Required
drinks	array	yes
strDrink	string/null	yes
strDrinkAlternative	string/null	no
strTags	string/null	yes
strVideo	string/null	no
strCategory	string/null	yes
strIBA	string/null	no
strAlcoholic	string/null	yes
strGlass	string/null	yes
strInstructions (ES/DE/FR/IT/ZH-HANS/ZH-HANT)	string/null	only strInstructions
strDrinkThumb	string/null	no
strIngredient1-15	string/null	only strIngredient1
strMeasure1-15	string/null	only strMeasure1
strImageSource	string/null	no
strImageAttribution	string/null	no
strCreativeCommonsConfirmed	string/null	yes
dateModified	string/null	yes
