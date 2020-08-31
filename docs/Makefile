clean:
	ps aux |grep jekyll |awk '{print $2}' | xargs kill -9

prod:
	JEKYLL_ENV=production jekyll build

run:
	bundle exec jekyll serve --watch
