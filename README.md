# Making your own Nitroless repo

 If you'd like to make your own collection of emotes for Nitroless, make a fork of this repo by pressing `Use this template` and follow the steps below!

 1. You'll want to have Node JS installed to run the automated script to generate the manifest JSON and resize emotes automatically. You can download it [here](https://nodejs.org/en/download/).

 2. Edit repoData.js with the appropriate details for your repo. For example:
 
 ```js
//Add Name of your Repo here
exports.name = `Example Repo`;
//Add Name and Type of Image Icon you want to use here, icon must be png
exports.icon = 'CoolIcon.png';
//Add the folder name where all your emotes are saved
exports.pathName = 'emotes';
//Add your name here, or remove the line if you don't need your name displayed under the repo's title in our clients
exports.author = 'Joe';
//Add your description here, or remove the line if you don't need any description for your repo, this is useful for SEO and Web Crawlers
exports.description = 'Cool Description';
//Add the folder name where all your stickers are saved
exports.stickerPath = 'stickers'
```

3. Add all of your emotes to the folder you're using. Make sure they're all PNGs, JPGs or GIFs. 

### GitHub Pages
> This is the recommended route for people who are beginners or are not too sure about hosting services.

4. A GitHub Actions workflow is already set up to automatically build and deploy to the gh-pages branch. Make sure your emotes are all uploaded and repoData.js is filled in.

5. Go to repository settings and head to the Pages tab. Set the Branch to gh-pages and then hit Save. Your repo will be available at `https://<your-username>.github.io`!

> If the gh-pages branch does not exist, hit refresh occasionally until it shows up. The workflow might not have created the branch yet.

> Setting up a custom domain is not documented here, but you can google `how to set up github pages custom domain`.

### Self-hosted

4. Run `npm i` to install dependencies, then run `npm run start` to build your website.

5. Now you may statically host the root of your repository anywhere.

> Taking the self-hosted route assumes you know what you're doing and have a place to host your repository.



## Pushing Updates

Pushing updates is easy!

### GitHub Pages
Just upload or push your new emotes or edits to repoData.js and your wehsite will update in a few minutes.

### Self-hosted
Just run `npm run start` (assuming you have dependencies installed from previously) and then upload your changes to your static webhost.
