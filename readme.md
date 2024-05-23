
framework:  https://www.mkdocs.org

theme:  https://github.com/FernandoCelmer/mkdocs-simple-blog

hosting:  https://akuafo.github.io/evals-and-inference/

text editor:  obsidian mac client

add notes/drafts to the rawnotes directory

when ready to publish, copy the files to the githubsite directory

edit the navigation for the new pages:  mkdocs.yml

deploy everything to git (main branch)
> git add .
> git commit -m ''
> git push origin main

deploy the githubsite directory to github pages
> mkdocs gh-deploy
