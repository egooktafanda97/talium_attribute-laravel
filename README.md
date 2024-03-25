### Manual Install

## composer

```php
//app.php
"talium_attribute/laravel": "dev-main",
"repositories": [{
        "type": "path",
        "url": "./package/*"
}],

TaliumAttributes\Provider\TaliumAttributesServiceProvider::class

php artisan router-attribute:push
```

### Contoh Controller

```php
use TaliumAttributes\Collection\Controller\RestController;
use TaliumAttributes\Collection\Rutes\Get;
use TaliumAttributes\Collection\Rutes\Group;
use TaliumAttributes\Collection\Rutes\Name;
use TaliumAttributes\Collection\Rutes\Post;

#[RestController()] // api | #[Controller()] // web
#[Group(["name" => "x", "prefix" => "x"])]
#[Name("x")]
class XController extends Controller
{
    public function __construct()
    {
    }

    #[Get("")]
    public function index(Request $requests)
    {
        return view('page');
    }
}
```
