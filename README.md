# NOAA distill website template

This is a distill website using RMarkdown and the postcards package to create the layout for the individual pages. Here postcards layout is only used for the index page, but you can use it for any page. See the [postcards](https://github.com/seankross/postcards) GitHub readme for the different layouts available.

The NMFS palette and fonts are being set in `css/nmfs-palette-theme.css`. You can try `css\theme.css` to see the distill default.

## RStudio Set-up

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

## GitHub set-up

* Go to Settings > Actions > General and check that Actions are enabled.
* Go to Settings > Actions > Pages and make sure it is set to publish from the main branch and docs folder.








