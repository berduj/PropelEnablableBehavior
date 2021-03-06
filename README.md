PropelEnableDisableBehavior for [Propel2] (https://github.com/propelorm/Propel2)
==================================

The Behavior adds "enabled" column in table, and adds methods to enable/disable each rows.

Installation
------------

Add the package to your `composer.json`:

```json
{
    "require": {
        "berduj/PropelEnableDisableBehavior"
    }
}
```

Usage
-----

```xml
    <table name="sample_table">
        <column name="id" required="true" primaryKey="true" autoIncrement="true" type="INTEGER" />
        <column name="title" type="VARCHAR" />

        <behavior name="enable-disable"/>
    </table>
```

Added methods :


Object methods:

```
$object->enable();
$object->disable();
```

Query methods:

```
ObjectQuery::create()->findEnabled();
ObjectQuery::create()->findDisabled();
```


License
-------

See the [LICENSE](LICENSE) file.
