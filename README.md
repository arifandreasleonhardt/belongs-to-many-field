# NovaFields

This package will include a group of fields that haven't been updated yet for nova v4
The first one is Benjacho/belongs-to-many-field-nova



## Belongs To Many Field Nova With Dependant
Belongs To Many field to represent many to many relationship in field. This Field allow attaching relationships easily.

<img width="914" alt="Screen Shot 2022-05-06 at 5 07 55 AM" src="https://user-images.githubusercontent.com/5789902/167112419-0cf2769e-88e0-4376-ac18-07e86378b634.png">

### Installation

```composer.json
...
   "repositories": [
        ...
		{
            "type": "vcs",
            "url": "https://github.com/arifandreasleonhardt/belongs-to-many-field"
        },
		...
    ],
...
```

```bash
composer require benjacho/belongs-to-many-field
```

### Usage

In the resource you need to pass:

- Method make ('label', 'many to many relationship function name', 'Nova Resource Relationship')

```php
use Benjacho\\BelongsToManyField\\NovaFields\BelongsToManyField;

public function fields(Request $request){
    return [
        ..., //If you are using with BelongsToMany native Field, put this field after

        BelongsToManyField::make('Role Label', 'roles', Role::class),
    ];
}
```


## License

The MIT License (MIT). Please see [License File](https://raw.githubusercontent.com/OsTheNeo/NovaFields/master/LICENSE) for more information.
