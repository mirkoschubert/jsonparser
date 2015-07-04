# How to use the JSONParser Class

## Open or Create a JSON File

There is an optional language variable for creating multi-language JSON files.

```php
$json = new JSONParser('filename.json', 'en-en');
```

## Create a new Entry

The 'name' variable must be set as an identificator

```php
$brian = new stdClass();
$brian->name = 'brian';
$brian->city = 'memphis';
$json->appendEntry($brian);
```

## Edit an existing Entry

```php
$brian = selectEntryByName('brian');
unset($brian->city);
$brian->surname = 'walker';
$json->updateEntry($brian);
```

## Delete an Entry

```php
$json->deleteEntry('brian');
```

## Access JSON stream directly

For API porposes there are two variables:

```php
$json->stream
```

Full JSON Stream with language, created and updated dates and status messages.

```php
$json->data
```

Data stream to manipulate the JSON data directly.

Have fun!