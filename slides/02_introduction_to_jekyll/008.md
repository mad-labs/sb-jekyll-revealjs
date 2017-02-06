
### Collections

Not everything is a post or a page. Collections allow you to define a new type of document that behave like Pages or Posts do normally, but also have their own unique properties and namespace.
<!-- vertical-slide -->

### Using Collections - Step 1

Tell Jekyll to read in your collection, adding the following to your site’s 

```sh
_config.yml
```

replacing my_collection with the name of your collection:

```yaml
collections:
- my_collection
```

You can optionally specify metadata for your collection in the configuration:

```yaml
collections:
  my_collection:
    foo: bar
```
<!-- vertical-slide -->

### Using Collections - Step 2

Create a corresponding folder 

```sh
_my_collection /
```

and add documents. 

YAML Front Matter is read in as data if it exists, and everything after it is stuck in the Document’s content attribute. If no YAML Front Matter is provided, Jekyll will not generate the file in your collection.

Be sure to name your directories correctly: *the folder* must be named *identically* to the collection you defined in your \_config.yml file, with the addition of the preceding _ character.
<!-- next-slide -->