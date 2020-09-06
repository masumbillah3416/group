# Use same vendor folder in multiple  project 


        "config": {
            ...,
            "vendor-dir": "../vendor"
        },
Then run ``composer update``

Then you need to change three files:
1. For your app:  ``   public/index.php  ``
    ```

     require __DIR__.'/../../vendor/autoload.php';
    ```

1. Your artisan command in the root folder:  `` artisan  ``
    ```
     require __DIR__.'/../vendor/autoload.php';
    ```


1. Package auto-discovery in `` Illuminate\Foundation\PackageManifest: ``
    ```
    $this->vendorPath = $basePath.'/../vendor'; //Change this line in constructor
    ```
after all then run 
        
        php artisan package:discover --ansi