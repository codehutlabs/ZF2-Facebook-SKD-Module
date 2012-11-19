ZF2-Facebook-SKD-Module
=======================

Zend Framework 2 Facebook SDK Module

Include the module in your config/application.config.php


Usage:
-----------------------

	use Facebook\Controller\Facebook;
	use Facebook\Controller\FacebookApiException;
	use \Exception;



And in your class:
-----------------------

	public $facebook;

	public function  __construct() {
		
		$this->facebook = new Facebook(array(
			'appId'  => 'yourAppId',
			'secret' => 'yourSecret'
		));

	}


Use it in your action function:
-----------------------

	try {
  	  $user = $this->facebook->getUser();
	} catch (Exception $e) {
		print_r($e);
	}

