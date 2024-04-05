# My Part-time writing

---

## Post with Jekyll

Step 1. Start the Jekyll project

```powershell
# Install the jekyll and bundler gems
gem install bundler jekyll

# Create a new Jekyll site at ./myblog
jekyll new myblog

# Change into your new directory
cd myblog

# Fit the project, see Step 2

# Build the site and make it available on a local server.
bundle exec jekyll serve
```

Step 2. Fit the project
It tells the Jekyll where to place your posts.
The posts are the html files inside the [./myblog/_site/full-content/](./myblog/_site/full-content/) folder.

```yml
# --------------------
# Add the following to the myblog/_config.yml
permalink: /full-content/:year-:month-:day-:title
```

Step 3. Run the [./python/app.py](./python/app.py) to update your articles inside [./article](./article) folder.
The jekyll will **automatically** update the [./myblog/_site](./myblog/_site) folder since the [_posts](./myblog/_posts) is changed by the app.
Moreover, the app also copies the folders with the images into the [./myblog/_site/full-content/](./myblog/_site/full-content/) folder, where the posted articles are stored as html.

```powershell
python python/app.py
```
