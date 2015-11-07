# Games

Game top lists.

## Functions

```$options``` is an optional parameter.

```php
<?php

// Get list of top games
$options = [
    'limit'  => 10,
    'offset' => 0,
];
topGames($options);

```

## Example Usage

File: ```app/Https/Controllers/GamesController.php```

```php
<?php

namespace App\Http\Controllers;

use TwitchApi;
use App\Http\Requests;
use Illuminate\Http\Request;
use App\Http\Controllers\Controller;

class GamesController extends Controller
{
    public function followList()
    {
        $options = [
            'limit' => 5,
        ];
        return TwitchToken::topGames($options);
    }
}
```