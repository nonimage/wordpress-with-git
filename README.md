## Set up

	git clone https://github.com/nonimage/wordpress-with-git.git [directory]

	cd [directory]

	git rm --cached Production/local-config.php

	git commit -am "Initial commit"

	git submodule add git://github.com/WordPress/WordPress.git Production/wordpress
	
	cd Production/wordpress

	git fetch --tags

	git checkout [latest stable version eg. 3.3.2]

	cd ../..
	
	git add -A

	git commit -am "Added Wordpress, updated Wordpress to latest stable version"

Add theme folder

Edit Production/local-config.php (NOT Production/wp-config.php) - theme directory name and database settings

	git commit -am "Added theme and database details"
	
## Change git remote

	git remote set-url origin git://[url]


## Update Wordpress

	cd Production/wordpress

	git fetch --tags

	git checkout [version eg. 3.3.2]

	cd ../..

	git commit -m "Updated Wordpress to [version]"


## Original

'[Install and manage WordPress with Git](http://davidwinter.me/articles/2012/04/09/install-and-manage-wordpress-with-git/)' by David Winter.