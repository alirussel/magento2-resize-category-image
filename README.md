Magento 2 Resize Category Images
================================

## How to install?


Install with Composer!

	```
	composer required ali/magento2-rimage
	php bin/magento module:enable Ali_Rimage
	php bin/magento setup:upgrade
	php bin/magento setup:di:compile
	php bin/magento setup:static-content:deploy
	php bin/magento cache:flush
	```


Install manually!

  * Download
  * Extract files
  * In your Magento 2 root directory create folder app/code/Ali/Rimage
  * Copy files and folders from archive to that folder
  * In command line, using "cd", navigate to your Magento 2 root directory
  * Run the commands:
	```
	php bin/magento setup:upgrade
	php bin/magento setup:di:compile
	php bin/magento setup:static-content:deploy
	php bin/magento cache:flush
	```



## How to use this?

	Add helper on top:

	```PHP
	$_helper_cat_image = $this->helper('Ali\Rimage\Helper\Resizer')

	```

	Put follow code to Resize image:

	```PHP
	$image_path = "/catalog/category/".$_category->getImage();
	<img src="<?php echo $_helper_cat_image->resizeImage($image_path,450,285);?>">
	```


## License
	* Its free
