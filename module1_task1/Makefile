build:
	Hugo -D

.PHONY:
clean :
	rm -rf ./dist/

post:
	cd ./content/posts/
	touch $(POST_NAME)
	echo "---\ntitle: $(POST_TITLE)\ndate: 2010-03=26T08:47:11+01:00\ndraft:false\n---" >> ./content/posts/$(POST_NAME).md
	cd ..
	cd ..	
