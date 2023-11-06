# Interdisciplinary Center for Brain Information (ICBI)

This is the website of our academic research group at Shenzhen Institutes of Advanced Technology, Chinese Academy of Sciences.

This website is powered by Jekyll and some Bootstrap, Bootwatch. It was customized based on a template generously provided from [Allan Lab](https://github.com/mpa139/allanlab).

Go to *aboutwebsite.md*  to learn how to copy and modidy this page for your purpose. 

## test the site:
```
cd DIR_OF_ICBI_SIAT_GITHUB_IO
bundle exec jekyll serve --watch
```

## How to deploy the website 
```
jekyll build 
lftp icbi:password@icbi.siat.ac.cn

#within lftp 
mirror -R _site/ / 
```

To midify the site, start from the following path:

index.html

team/_posts/

blog/_posts/

papers/_posts/

misc/_posts/

projects/index.html


Copyright ICBI@2020. Code released under the MIT License.

