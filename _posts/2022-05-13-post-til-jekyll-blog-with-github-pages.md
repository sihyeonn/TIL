---
layout: post
slug: jekyll blog with github pages
title: "Jekyll Blog with Github Pages"
category: general
---

### How to start a new blog with github pages:
1. Jekyll themes에서 마음에 드는 Jekyll theme을 찾는다.
2. 선택한 theme에서 homepage button을 클릭하여, github repository로 이동한다.
3. 해당 github repository를 우상단의 fork button을 클릭하여 원하는 이름으로 변경한다.
4. fork한 repository에서 `settings > pages` 로 이동 후, source branch를 master로 설정한다.
5. 이 때 상단에 `https://sihyeonn.github.io/TIL` 과 같이 blog 주소가 뜨게 되는데 이를 복사한다. 
6. 복사한 주소를 `_config.yml`의 url과 baseurl에 `https://sihyeonn.github.io`, `/TIL` 과 같이 각각 넣어준다.
7. 약 1분 후, Github Actions를 통해 변경된 내용이 반영되면, 복사한 주소로 접속 시 블로그가 뜬다.
8. 이 때, 블로그가 뜨지 않을 경우 fork한 repository에서 `actions` 로 이동하여 workflow가 정상적으로 진행되었는 지 확인한다.
  ```bash
  /usr/local/bundle/gems/jekyll-3.9.2/lib/jekyll/theme.rb:84:in `rescue in gemspec': The no-style-please theme could not be found. (Jekyll::Errors::MissingDependencyException)
  ```
   - 나의 경우 위의 에러가 발생하여, `_config.yml` 파일에서 `theme: no-style-please` 부분을 `remote_theme: riggraz/no-style-please` 로 수정해주었다.

---
{: data-content="references"}
- [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
- [Jekyll themes](http://jekyllthemes.org/)
- [no style, please! theme](https://github.com/riggraz/no-style-please)
