This repository contains all supplemental materials for evaluating the paper "MCKG: A Community-Driven Knowledge Graph on Medieval Charters", submitted to the [Semantic Web Journal](https://www.semantic-web-journal.net/).

The sole exception is the Medieval Charters Knowledge Graph, which is publicly available at [Wikibase cloud](https://medievalcharterskg.wikibase.cloud/wiki/Main_Page).

All resources are bundled in _mckg.zip_ and organized as follows:
* _datasets_ contains RDF datasets produced by applying our pipeline to the AMSPO corpus:
  * _Community Dataset_ includes the RDF files generated from community contributions via semi-automatic analysis.
  * _Domain Expert Dataset_ includes the RDF files created from manual expert annotations.
* _code_ contains Jupyter Notebooks implementing key pipeline components:
  * _CSVGenerator_ performs RDF-to-CSV conversion for Wikibase ingestion.
  * _Medieval NER with Roberta_ performs domain-specific NER to facilitate data extraction by community contributors.
  * _Shexer_ extracts Shape Expressions from the RDF datasets for validation and EntitySchema construction.
  * _WikibaseIntegration_ loads into the MCKG core entities and properties of the data model, as well as the processed datasets in CSV format.
* _csv_ contains the csv files used in _WikibaseIntegration_. Those with the prefix _wikibase_import_dataset_ are an output of CSVGenerator.
* _shapes_ stores both Shape Expressions extracted by _sheXer_ and the resulting EntitySchemas, available as well in the MKCG for validation.
* _sparql_ includes all SPARQL queries used for generating statistics as well as the queries corresponding to the application examples. Those are also available as examples in the MCKG Query Service.
* _NER_ contains RoBERTa NER outputs, used as support for community contributions.

This README is included in both the ZIP file and repository root for clarity.

