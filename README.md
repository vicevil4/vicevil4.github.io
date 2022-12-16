# vicevil4.github.io

## Install jekyll

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

# install default bundle
> rm -rf index.html
> jekyll new ./ --force
> bundle install
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

## 참고

- [1.나만의 블로그 만들기 Git hub blog!! (github.io)](https://supermemi.tistory.com/144)
- [2. Jekyll 으로 꾸며 보자! (github.io)](https://supermemi.tistory.com/145)

