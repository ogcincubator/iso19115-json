
# Prior BP (Schema)

`ogc.metacat.iso19115.bp17-084` *v1.0*

This is a building block based on OGC 17-084 EO Collection GeoJSON(-LD) Encoding. 

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Refactoring to use standard building blocks

This Building Block documents the proposal in "EO Collection GeoJSON(-LD) Encoding"

The schemas have been updated to be consistent with current JSON schema drafts ( from draft-04)

Normative schemas for OGC FG-JSON have been used to replace copies of GeoJSON elements.

The original examples are referenced for testing purposes.

The JSON-LD context file is copied in situ and should be refactored to remove references to component building block elements.


## Examples

### Landsat example from BP 17-084.
original example
#### json
```json
{

	"type": "Feature",
	"id": "http://fedeo.esa.int/opensearch/request/?httpAccept=application/geo%2Bjson&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC",
	"geometry": {
		"type": "Polygon",
		"coordinates": [
			[
				[
					-180,
					-90
				],
				[
					180,
					-90
				],
				[
					180,
					90
				],
				[
					-180,
					90
				],
				[
					-180,
					-90
				]
			]
		]
	},
	"properties": {
		"title": "LANDSAT 7 ETM+ (Enhanced Thematic Mapper Plus) Geolocated Terrain Corrected Systematic processing (LANDSAT.ETM.GTC)",
		"kind": "http://purl.org/dc/dcmitype/Collection",
		"identifier": "LANDSAT.ETM.GTC",
		"abstract": "This dataset contains all the Landsat 7 Enhanced Thematic Mapper high-quality ortho-rectified L1T dataset over Kiruna, Maspalomas and Matera visibility masks. The Landsat 7 ETM+ scenes typically covers 185 x 170 km. A standard full scene is nominally centred on the intersection between a Path and Row (the actual image centre can vary by up to 100m). Each band requires 50MB (uncompressed), and Band 8 requires 200MB (panchromatic band with resolution of 15m opposed to 30m).",
		"date": "1999-07-01T00:00:00Z/2003-12-31T00:00:00Z",
		"updated": "2003-12-31T00:00:00Z",
		"temporal": {
			"beginningDateTime": "1999-07-01T00:00:00Z",
			"endingDateTime": "2003-12-31T00:00:00Z"
		},
		"isPrimaryTopicOf": {
			"type": "CatalogRecord",
			"updated": "2019-07-17T00:00:00Z",
			"published": "1999-07-01T00:00:00Z",
			"lang": "en"
		},
		"categories": [
			{
				"term": "http://www.eionet.europa.eu/gemet/concept/3650",
				"label": "Geology"
			},
			{
				"term": "http://gcmdservices.gsfc.nasa.gov/kms/concept/03f0c0a3-04a7-4ef8-8ec0-3c2266510815",
				"label": "Science Keywords > Earth Science > Spectral/Engineering > Visible Wavelengths > Visible Imagery"
			},
			{
				"term": "http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4",
				"label": "LANDSAT-7"
			}
		],
		"offerings": [
			{
				"code": "http://www.opengis.net/spec/owc-geojson/1.0/req/wps",
				"operations": [
					{
						"code": "Execute",
						"method": "POST",
						"href": "http://185.52.193.7/wps-proxy/"
					}
				]
			},
			{
				"code": "http://www.opengis.net/spec/owc-geojson/1.0/req/wcs",
				"operations": [
					{
						"code": "GetCapabilities",
						"method": "GET",
						"href": "http://131.176.196.55/wcs?service=WCS&Request=GetCapabilities"
					},
					{
						"code": "DescribeCoverage",
						"method": "GET",
						"type": "application/xml",
						"href": "http://131.176.196.55/wcs?service=WCS&Request=DescribeCoverage&version=2.0.0&CoverageId=LE7_RGB"
					}
				]
			}
		],
		"license": [
			{
				"type": "LicenseDocument",
				"label": "Fast Registration with immediate access Data is available via EOLI-SA upon registration for the On The Fly Service. For information on access and use of the On-The-Fly service please refer to the OTF FAQ page and news of 28 July 2016."
			}
		],
		"accessRights": [
			{
				"type": "RightsStatement",
				"label": "Utilisation of this data is subject to ESA's Earth Observation Terms and Conditions"
			}
		],
		"links": {
			"profiles": [
				{
					"href": "http://www.opengis.net/spec/owc-geojson/1.0/req/core"
				},
				{
					"href": "http://www.opengis.net/spec/eoc-geojson/1.0/req/core"
				}
			],
			"alternates": [
				{
					"href": "http://fedeo.esa.int/opensearch/request/?httpAccept=application/atom%2Bxml&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC&recordSchema=server-choice",
					"type": "application/atom+xml",
					"title": "Atom format"
				},
				{
					"href": "http://fedeo.esa.int/opensearch/request/?httpAccept=application/vnd.iso.19139-2%2Bxml&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC&recordSchema=iso19139-2",
					"type": "application/vnd.iso.19139-2+xml",
					"title": "ISO 19139-2 metadata"
				}
			],
			"describedby": [
				{
					"href": "https://earth.esa.int/web/guest/data-access/browse-data-products/-/asset_publisher/y8Qb/content/landsat-7-etm-enhanced-thematic-mapper-plus-geolocated-terrain-corrected-systematic-processing-over-kiruna-and-masplomas",
					"type": "text/html",
					"title": "Described by"
				}
			],
			"search": [
				{
					"href": "http://fedeo.esa.int/opensearch/description.xml?parentIdentifier=LANDSAT.ETM.GTC&sensorType=OPTICAL&startDate=1999-07-01T00:00:00Z&endDate=2003-12-31T00:00:00Z",
					"type": "application/opensearchdescription+xml"
				}
			],
			"previews": [
				{
					"href": "http://fedeo.esa.int/opensearch/images/esa.png",
					"type": "image/png",
					"title": "Quicklook"
				}
			]
		},
		"acquisitionInformation": [
			{
				"type": "AcquisitionInformation",
				"platform": {
					"type": "Platform",
					"id": "http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4",
					"platformShortName": "Landsat",
					"platformSerialIdentifier": "7"
				},
				"instrument": {
					"type": "Instrument",
					"id": "http://gcmdservices.gsfc.nasa.gov/kms/concept/4dbe7764-a2ea-4a19-b754-696c35ac3205",
					"instrumentShortName": "ETM",
					"sensorType": "OPTICAL"
				},
				"acquisitionParameters": {
					"beginningDateTime": "1999-07-01T00:00:00Z",
					"endingDateTime": "2003-12-31T00:00:00Z"
				}
			}
		]
	}
}
```

