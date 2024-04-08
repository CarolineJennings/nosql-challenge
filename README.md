# nosql-challenge
# Part 1
- Import the data provided. 
- Import the libraries needed in Notebook: PyMongo and Pretty Print (pprint).
- Create an instance of the Mongo Client.
- Confirm that you created the database and loaded the data properly:
- List the databases you have in MongoDB. Confirm that uk_food is listed.
- List the collection(s) in the database to ensure that establishments is there.
- Find and display one document in the establishments collection using find_one and display with pprint.
- Assign the establishments collection to a variable to prepare the collection for use.

# Part 2: Update the Database
- Make the following changes to the establishments collection:

- An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. Add the following information to the database:

{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}

# Then 
- Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
-Update the new restaurant with the BusinessTypeID you found.
-The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
- Some of the number values are stored as strings, when they should be stored as numbers.
- Use update_many to convert latitude and longitude to decimal numbers.
-Use update_many to convert RatingValue to integer numbers.

# Part 3: Exploratory Analysis
Answer the following questions while exploring the database:

- Unless otherwise stated, for each question:
Use count_documents to display the number of documents contained in the result.

- Display the first document in the results using pprint.
- Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

* Which establishments have a hygiene score equal to 20?
* Which establishments in London have a RatingValue greater than or equal to 4?
* What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
* How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.


