## MongoDB

MonogDB is a database that stores information as easy to read "documents". We'll use it to store data in our Node.js and Express stack.

The installation instructions can be found [here](https://docs.mongodb.com/manual/administration/install-community/) for all operating systems. However, we'll go through the steps for Mac users together.


### Install MongoDB on Mac

1. First check if Mongo DB is already installed on your machine by running this command.
```bash
which mongo
```
**If you get an output that shows a file path that means you already have it installed and do not need to follow any of the below instructions for installing Mongo DB.**

If you get an output that says `mongo not found`, that means you should install Mongo DB and follow the instructions below.

<br/>

---

<br/>

2. Run this command to get the updated brew tap for mongo.
```bash
brew tap mongodb/brew
```

<br/>

---

<br/>

3. Install Mongo DB Community
```bash
brew install mongodb-community@5.0
```

<br/>

---

<br/>

4. Start the Mongo service running in the background

```bash
brew services start mongodb-community@5.0
```

<br/>

5. After the installation, run the `which` command to verify the install was successful.

```bash
which mongo
```

If this has worked correctly, you should see a file path as output.
