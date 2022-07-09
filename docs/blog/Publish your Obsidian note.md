# Publish your Obsidian note

Using a nice [template based on mkdocs](https://github.com/jobindj/obsidian-publish-mkdocs) it's easy to publish your notes. It uses GitHub, so it's a little developer oriented, but it's not that complex.
## How does it work?
Developers use a tool named _git_ to secure and share code and data. They put  it in a folder and using git they create a _repository_ on their computer or they start from an existing repository hosted somewhere - or create a _repository_ there - and _clone_ (that is a special form of copy) it on a local device.
This system is used here to sync a folder inside your Obsidian tree to a remote repository you create on a free service GitHub which automatically publishes the content on connected _GitHub pages_. Sounds complicated, but you only have to do your part.
## What you need to do
- Follow the directions above 
- Create your free GitHub account if needed
- Install a git tool and learn a little about git [here](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners) you can skip step 5, 8 and 9
- (in short: 
  inside your new Obsidian folder (= your local repository):
	  - git add . (collect your changes)
	  - git commit -m "update" (or use other text)
	  - git push (send you changes to your GitHub repo) 
	  - (your changes are - after a short time - published at `https://<your github username>.github.io/<reponame>/<foldername>`)
To be able to use images in your posts, you need to move your 'attachments' folder _inside_ your repo folder. Otherwise, the images are not going to be found in the published pages.

## Security risk!

But do you want all attachments in your repo? Note that your repo settings should be 'Public'. If you changed that to 'private' the system breaks. So you don't want to upload all your attachments to GitHub. 
It's better to only add the images to your repo you really need in your published notes. One way of doing this is to selectively use 'git add' to add only the images you need. You can also - it's a bit more work up front - put your other attachments in a folder 'private' inside your attachments folder and exclude that folder from your repo. Note that Obsidian still seems to find the attachments in your existing links. 
To do that add a line to the .gitignore file in your repository. 

.gitignore file:

docs/03-Attachmemts/private

Replace 'docs' with the name of your local repo folder. 

Now, if you use 'git add .' only the attachments in the root folder are added to your repo. 

_You still have to be careful to place new Obsidian attachments in the safe private folder._
