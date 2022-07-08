# Publish your Obsidian note

Using the great plugin https://github.com/jobindj/obsidian-publish-mkdocs it's easy to publish your notes. It uses GitHub, so it's a little developer oriented, but it's not that complex.

# What you need to do
- Add the plugin in Obsidian
- Follow the directions above 
- Create your free GitHub account
- Install a git tool and learn a little about git [here](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners) you can skip step 5, 8 and 9
- (in short: 
  inside your new Obsidian folder (= your local repo):
	  - git add . (collect your changes)
	  - git commit -m "update" (or use other text)
	  - git push (send you changes to your GitHub repo) 
	  - (your changes are - after a short time - published at `https://<your github username>.github.io/<reponame>/<foldername>`)
To be able to use images in your posts, you need to move your 'attachments' folder _inside_ your repo folder. Otherwise, the images are not going be found in the published pages.

## Security risk!

But do you want all attachments in your repo? Note that your repo is defaulting to 'Public'. Even after you change that to 'private' see he [docs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility) Maybe you don't want to upload all your attachments to GitHub. (Unless you really want an extra backup.) 
It's better to only add the images you really need in your published notes. One way of doing this is to put your attachments in a folder 'private' inside your attachments folder and exclude that folder from your repo. To do that add a line to the .gitignore file 

``` .gitignore file

docs/03-Attachmemts/private

```

Replace 'docs' with the name of your local repo folder