#### jsonld
```jsonld
{
  "@context": [
    {
      "mynamespace": "http://example.com/mythings/"
    },
    "https://ogcincubator.github.io/iso19115-json/build/annotated/metacat/iso19115/bp17-084/context.jsonld"
  ],
  "type": "Feature",
  "id": "http://fedeo.esa.int/opensearch/request/?httpAccept=application/geo%2Bjson&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC",
  "geometry": {
    "type": "Polygon",
    "coordinates": [
      [
        [
          -180,
          -90
        ],
        [
          180,
          -90
        ],
        [
          180,
          90
        ],
        [
          -180,
          90
        ],
        [
          -180,
          -90
        ]
      ]
    ]
  },
  "properties": {
    "title": "LANDSAT 7 ETM+ (Enhanced Thematic Mapper Plus) Geolocated Terrain Corrected Systematic processing (LANDSAT.ETM.GTC)",
    "kind": "http://purl.org/dc/dcmitype/Collection",
    "identifier": "LANDSAT.ETM.GTC",
    "abstract": "This dataset contains all the Landsat 7 Enhanced Thematic Mapper high-quality ortho-rectified L1T dataset over Kiruna, Maspalomas and Matera visibility masks. The Landsat 7 ETM+ scenes typically covers 185 x 170 km. A standard full scene is nominally centred on the intersection between a Path and Row (the actual image centre can vary by up to 100m). Each band requires 50MB (uncompressed), and Band 8 requires 200MB (panchromatic band with resolution of 15m opposed to 30m).",
    "date": "1999-07-01T00:00:00Z/2003-12-31T00:00:00Z",
    "updated": "2003-12-31T00:00:00Z",
    "temporal": {
      "beginningDateTime": "1999-07-01T00:00:00Z",
      "endingDateTime": "2003-12-31T00:00:00Z"
    },
    "isPrimaryTopicOf": {
      "type": "CatalogRecord",
      "updated": "2019-07-17T00:00:00Z",
      "published": "1999-07-01T00:00:00Z",
      "lang": "en"
    },
    "categories": [
      {
        "term": "http://www.eionet.europa.eu/gemet/concept/3650",
        "label": "Geology"
      },
      {
        "term": "http://gcmdservices.gsfc.nasa.gov/kms/concept/03f0c0a3-04a7-4ef8-8ec0-3c2266510815",
        "label": "Science Keywords > Earth Science > Spectral/Engineering > Visible Wavelengths > Visible Imagery"
      },
      {
        "term": "http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4",
        "label": "LANDSAT-7"
      }
    ],
    "offerings": [
      {
        "code": "http://www.opengis.net/spec/owc-geojson/1.0/req/wps",
        "operations": [
          {
            "code": "Execute",
            "method": "POST",
            "href": "http://185.52.193.7/wps-proxy/"
          }
        ]
      },
      {
        "code": "http://www.opengis.net/spec/owc-geojson/1.0/req/wcs",
        "operations": [
          {
            "code": "GetCapabilities",
            "method": "GET",
            "href": "http://131.176.196.55/wcs?service=WCS&Request=GetCapabilities"
          },
          {
            "code": "DescribeCoverage",
            "method": "GET",
            "type": "application/xml",
            "href": "http://131.176.196.55/wcs?service=WCS&Request=DescribeCoverage&version=2.0.0&CoverageId=LE7_RGB"
          }
        ]
      }
    ],
    "license": [
      {
        "type": "LicenseDocument",
        "label": "Fast Registration with immediate access Data is available via EOLI-SA upon registration for the On The Fly Service. For information on access and use of the On-The-Fly service please refer to the OTF FAQ page and news of 28 July 2016."
      }
    ],
    "accessRights": [
      {
        "type": "RightsStatement",
        "label": "Utilisation of this data is subject to ESA's Earth Observation Terms and Conditions"
      }
    ],
    "links": {
      "profiles": [
        {
          "href": "http://www.opengis.net/spec/owc-geojson/1.0/req/core"
        },
        {
          "href": "http://www.opengis.net/spec/eoc-geojson/1.0/req/core"
        }
      ],
      "alternates": [
        {
          "href": "http://fedeo.esa.int/opensearch/request/?httpAccept=application/atom%2Bxml&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC&recordSchema=server-choice",
          "type": "application/atom+xml",
          "title": "Atom format"
        },
        {
          "href": "http://fedeo.esa.int/opensearch/request/?httpAccept=application/vnd.iso.19139-2%2Bxml&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC&recordSchema=iso19139-2",
          "type": "application/vnd.iso.19139-2+xml",
          "title": "ISO 19139-2 metadata"
        }
      ],
      "describedby": [
        {
          "href": "https://earth.esa.int/web/guest/data-access/browse-data-products/-/asset_publisher/y8Qb/content/landsat-7-etm-enhanced-thematic-mapper-plus-geolocated-terrain-corrected-systematic-processing-over-kiruna-and-masplomas",
          "type": "text/html",
          "title": "Described by"
        }
      ],
      "search": [
        {
          "href": "http://fedeo.esa.int/opensearch/description.xml?parentIdentifier=LANDSAT.ETM.GTC&sensorType=OPTICAL&startDate=1999-07-01T00:00:00Z&endDate=2003-12-31T00:00:00Z",
          "type": "application/opensearchdescription+xml"
        }
      ],
      "previews": [
        {
          "href": "http://fedeo.esa.int/opensearch/images/esa.png",
          "type": "image/png",
          "title": "Quicklook"
        }
      ]
    },
    "acquisitionInformation": [
      {
        "type": "AcquisitionInformation",
        "platform": {
          "type": "Platform",
          "id": "http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4",
          "platformShortName": "Landsat",
          "platformSerialIdentifier": "7"
        },
        "instrument": {
          "type": "Instrument",
          "id": "http://gcmdservices.gsfc.nasa.gov/kms/concept/4dbe7764-a2ea-4a19-b754-696c35ac3205",
          "instrumentShortName": "ETM",
          "sensorType": "OPTICAL"
        },
        "acquisitionParameters": {
          "beginningDateTime": "1999-07-01T00:00:00Z",
          "endingDateTime": "2003-12-31T00:00:00Z"
        }
      }
    ]
  }
}
```

