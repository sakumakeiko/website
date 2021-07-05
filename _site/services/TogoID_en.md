# TogoID
## About TogoID
TogoID is a web application that allows you to search and convert links between identifier(ID)s of databases(DBs) in the life sciences. [https://togoid.dbcls.jp/](https://togoid.dbcls.jp/)

## Features of TogoID
- When you enter a list of IDs (up to thousands), DBs of conversion candidates are listed, and then you can convert them to the corresponding IDs. In addition to one-to-one ID conversion, it is also possible to convert including the route to the target DB.
- TogoID provides the ability to retrieve converted IDs in various formats: 1. copy it to the clipboard for immediate use in other services, 2. get a list of converted IDs in text format, 3. get a list of converted IDs in a format that includes a link URL to the original DB, 4. get a list of converted IDs in CSV format that includes all of the conversion routes.
- Links between databases is maintained by the [togoid-config](https://github.com/dbcls/togoid-config) which extracts a pair of identifiers from a SPARQL query for RDF data, database specific APIs, and the flat files of original data sources. See the "DATABASES" tab on the TogoID website for a list of supported databases.
- As of July 2021, TogoID contains more than 150 ID pairs from more than 60 DBs(constantly expanding). By maintaining the metadata about the IDs in the target DB, the update method of ID pairs, and the update frequency, TogoID provides the latest information on the links between IDs.
- The TogoID service is also available as an API, which allows other applications to use it for ID conversion.
    - Examples:
        1. [https://api.togoid.dbcls.jp/convert?ids=5460,6657,9314,4609&route=ncbigene,ensembl_gene&format=json](https://api.togoid.dbcls.jp/convert?ids=5460,6657,9314,4609&route=ncbigene,ensembl_gene&format=json)
        2. [https://api.togoid.dbcls.jp/convert?ids=5460,6657,9314,4609&route=ncbigene,ensembl_gene,uniprot&format=json](https://api.togoid.dbcls.jp/convert?ids=5460,6657,9314,4609&route=ncbigene,ensembl_gene,uniprot&format=json)
        3. [https://api.togoid.dbcls.jp/convert?format=json&include=pair&route=pubchem_compound,chebi,reactome_reaction,uniprot,ncbigene&ids=649](https://api.togoid.dbcls.jp/convert?format=json&include=pair&route=pubchem_compound,chebi,reactome_reaction,uniprot,ncbigene&ids=649)

## Screenshots

### ID conversion from top page

![Fig-1](https://raw.githubusercontent.com/dbcls/website/master/services/images/TogoID_fig-1_20210614.png)

### Results of ID conversion

![Fig-2](https://raw.githubusercontent.com/dbcls/website/master/services/images/TogoID_fig-2_20210614.png)

### Metadata about the IDs of the listed DBs

![Fig-3](https://raw.githubusercontent.com/dbcls/website/master/services/images/TogoID_fig-3_20210614.png)

