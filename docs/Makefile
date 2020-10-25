clean:
	ps aux |grep jekyll |awk '{print $2}' | xargs kill -9

prod:
	JEKYLL_ENV=production bundle exec jekyll build

publish:
	make prod
	git push

run:
	bundle exec jekyll serve --watch