#### ttl
```ttl
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix dcmitype: <http://purl.org/dc/dcmitype/> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix eop: <http://www.opengis.net/ont/eo-geojson/1.0/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix gj: <https://purl.org/geojson/vocab#> .
@prefix owc: <http://www.opengis.net/ont/owc/1.0/> .
@prefix prov: <http://www.w3.org/ns/prov#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://fedeo.esa.int/opensearch/request/?httpAccept=application/geo%2Bjson&parentIdentifier=EOP%3AESA%3AFEDEO%3ACOLLECTIONS&uid=LANDSAT.ETM.GTC> a gj:Feature ;
    dct:accessRights [ a dct:RightsStatement ;
            rdfs:label "Utilisation of this data is subject to ESA's Earth Observation Terms and Conditions" ] ;
    dct:date "1999-07-01T00:00:00Z/2003-12-31T00:00:00Z" ;
    dct:description "This dataset contains all the Landsat 7 Enhanced Thematic Mapper high-quality ortho-rectified L1T dataset over Kiruna, Maspalomas and Matera visibility masks. The Landsat 7 ETM+ scenes typically covers 185 x 170 km. A standard full scene is nominally centred on the intersection between a Path and Row (the actual image centre can vary by up to 100m). Each band requires 50MB (uncompressed), and Band 8 requires 200MB (panchromatic band with resolution of 15m opposed to 30m)." ;
    dct:identifier "LANDSAT.ETM.GTC" ;
    dct:license [ a dct:LicenseDocument ;
            rdfs:label "Fast Registration with immediate access Data is available via EOLI-SA upon registration for the On The Fly Service. For information on access and use of the On-The-Fly service please refer to the OTF FAQ page and news of 28 July 2016." ] ;
    dct:modified "2003-12-31T00:00:00Z" ;
    dct:temporal [ dcat:endDate "2003-12-31T00:00:00Z" ;
            dcat:startDate "1999-07-01T00:00:00Z" ] ;
    dct:title "LANDSAT 7 ETM+ (Enhanced Thematic Mapper Plus) Geolocated Terrain Corrected Systematic processing (LANDSAT.ETM.GTC)" ;
    dct:type dcmitype:Collection ;
    owc:links [ ] ;
    dcat:endpointDescription [ owc:code <http://www.opengis.net/spec/owc-geojson/1.0/req/wcs> ;
            owc:operations [ owc:code <file:///github/workspace/GetCapabilities> ;
                    owc:href "http://131.176.196.55/wcs?service=WCS&Request=GetCapabilities" ;
                    owc:method "GET" ],
                [ owc:code <file:///github/workspace/DescribeCoverage> ;
                    owc:href "http://131.176.196.55/wcs?service=WCS&Request=DescribeCoverage&version=2.0.0&CoverageId=LE7_RGB" ;
                    owc:method "GET" ;
                    owc:type "application/xml" ] ],
        [ owc:code <http://www.opengis.net/spec/owc-geojson/1.0/req/wps> ;
            owc:operations [ owc:code <file:///github/workspace/Execute> ;
                    owc:href "http://185.52.193.7/wps-proxy/" ;
                    owc:method "POST" ] ] ;
    dcat:theme <http://gcmdservices.gsfc.nasa.gov/kms/concept/03f0c0a3-04a7-4ef8-8ec0-3c2266510815>,
        <http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4>,
        <http://www.eionet.europa.eu/gemet/concept/3650> ;
    prov:wasGeneratedBy [ a <file:///github/workspace/AcquisitionInformation> ;
            dcat:endDate "2003-12-31T00:00:00Z" ;
            dcat:startDate "1999-07-01T00:00:00Z" ;
            prov:used [ eop:id "http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4" ;
                    eop:platformSerialIdentifier "7" ;
                    eop:platformShortName "Landsat" ;
                    eop:type "Platform" ],
                [ eop:id "http://gcmdservices.gsfc.nasa.gov/kms/concept/4dbe7764-a2ea-4a19-b754-696c35ac3205" ;
                    eop:instrumentShortName "ETM" ;
                    eop:sensorType eop:OPTICAL ;
                    eop:type "Instrument" ] ] ;
    foaf:isPrimaryTopicOf [ a dcat:CatalogRecord ;
            dct:issued "1999-07-01T00:00:00Z" ;
            dct:language <http://id.loc.gov/vocabulary/iso639-1/en> ;
            dct:modified "2019-07-17T00:00:00Z" ] ;
    gj:geometry [ a gj:Polygon ;
            gj:coordinates ( ( ( -180 -90 ) ( 180 -90 ) ( 180 90 ) ( -180 90 ) ( -180 -90 ) ) ) ] .

<http://gcmdservices.gsfc.nasa.gov/kms/concept/03f0c0a3-04a7-4ef8-8ec0-3c2266510815> skos:prefLabel "Science Keywords > Earth Science > Spectral/Engineering > Visible Wavelengths > Visible Imagery" .

<http://gcmdservices.gsfc.nasa.gov/kms/concept/c7a09e9f-3c99-4b31-a521-313c379ba2b4> skos:prefLabel "LANDSAT-7" .

<http://www.eionet.europa.eu/gemet/concept/3650> skos:prefLabel "Geology" .


```

## Schema

