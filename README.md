# todo_kanbanboard

just how to connect the new react app to an existing git pages with existing app.

Procedure :

1- First create a repository named my-app using create-react-app.
npm init react-app todo_kanbanboard

2- We need to install GitHub Pages package as a dev-dependency.
cd todo_kanbanboard
npm install gh-pages --save-dev

3- Add properties to package.json file.
The first property we need to add at the top level homepage second we will define this as a string and the value will be "http://{username}.github.io/{repo-name}" {username} is your GitHub username, and {repo-name} is the name of the GitHub repository you created it will look like this :

"homepage": "http://soundarbalaji.github.io/todo_kanbanboard"

Second in the existing scripts property we to need to add predeploy and deploy.

"scripts": {
//...
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
}

4- Create a Github repository and initialize it and add it as a remote in your local git repository.
Now, create a remote GitHub repository with your app name and go back initialize this
git init
add it as remote
git remote add origin git@github.com:Yuribenjamin/my-app.git

5- Now deploy it to GitHub Pages.
just run the following command :

npm run deploy

6- commit and push your commit to GitHub. Optionally
git add .
git commit -m "Your awesome message"
git push origin master
