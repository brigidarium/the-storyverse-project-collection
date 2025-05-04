# The Storyverse Project ~ Collection



## Overview of the setup and approach

This collection was built by using the CollectionBuilder-CSV templates. 
+ This includes GitHub Pages output, and related GitHub Action to (re)build/deploy the site.

I've customized the CSV metadata template based on the scope and content of my collection. 
I've customized the theme.yml based on the baseline CSV metadata approach.
+ For example, having multiple fields in the CSV file that are displayed in the 'Subjects' word cloud tab (not only the 'subject' field).

### Using Obsidian
The underlying metadata and content is maintained and curated by me, using Obsidian. [Obsidian](https://obsidian.md) is a markdown-based personal knowledge management application.
+ I'm using an Obsidian Vault as the 'front end' to add and update content. 
    + Properties and tags are used to structure the metadata.
    + One key benefit of Obsidian here is hierarchical tags and the tag view, which support a lightweight and flexible way to manage 'taxonomies' and consistent values.
         > **Example A: tags for standard values required by the collectionbuilder CSV template**
         > 
         >  + `-display-template/`
         >      + `image`
         >

         > **Example B: hierarchical tags for curated/'folksonomy' tags**
         >
         > *`#svf/` prefix groups within the tag hierarchy (svf for 'storyverse folksonomy');* 
         > *this example is lgbtq representation, with hierarchy including down to level of*
         > *whether representation is main or supporting character*
         >  
         >  + `#svf/rep-lgbtq`
         >  + `#svf/rep-lgbtq/g`
         >  + `#svf/rep-lgbtq/g/supporting-character`
         >  + `#svf/rep-lgtbq`
         >  + `#svf/rep-lgtbq/b`
         >  + `#svf/rep-lgtbq/b/main-character`
         >

+ In Obsidian, my setup includes:
    + using the Dataview plugin for a table in the format needed for the collectionbuilder CSV template
        +  includes some 'data normalization' (e.g., some `regexreplace` and `join` steps) within the dataview criteria
    + using the Table to CSV Exporter plugin to generate the `data/the-storyverse-project-collection-metadata.csv` file
        + this is an easy way to generate refreshed CSV files, and manual steps are limited to then copying the 'validated' CSV file over to the appropriate folder to be able to add/commit to the repository.
+ The Obsidian Vault is backed up to a  separate repository ([the-storyverse-project](https://github.com/brigidarium/the-storyverse-project)), including as it will be used not just for this collection/GitHub pages.




----------
----------

## CollectionBuilder | CollectionBuilder-CSV
*(from original CollectionBuilder template)*

<https://collectionbuilder.github.io/> |  [CollectionBuilder Docs](https://collectionbuilder.github.io/cb-docs/) 

CollectionBuilder is a project of University of Idaho Library's [Digital Initiatives](https://www.lib.uidaho.edu/digital/) and the [Center for Digital Inquiry and Learning](https://cdil.lib.uidaho.edu) (CDIL) following the [Lib-Static](https://lib-static.github.io/) methodology. 
Powered by the open source static site generator [Jekyll](https://jekyllrb.com/) and a modern static web stack, it puts collection metadata to work building beautiful sites.

The basic theme is created using [Bootstrap](https://getbootstrap.com/).
Metadata visualizations are built using open source libraries such as [DataTables](https://datatables.net/), [Leafletjs](http://leafletjs.com/), [Spotlight gallery](https://github.com/nextapps-de/spotlight), [lazysizes](https://github.com/aFarkas/lazysizes), and [Lunr.js](https://lunrjs.com/).
Object metadata is exposed using [Schema.org](http://schema.org) and [Open Graph protocol](http://ogp.me/) standards.

Questions can be directed to **collectionbuilder.team@gmail.com**

## License

CollectionBuilder documentation and general web content is licensed [Creative Commons Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/). 
This license does *NOT* include any objects or images used in digital collections, which may have individually applied licenses described by a "rights" field.
CollectionBuilder code is licensed [MIT](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/master/LICENSE). 
This license does not include external dependencies included in the `assets/lib` directory, which are covered by their individual licenses.