```yaml
title: GeoJSON encoding of EO Collection metadata
description: 'Definition of document with EO Collection metadata in GeoJSON encoding.  Note
  that numbers in the instance should not be surrounded by double-quotes to validate
  against this schema. '
allOf:
- $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/json-fg/feature-lenient/schema.yaml
- properties:
    properties:
      $ref: '#/$defs/Properties'
      x-jsonld-id: '@nest'
$defs:
  LinkOGC:
    $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/ogc-utils/json-link/schema.yaml
  Link:
    description: OGC 14-055r2
    type: object
    properties:
      href:
        type: string
        format: uri
        x-jsonld-id: '@id'
      type:
        description: MIME type
        type: string
        x-jsonld-id: '@type'
      title:
        type: string
        x-jsonld-id: http://purl.org/dc/terms/title
      length:
        type: integer
        minimum: 0
        x-jsonld-id: http://www.w3.org/2005/Atom/length
      lang:
        description: RFC-3066
        type: string
        x-jsonld-id: http://purl.org/dc/terms/language
        x-jsonld-type: '@id'
        x-jsonld-base: http://id.loc.gov/vocabulary/iso639-1/
    required:
    - href
  Links:
    title: Links
    description: OGC 14-055r2
    type: object
    properties:
      type:
        type: string
        enum:
        - Links
        x-jsonld-id: '@type'
    patternProperties:
      ^(profiles|alternates|via|previews)$:
        description: OGC 14-055r2
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Link'
      ^(search|describedby|related)$:
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Link'
    additionalProperties:
      type: array
      minItems: 1
      items:
        $ref: '#/$defs/Link'
  Properties:
    title: Properties
    type: object
    allOf:
    - type: object
      properties:
        type:
          type: string
          enum:
          - Properties
          x-jsonld-id: '@type'
        isPrimaryTopicOf:
          $ref: '#/$defs/MetadataInformation'
          x-jsonld-id: http://xmlns.com/foaf/0.1/isPrimaryTopicOf
        temporal:
          $ref: '#/$defs/TemporalExtent'
          x-jsonld-id: http://purl.org/dc/terms/temporal
        spatial:
          $ref: '#/$defs/Location'
          x-jsonld-id: http://purl.org/dc/terms/spatial
        acquisitionInformation:
          description: OGC 17-003
          type: array
          items:
            $ref: '#/$defs/AcquisitionInformation'
          x-jsonld-id: http://www.w3.org/ns/prov#wasGeneratedBy
        productInformation:
          $ref: '#/$defs/ProductInformation'
          x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/productInformation
    - $ref: '#/$defs/DataIdentification'
    - $ref: '#/$defs/DescriptiveKeywords'
    - $ref: '#/$defs/RelatedUrl'
  Offering:
    title: Offering
    description: Offering as defined in OGC 14-055r2
    type: object
    properties:
      code:
        type: string
        format: uri
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/code
        x-jsonld-type: '@id'
      operations:
        type: array
        items:
          $ref: '#/$defs/Operation'
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/operations
      contents:
        type: array
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/contents
      styles:
        type: array
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/styles
    required:
    - code
  Operation:
    description: OGC 14-055r2
    type: object
    properties:
      code:
        type: string
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/code
        x-jsonld-type: '@id'
      method:
        type: string
        enum:
        - GET
        - POST
        - PUT
        - HEAD
        - PATCH
        - DELETE
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/method
      type:
        description: Media type
        type: string
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/type
      href:
        type: string
        format: uri
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/href
      request:
        type: object
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/request
      result:
        type: object
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/result
    required:
    - code
    - method
    - href
  Agent:
    description: vcard:Kind, foaf:Agent subset. OGC 14-055r2.
    type: object
    minProperties: 1
    properties:
      type:
        type: string
        enum:
        - Individual
        - Kind
        - Person
        - Organization
        - Agent
        x-jsonld-id: http://xmlns.com/foaf/0.1/type
      name:
        type: string
        x-jsonld-id: http://xmlns.com/foaf/0.1/name
      email:
        type: string
        format: email
        x-jsonld-id: http://xmlns.com/foaf/0.1/mbox
      uri:
        type: string
        format: uri
        x-jsonld-id: http://xmlns.com/foaf/0.1/page
        x-jsonld-type: '@id'
  Category:
    description: "OGC 14-055r2 \xA77.1.1.15"
    type: object
    properties:
      type:
        type: string
        enum:
        - Category
        x-jsonld-id: '@type'
      scheme:
        type: string
        format: uri
        x-jsonld-id: http://www.w3.org/2004/02/skos/core#inScheme
      term:
        type: string
        x-jsonld-id: '@id'
      label:
        type: string
        x-jsonld-id: http://www.w3.org/2004/02/skos/core#prefLabel
    required:
    - term
    additionalProperties: false
  DescriptiveKeywords:
    type: object
    properties:
      subject:
        description: Topic category
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Category'
        x-jsonld-id: http://purl.org/dc/terms/subject
      categories:
        description: OGC 14-055r2 - Keywords associated with a controlled vocabulary.
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Category'
        x-jsonld-id: http://www.w3.org/ns/dcat#theme
      keyword:
        description: Keywords not associated with a controlled vocabulary.
        type: array
        minItems: 1
        items:
          type: string
          minLength: 1
        x-jsonld-id: http://www.w3.org/ns/dcat#keyword
  DataContact:
    type: object
    properties:
      publisher:
        description: role="publisher" (OGC 14-055r2)
        type: string
      authors:
        description: role="creator" (OGC 14-055r2)
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Agent'
        x-jsonld-id: http://purl.org/dc/terms/creator
      contactPoint:
        description: Role="contact point"
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Agent'
        x-jsonld-id: http://www.w3.org/ns/dcat#contactPoint
      qualifiedAttribution:
        description: Role=other
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Attribution'
        x-jsonld-id: http://www.w3.org/ns/prov#qualifiedAttribution
  MetadataInformation:
    description: dcat:CatalogRecord
    type: object
    properties:
      type:
        description: dcat:CatalogRecord
        type: string
        enum:
        - CatalogRecord
        x-jsonld-id: '@type'
      created:
        description: dct:created
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/created
      published:
        description: dct:issued
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/issued
      updated:
        description: dct:modified
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/modified
      lang:
        description: dct:language
        type: string
        x-jsonld-id: http://purl.org/dc/terms/language
        x-jsonld-type: '@id'
        x-jsonld-base: http://id.loc.gov/vocabulary/iso639-1/
      conformsTo:
        $ref: '#/$defs/Standard'
        x-jsonld-id: http://purl.org/dc/terms/conformsTo
  DataIdentification:
    type: object
    allOf:
    - type: object
      properties:
        kind:
          description: dct:type
          type: string
          format: uri
          x-jsonld-id: http://purl.org/dc/terms/type
          x-jsonld-type: '@id'
        title:
          description: dct:title - OGC 14-055r2
          type: string
          x-jsonld-id: http://purl.org/dc/terms/title
        identifier:
          type: string
          x-jsonld-id: http://purl.org/dc/terms/identifier
        bibliographicCitation:
          description: dct:bibliographicCitation
          type: string
          x-jsonld-id: http://purl.org/dc/terms/bibliographicCitation
        abstract:
          description: dct:description - OGC 14-055r2
          type: string
          x-jsonld-id: http://purl.org/dc/terms/description
        provenance:
          description: dct:ProvenanceStatement
          type: array
          minItems: 1
          items:
            $ref: '#/$defs/ProvenanceStatement'
          x-jsonld-id: http://purl.org/dc/terms/provenance
        wasUsedBy:
          description: prov:Activity
          type: array
          minItems: 1
          items:
            $ref: '#/$defs/Activity'
          x-jsonld-id: http://www.w3.org/ns/prov#wasUsedBy
        doi:
          description: adms:identifier
          type: string
          x-jsonld-id: http://www.w3.org/ns/adms#identifier
          x-jsonld-type: '@id'
          x-jsonld-base: https://doi.org/
        versionInfo:
          description: owl:versionInfo
          type: string
          x-jsonld-id: http://www.w3.org/2002/07/owl#versionInfo
        versionNotes:
          description: adms:versionNotes
          type: string
          x-jsonld-id: http://www.w3.org/ns/adms#versionNotes
      required:
      - title
      - identifier
    - $ref: '#/$defs/DataContact'
    - $ref: '#/$defs/ResourceConstraints'
    - $ref: '#/$defs/DataDates'
  Attribution:
    description: prov:Attribution
    type: object
    properties:
      type:
        type: string
        enum:
        - Attribution
        x-jsonld-id: http://www.w3.org/2006/vcard/ns#type
      role:
        description: ResponsibleParty role
        type: string
        enum:
        - resourceProvider
        - custodian
        - owner
        - user
        - distributor
        - originator
        - pointOfContact
        - principalInvestigator
        - processor
        - publisher
        - author
        x-jsonld-id: http://purl.org/dc/terms/type
        x-jsonld-type: '@id'
        x-jsonld-base: http://inspire.ec.europa.eu/metadata-codelist/ResponsiblePartyRole/
      agent:
        type: array
        items:
          $ref: '#/$defs/Agent'
        x-jsonld-id: http://www.w3.org/ns/prov#agent
    required:
    - role
    - agent
  AcquisitionParameters:
    type: object
    allOf:
    - $ref: '#/$defs/TemporalExtent'
  TemporalExtent:
    type: object
    properties:
      type:
        type: string
        enum:
        - PeriodOfTime
        x-jsonld-id: '@type'
      beginningDateTime:
        type: string
        format: date-time
        x-jsonld-id: http://www.w3.org/ns/dcat#startDate
      endingDateTime:
        type: string
        format: date-time
        x-jsonld-id: http://www.w3.org/ns/dcat#endDate
  AcquisitionInformation:
    type: object
    properties:
      type:
        type: string
        enum:
        - AcquisitionInformation
        x-jsonld-id: '@type'
      platform:
        $ref: '#/$defs/Platform'
        x-jsonld-id: http://www.w3.org/ns/prov#used
      instrument:
        $ref: '#/$defs/Instrument'
        x-jsonld-id: http://www.w3.org/ns/prov#used
      acquisitionParameters:
        $ref: '#/$defs/TemporalExtent'
        x-jsonld-id: '@nest'
  Platform:
    type: object
    minProperties: 1
    properties:
      type:
        type: string
        enum:
        - Platform
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/type
      id:
        type: string
        format: uri
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/id
      platformShortName:
        type: string
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/platformShortName
      platformSerialIdentifier:
        type: string
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/platformSerialIdentifier
      orbitType:
        type: string
        enum:
        - GEO
        - LEO
        x-jsonld-type: '@id'
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/orbitType
        x-jsonld-base: http://www.opengis.net/ont/eo-geojson/1.0/
    required:
    - platformShortName
    additionalProperties: false
  Instrument:
    type: object
    properties:
      type:
        type: string
        enum:
        - Instrument
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/type
      id:
        type: string
        format: uri
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/id
      sensorType:
        type: string
        enum:
        - OPTICAL
        - RADAR
        - ATMOSPHERIC
        - ALTIMETRIC
        - LIMB
        x-jsonld-type: '@id'
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/sensorType
        x-jsonld-base: http://www.opengis.net/ont/eo-geojson/1.0/
      instrumentShortName:
        type: string
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/instrumentShortName
      description:
        type: string
        x-jsonld-id: http://purl.org/dc/terms/description
    required:
    - instrumentShortName
    additionalProperties: false
  ProductInformation:
    description: OGC 17-003
    type: object
    properties:
      type:
        type: string
        enum:
        - ProductInformation
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/type
      processingLevel:
        description: eop:processingLevel - OGC 17-003
        type: string
        enum:
        - 1A
        - 1B
        - 1C
        - '2'
        - '3'
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/processingLevel
      productType:
        description: eop:productType - OGC 17-003
        type: array
        items:
          type: string
          minLength: 1
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/productType
      resolution:
        type: array
        minItems: 1
        items:
          type: number
          minimum: 0
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/resolution
      referenceSystemIdentifier:
        type: string
        x-jsonld-type: '@id'
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/referenceSystemIdentifier
      timeliness:
        description: eop:timeliness - OGC 17-003
        type: string
        x-jsonld-id: http://www.opengis.net/ont/eo-geojson/1.0/timeliness
  RelatedUrl:
    type: object
    properties:
      links:
        $ref: '#/$defs/Links'
        x-jsonld-id: http://www.opengis.net/ont/owc/1.0/links
      offerings:
        description: OGC 14-055r2
        type: array
        minItems: 1
        items:
          $ref: '#/$defs/Offering'
        x-jsonld-id: http://www.w3.org/ns/dcat#endpointDescription
    required:
    - links
  Location:
    description: dct:Location (alternative representation of geometry).
    type: object
    properties:
      type:
        type: string
        enum:
        - Location
        x-jsonld-id: '@type'
      id:
        type: string
        format: uri
        x-jsonld-id: '@id'
      geometry:
        description: locn:geometry
        type: array
        items:
          description: locn:Geometry
          type: object
          properties:
            type:
              type: string
              x-jsonld-id: '@type'
            value:
              type: string
              x-jsonld-id: '@value'
        x-jsonld-id: http://www.w3.org/ns/locn#geometry
  ResourceConstraints:
    type: object
    properties:
      rights:
        description: "OGC 14-055r2 \xA77.1.2.7"
        type: string
        x-jsonld-id: http://purl.org/dc/terms/rights
      license:
        description: dct:LicenseDocument
        type: array
        items:
          $ref: '#/$defs/LicenseDocument'
        x-jsonld-id: http://purl.org/dc/terms/license
      accessRights:
        description: dct:RightsStatement
        type: array
        items:
          $ref: '#/$defs/RightsStatement'
        x-jsonld-id: http://purl.org/dc/terms/accessRights
  LicenseDocument:
    description: dct:LicenseDocument
    type:
    - object
    - string
    oneOf:
    - type: object
      properties:
        type:
          type: string
          enum:
          - LicenseDocument
          x-jsonld-id: '@type'
        label:
          description: rdfs:label
          type: string
          x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
      required:
      - label
    - description: '@id'
      type: string
      format: uri
  RightsStatement:
    description: dct:RightsStatement
    type:
    - object
    - string
    oneOf:
    - type: object
      properties:
        type:
          type: string
          enum:
          - RightsStatement
          x-jsonld-id: '@type'
        label:
          description: rdfs:label
          type: string
          x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
      required:
      - label
    - description: '@id'
      type: string
      format: uri
  ProvenanceStatement:
    title: dct:provenance
    description: dct:ProvenanceStatement
    type: object
    properties:
      type:
        type: string
        enum:
        - ProvenanceStatement
        x-jsonld-id: '@type'
      label:
        description: rdfs:label
        type: string
        x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
    required:
    - label
  Activity:
    description: prov:Activity
    type: object
    properties:
      type:
        type: string
        enum:
        - Activity
        x-jsonld-id: '@type'
      generated:
        $ref: '#/$defs/Entity'
        x-jsonld-id: http://www.w3.org/ns/prov#generated
      qualifiedAssociation:
        $ref: '#/$defs/Association'
        x-jsonld-id: http://www.w3.org/ns/prov#qualifiedAssociation
    required:
    - generated
    - qualifiedAssociation
  Entity:
    description: prov:Entity
    type: object
    properties:
      type:
        type: string
        enum:
        - Entity
        x-jsonld-id: '@type'
      degree:
        type: string
        format: uri
        x-jsonld-id: http://purl.org/dc/terms/type
        x-jsonld-type: '@id'
      description:
        type: string
        x-jsonld-id: http://purl.org/dc/terms/description
    required:
    - degree
  Association:
    description: prov:Association
    type: object
    properties:
      type:
        type: string
        enum:
        - Association
        x-jsonld-id: '@type'
      hadPlan:
        $ref: '#/$defs/Plan'
        x-jsonld-id: http://www.w3.org/ns/prov#hadPlan
    required:
    - hadPlan
  Plan:
    description: prov:Plan
    type: object
    properties:
      type:
        type: string
        enum:
        - Plan
        x-jsonld-id: '@type'
      wasDerivedFrom:
        $ref: '#/$defs/Standard'
        x-jsonld-id: http://www.w3.org/ns/prov#wasDerivedFrom
    required:
    - wasDerivedFrom
  Standard:
    description: dct:Standard
    type: object
    properties:
      type:
        type: string
        enum:
        - Standard
        x-jsonld-id: '@type'
      title:
        description: dct:title
        type: string
        x-jsonld-id: http://purl.org/dc/terms/title
      issued:
        description: dct:issued
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/issued
      versionInfo:
        description: owl:versionInfo
        type: string
        x-jsonld-id: http://www.w3.org/2002/07/owl#versionInfo
    required:
    - title
  DataDates:
    type: object
    properties:
      created:
        description: dct:created
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/created
      published:
        description: dct:issued
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/issued
      updated:
        description: dct:modified
        type: string
        format: date-time
        x-jsonld-id: http://purl.org/dc/terms/modified
      date:
        description: dct:date - OGC 14-055r2
        type: string
        x-jsonld-id: http://purl.org/dc/terms/date
    required:
    - updated
x-jsonld-extra-terms:
  LicenseDocument: http://purl.org/dc/terms/LicenseDocument
  RightsStatement: http://purl.org/dc/terms/RightsStatement
  ProvenanceStatement: http://purl.org/dc/terms/ProvenanceStatement
  Activity: http://www.w3.org/ns/prov#Activity
  Association: http://www.w3.org/ns/prov#Association
  Entity: http://www.w3.org/ns/prov#Entity
  Plan: http://www.w3.org/ns/prov#Plan
  Standard: http://purl.org/dc/terms/Standard
  CatalogRecord: http://www.w3.org/ns/dcat#CatalogRecord
  creator: http://purl.org/dc/terms/creator
  subtitle: http://purl.org/dc/terms/description
  Location: http://purl.org/dc/terms/Location
  PeriodOfType: http://purl.org/dc/terms/PeriodOfTime
  distribution:
    x-jsonld-id: http://www.w3.org/ns/dcat#distribution
    x-jsonld-context:
      label: http://www.w3.org/2000/01/rdf-schema#label
  Distribution: http://www.w3.org/ns/dcat#Distribution
  Links: http://www.opengis.net/ont/owc/1.0/Links
  Link: http://www.w3.org/2005/Atom/link
  Category: http://www.w3.org/2004/02/skos/core#Concept
  hasGeometry: http://www.opengis.net/ont/geosparql#hasGeometry
  asWKT: http://www.opengis.net/ont/geosparql#asWKT
  Feature: http://www.w3.org/ns/dcat#Dataset
  FeatureCollection: https://purl.org/geojson/vocab#FeatureCollection
  GeometryCollection: https://purl.org/geojson/vocab#GeometryCollection
  LineString: https://purl.org/geojson/vocab#LineString
  MultiLineString: https://purl.org/geojson/vocab#MultiLineString
  MultiPoint: https://purl.org/geojson/vocab#MultiPoint
  MultiPolygon: https://purl.org/geojson/vocab#MultiPolygon
  Point: https://purl.org/geojson/vocab#Point
  Polygon: https://purl.org/geojson/vocab#Polygon
  bbox:
    x-jsonld-container: '@list'
    x-jsonld-id: https://purl.org/geojson/vocab#bbox
  coordinates:
    x-jsonld-container: '@list'
    x-jsonld-id: https://purl.org/geojson/vocab#coordinates
  features:
    x-jsonld-container: '@set'
    x-jsonld-id: https://purl.org/geojson/vocab#features
  Platform: http://www.opengis.net/ont/eo-geojson/1.0/Platform
  Instrument: http://www.opengis.net/ont/eo-geojson/1.0/Instrument
  ProductInformation: http://www.opengis.net/ont/eo-geojson/1.0/ProductInformation
x-jsonld-prefixes:
  dct: http://purl.org/dc/terms/
  rdfs: http://www.w3.org/2000/01/rdf-schema#
  prov: http://www.w3.org/ns/prov#
  adms: http://www.w3.org/ns/adms#
  foaf: http://xmlns.com/foaf/0.1/
  dcat: http://www.w3.org/ns/dcat#
  owl: http://www.w3.org/2002/07/owl#
  gj: https://purl.org/geojson/vocab#
  locn: http://www.w3.org/ns/locn#
  owc: http://www.opengis.net/ont/owc/1.0/
  atom: http://www.w3.org/2005/Atom/
  iana: http://www.iana.org/assignments/relation/
  skos: http://www.w3.org/2004/02/skos/core#
  gsp: http://www.opengis.net/ont/geosparql#
  eop: http://www.opengis.net/ont/eo-geojson/1.0/
  vcard: http://www.w3.org/2006/vcard/ns#
  os: http://a9.com/-/spec/opensearch/1.1/
  xsd: http://www.w3.org/2001/XMLSchema#
  schema: http://schema.org/

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/iso19115-json/build/annotated/metacat/iso19115/bp17-084/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/iso19115-json/build/annotated/metacat/iso19115/bp17-084/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": "@type",
    "id": "@id",
    "properties": "@nest",
    "geometry": "geojson:geometry",
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "links": {
      "@context": {
        "href": {
          "@type": "@id",
          "@id": "@id"
        },
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "hreflang": "dct:language",
        "length": "atom:length",
        "lang": {
          "@context": {
            "@base": "http://id.loc.gov/vocabulary/iso639-1/"
          },
          "@id": "dct:language",
          "@type": "@id"
        }
      },
      "@id": "owc:links"
    },
    "featureType": "@type",
    "time": {
      "@context": {
        "date": {
          "@id": "owlTime:hasTime",
          "@type": "xsd:date"
        },
        "timestamp": {
          "@id": "owlTime:hasTime",
          "@type": "xsd:dateTime"
        },
        "interval": {
          "@id": "owlTime:hasTime",
          "@container": "@list"
        }
      },
      "@id": "dct:time"
    },
    "coordRefSys": "http://www.opengis.net/def/glossary/term/CoordinateReferenceSystemCRS",
    "place": "dct:spatial",
    "Polyhedron": "geojson:Polyhedron",
    "MultiPolyhedron": "geojson:MultiPolyhedron",
    "Prism": {
      "@id": "geojson:Prism",
      "@context": {
        "base": "geojson:prismBase",
        "lower": "geojson:prismLower",
        "upper": "geojson:prismUpper"
      }
    },
    "MultiPrism": {
      "@id": "geojson:MultiPrism",
      "@context": {
        "prisms": "geojson:prisms"
      }
    },
    "coordinates": {
      "@container": "@list",
      "@id": "geojson:coordinates"
    },
    "geometries": {
      "@id": "geojson:geometry",
      "@container": "@list"
    },
    "isPrimaryTopicOf": {
      "@context": {
        "lang": {
          "@context": {
            "@base": "http://id.loc.gov/vocabulary/iso639-1/"
          },
          "@id": "dct:language",
          "@type": "@id"
        },
        "conformsTo": {
          "@context": {
            "issued": "dct:issued"
          },
          "@id": "dct:conformsTo"
        }
      },
      "@id": "foaf:isPrimaryTopicOf"
    },
    "temporal": {
      "@context": {
        "beginningDateTime": "dcat:startDate",
        "endingDateTime": "dcat:endDate"
      },
      "@id": "dct:temporal"
    },
    "spatial": {
      "@context": {
        "geometry": {
          "@context": {
            "value": "@value"
          },
          "@id": "locn:geometry"
        }
      },
      "@id": "dct:spatial"
    },
    "acquisitionInformation": {
      "@context": {
        "platform": {
          "@context": {
            "type": "eop:type",
            "id": "eop:id",
            "platformShortName": "eop:platformShortName",
            "platformSerialIdentifier": "eop:platformSerialIdentifier",
            "orbitType": {
              "@context": {
                "@base": "http://www.opengis.net/ont/eo-geojson/1.0/"
              },
              "@type": "@id",
              "@id": "eop:orbitType"
            }
          },
          "@id": "prov:used"
        },
        "instrument": {
          "@context": {
            "type": "eop:type",
            "id": "eop:id",
            "sensorType": {
              "@context": {
                "@base": "http://www.opengis.net/ont/eo-geojson/1.0/"
              },
              "@type": "@id",
              "@id": "eop:sensorType"
            },
            "instrumentShortName": "eop:instrumentShortName",
            "description": "dct:description"
          },
          "@id": "prov:used"
        },
        "beginningDateTime": "dcat:startDate",
        "endingDateTime": "dcat:endDate",
        "acquisitionParameters": "@nest"
      },
      "@id": "prov:wasGeneratedBy"
    },
    "productInformation": {
      "@context": {
        "type": "eop:type",
        "processingLevel": "eop:processingLevel",
        "productType": "eop:productType",
        "resolution": "eop:resolution",
        "referenceSystemIdentifier": {
          "@type": "@id",
          "@id": "eop:referenceSystemIdentifier"
        },
        "timeliness": "eop:timeliness"
      },
      "@id": "eop:productInformation"
    },
    "kind": {
      "@id": "dct:type",
      "@type": "@id"
    },
    "title": "dct:title",
    "identifier": "dct:identifier",
    "bibliographicCitation": "dct:bibliographicCitation",
    "abstract": "dct:description",
    "provenance": {
      "@context": {
        "label": "rdfs:label"
      },
      "@id": "dct:provenance"
    },
    "wasUsedBy": {
      "@context": {
        "generated": {
          "@context": {
            "degree": {
              "@id": "dct:type",
              "@type": "@id"
            },
            "description": "dct:description"
          },
          "@id": "prov:generated"
        },
        "qualifiedAssociation": {
          "@context": {
            "hadPlan": {
              "@context": {
                "wasDerivedFrom": {
                  "@context": {
                    "issued": "dct:issued"
                  },
                  "@id": "prov:wasDerivedFrom"
                }
              },
              "@id": "prov:hadPlan"
            }
          },
          "@id": "prov:qualifiedAssociation"
        }
      },
      "@id": "prov:wasUsedBy"
    },
    "doi": {
      "@context": {
        "@base": "https://doi.org/"
      },
      "@id": "adms:identifier",
      "@type": "@id"
    },
    "versionInfo": "owl:versionInfo",
    "versionNotes": "adms:versionNotes",
    "authors": {
      "@context": {
        "type": "foaf:type",
        "name": "foaf:name",
        "email": "foaf:mbox",
        "uri": {
          "@id": "foaf:page",
          "@type": "@id"
        }
      },
      "@id": "dct:creator"
    },
    "contactPoint": {
      "@context": {
        "type": "foaf:type",
        "name": "foaf:name",
        "email": "foaf:mbox",
        "uri": {
          "@id": "foaf:page",
          "@type": "@id"
        }
      },
      "@id": "dcat:contactPoint"
    },
    "qualifiedAttribution": {
      "@context": {
        "type": "vcard:type",
        "role": {
          "@context": {
            "@base": "http://inspire.ec.europa.eu/metadata-codelist/ResponsiblePartyRole/"
          },
          "@id": "dct:type",
          "@type": "@id"
        },
        "agent": {
          "@context": {
            "type": "foaf:type",
            "name": "foaf:name",
            "email": "foaf:mbox",
            "uri": {
              "@id": "foaf:page",
              "@type": "@id"
            }
          },
          "@id": "prov:agent"
        }
      },
      "@id": "prov:qualifiedAttribution"
    },
    "rights": "dct:rights",
    "license": {
      "@context": {
        "label": "rdfs:label"
      },
      "@id": "dct:license"
    },
    "accessRights": {
      "@context": {
        "label": "rdfs:label"
      },
      "@id": "dct:accessRights"
    },
    "created": "dct:created",
    "published": "dct:issued",
    "updated": "dct:modified",
    "date": "dct:date",
    "subject": {
      "@context": {
        "scheme": "skos:inScheme",
        "term": "@id",
        "label": "skos:prefLabel"
      },
      "@id": "dct:subject"
    },
    "categories": {
      "@context": {
        "scheme": "skos:inScheme",
        "term": "@id",
        "label": "skos:prefLabel"
      },
      "@id": "dcat:theme"
    },
    "keyword": "dcat:keyword",
    "offerings": {
      "@context": {
        "code": {
          "@id": "owc:code",
          "@type": "@id"
        },
        "operations": {
          "@context": {
            "method": "owc:method",
            "type": "owc:type",
            "href": "owc:href",
            "request": "owc:request",
            "result": "owc:result"
          },
          "@id": "owc:operations"
        },
        "contents": "owc:contents",
        "styles": "owc:styles"
      },
      "@id": "dcat:endpointDescription"
    },
    "LicenseDocument": "dct:LicenseDocument",
    "RightsStatement": "dct:RightsStatement",
    "ProvenanceStatement": "dct:ProvenanceStatement",
    "Activity": "prov:Activity",
    "Association": "prov:Association",
    "Entity": "prov:Entity",
    "Plan": "prov:Plan",
    "Standard": "dct:Standard",
    "CatalogRecord": "dcat:CatalogRecord",
    "creator": "dct:creator",
    "subtitle": "dct:description",
    "Location": "dct:Location",
    "PeriodOfType": "dct:PeriodOfTime",
    "distribution": {
      "@id": "dcat:distribution",
      "@context": {
        "label": "rdfs:label"
      }
    },
    "Distribution": "dcat:Distribution",
    "Links": "owc:Links",
    "Link": "atom:link",
    "Category": "skos:Concept",
    "hasGeometry": "gsp:hasGeometry",
    "asWKT": "gsp:asWKT",
    "Platform": "eop:Platform",
    "Instrument": "eop:Instrument",
    "ProductInformation": "eop:ProductInformation",
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "owlTime": "http://www.w3.org/2006/time#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "prov": "http://www.w3.org/ns/prov#",
    "adms": "http://www.w3.org/ns/adms#",
    "foaf": "http://xmlns.com/foaf/0.1/",
    "dcat": "http://www.w3.org/ns/dcat#",
    "owl": "http://www.w3.org/2002/07/owl#",
    "gj": "https://purl.org/geojson/vocab#",
    "locn": "http://www.w3.org/ns/locn#",
    "owc": "http://www.opengis.net/ont/owc/1.0/",
    "atom": "http://www.w3.org/2005/Atom/",
    "iana": "http://www.iana.org/assignments/relation/",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "gsp": "http://www.opengis.net/ont/geosparql#",
    "eop": "http://www.opengis.net/ont/eo-geojson/1.0/",
    "vcard": "http://www.w3.org/2006/vcard/ns#",
    "os": "http://a9.com/-/spec/opensearch/1.1/",
    "schema": "http://schema.org/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/iso19115-json/build/annotated/metacat/iso19115/bp17-084/context.jsonld)

## Sources

* [EO Collection GeoJSON(-LD) Encoding](https://docs.ogc.org/bp/17-084r1/17-084r1.html#toc70)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/iso19115-json](https://github.com/ogcincubator/iso19115-json)
* Path: `_sources/bp17-084`

