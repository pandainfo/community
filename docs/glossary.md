# Glossary

This section lists some terms that are being used
throughout this project with which contributors should
become familiar. Obviously we cannot explain all terms
relevant to e-commerce or ERP. A look at Wikipedia and
at the [GS1 Glossary](https://xchange.gs1.org/sites/glossary) is recommended.

## ONIX

* **ONIX stands for ONline Information eXchange**

  ONIX is a metadata standard for the exchange
  of product information and bibliographic data.
  As such, ONIX is a modern Semantic Web or Web 3.0
  solution using XML, the Extensible Markup Language.
  Its content consists of descriptive data that may
  be easily stored in web-accessible databases. This
  can be a relational database like MySQL or
  PostgreSQL or a NoSQL DB like [CouchDB] or a
  document store like [BaseX] – a native XML database.
  Valid ONIX identifiers are – among others – [DOI],
  [ISBN], [ISNI], and [ISSN].

  ONIX enables automated data exchange and workflows
  for all players and the entire supply chain of the
  book trade. In addition to bibliographic information,
  the ONIX format – which has become the international
  standard in the book trade – also contains marketing
  information such as addresses, delivery details or
  prices. The sale of books without associated product
  data has become unthinkable with the advent of
  eCommerce. Thus, the automated exchange of metadata
  is becoming increasingly important for bookstores.
  ONIX files must be [DTD-valid](#dtd). To minimize potential
  errors, it is recommended to use [XSD-valid](#xsd) files.

[DOI]: https://www.doi.org/ "Digital Object Identifier System"
[ISBN]: https://www.isbn-international.org/ "International Standard Book Number"
[ISNI]: https://isni.org/ "International Standard Name Identifier"
[ISSN]: https://www.issn.org/ "International Standard Serial Number"
[CouchDB]: https://github.com/apache/couchdb "Apache CouchDB"
[BaseX]: https://github.com/BaseXdb/basex "The XML Framework"

## DTD

* **DTD stands for Document Type Definition**

  DTDs are declarations that define the document type and
  document structure for a markup language of the SGML family
  like XML or HTML starting with an XML declaration followed
  by a DOCTYPE which contains the respective system identifiers.
  In our case the DTD defines the [ONIX](#onix) data elements.
  The XML parser needs the DTD for schema validation. Such a
  parser is called DTD-validating parser. There are also
  non-validating parsers that only check if the XML syntax of
  the document body is well-formed (according to the document
  type declarations).

  An XML declaration for a file with UFT-8 encoding for special
  characters looks like this:

  `<?xml version="1.0" encoding="UTF-8"?>`

## XSD

* **XSD stands for XML Schema Definition**

  XSDs or XML Schema Definitions by W3C are the successor to [DTDs](#dtd),
  and use stronger typing. Both the DTD scheme as well as the
  stricter XSD scheme check the correct structure of your [ONIX](#onix)
  files. An XML schema definition consists of a separate XML
  document, while a DTD itself is not an XML document. The XSD
  schema files for ONIX can be downloaded from [EDItEUR](https://www.editeur.org/8/ONIX).
  These XML schemes describe the grammar of ONIX, i.e. whether
  sentences are valid and which vocabulary may be used for error-free
  parsing. ONIX for Books code lists are available for download [here][onix-code-lists].
  Further information about the XSD language together with
  criticism, code examples, and comparisons with the much simpler
  DTD language can be found on [Wikipedia][xsd-wiki].

[onix-code-lists]: https://www.editeur.org/14/Code-Lists/ "ONIX for Books code lists by EDItEUR"
[xsd-wiki]: https://en.wikipedia.org/wiki/XML_Schema_(W3C) "XML Schema (W3C) on Wikipedia"

## GTIN

* **GTIN stands for Global Trade Item Number**

  GTIN is an international standard for identifying product
  information developed by GS1, the inventor of article barcodes
  and of the [EDI] standards. EAN-13 (now GTIN-13) – the 13 digits
  long European Article Number – and ISBN-13, the International
  Standard Book Number – are subsets of GTIN.

  Schema.org defines the respective Semantic Web schemas for
  structured metadata and vocabulary used in HTML websites and
  RSS feeds, XML elements and RDFa content authoring, REST APIs,
  mail and SEO. Supported formats include RDFa, Microdata, and
  JSON-LD. Apart from [ISBNs] for [books] or [GTIN] codes other
  [identifiers] like the [serialNumber] property or [productID]
  can be used. While the default for WooCommerce is [SKU] – the
  Stock Keeping Unit – this will be overwritten by the GTIN property
  in Panda, as GTINs unlike SKUs are standardized and (EU) regulated.
  Both SKUs and GTINs (ISBNs/EANs/UCCs) are represented in scannable
  barcodes used for POS sales, for B2B (re)ordering and for inventory
  control.

  GTIN-13 consists of a 3 digits GS1 prefix identifying the country
  of origin (of the manufacturer, not of the product), the
  manufacturer code, and the product code, followed by a check
  digit that works as checksum to verify correct scanning of barcodes.
  A book's GTIN or ISBN regardless of the place of publication always
  starts with the country code 978 or 979, sometimes called bookland.
  Thus, such a GTIN-13/EAN-13 is also referred as Bookland EAN.
  To exchange product data we may use a data pool from this [GS1 list].

  Participating manufacturers have a GLN or Global Location Number.
  GLNs and the corresponding GTINs can be verified using the [GEPIR]
  service.

[EDI]: https://www.gs1.org/standards/edi "Electronic Data Interchange"
[ISBNs]: https://schema.org/isbn "isbn – schema.org Property"
[books]: https://schema.org/Book "Book – schema.org Type"
[GTIN]: https://schema.org/gtin "gtin – schema.org Property"
[identifiers]: https://schema.org/identifier "identifier – schema.org Property"
[serialNumber]: https://schema.org/serialNumber "serialNumber – schema.org Property"
[productID]: https://schema.org/productID "productID – schema.org Property"
[SKU]: https://schema.org/sku "sku – schema.org Property"
[GS1 list]: https://www.gs1.org/services/gdsn/certified-data-pools-list "Certified data pool list"
[GEPIR]: https://gepir.gs1.org "Global Electronic Party Information Registry"
