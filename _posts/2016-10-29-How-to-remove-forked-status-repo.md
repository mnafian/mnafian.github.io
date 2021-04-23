---
layout : post
tittle : How to remove forked repository status from our account
---
Yesterday, I always got the problem with my contribution stream activity in Github. I dont know what exactly the reason why github not count my activity in my gh-pages, And my old gh-pages is the [jekyll-now](https://github.com/barryclark/jekyll-now) theme from forked respository. I am already do all instruction from this [link](https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profil), but still not working after all. So I am decide to delete the fork status in my gh-pages and want to change with other jekyll themes that I am using now, I am using [Mediator](https://github.com/dirkfabisch/mediator) theme, but I dont want to fork it again, just want to repush the new downloaded code to my latest gh pages repository. This is my step to do that.

Use this command to clone the repository git that we have.

```sh
$ git clone --bare git@github.com:mnafian/mnafian.github.io.git
```

After that, delete the main repository in the remote github, and then create new one with same name, after that push our clonerepository to that new repository that we just created with this command.

```sh
$ git push --mirror
```

Check our repository in github and then viola!!, our new repository is non forked repository again, after that I am totally replace the theme with the Mediator theme.

Thank you for reading, and Happy coding!!
