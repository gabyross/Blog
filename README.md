# Blog
Personal blog made with React  

## Steps to get into this project
-   Download the zip project and extract all into a folder (be sure you know where is saved because we are going to come back).
-   Open you folder and the project with your code editor.
-   Open your terminal and in the projects directory run  `npm install`, this will install all dependencies needed, do it also into *jsonserver* directory.
- Then, open three separate terminal windows
- Open the Jason server directory inside the first one and run `npm run db`.
	- If you see something like *air port is in use*, then you probably already have another service running on port three thousand on your computer. 
	- To solve this problem you can either close that other service and re-run the `npm run db` command or, alternatively, you can go to the file (within the same directory) *package.json* and in the `db` command you can add `-p` along with some different port to run, such as perhaps port three 3001 or 3002. Example: 
	``` 
	"scripts": {
	 "db": "json-server -w db.json -p 3001",
	 "tunnel": "ngrok http 3001"
	}
	 ```
	 - if you add a port in db, the port in tunnel must be the same
	- If you don't notice anything related to *airport is in use*, everything should work correctly.
- In the next window, run `npm run tunnel`. 
	- In this window you will see something similar to *Forwarding http://4ccb4d3696a7.ngrok.io* etc. You have to copy only the elance that appears, go to the project, folder *src/api/jsonServer.js* and paste the new link in baseURL, i.e. it should look something like:
	`baseURL: "http://4ccb4d3696a7.ngrok.io",`
- And in the last window, run `npm start` inside the project

### Note:

The previous steps is because we are going to install a little tool on our local machine called *ngrok*, this is a server that essentially makes your computer and/or services you run on your computer available to the outside world.

And so you can easily configure your phone to communicate with your server running on your computer's drive using it.

For you to understand how this was accomplished, read what was done into an essential part of the projext:
- First, we make a new directory and run `npm init`.
- Then, inside it we run`npm install json-server ngrok`.
- Finally, we modify *scripts* along with a file called *db.json`.


# About Blog app
So the first screen we're going to look at is an *index page* of sorts on the screen.

We're going to show a list of different blogs that the user has created.

We will list them all out in order and on the right hand side it also has a button that a user can use to delete a blog.

If a user wants to *create* a blog, they can click a little plus icon.

When they do so, we're going to navigate a user over to the *create page* where a user will then be prompted to enter in a title in some amount of content for a blog post.

Once they click on that save button, we're then going to save the blog and return the user either to the *index screen* or show them that very *particular blog*.

If a user ever wants to go to the *show screen* by tapping on one of these blogs, they can see the title of log in the content as well.

They can also click on the little edit icon right there and go to the *edit screen* where they can enter a new title or some amount of new content and then save it.