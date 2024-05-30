# PyshinStart
Introduction Page of PyshinImpact

powered by jekyllrb.com

## Setup

follow the steps on https://jekyllrb.com/docs/installation/macos/ to install all prerequisites

## Development

This project is based on jekyll. The basic concepts and tutorial of jekyll can be found in https://jekyllrb.com/docs/.

However, the basic development only requires knowledge in Markdown syntax. All of our pages contains two main parts:
- Front Matter part:
    
    The upper part of each markdown field surrounded by "---". It contains config info of the page and is essential to jekyll build process. Do not remove them and copy them when you add new files!
- Content part:

    The lower part of each markdown field. It completely follows markdown syntax.

Typically when you need to add pages, the steps you need to follow are:

1. copy the Front Matter part of same type pages to your new page
2. update config in your Front Matter part
3. update Content part using markdown syntax

### add/update service description

To update services main page, for example, adding general information like "我们提供以下服务:", you need to update `./service.md`

service descriptions can be found in `./_services/`. To add a new service, you can simply create a file following the previous style, it will be automatically added to service list page. To change the service title listed in the service main page, you need to update `title` field in Front Matter part. To update service image, you should put your image in `./images` and update the Front Matter part.

### add/update cases

The cases main page is `./case.md`. All cases should be put under `./_posts`. To add a new case, you should create a file under `./_posts` folder and follow the previous style, INCLUDING the file naming style, otherwise, it cannot be sorted correctly in case archive page. After you adding a new file, it will automatically display in case archive page.

You also need to assign related programs to your new cases. To do this, you should modified the `categories` field in the Front Matter part. Programs can be separated by blankspace. They will be automatically collected into your configurated program in program page.

### add/update members

The member main page is `./member.md`. All members should be put under `./_members`. You should also put member image under `./images` and link them to your profile.

### update side config

The title, logo, and any other configurations can be found in `./_config.yml`. Do not change it unless you know what you are doing.


## Test locally

If you only add/update the markdown part, you can simply test by preview the markdown and submit your change directly.

Otherwise, you should test on your local env before submitting a pull request:

```sh
bundle exec jekyll serve
# browse to localhost:4000
```

## Possible issues

### Update ruby version

```
brew install ruby
brew link --overwrite ruby --force
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```