# MongoDB

MonogDB is a database that stores information as easy to read "documents". We'll use it to store data in our Node.js and Express stack.

The installation instructions can be found [here](https://docs.mongodb.com/manual/administration/install-community/) for all operating systems. However, we'll go through the steps for Mac users together.

<br/>

---

<br/>

1. First check if Mongo DB is already installed on your machine by running this command.
```bash
which mongo
```

If you get an output that shows a file path like this
```bash
/usr/local/bin/mongo
```
you already have MongoDB and **do not need to continue with the instructions below.**

If you get an output that says `mongo not found`, that means **you should install Mongo DB and follow the instructions below.**

<br/>

---

<br/>

## For Mac M1 Chip Users

<details>
<summary>Mac M1 Chip users follow these steps before continuing past this point.</summary>

1. Check where Homebrew installs packages.
```bash
brew --prefix
```
You may see `/usr/local`. We'll update this so that homebrew installs packages in the proper location (`/opt/homebrew`).

<br/>

---

<br/>

2. The following steps will create the proper directory, set up the permissions, and download Homebrew.
```bash
sudo mkdir -p /opt/homebrew
sudo chown -R $(whoami):staff /opt/homebrew
cd /opt
curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
```

<br/>

---

<br/>

3. Add the Homebrew bin to your PATH variable.
```bash
echo export PATH="/opt/homebrew/bin:/usr/local/bin:$PATH" >> ~/.zprofile
echo export PATH="/opt/homebrew/bin:/usr/local/bin:$PATH" >> ~/.zshrc
```

<br/>

---

<br/>

4. Quit out of your terminal completely with `cmd + q` and then open it up again.

<br/>

---

<br/>

5. Check if the Homebrew install location has been updated.
```bash
brew --prefix
```
You should now see `/opt/homebrew` and are good to continue.

</details>

## Install MongoDB on Mac

---

<br/>

1. Run this command to get the updated brew tap for mongo.
```bash
brew tap mongodb/brew
```

<br/>

---

<br/>

2. Install Mongo DB Community
```bash
brew install mongodb-community@5.0
```

<br/>

---

<br/>

3. Start the Mongo service running in the background

```bash
brew services start mongodb-community@5.0
```

<br/>

---

<br/>

4. After the installation, run the `which` command to verify the install was successful.

```bash
which mongo
```

If this has worked correctly, you should see a file path as output.

You are all set and ready to Mongo!