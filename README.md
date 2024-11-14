### README

# MongoDB Shell Commands for Codetribe Database

This README provides detailed instructions on how to use the MongoDB shell (Mongosh) to create and interact with the **Codetribe** database, including creating collections and inserting documents.

---

## Starting the MongoDB Shell (Mongosh)

1. **Ensure MongoDB is installed**:
   - Install MongoDB Community Edition from [MongoDB Download Center](https://www.mongodb.com/try/download/community) if not already installed.

2. **Start the MongoDB server**:
   - Open your terminal or command prompt and start the MongoDB server using:
     ```bash
     mongod
     ```

3. **Open the MongoDB shell**:
   - Open a new terminal or command prompt and type:
     ```bash
     mongosh
     ```

---

## Commands to Achieve Project Outcomes

### 1. Create the Database
To create the **Codetribe** database:
```javascript
use Codetribe
```
This will switch to the `Codetribe` database or create it if it doesn't exist.

---

### 2. Create Collections

#### a) Facilitators Collection
To create the **Facilitators** collection and insert a document:
```javascript
db.createCollection("Facilitators")

db.Facilitators.insertOne({
    Name: "John Doe",
    Location: "Johannesburg",
    Course: "Web Development"
})
```

#### b) Trainees Collection
To create the **Trainees** collection and insert a document:
```javascript
db.createCollection("Trainees")

db.Trainees.insertOne({
    Name: "Jane Smith",
    Location: "Cape Town",
    Facilitator: "John Doe"
})
```

#### c) Projects Collection
To create the **Projects** collection and insert a document:
```javascript
db.createCollection("Projects")

db.Projects.insertOne({
    Name: "E-commerce App",
    Course: "Web Development",
    Lesson: "React Components"
})
```

---

### 3. Verify the Data
To confirm that the data was inserted correctly, use the following commands:

- **Facilitators**:
  ```javascript
  db.Facilitators.find().pretty()
  ```
- **Trainees**:
  ```javascript
  db.Trainees.find().pretty()
  ```
- **Projects**:
  ```javascript
  db.Projects.find().pretty()
  ```

---

## Notes

- Always ensure the MongoDB server (`mongod`) is running before using the MongoDB shell (`mongosh`).
- The `pretty()` function formats the output for better readability.
- Additional documents can be inserted using the `insertOne` or `insertMany` commands.

---

By following these steps and commands, you can effectively create the **Codetribe** database and its collections, as well as insert and manage data in MongoDB.
