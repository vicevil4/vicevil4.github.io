# vicevil4.github.io

## Install Jekyll

ruby & jekyll 설치하기

```shell
# install ruby
> brew install rbenv ruby-build
> rbenv versions
* system
> rbenv install -l
2.7.7
3.0.5
3.1.3
jruby-9.4.0.0
mruby-3.1.0
picoruby-3.0.0
rbx-5.0
truffleruby-22.3.0
truffleruby+graalvm-22.3.0

> rbenv install 3.1.3     # install ruby
> rbenv global 3.1.3      # change ruby version

# config environment
> vi ~/.zshrc
export PATH={$Home}/.rbenv/bin:$PATH && \
eval "$(rbenv init -)"
> source ~/.zshrc

# install gem bundler
> gem install bundler
> rbenv rehash

# download jekyll in root directory
> cd /path/to/repository
> gem install jekyll
> gem install github-pages

# install default bundle
> rm -rf index.html
> jekyll new ./ --force
> bundle install

# run local server
> bundle exec jekyll serve
Configuration file: /Users/aincc/Works/vicevil4/vicevil4.github.io/_config.yml
            Source: /Users/aincc/Works/vicevil4/vicevil4.github.io
       Destination: /Users/aincc/Works/vicevil4/vicevil4.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 0.497 seconds.
 Auto-regeneration: enabled for '/Users/aincc/Works/vicevil4/vicevil4.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

## Install Jekyll Theme

```shell
# download theme
> git clone https://github.com/Sylhare/Type-on-Strap.git /path/to/Type-on-Strap

# clear root directory
> cd /path/to/repository
> rm XXX ...

# copy theme and bundle install
> cp -R /path/to/Type-on-Strap/* ./
> bundle install

# config custom _config.yml
baseurl: ""
url: "https://vicevil4.github.io"

# run local server
> bundle exec jekyll serve
```

## Type-on-Strap Theme Structure

```shell
Type-on-Strap
├── _includes                # Theme includes
├── _layouts                   # Theme layouts (see below for details)
├── _portfolio                # Collection of articles for the portfolio page
├── _posts                     # Blog posts
├── _sass                      # Sass partials (compiled into css at runtime)
├── assets
|  ├── js                # JS compiled for distribution + raw sources
|  ├── css                     # CSS compiled for distribution
|  ├── fonts         # Font-Awesome, and other fonts
|  └── img         # Images used for the template
├── pages
|   ├── 404.md         # To be displayed when url is wrong
|   ├── about.md               # About example page
|   ├── gallery.md             # Gallery page for your photos
|   ├── portfolio.md        # Portfolio page for your projects
|   ├── search.md        # Search page
|   └── tags.md                # The tag page
├── _config.yml                # sample configuration
├── _data.yml
|  ├── authors.yml             # Update the post authors configurations 
|  ├── language.yml            # Localization configuration
|  ├── biblio.yml              # To create a reference bibliography
|  ├── social.yml              # Social configurations to share posts (RSS, shares, ...)
|  └── icons.yml               # Footer icons (Twitter, Github, Stackoverflow, ...)
└── index.html                 # sample home page (blog page paginated)
```

## 참고

- [1. 나만의 블로그 만들기 Git hub blog!! (github.io)](https://supermemi.tistory.com/144)
- [2. Jekyll 으로 꾸며 보자! (github.io)](https://supermemi.tistory.com/145)
- [3. 깃헙 블로그에 Hydejack 테마 적용해보기 (github with Jekyll and Hydejack theme)](https://supermemi.tistory.com/146)
- [jekyll theme - Type-on-Strap](https://github.com/sylhare/Type-on-Strap)
