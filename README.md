#Entry Count Plugin (for Craft 3)

The Entry Count Plugin was built specifically for training purposes and is used in the [Craft Plugin Development video course](https://mijingo.com/products/screencasts/craft-plugin-development/).

It allows you to count and display the number of times that an entry has been viewed.

##Twig Tags

**count(entry.id)**

    {% set count = craft.entrycount.count(entry.id) %}

    Entry count: {{ count }}
    First count: {{ count.dateCreated }}
    Last count: {{ count.dateUpdated }}

**entries**

    {% set countedEntries = craft.entrycount.entries %}

    {% for entry in entries %}
        {% set count = craft.entrycount.count(entry.id) %}
        {{ entry.title }} ({{ count }} views)
    {% endfor %}

**increment(entry.id)**

    {% do craft.entrycount.increment(entry.id) %}
