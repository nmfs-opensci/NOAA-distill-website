[![](https://img.shields.io/badge/Open%20In-RStudio%20Cloud-green)](https://rstudio.cloud/content/4772998) *Try without installing anything. Make sure to make click the Make a Copy button or you will lose all your changes.*


# NOAA distill website template

This is a distill website using RMarkdown and the postcards package to create the layout for the individual pages. Here postcards layout is only used for the index page, but you can use it for any page. See the [postcards](https://github.com/seankross/postcards) GitHub readme for the different layouts available.

The NMFS palette and fonts are being set in `css/nmfs-palette-theme.css`. You can try `css\theme.css` to see the distill default.

## GitHub set-up

* Click the green "Use This Template" button to make a repository with this content. Make sure to make your repo public (since GitHub Pages doesn't work on private repos unless you have a paid account).

* Turn on GitHub Actions under Settings > Actions > General
<img width="719" alt="image" src="https://user-images.githubusercontent.com/2545978/196808404-0c075fcf-db03-4516-88dd-3143b9fca475.png">

* Go to Settings > Actions > Pages and make sure it is set to publish from the main branch and docs folder.
<img width="646" alt="image" src="https://user-images.githubusercontent.com/2545978/196588577-563c75f0-b6fd-4311-b499-78669233f7ec.png">

* Edit the repo description and Readme to add a link to the webpage. When you edit the description, you will see the link url in the url box or you can click on the Actions tab or the  Settings > Pages page to find the url of the distill website

## Edit in the browser directly

Because the GitHub Action will load R and run everything, you can just edit and add files in the browser. You can click the Actions tab to watch the progress. This is a common workflow once you have your site developed and you just need to do a quick update.

## Edit locally using RStudio

### RStudio Set-up

* First clone your new repo to your local computer. How? From RStudio, do File > New Project > Version Control > Git. Then paste the url of **your** repo.

* Install the needed packages. You only need to do this once.

```
install.packages(c("rmarkdown", "distill", "postcards", "knitr")
```

### Building the website

There is a GitHub Action that will automatically build the site whenever you edit the content on GitHub (directly or via a local change and then push).

You can build the site locally in RStudio, by going to the Build tab and clicking Build website. Don't see that? Go to Tools > Project Options > Build Tools and make sure the top dropdown says "Website".

### Customize

* `index.Rmd` will be the front page. You can change the layout by changing `postcards::trestles`
* Edit `_site.yml` to change the top navbar
* Add pages like `Page1.Rmd` and then add those to `_site.yml`
* Add your images (like logos) to `images` and a favicon to `favicon.ico`
* Push your changes back up to GitHub and the GitHub Action will rebuild the website.









