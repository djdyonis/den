JsonTable
===

Usage:

```php
$data = [
    'key1' => 'val1',
    'key2' => 'val2',
    'key3' => ['key4' => 'val4','key4.1' => 'val4.1'],
    'key5' => 'val5'
];

echo JsonTable::render($data,[
    'attr' => [
        'class' => 'table table-striped',
        'data-table-id' => 'mytable'
    ]
]);
```

