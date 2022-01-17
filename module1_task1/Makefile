build:
	Hugo -D

.PHONY:
clean :
	rm -rf ./dist/

post:
	mkdir ./content/posts/
	cd ./content/posts/
	touch welcome.md
	echo "---\ntitle: "Welcome to Awesome Inc."\ndate: 2010-03=26T08:47:11+01:00\ndraft:false\n---" >> ./content/posts/welcome.md
	cd ./module1_task1/	
