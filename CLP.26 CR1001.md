DATA MODELS

Table of Contents

[1 Introduction 5](#_Toc461716337)

[1.1 Overview 5](#overview)

[1.2 Scope 5](#scope)

[1.3 Abbreviations 5](#_Toc461716340)

[1.4 References 5](#_Toc461716341)

[2 Harmonised Data Models 6](#harmonised-data-models)

[2.1 Vertical Segments 6](#vertical-segments)

[2.2 Attribute types 6](#_Toc461716344)

[2.2.1 ExtQuantitativeValue Attribute type 8](#extquantitativevalue-attribute-type)

[2.3 Generic Entity Data Model 9](#generic-entity-data-model)

[2.3.1 AgriCrop 11](#agricrop)

[2.3.2 AgriGreenHouse 15](#agrigreenhouse)

[2.3.3 AgriParcel 19](#agriparcel)

[2.3.4 AgriParcelOperation 22](#agriparceloperation)

[2.3.5 AgriParcelRecord 26](#agriparcelrecord)

[2.3.6 AgriPest 30](#agripest)

[2.3.7 AgriProduct 32](#agriproduct)

[2.3.8 AgriProductType 35](#agriproducttype)

[2.3.9 AgriSoil 37](#agrisoil)

[2.3.10 AirQualityObserved 39](#airqualityobserved)

[2.3.11 Building 42](#building)

[2.3.12 BuildingOperation 47](#_Toc461716358)

[2.3.13 BuildingType 51](#buildingtype)

[2.3.14 Device 53](#device)

[2.3.15 DeviceModel 58](#devicemodel)

[2.3.16 DeviceOperation 61](#deviceoperation)

[2.3.17 EnvironmentObserved 65](#environmentobserved)

[2.3.18 Machine 68](#machine)

[2.3.19 MachineModel 72](#machinemodel)

[2.3.20 MachineOperation 76](#machineoperation)

[2.3.21 PointOfInterest 80](#pointofinterest)

[2.3.22 Road 83](#road)

[2.3.23 RoadSegment 85](#roadsegment)

[2.3.24 Subscriber 88](#subscriber)

[2.3.25 SubscriptionService 91](#subscriptionservice)

[2.3.26 Vehicle 93](#vehicle)

[2.3.27 VehicleFault 96](#vehiclefault)

[2.3.28 VehicleType 99](#vehicletype)

[2.3.29 WaterQualityObserved 101](#waterqualityobserved)

[2.3.30 WeatherForecast 107](#weatherforecast)

[2.3.31 WeatherObserved 113](#weatherobserved)

[Annex A ExtQuantitativeValue and NGSIv2 metadata compatibility (Informative) 118](#_Toc461716378)

[Annex B Referenced Schema.org entities (Informative) 119](#_Toc461716379)

[B.1 Schema.org entity descriptions: Offer 119](#_Toc461716380)

[B.2 Schema.org entity descriptions: Organisation 124](#_Toc461716381)

[B.3 Schema.org entity descriptions: Person 127](#_Toc461716382)

[B.4 Schema.org entity descriptions: PostalAddress 131](#_Toc461716383)

[B.5 Schema.org entity descriptions: Product 132](#_Toc461716384)

[B.6 Schema.org entity descriptions: QuantitativeValue 135](#_Toc461716385)

[B.7 Schema.org entity descriptions: Vehicle 136](#_Toc461716386)

[Annex C Document Management 140](#_Toc461716387)

[C.1 Document History 140](#_Toc461716388)

[C.2 Other Information 140](#_Toc461716389)

<span id="_Toc461716337" class="anchor"><span id="_Toc327547998" class="anchor"><span id="_Toc327548198" class="anchor"><span id="_Toc101946531" class="anchor"></span></span></span></span>Introduction
========================================================================================================================================================================================================

Overview
--------

Data interoperability has been identified \[1\] as a technical barrier that prohibits the realisation of the full potential value of IoT Big Data. To help address that problem, in this document data models are defined of entities or things that are commonly used in IoT Big Data applications. The definitions of the data entities have been developed through contributions from participating mobile operators and aligned with existing industry work and namespaces where possible, for example, oneM2M in Smart Home \[2\], OASC for Smart Cities \[3\] and schema.org \[4\] for generic entities.

These collaboratively developed harmonised data models, together with the accompanying documents “IoT Big Data Framework Architecture” \[9\] and “IoT Big Data NGSIv2 Profile” \[10\], aim to define a framework of how mobile operators can approach the delivery of IoT Big Data services.

All sections and appendixes, except “Scope” and “Introduction”, are normative, unless they are explicitly indicated to be informative.

Scope
-----

This document specifies harmonised data models that are approved for use by all the participants of the IoT Big Data Ecosystem Project.

The harmonised data models are expected to evolve over time, potentially new entities will be added and entity definitions changed. The harmonised entity definitions defined within this document will be published and accessible via the GSMA IoT Big Data API Directory and will be developed and maintained in a collaborative manner. Contributions are welcome from the wider IoT community to develop and update the data entities. In the short to medium term, these changes will be managed through the standard GSMA PRD process with the IoT Big Data project/PSMC being the approval authority.

<span id="_Toc327447334" class="anchor"><span id="_Toc327548002" class="anchor"><span id="_Toc327548202" class="anchor"><span id="_Toc461716340" class="anchor"></span></span></span></span>Abbreviations
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

| Term  | Description                 |
|-------|-----------------------------|
| CNC   | Computer Numerical Control  |
| IoT   | Internet of Things          |
| IoTBD | Internet of Things Big Data |
| JSON  | JavaScript Object Notation) |
| ppt   | parts per thousand          |

<span id="_Toc327447332" class="anchor"><span id="_Toc327547999" class="anchor"><span id="_Toc327548199" class="anchor"><span id="_Toc461716341" class="anchor"></span></span></span></span>References 
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

| Ref                                                 | Doc Number        | Title                                                                                            |
|-----------------------------------------------------|-------------------|--------------------------------------------------------------------------------------------------|
| 1.  <span id="_Ref325119390" class="anchor"></span> |                   | Unlocking the Value of IoT Through Big Data.                                                     
                                                                                                                                                                             
                                                                           <http://www.gsma.com/connectedliving/unlocking-the-value-of-iot-through-big-data/>                |
| 1.  <span id="_Ref461118771" class="anchor"></span> | oneM2M            | <http://www.onem2m.org/>                                                                         |
| 1.  <span id="_Ref461118795" class="anchor"></span> | OASC              | <http://oascities.org/>                                                                          |
| 1.  <span id="_Ref461118814" class="anchor"></span> | Schema.org        | <http://schema.org/>                                                                             |
| 1.  <span id="_Ref461118852" class="anchor"></span> | JSON              | <http://www.json.org/>                                                                           |
| 1.  <span id="_Ref327455043" class="anchor"></span> | FIWARE NGSIv2     | FIWARE-NGSIv2 Specification available at <http://fiware.github.io/specifications/ngsiv2/stable/> |
| 1.                                                  | FIWARE DataModels | <http://fiware-datamodels.readthedocs.io/en/latest/>                                             |
| 1.  <span id="_Ref461118932" class="anchor"></span> | Lower camel case  | <https://en.wikipedia.org/wiki/CamelCase>                                                        |
| 1.                                                  | PRD CLP.25        | IoT Big Data Framework Architecture                                                              |
| 1.                                                  | PRD CLP.24        | IoT Big Data NGSIv2 Profile                                                                      |

Harmonised Data Models
======================

Vertical Segments
-----------------

The harmonised data entities contained in this document originate from and are used in the following industry verticals (or IoT Domains):

Agriculture

Automotive

Environment

Industry

Smart City

Smart Home

The data entity definitions include a list of the applicable industry verticals to assist with entity classification and discovery.

<span id="_Toc458186015" class="anchor"><span id="_Toc461716344" class="anchor"></span></span>Attribute types
-------------------------------------------------------------------------------------------------------------

Attribute types used within this document broadly follow the JSON (JavaScript Object Notation) type specification \[5\], the NGSIv2 \[6\] type specification and the schema.org type specification \[4\] as tabulated below:

| **Attribute Type name** | **Usage**                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Array                   | An ordered list of values that are referenced by numerical index. There can be arrays containing elements which type corresponds to any of the types described below. |
| Boolean                 | Logical value of **true** or **false**.                                                                                                                               |
| Date                    | A sequence of characters using ISO 8601 encoding to represent a Date.                                                                                                 
                                                                                                                                                                                                  
                           (<https://schema.org/Date>)                                                                                                                                            |
| DateTime                | A sequence of characters using ISO 8601 encoding to represent a timestamp (date plus time).                                                                           
                                                                                                                                                                                                  
                           (<https://schema.org/DateTime>)                                                                                                                                        |
| ExtQuantitativeValue    | An extended collection of key value pairs describing a point value characteristic of an entity.                                                                       
                                                                                                                                                                                                  
                           Specifically adding a **timestamp** (the date and time or the observation) to the existing Quantitative Value as defined by schema.org.                                
                                                                                                                                                                                                  
                           (<https://schema.org/QuantitiativeValue>)                                                                                                                              |
| geo:json                | Defines a location specified using geo:json encoding. (<https://tools.ietf.org/html/rfc7946>)                                                                         |
| Number                  | An integer or floating point number. (<https://schema.org/Number>)                                                                                                    |
| Offer                   | An offer definition for goods or services as defined by schema.org. (<https://schema.org/Offer>)                                                                      |
| Organization            | An organisation definition as defined by schema.org.(<https://schema.org/Organization>)                                                                               |
| Person                  | A person definition as defined by schema.org.(<https://schema.org/Person>)                                                                                            |
| Place                   | A place definition as defined by schema.org.(<https://schema.org/Place>)                                                                                              |
| PostalAddress           | A Postal Address of an item as defined by schema.org.                                                                                                                 
                                                                                                                                                                                                  
                           (<https://schema.org/PostalAddress>)                                                                                                                                   |
| Product                 | A product definition as defined by schema.org.                                                                                                                        
                                                                                                                                                                                                  
                           (<https://schema.org/Product>)                                                                                                                                         |
| QuantitativeValue       | A collection of key value pairs describing a point value characteristic of an entity or attribute as defined by schema.org.                                           
                                                                                                                                                                                                  
                           (<https://schema.org/QuantitiativeValue>)                                                                                                                              |
| Reference               | A sequence of characters which represents a reference to another entity.                                                                                              |
| StructuredValue         | A collection of key value pairs. Values may themselves be a Text, Number, Boolean, Array, StructuredValue or DateTime as defined by schema.org.                       
                                                                                                                                                                                                  
                           (<https://schema.org/StructuredValue>)                                                                                                                                 |
| Text                    | A sequence of characters. (<https://schema.org/Text>)                                                                                                                 |
| Time                    | A sequence of characters using ISO 8601 encoding to represent a Time.                                                                                                 
                                                                                                                                                                                                  
                           (<https://schema.org/Time>)                                                                                                                                            |
| URL                     | A sequence of characters. Defining a URL. (<https://schema.org/URL>)                                                                                                  |

In addition, all the entities defined in this document are valid attribute types.

### ExtQuantitativeValue Attribute type

The ExtQuantitativeValue attribute type is defined below:

| **Property**                                                                          | **Expected Type**                                              | **Description**                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from ** [**ExtQuantitativeValue**](https://schema.org/QuantitativeValue) |
| [**additionalProperty**](https://schema.org/additionalProperty)                       | [PropertyValue](https://schema.org/PropertyValue)              | A property-value pair representing an additional characteristics of the entitity, e.g. a product feature or another characteristic for which there is no matching property in schema.org.                                                                                                                               
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   
                                                                                                                                                          Note: Publishers should be aware that applications designed to use specific schema.org properties (e.g. http://schema.org/width, http://schema.org/color, http://schema.org/gtin13, ...) will typically expect such data to be provided using those properties, rather than using the generic property/value mechanism.  |
| [**maxValue**](https://schema.org/maxValue)                                           | [Number](https://schema.org/Number)                            | The upper value of some characteristic or property.                                                                                                                                                                                                                                                                     |
| [**minValue**](https://schema.org/minValue)                                           | [Number](https://schema.org/Number)                            | The lower value of some characteristic or property.                                                                                                                                                                                                                                                                     |
| **Timestamp<sup>\*</sup>**                                                            | DateTime                                                       | The ISO8601 sequence of characters at which the observation was made in UTC.                                                                                                                                                                                                                                            |
| [**unitCode**](https://schema.org/unitCode)                                           | [Text](https://schema.org/Text)  or                            
                                                                                         [URL](https://schema.org/URL)                                   | The unit of measurement given using the UN/CEFACT Common Code (3 characters) or a URL. Other codes than the UN/CEFACT Common Code may be used with a prefix followed by a colon.                                                                                                                                        |
| [**unitText**](https://schema.org/unitText)                                           | [Text](https://schema.org/Text)                                | A string or text indicating the unit of measurement. Useful if you cannot provide a standard unit code for [unitCode](https://schema.org/unitCode).                                                                                                                                                                     |
| [**value**](https://schema.org/value)                                                 | [Boolean](https://schema.org/Boolean)  or                      
                                                                                         [Number](https://schema.org/Number)  or                         
                                                                                         [StructuredValue](https://schema.org/StructuredValue)  or       
                                                                                         [Text](https://schema.org/Text)                                 | The value of the quantitative value or property value node.                                                                                                                                                                                                                                                             
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   
                                                                                                                                                          -   For [QuantitativeValue](https://schema.org/QuantitativeValue) and [MonetaryAmount](https://schema.org/MonetaryAmount), the recommended type for values is 'Number'.                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   
                                                                                                                                                          -   For [PropertyValue](https://schema.org/PropertyValue), it can be 'Text;', 'Number', 'Boolean', or 'StructuredValue'.                                                                                                                                                                                                 |
| [**valueReference**](https://schema.org/valueReference)                               | [Enumeration](https://schema.org/Enumeration)  or              
                                                                                         [PropertyValue](https://schema.org/PropertyValue)  or           
                                                                                         [QualitativeValue](https://schema.org/QualitativeValue)  or     
                                                                                         [QuantitativeValue](https://schema.org/QuantitativeValue)  or   
                                                                                         [StructuredValue](https://schema.org/StructuredValue)           | A pointer to a secondary value that provides additional information on the original value, e.g. a reference temperature.                                                                                                                                                                                                |

\*the timestamp field is the only additional property to the schema.org QuantitativeValue

The ExtQuantitativeValue attribute type has an equivalent format rendered using NGSIv2 attribute value and metadata, the alternate format, equivalence and compatibility are explained in further details in Annex A

Generic Entity Data Model
-------------------------

This generic entity Data Model enables each instance of an entity or thing to be uniquely described using an agreed set of harmonised attributes in a uniform and consistent way. All the entities defined in this section are normative.

In this document we follow this entity definition convention:

Common mandatory attributes are always presented first and by definition are included in all entities. These are followed by entity specific mandatory attributes and finally entity specific optional attributes. Attribute naming will follow the lower camel case convention \[8\]. Generic entity definitions are taken from the schema.org \[3\] vocabulary wherever possible.

&lt;Entity Name&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                                                                                                                                 | Mandatory/Optional | May be Null |
|----------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity. A globally unique reference to this entity instance.                                                                                             
                                                                                                                                                                                                                                
                                   It is recommended ids comply with RFC4122.                                                                                                                                                   | M                  | N           |
| type           | Text           | The type of the entity. A choice of one of the entity types defined in this document.                                                                                                       | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                                                                                                                                  | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity. A null value in this field means the entity has not been modified since being created.                                                    | M                  | Y           |
| source         | URL            | A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object. | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the provider of the harmonised data entity.                                                                                                            | M                  | Y           |

In addition to the generic entity attributes which are common to all entities, there are a set of entity specific attributes. In this document the entity specific attributes are listed for convenience in a separate table per entity as shown below:

&lt;Entity Name&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type         | Description                                                       | Mandatory/Optional | May be Null |
|----------------|------------------------|-------------------------------------------------------------------|--------------------|-------------|
| specificMan1   | A valid attribute type | Some text describing a mandatory attribute which may not be null. | M                  | N           |
| specificManN   | A valid attribute type | Some text describing a mandatory attribute which may be null.     | M                  | Y           |
| specificOptN   | A valid attribute type | Some text describing an optional attribute which may be null.     | O                  | Y           |

The combination of &lt;Entity Name&gt;&lt;Generic Attributes&gt; and &lt;Entity Name&gt;&lt;Entity Specific Attributes&gt; provides the definition of the complete harmonised data model of an Entity.

### AgriCrop

This entity contains a harmonised description of a generic crop. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriCrop&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriCrop**".                                              | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | URL            | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriCrop&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name     | Attribute Type     | Description                                                                                                                                                                                        | Mandatory/Optional | May be Null |
|--------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name               | Text               | The name of this crop.                                                                                                                                                                             | M                  | N           |
| alternateName      | Text               | An alternative name for this crop.                                                                                                                                                                 | O                  | Y           |
| description        | Text               | A description of this crop.                                                                                                                                                                        | O                  | Y           |
| refAgriSoil        | Array of Reference | An array containing a JSON encoded sequence of characters that reference the unique Ids of the recommended soil(s).                                                                                | O                  | Y           |
| refAgriFertilizer  | Array of Reference | An array containing a JSON encoded sequence of characters that reference the unique Ids of the recommended fertiliser product(s).                                                                  | O                  | Y           |
| refAgriPest        | Array of Reference | An array containing a JSON encoded sequence of characters that reference the unique Ids of the pest(s) known to attack this crop.                                                                  | O                  | Y           |
| plantingInterval   | Array of Text      | An array containing a JSON encoded sequence of characters of the recommended planting interval date(s) for this crop. Using The ISO8601 sequence of characters for each repeating date interval:   
                                                                                                                                                                                                                                               
                                           **interval**, **description**                                                                                                                                                                       
                                                                                                                                                                                                                                               
                                           Where **interval** is in the form of                                                                                                                                                                
                                                                                                                                                                                                                                               
                                           start date/end date                                                                                                                                                                                 
                                                                                                                                                                                                                                               
                                           --MM-DD/--MM-DD                                                                                                                                                                                     
                                                                                                                                                                                                                                               
                                           Meaning repeat each year from this start date to this end date.                                                                                                                                     | O                  | Y           |
| harvestingInterval | Array of Text      | An array containing a JSON encoded sequence of characters of the recommended harvesting interval date(s) for this crop. Using The ISO8601 sequence of characters for each repeating date interval: 
                                                                                                                                                                                                                                               
                                           **interval** , **description**                                                                                                                                                                      
                                                                                                                                                                                                                                               
                                           Where **interval** is in the form of                                                                                                                                                                
                                                                                                                                                                                                                                               
                                           start date/end date                                                                                                                                                                                 
                                                                                                                                                                                                                                               
                                           --MM-DD/--MM-DD                                                                                                                                                                                     
                                                                                                                                                                                                                                               
                                           Meaning repeat each year between the specified start date and the specified end date.                                                                                                               | O                  | Y           |
| wateringFrequency  | Text               | A description of the recommended watering schedule. A choice from an enumerated list. One of:                                                                                                      
                                                                                                                                                                                                                                               
                                           **daily, weekly, biweekly, monthly, onDemand, other**                                                                                                                                               | O                  | Y           |

#### 
AgriCrop JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/00685ca0edd54411cad5be84ee658da8>

{

"id": "df72dc57-1eb9-42a3-88a9-8647ecc954b4",

"type": "AgriCrop",

"dateCreated": {

"value": "2016-08-22T19:20+00:00",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T19:20+00:00",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "Wheat",

"type": "Text"

},

"alternateName": {

"value": "Triticum aestivum",

"type": "Text"

},

"description": {

"value": "Spring wheat",

"type": "Text"

},

"refAgriSoil": \[

"00411b56-bd1b-4551-96e0-a6e7fde9c840",

"e8a8389a-edf5-4345-8d2c-b98ac1ce8e2a"

\],

"refAgriFertilizer": \[

"1b0d6cf7-320c-4a2b-b2f1-4575ea850c73",

"380973c8-4d3b-4723-a899-0c0c5cc63e7e"

\],

"refAgriPest": \[

"10b52f07-079a-4390-8237-bf6a1c049a85",

"66bdb09b-4fe0-4932-a267-f9eda4474d2a"

\],

"plantingInterval": \[

"-09-28/-10-12, Best Season",

"-10-11/-10-18, Season OK"

\],

"harvestingInterval": \[

"-03-21/-04-01, Best Season",

"-04-02/-04-15, Season OK"

\],

"wateringFrequency": {

"value": "weekly",

"type": "Text"

}

}

### AgriGreenHouse

This entity contains a harmonised description of the conditions recorded within a generic greenhouse, a type of AgriParcel. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriGreenHouse&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriGreenHouse**"                                         | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | URL            | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriGreenHouse&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name          | Attribute Type                | Description                                                                                                | Mandatory/Optional | May be Null |
|-------------------------|-------------------------------|------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refAgriParcel           | Reference                     | Reference to the Unique id of the AgriParcel to which this record relates.                                 | M                  | N           |
| refWeatherObserved      | Reference                     | A JSON encoded sequence of characters that reference the unique id of the related weather observed record. | O                  | Y           |
| relativeHumidity        | ExtQuantitativeValue (Number) | The inside relative humidity expressed as a number between 0 and 1.                                        
                                                                                                                                                                       
                                                           0 ≤ relativeHumidity ≤ 1                                                                                    
                                                                                                                                                                       
                                                           Encoded as a ExtQuantitiativeValue                                                                          | O                  | Y           |
| refAgriParcelRecord     | Array of Reference            | Related AgriParcelRecords for this greenhouse.                                                             | O                  | Y           |
| leafTemperature         | ExtQuantitativeValue(Number)  | The average greenhouse air temperature in degrees centigrade.                                              
                                                                                                                                                                       
                                                           Encoded as a ExtQuantitiativeValue.                                                                         | O                  | Y           |
| co2                     | ExtQuantitativeValue(Number)  | The inside C02 concentration in mg/L.                                                                      
                                                                                                                                                                       
                                                           Encoded as a ExtQuantitativeValue.                                                                          | O                  | Y           |
| dailyLight              | ExtQuantitativeValue (Number) | Daily Accumulated light measured in kW/m<sup>2</sup>                                                       
                                                                                                                                                                       
                                                           Encoded as a ExtQuantitativeValue.                                                                          | O                  | Y           |
| drainFlow               | ExtQuantitativeValue (Number) | The observed drain flow rate in litres per second encoded as a                                             
                                                                                                                                                                       
                                                           ExtQuantitativeValue.                                                                                       | O                  | Y           |
| refWaterQualityObserved | Array of Reference            | Reference to the id(s) of the WaterQualityObserved records relating to this greenhouse.                    | O                  | Y           |

#### AgriGreenHouse JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/ba3f1acd21bd476600ad0f4a21f1260b>

{

"id": "ad500806-05ea-4ab6-812a-7a315d98e88d",

"type": "AgriGreenHouse",

"dateCreated": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refAgriParcel": {

"value": "c8b475e5-84a8-4346-ad79-cde1d2a4028b",

"type": "Reference"

},

"refWeatherObserved": {

"value": "c720cec5-ac6f-40b7-8e89-becb75702d0d",

"type": "Reference"

},

"relativeHumidity": {

"value": {

"value": 0.4,

"unitCode": "RA",

"timestamp": "2016-08-22T19:20+00:00"

},

"type": "ExtQuantitativeValue"

},

"refAgriParcelRecord": \[

"8c3a525d-b42e-4048-bcdd-a119d8ddb0a5",

"178d74c1-e6fe-4042-b955-2c164fc90b83"

\],

"leafTemperature": {

"value": {

"value": 22,

"unitCode": "CEL",

"timestamp": "2016-08-22T19:20+00:00"

},

"type": "ExtQuantitativeValue"

},

"co2": {

"value": {

"value": 28,

"unitCode": "M1",

"timestamp": "2016-08-22T19:20+00:00"

},

"type": "ExtQuantitativeValue"

},

"dailyLight": {

"value": {

"value": 24,

"unitCode": "N78",

"timestamp": "2016-08-22T19:20+00:00"

},

"type": "ExtQuantitativeValue"

},

"drainFlow": {

"type": "ExtQuantitativeValue",

"value": {

"value": 33,

"maxValue": 50,

"minValue": 25,

"unitCode": "G51",

"unitText": "Litre per second",

"timestamp": "2016-08-22T19:20+00:00"

}

},

"refWaterQualityObserved": \[

"49f86e0b-bb90-4751-a1c3-d5a891920807"

\]

}

### AgriParcel

This entity contains a harmonised description of a generic parcel of land. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriParcel&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriParcel**".                                            | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriParcel&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name  | Attribute Type                          | Description                                                                                          | Mandatory/Optional | May be Null |
|-----------------|-----------------------------------------|------------------------------------------------------------------------------------------------------|--------------------|-------------|
| location        | geo:json                                | The geo:json encoded polygon describing this parcel.                                                 | M                  | N           |
| area            | Number or ExtQuantitativeValue (Number) | The area of the parcel in square meters encoded as a number or a ExtQuantitativeValue.               | M                  | N           |
| description     | Text                                    | A description of the parcel.                                                                         | O                  | Y           |
| category        | Array                                   | A choice from an enumerated list describing the parcel category. **greenhouse, irrigated, rainfed.** | O                  | Y           |
| refAgriCrop     | Reference                               | A reference to the unique id of the AgriCrop associated with this Parcel.                            | M                  | N           |
| cropStatus      | Text                                    | A choice from an enumerated list describing the crop planting status One of:                         
                                                                                                                                                                   
                                                             **seeded, justBorn, growing, maturing, readyForHarvesting.**                                          | O                  | Y           |
| refAgriSoil     | Reference                               | A reference to the unique id of the soil associated with this Parcel.                                | O                  | Y           |
| dateLastPlanted | DateTime                                | The ISO8601 sequence of characters at which the AgriCrop was planted in UTC.                         | O                  | Y           |
| refDevice       | Array of Reference                      | A reference to the unique ids of the Devices used to monitor this parcel.                            | O                  | Y           |

#### AgriParcel JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/80f69a2558080798d6e661122d3f0cf8>

{

"id": "72d9fb43-53f8-4ec8-a33c-fa931360259a",

"type": "AgriParcel",

"dateCreated": {

"value": "2016-08-22T10:18:16Z ",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z ",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"location": {

"value": {

"type": "Polygon",

"coordinates": \[

\[100, 0\],

\[101, 0\],

\[101, 1\],

\[100, 1\],

\[100, 0\]

\]

},

"type": "geo:json"

},

"area": {

"value": 2000,

"type": "Number"

},

"description": {

"value": "North greenhouse (glass)",

"type": "Text"

},

"category": \[

"greenhouse"

\],

"refAgriCrop": {

"value": "af3b2a4f-3133-4747-8e00-ba5e4cf1708b",

"type": "Reference"

},

"cropStatus": {

"value": "seeded",

"type": "Text"

},

"refAgriSoil": {

"value": "791f80c4-d621-4686-9bc0-84487084b9cf",

"type": "Reference"

},

"dateLastPlanted": {

"value": "2016-08-09T10:18:16Z",

"type": "DateTime"

},

"refDevice": \[

"276805ff-d3fb-41bf-9714-ed0ecf2ee12b",

"59b241f5-2827-44ea-bd1f-938567d271ea"

\]

}

### AgriParcelOperation

This entity contains a harmonised description of a generic operations performed on a parcel of land. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriParcelOperation&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriParcelOperation**".                                   | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriParcelOperation&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type               | Description                                                                                | Mandatory/Optional | May be Null |
|----------------|------------------------------|--------------------------------------------------------------------------------------------|--------------------|-------------|
| refAgriParcel  | Reference                    | A reference to the unique id of the AgriParcel related to this operation.                  | M                  | N           |
| operationType  | Text                         | A choice from an enumerated list describing the operation performed on the parcel. One of: 
                                                                                                                                             
                                                 **fertiliser, inspection, pesticide, water, other.**                                        | O                  | Y           |
| description    | Text                         | A description of the operation.                                                            | O                  | Y           |
| result         | Text                         | A description of the results of the operation. One of (“ok”, “aborted”).                   | O                  | Y           |
| startDate      | DateTime                     | The planned start date for the operation.                                                  | M                  | Y           |
| endDate        | DateTime                     | The planned end date for the operation.                                                    | M                  | Y           |
| status         | Text                         | A choice from an enumerated list describing the status. One of:                            
                                                                                                                                             
                                                 **planned, ongoing, finished, scheduled, cancelled.**                                       | O                  | Y           |
| operator       | Person                       | The operator performing this action encoded as a Schema.org person.                        
                                                                                                                                             
                                                 <https://schema.org/Person>                                                                 | O                  | Y           |
| dateStarted    | DateTime                     | Timestamp when the operation actually started to be performed.                             | O                  | Y           |
| dateFinished   | DateTime                     | Timestamp when the operation actually finished.                                            | O                  | Y           |
| refAgriProduct | Reference                    | A reference to the unique id of the AgriProduct used.                                      | O                  | Y           |
| quantity       | ExtQuantitativeValue(Number) | The amount of water or product used encoded as a ExtQuantitativeValue.                     | O                  | Y           |
| waterSource    | Text                         | A choice from an enumerated list describing the water source. One of:                      
                                                                                                                                             
                                                 **rainfall, watering.**                                                                     | O                  | Y           |

#### AgriParcelOperation JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/52a05ec2f4d55181cec3f1aba6157a1d>

{

"id": "e1e9d3a3-074f-46f1-9375-52000d05a62b",

"type": "AgriParcelOperation",

"dateCreated": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refAgriParcel": {

"value": "318366a9-7643-4d8e-9a11-c76a8c29d8eb",

"type": "Reference"

},

"operationType": {

"value": "fertiliser",

"type": "Text"

},

"description": {

"value": "Monthly fertiliser application",

"type": "Text"

},

"result": {

"value": "Completed successfully ",

"type": "Text"

},

"startDate": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"endDate": {

"value": "2016-08-28T10:18:16Z",

"type": "DateTime"

},

"status": {

"value": "ongoing",

"type": "Text"

},

"operator": {

"value": {

"givenName": "John Smith",

"jobTitle": "Tractor Operator"

},

"type": "Person"

},

"dateStarted": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateFinished": {

"value": "2016-08-28T10:18:16Z",

"type": "DateTime"

},

"refAgriProduct": {

"value": "a8f616b8-13fb-473a-8e61-b7a80c6c93ec",

"type": "Reference"

},

"quantity": {

"value": {

"value": 40,

"unitCode": "GM"

},

"type": "ExtQuantitativeValue"

},

"waterSource": {

"value": "watering",

"type": "Text"

}

}

<span id="_Toc461634078" class="anchor"></span>

### AgriParcelRecord

This entity contains a harmonised description of the conditions recorded on a generic parcel of land. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriParcelRecord&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriParcelRecord**".                                      | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriParcelRecord&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name      | Attribute Type                | Description                                                                                       | Mandatory/Optional | May be Null |
|---------------------|-------------------------------|---------------------------------------------------------------------------------------------------|--------------------|-------------|
| refAgriParcel       | Reference                     | Unique id of the AgriParcel to which this record relates.                                         | M                  | N           |
| location            | geo:json                      | The geo:json encoded polygon of this AgriParcelRecord.                                            | M                  | N           |
| soilTemperature     | ExtQuantitativeValue(Number)  | The observed soil temperature in degrees centigrade encoded as a ExtQuantitativeValue.            | O                  | Y           |
| temperature         | ExtQuantitativeValue(Number)  | The observed air temperature in degrees centigrade encoded as a ExtQuantitativeValue.             | O                  | Y           |
| soilMoistureVwc     | ExtQuantitativeValue(Number)  | Measured as Volumetric Water Content, VWC as a percentage.                                        
                                                                                                                                                          
                                                       0 ≤soilMoistureVwc ≤ 100                                                                           
                                                                                                                                                          
                                                       encoded as a ExtQuantitativeValue                                                                  | O                  | Y           |
| soilMoistureEc      | ExtQuantitativeValue(Number)  | Measured as                                                                                       
                                                                                                                                                          
                                                       Electrical Conductivity, EC in units of Siemens per meter (S/m) encoded as a ExtQuantitativeValue  | O                  | Y           |
| solarRadiation      | ExtQuantitativeValue (Number) | Measured in kW/m<sup>2</sup> encoded as a ExtQuantitativeValue.                                   | O                  | Y           |
| relativeHumidity    | ExtQuantitativeValue(Number)  | Relative Humidity a number between 0 and 1                                                        
                                                                                                                                                          
                                                       0 ≤ relativeHumidity ≤ 1 encoded as a ExtQuantitativeValue.                                        | O                  | Y           |
| atmosphericPressure | ExtQuantitativeValue(Number)  | Atmospheric Pressure in units of Hecto Pascal encoded as a ExtQuantitativeValue.                  | O                  | Y           |
| description         | Text                          | Description of this AgriParcelRecord.                                                             | O                  | Y           |

#### AgriParcelRecord JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/bc089529b7966099cd11bc0e2b0bb283>

{

"id": "8f5445e6-f49b-496e-833b-e65fc97fcab7",

"type": "AgriParcelRecord",

"dateCreated": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refAgriParcel": {

"value": "d3676010-d815-468c-9e01-25739c5a25ed",

"type": "Reference"

},

"location": {

"value": {

"type": "Polygon",

"coordinates": \[

\[100, 0\],

\[101, 0\],

\[101, 1\],

\[100, 1\],

\[100, 0\]

\]

},

"type": "geo:json"

},

"soilTemperature": {

"value": {

"value": 27,

"unitCode": "CEL"

},

"type": "ExtQuantitativeValue"

},

"temperature": {

"value": {

"value": 33,

"unitCode": "CEL"

},

"type": "ExtQuantitativeValue"

},

"soilMoistureVwc": {

"value": {

"value": 8,

"unitCode": "P1"

},

"type": "ExtQuantitativeValue"

},

"soilMoistureEc": {

"value": {

"value": 17,

"unitCode": "D10"

},

"type": "ExtQuantitativeValue"

},

"solarRadiation": {

"value": {

"value": 15,

"unitCode": "N78"

},

"type": "ExtQuantitativeValue"

},

"relativeHumidity": {

"value": {

"value": 0.15

},

"type": "ExtQuantitativeValue"

},

"atmosphericPressure": {

"value": {

"value": 101325,

"unitCode": "PAL"

},

"type": "ExtQuantitativeValue"

},

"description": {

"value": "North greenhouse. Planting zone A ",

"type": "Text"

}

}

### AgriPest

This entity contains a harmonised description of a generic agricultural pest. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriPest&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriPest**".                                              | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriPest&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                                                                       | Mandatory/Optional | May be Null |
|----------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name           | Text               | The name of this agricultural pest.                                                                                               | M                  | N           |
| alternateName  | Text               | Alternative name of this agricultural pest.                                                                                       | O                  | Y           |
| description    | Text               | A description of this agricultural pest.                                                                                          | O                  | Y           |
| refAgriProduct | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique ids of the recommended AgriProduct pesticide(s). | O                  | Y           |

#### AgriPest JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/cbab7c37630eb7ea87b503267d0696a1>

{

"id": "fb3f1295-500c-4aa3-b995-c909097d5c01",

"type": "AgriPest",

"dateCreated": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "Grasshopper",

"type": "Text"

},

"alternateName": {

"value": "Chorthippus parallelus",

"type": "Text"

},

"description": {

"value": "Common European grasshopper",

"type": "Text"

},

"refAgriProduct": \[

"7f1d962b-0d14-479b-a50a-baaef261263a"

\]

}

### AgriProduct

This entity contains a harmonised description of a generic agricultural product. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriProduct&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriProduct**".                                           | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriProduct&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name     | Attribute Type | Description                                                     | Mandatory/Optional | May be Null |
|--------------------|----------------|-----------------------------------------------------------------|--------------------|-------------|
| name               | Text           | The name of this agricultural product.                          | M                  | N           |
| refAgriProductType | Reference      | Unique id of this product type. Selected from AgriProductType.  | M                  | N           |
| description        | Text           | A description of this agricultural product.                     | O                  | Y           |
| manufacturerName   | Text           | The name of manufacturer of this agricultural product.          | O                  | Y           |
| brandName          | Text           | A description of this agricultural product brand name.          | O                  | Y           |
| supplierName       | Text           | The details of the local retailer of this agricultural product. | O                  | Y           |
| category           | Array          | A choice from an enumerated list. including:                    
                                                                                                        
                                       **fertiliser, herbicide, pesticide, other**                      | O                  | Y           |

#### AgriProduct JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/73d3eb307e8b2431fed1b7c91248c32a>

{

"id": "410ee08d-805e-4aab-9fba-065533b7bd76",

"type": "AgriProduct",

"dateCreated": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "Banana seedlings",

"type": "Text"

},

"refProductType": {

"value": "ec6de3dc-7668-11e6-9c73-f752f61f61f9",

"type": "Reference"

},

"description": {

"value": "Banana cultivar Musa acuminata",

"type": "Text"

},

"manufacturerName": {

"value": "ACME Banana Supplies Company Ltd",

"type": "Text"

},

"brandName": {

"value": "5ADay",

"type": "Text"

},

"supplierName": {

"value": "A&B Wholesaling Limited",

"type": "Text"

},

"category": \[

"other"

\]

}

### AgriProductType

This entity contains a harmonised description of a generic agricultural product type. This entity is primarily associated with the agricultural vertical and related IoT applications. The AgriProductType includes a hierarchical structure that allows product types to be grouped in a flexible way.

&lt;AgriProductType&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriProductType**".                                       | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriProductType&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                                                                            | Mandatory/Optional | May be Null |
|----------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name           | Text               | The name of this AgriProductType.                                                                                                      | M                  | N           |
| description    | Text               | A description of this AgriProductType.                                                                                                 | M                  | N           |
| root           | Boolean            | A logical indicator that this product is the root of a AgriProductType hierarchy. Logical TRUE indicates it is a root.                 | M                  | N           |
| refParentType  | Array of Reference | A JSON encoded sequence of characters referencing the unique ids of the AgriProductType groupings this AgriProductType is a member of. | O                  | Y           |

#### AgriProductType JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/e78f090452ce8f63adfba472fe43c5d7>

{

"id": "398aa5f4-6a81-4dea-9f85-e9869441a257",

"type": "AgriProductType",

"dateCreated": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "Soft Fruits",

"type": "Text"

},

"description": {

"value": "Soft edible fruits",

"type": "Text"

},

"root": {

"value": "FALSE",

"type": "Text"

},

"refParentType": \[

"b99c940d-7156-4280-9a2b-4a9e533cd20e"

\]

}

### AgriSoil

This entity contains a harmonised description of soil. This entity is primarily associated with the agricultural vertical and related IoT applications.

&lt;AgriSoil&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AgriSoil**".                                              | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AgriSoil&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                                                                                           | Mandatory/Optional | May be Null |
|----------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name           | Text               | The name of this soil type.                                                                                                                           | M                  | N           |
| alternateName  | Text               | Alternative name of this soil type.                                                                                                                   | O                  | Y           |
| description    | Text               | A description of this soil.                                                                                                                           | O                  | Y           |
| refAgriProduct | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique ids of the recommended AgriProduct fertiliser (or other) product(s). | O                  | Y           |

#### AgriSoil JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/3df400c35ce449a78ae5124ce07d99ce>

{

"id": "789363b4-c771-43d6-8505-ca582efe8fcd",

"type": "AgriSoil",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.samplefarmproduct.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "Clay",

"type": "Text"

},

"alternateName": {

"value": "Heavy soil",

"type": "Text"

},

"description": {

"value": "Fine grained, poor draining soil. Particle size less than 0.002mm",

"type": "Text"

},

"refAgriProduct": \[

"ea54eedf-d5a7-4e44-bddd-50e9935237c0",

"275b4c08-5e52-4bb7-8523-74ce5d0007de"

\]

}

### AirQualityObserved

This entity contains a harmonised description of the air quality observed at a particular location and time. This entity is primarily associated with the vertical segment of the environment and may also be used in smart homes, smart cities, agriculture, industry and related IoT applications.

&lt;AirQualityObserved&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**AirQualityObserved**".                                    | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;AirQualityObserved&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                               | Mandatory/Optional | May be Null |
|----------------|--------------------|-------------------------------------------------------------------------------------------|--------------------|-------------|
| refDevice      | Array of Reference | An array of references to the unique ids of the devices that originated this observation. | O                  | N           |
| location       | geo:json           | The geo:json encoded polygon or point location, of this observation.                      | M                  | N           |
| dateObserved   | DateTime           | The date and time of this observation in ISO8601 UTCformat.                               | M                  | N           |
| measurand      | Array of Text      | An array containing a JSON encoded sequence of characters of the measurand observed.      
                                                                                                                                  
                                       **measurand** , **observedValue**, **unitcode**, **description**.                          
                                                                                                                                  
                                       Unitcode defined as in schema.org/QuantitativeValue                                        
                                                                                                                                  
                                       The unit of measurement given using the UN/CEFACT Common Code (3 characters)               
                                                                                                                                  
                                       <http://wiki.goodrelations-vocabulary.org/Documentation/UN/CEFACT_Common_Codes>            
                                                                                                                                  
                                       Example;                                                                                   
                                                                                                                                  
                                       **"CO,500,M1,Carbon Monoxide"**                                                            
                                                                                                                                  
                                       **"NO,45,M1,Nitrogen Monoxide"**                                                           
                                                                                                                                  
                                       **"NO2,69,M1,Nitrogen Dioxide"**                                                           
                                                                                                                                  
                                       **"NOx,139,M1,Nitrogen oxides"**                                                           
                                                                                                                                  
                                       **"SO2,11,M1,Sulfur Dioxide"**                                                             | M                  | Y           |

#### AirQualityObserved JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/95ae1e455d471443c1a7af72e26e3fe2>

{

"id": "c9f32b35-a185-48e2-835f-c521efc294ab",

"type": "AirQualityObserved",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refDevice": \[

"5c9fb9dd-fc13-4fda-8f4c-f99a04f6f858"

\],

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"dateObserved": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"measurand": \[

"CO, 500, M1, Carbon monoxide concentration",

"CO2, 1500, M1, Carbon dioxide concentration"

\]

}

### Building

This entity contains a harmonised description of a Building. This entity is associated with the vertical segments of smart homes, smart cities, industry and related IoT applications.

&lt;Building&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**Building**".                                              | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Building&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name         | Attribute Type                                      | Description                                                                                                                                  | Mandatory/Optional | May be Null |
|------------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refBuildingType        | Reference                                           | Refers to the buildingType that this building is an instance of.                                                                             | M                  | N           |
| category               | Array of Text                                       | One or more categories relevant to the building with choices based on for example <http://wiki.openstreetmap.org/wiki/Map_Features#Building> | O                  | Y           |
| containedInPlace       | geo:json                                            | The geo:json encoded polygon of the building plot in which this building sits.                                                               | O                  | Y           |
| location               | geo:json                                            | The geo:json encoded polygon of this building.                                                                                               | M                  | N           |
| address                | PostalAddress                                       | The building PostalAddress encoded as a Schema.org PostalAddress.                                                                            
                                                                                                                                                                                                                              
                                                                                [https://schema.org/PostalAddress](https://schema.org/Address)                                                                                | M                  | Y           |
| owner                  | Array of references to Person(s) or Organization(s) | An array containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s).                                        
                                                                                                                                                                                                                              
                                                                                Related to a Schema.org person or organization.                                                                                               
                                                                                                                                                                                                                              
                                                                                <https://schema.org/Person>                                                                                                                   
                                                                                                                                                                                                                              
                                                                                <https://schema.org/Organization>                                                                                                             | M                  | Y           |
| occupier               | Array of references to Person(s) or Organization(s) | An array containing a JSON encoded sequence of characters referencing the unique Ids of the occupiers(s).                                    
                                                                                                                                                                                                                              
                                                                                Related to a Schema.org person or organization.                                                                                               
                                                                                                                                                                                                                              
                                                                                <https://schema.org/Person>                                                                                                                   
                                                                                                                                                                                                                              
                                                                                <https://schema.org/Organization>                                                                                                             | M                  | Y           |
| refSubscriptionService | Array of Reference                                  | An array containing a JSON encoded sequence of characters of the unique Ids of the subscription service(s) related to this building.         | O                  | Y           |
| floorsAboveGround      | Number                                              | The number of floors above ground level in this building.                                                                                    | O                  | Y           |
| floorsBelowGround      | Number                                              | The number of floors below ground level in this building.                                                                                    | O                  | Y           |
| description            | Text                                                | An optional description of the entity.                                                                                                       | O                  | Y           |
| mapUrl                 | URL                                                 | A URL to a mapping service which shows the location of the building.                                                                         | O                  | Y           |
| notes                  | Array of Text                                       | Free format notes relating to the building e.g. published occupants, opening hours etc.                                                      | O                  | Y           |

#### Building JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/4994b9f4f6907a9a96bdb499899cc27f>

{

"id": "f95c06e3-776e-4a57-9b00-a85e3da145c1",

"type": "Building",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refBuildingType": {

"value": "8b1f2bf0-5093-4182-ad4b-224182bb3b9f",

"type": "Reference"

},

"category": \[

"House"

\],

"containedInPlace": {

"value": {

"type": "Polygon",

"coordinates": \[

\[100, 0\],

\[101, 0\],

\[101, 1\],

\[100, 1\],

\[100, 0\]

\]

},

"type": "geo:json"

},

"location": {

"value": {

"type": "Polygon",

"coordinates": \[

\[100, 0\],

\[101, 0\],

\[101, 1\],

\[100, 1\],

\[100, 0\]

\]

},

"type": "geo:json"

},

"address": {

"type": "PostalAddress",

"value": {

"addressLocality": "London",

"postalCode": "EC4N 8AF",

"streetAddress": "25 Walbrook"

}

},

"owner": \[

"cdfd9cb8-ae2b-47cb-a43a-b9767ffd5c84",

"1be9cd61-ef59-421f-a326-4b6c84411ad4"

\],

"occupier": \[

"9830f692-7677-11e6-838b-4f9fb3dc5a4f"

\],

"refSubscriptionService": \[

"b4fb8bff-1a8f-455f-8cc0-ca43c069f865onService1",

"55c24793-3437-4157-9bda-667c9e1531fc"

\],

"floorsAboveGround": {

"value": 7,

"type": "Number"

},

"floorsBelowGround": {

"value": 0,

"type": "Number"

},

"description": {

"value": "Office block",

"type": "Text"

},

"mapUrl": {

"value": "http://www.example.com",

"type": "URL"

},

"notes": {

"value": "Intelligent entry barrier system, intelligent air conditioning units",

"type": "Text"

}

}

### <span id="_Toc461019846" class="anchor"><span id="_Toc461716358" class="anchor"></span></span>BuildingOperation

This entity contains a harmonised description of a generic operation (related to smart buildings) applied to the referenced building. The building operation contains dynamic data reported by, or associated with a building or operations applicable to the building. This entity is associated with the vertical segments of smart homes, smart cities, industry and related IoT applications.

&lt;BuildingOperation&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**BuildingOperation**".                                     | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;BuildingOperation&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name              | Attribute Type     | Description                                                                                                                                | Mandatory/Optional | May be Null |
|-----------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refBuilding                 | Reference          | Refers to the unique entity Id of the building to which this building record relates.                                                      | M                  | N           |
| operationType               | Text               | Defines the type of operation conducted/ requested. This will be one of a defined list of operation types specific to the building.        | O                  | Y           |
| description                 | Text               | A description of the operation.                                                                                                            | O                  | Y           |
| result                      | Text               | A description of the results of the operation. One of (“ok”, “aborted”).                                                                   | O                  | Y           |
| startDate                   | DateTime           | The planned start date for the operation.                                                                                                  | M                  | Y           |
| endDate                     | DateTime           | The planned end date for the operation                                                                                                     | M                  | Y           |
| status                      | Text               | A choice from an enumerated list describing the status. One of:                                                                            
                                                                                                                                                                                                
                                                    **planned, ongoing, finished, scheduled, cancelled**                                                                                        | O                  | Y           |
| operator                    | Person             | The operator performing this action encoded as a Schema.org person.                                                                        
                                                                                                                                                                                                
                                                    <https://schema.org/Person>                                                                                                                 | O                  | Y           |
| dateStarted                 | DateTime           | Timestamp when the operation actually started to be performed.                                                                             | O                  | Y           |
| dateFinished                | DateTime           | Timestamp when the operation actually finished.                                                                                            | O                  | Y           |
| operationSequence           | Text               | The sequence of operations executed/ requested for the building in a representation format relevant to the building.                       | O                  | Y           |
| refRelatedBuildingOperation | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique ids of any related building operations.                   | O                  | Y           |
| refRelatedOperation         | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique ids of any related operations (device, machine or other). | O                  | Y           |

#### BuildingOperation JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/bf5d982f79ab40934d6d38767b5f8f82>

{

"id": "57b912ab-eb47-4cd5-bc9d-73abece1f1b3",

"type": "BuildingOperation",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refBuilding": {

"value": "f59e2074-0032-4ccd-b0dd-f06370ffb6af",

"type": "Reference"

},

"operationType": {

"value": "Air Conditioning Switch To Low Power",

"type": "Text"

},

"description": {

"value": "Air conditioning levels reduced due to out of hours",

"type": "Text"

},

"result": {

"value": "Operation successful",

"type": "Text"

},

"startDate": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"endDate": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"status": {

"value": "Air conditioning fan & target temperature adjusted",

"type": "Text"

},

"dateStarted": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateFinished": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"operationSequence": {

"value": "Fan levels reduced to minimum. Target temperature set to 24 degrees Celsius. ",

"type": "Text"

},

"refRelatedBuildingOperation": \[

"b4fb8bff-1a8f-455f-8cc0-ca43c069f865onService1",

"55c24793-3437-4157-9bda-667c9e1531fc"

\],

"refRelatedDeviceOperation": \[

"36744245-6716-4a28-84c7-0e3d7520f143",

"33b2b713-9223-40a5-87a0-3f80a1264a6c"

\]

}

### BuildingType

This entity contains a harmonised description of a generic building type. This entity is associated with the vertical segments of smart home, smart cities, industry and related IoT applications. The building type includes a hierarchical structure that allows building types to be grouped in a flexible way.

&lt;BuildingType&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**BuildingType**".                                          | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;BuildingType&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                                                                                           | Mandatory/Optional | May be Null |
|----------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name           | Text               | The name of this BuildingType.                                                                                                                        | M                  | N           |
| description    | Text               | A description of this type.                                                                                                                           | O                  | Y           |
| root           | Boolean            | A logical indicator that this is the root of a BuildingType hierarchy. TRUE indicates it is the root, FALSE indicates that it is not the root.        | O                  | Y           |
| refParentType  | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique Ids of the building type groupings this BuildingType is a member of. | O                  | Y           |

#### BuildingType JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/e7553da5f75bc32e9f02024e7cdca0b1>

{

"id": "57b912ab-eb47-4cd5-bc9d-73abece1f1b3",

"type": "BuildingType",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "House",

"type": "Text"

},

"description": {

"value": "Standard building type definition for a domestic house",

"type": "Text"

},

"root": {

"value": "FALSE",

"type": "Boolean"

},

"refParentType": \[

"4146335f-839f-4ff9-a575-6b4e6232b734",

"c44fc765-51a7-4f71-bf1e-22e874c35180"

\]

}

### Device

This entity contains a harmonised description of a generic device. This entity provides an essentially static description of a generic device and is therefore applicable to all IoT segments and related IoT applications.

&lt;Device&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**Device**".                                                | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Device&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name      | Attribute Type                | Description                                                                                                                   | Mandatory/Optional | May be Null |
|---------------------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refDeviceModel      | Reference                     | Unique id of this device model selected from DeviceModel.                                                                     | M                  | N           |
| serialNumber        | Text                          | The serial number assigned by the manufacturer.                                                                               | M                  | N           |
| supplierName        | Text                          | The details of the supplier of this device.                                                                                   | O                  | Y           |
| manufacturerCountry | Text                          | The country where this device was manufactured.                                                                               | O                  | Y           |
| factory             | Text                          | The factory manufacturing this device.                                                                                        | O                  | Y           |
| dateManufactured    | DateTime                      | The ISO8601 sequence of characters at which the device was manufactured in UTC.                                               | M                  | N           |
| description         | Text                          | An optional description of this device.                                                                                       | O                  | Y           |
| owner               | Array of Reference            | An array containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s).                         
                                                                                                                                                                                      
                                                       Related to a Schema.org person or organization.                                                                                
                                                                                                                                                                                      
                                                       <https://schema.org/Person>                                                                                                    
                                                                                                                                                                                      
                                                       <https://schema.org/Organization>                                                                                              | O                  | Y           |
| dateInstalled       | DateTime                      | The ISO8601 sequence of characters at which the device was installed in UTC.                                                  | M                  | N           |
| dateFirstUsed       | DateTime                      | The ISO8601 sequence of characters at which the device was first used in UTC.                                                 | M                  | N           |
| hardwareVersion     | Text                          | The hardware version of this device.                                                                                          | M                  | N           |
| firmwareVersion     | Text                          | The firmware version of this device.                                                                                          | M                  | N           |
| softwareVersion     | Text                          | The software version of this device.                                                                                          | M                  | N           |
| osVersion           | Text                          | The operating system version of this device.                                                                                  | M                  | N           |
| supportedProtocol   | Array of Text                 | An array element per supported communication protocol.                                                                        | M                  | N           |
| location            | geo:json                      | The geo:json encoded location, of this device.                                                                                | O                  | Y           |
| online              | Boolean                       | The communication status of this device. A logical representation of Offline or Online.                                       | M                  | N           |
| status              | Text                          | The JSON format device status description. Manufacturer or device. specific status codes generated by the device.             | O                  | Y           |
| dateLastCalibration | DateTime                      | The date this device was last calibrated.                                                                                     | O                  | Y           |
| batteryLevel        | ExtQuantitativeValue (Number) | Battery level. It must be equal to:                                                                                           
                                                                                                                                                                                      
                                                       1.0 When the battery charge is full.                                                                                           
                                                                                                                                                                                      
                                                       0.0 When the battery charge empty.                                                                                             
                                                                                                                                                                                      
                                                       Null when it cannot be determined.                                                                                             
                                                                                                                                                                                      
                                                       encoded as a                                                                                                                   
                                                                                                                                                                                      
                                                       ExtQuantitativeValue.                                                                                                          | O                  | Y           |
| value               | ExtQuantitativeValue (Number) | The observed or reported value, for control applications the reported device setting value encoded as a ExtQuantitativeValue. | O                  | Y           |

#### Device JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/8bec6a39f34601fffc430b7b0f306df8>

{

"id": "ba2d4fd9-f57f-4610-a589-2d52670d14f3",

"type": "Device",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refDeviceModel": {

"value": "d1be2e61-d9e7-43cd-9c68-51e0861b3a49",

"type": "Reference"

},

"serialNumber": {

"value": "123456789",

"type": "Text"

},

"supplierName": {

"value": "ACME Direct, Inc.",

"type": "Text"

},

"manufacturerCountry": {

"value": "UK",

"type": "Text"

},

"factory": {

"value": "unknown",

"type": "Text"

},

"dateManufactured": {

"value": "2016-08-21T10:18:16Z",

"type": "DateTime"

},

"description": {

"value": "Thermocouple",

"type": "Text"

},

"owner": \[

"43c46ff2-b0f7-4e4f-838a-adee1c9cae88",

"ebf421c9-363b-4ed4-97a0-93a6e39786ff"

\],

"dateInstalled": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateFirstUsed": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"hardwareVersion": {

"value": "1.2",

"type": "Text"

},

"firmwareVersion": {

"value": "2.8.56",

"type": "Text"

},

"softwareVersion": {

"value": "2.5.11",

"type": "Text"

},

"osVersion": {

"value": "8.1",

"type": "Text"

},

"supportedProtocols": \[

"HTTP",

"HTTPS",

"FTP"

\],

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"online": {

"value": "TRUE",

"type": "Boolean"

},

"status": {

"value": "SC1001",

"type": "Text"

},

"dateLastCalibration": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"batteryLevel": {

"value": {

"value": 0.7

},

"type": "ExtQuantitativeValue"

},

"value": {

"value": {

"value": 1

},

"type": "ExtQuantitativeValue"

}

}

### DeviceModel

This entity contains a harmonised description of a generic device model and is therefore applicable to all IoT segments and related IoT applications. The Device Model includes an optional hierarchical structure that allows device types to be grouped in a flexible way.

&lt;DeviceModel&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**DeviceModel**".                                           | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;DeviceModel&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name       | Attribute Type     | Description                                                                                                                                                                                | Mandatory/Optional | May be Null |
|----------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name                 | Text               | The name of this DeviceModel.                                                                                                                                                              | M                  | N           |
| doc                  | URL                | Reference to Product Data Sheet or other manufacturer’s documentation about this device model including where relevant, details of the accuracy, trueness, precision and units of measure. | O                  | Y           |
| category             | Array of Text      | A choice from an enumerated list defining the category of this device including:                                                                                                           
                                                                                                                                                                                                                                         
                                             **sensor, actuator, meter, appliance, heater, chiller, lighting, boiler, vessel, airHandlingUnit, consumer, other.**                                                                        | O                  | Y           |
| description          | Text               | A description of this DeviceModel .                                                                                                                                                        | O                  | Y           |
| manufacturerName     | Text               | The name of manufacturer of this DeviceModel.                                                                                                                                              | O                  | Y           |
| brandName            | Text               | A description of the brand name of this DeviceModel.                                                                                                                                       | O                  | Y           |
| root                 | Boolean            | A logical indicator that this DeviceModel is the root of a DeviceModel hierarchy. TRUE indicates it is the root, FALSE indicates that it is not the root.                                  | O                  | Y           |
| refParentDeviceModel | Array of Reference | An array containing a JSON encoded sequence of characters of the unique Ids of the device model groupings this device model is a member of.                                                | O                  | Y           |

#### DeviceModel JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/6ca009c7e08f6c54377ba758adbe7908>

{

"id": "e01f13d1-fea4-4cc4-92c9-0d9fadb2c509",

"type": "DeviceModel",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "Sensor Model 501",

"type": "Text"

},

"doc": {

"value": "http://www.example.com",

"type": "URL"

},

"category": \[

"sensor"

\],

"description": {

"value": "Monomatics All Weather Temperature Sensor",

"type": "Text"

},

"manufacturerName": {

"value": "ACME Manufacturing, Inc.",

"type": "Text"

},

"brandName": {

"value": "SuperWidgets",

"type": "Text"

},

"root": {

"value": "FALSE",

"type": "Boolean"

},

"refParentDeviceModel": \[

"4146335f-839f-4ff9-a575-6b4e6232b734",

"c44fc765-51a7-4f71-bf1e-22e874c35180"

\]

}

### DeviceOperation

This entity contains a harmonised description of a generic device operation entity. The device operation entity contains dynamic data reported by a device and is therefore applicable to all IoT segments and related IoT applications.

&lt;DeviceOperation&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**DeviceOperation**".                                       | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;DeviceOperation&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                      | Mandatory/Optional | May be Null |
|----------------|----------------|----------------------------------------------------------------------------------|--------------------|-------------|
| refDevice      | Reference      | The unique entity Id of the device to which this device operation relates.       | M                  | N           |
| operationType  | Array of Text  | Choice form an enumerated list including:                                        
                                                                                                                     
                                   **event, maintenance, fault, installation, upgrade,other.**                       | O                  | Y           |
| description    | Text           | A description of the operation.                                                  | O                  | Y           |
| result         | Text           | A description of the results of the operation. One of (“**ok**”, “**aborted**”). | O                  | Y           |
| startDate      | DateTime       | The planned start date for the operation.                                        | M                  | Y           |
| endDate        | DateTime       | The planned end date for the operation.                                          | M                  | Y           |
| status         | Text           | A choice from an enumerated list describing the status. One of:                  
                                                                                                                     
                                   **planned, ongoing, finished, scheduled, cancelled.**                             | O                  | Y           |
| operator       | Person         | The operator performing this action encoded as a Schema.org person.              
                                                                                                                     
                                   <https://schema.org/Person>                                                       | O                  | Y           |
| dateStarted    | DateTime       | Timestamp when the operation actually started to be performed.                   | O                  | Y           |
| dateFinished   | DateTime       | Timestamp when the operation actually finished.                                  | O                  | Y           |
| dateReported   | DateTime       | The timestamp when the device event or fault was reported.                       | O                  | Y           |
| dateAddressed  | DateTime       | The timestamp when the event or fault was addressed or cleared.                  | O                  | Y           |

#### DeviceOperation JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/581d2de918e01fb05efd35f27686f361>

{

"id": "27577638-bd8a-4732-b418-fc8b949a0b0f",

"type": "DeviceOperation",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refDevice": {

"value": "2033a7c7-d31b-48e7-91c2-014dc426c29e",

"type": "Reference"

},

"operationType": \[

"fault"

\],

"description": {

"value": "Backup battery needs replacement",

"type": "Text"

},

"result": {

"value": "ok",

"type": "Text"

},

"startDate": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"endDate": {

"value": "2016-08-18T14:18:16Z",

"type": "DateTime"

},

"status": {

"value": "ongoing",

"type": "Text"

},

"operator": {

"value": {

"givenName": "John Dee"

},

"type": "Person"

},

"dateStarted": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"dateFinished": {

"value": "2016-08-18T10:18:16Z",

"type": "DateTime"

},

"dateReported": {

"value": "2016-08-18T10:18:16Z",

"type": "DateTime"

},

"dateAddressed": {

"value": "2016-08-18T10:18:16Z",

"type": "DateTime"

}

}

### EnvironmentObserved

This entity contains a harmonised description of the environmental conditions observed at a particular location and time. This entity is primarily associated with the vertical segment of the environment and agriculture but may also be used in smart home, smart cities, industry and related IoT applications.

&lt;EnvironmentObserved&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**EnvironmentObserved**".                                   | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;EnvironmentObserved&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name          | Attribute Type     | Description                                                                                                                         | Mandatory/Optional | May be Null |
|-------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| location                | geo:json           | The geo:json encoded map location, of this observation.                                                                             | M                  | N           |
| refWeatherObserved      | Array of Reference | An array containing a JSON encoded sequence of characters that reference the unique ids of the related weather entities.            | O                  | Y           |
| refAirQualityObserved   | Array of Reference | An array containing a JSON encoded sequence of characters that reference the unique ids of the related AirQualityObserved entities. | O                  | Y           |
| refWaterQualityObserved | Array of Reference | An array containing a JSON encoded sequence of characters that reference the unique ids of the related WaterQuality entities.       | O                  | Y           |
| measurand               | Array of Text      | An array containing a JSON encoded sequence of characters of the measurand observed.                                                
                                                                                                                                                                                     
                                                **measurand, observedValue, unitcode, description **                                                                                 
                                                                                                                                                                                     
                                                Unitcode defined as in schema.org/QuantitativeValue                                                                                  
                                                                                                                                                                                     
                                                The unit of measurement given using the UN/CEFACT Common Code (3 characters) – the unitcode.                                         
                                                                                                                                                                                     
                                                <http://wiki.goodrelations-vocabulary.org/Documentation/UN/CEFACT_Common_Codes>                                                      
                                                                                                                                                                                     
                                                Possible examples of typical measurands, descriptions and unitcodes are presented below:                                             
                                                                                                                                                                                     
                                                O2. The level of free, non-compound oxygen present. (*M1*)                                                                           
                                                                                                                                                                                     
                                                Hg. The level of compound mercury present. (*M1*)                                                                                    
                                                                                                                                                                                     
                                                NH4. Concentration of ammonium. (*M1*)                                                                                               
                                                                                                                                                                                     
                                                Cl-. Concentration of chlorides. (*M1*)                                                                                              
                                                                                                                                                                                     
                                                NO3-. Concentration of nitrates. (*M1*)                                                                                              
                                                                                                                                                                                     
                                                etc.                                                                                                                                 | O                  | Y           |

#### EnvironmentObserved JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/c393d8082375c9f211ef797d5581c602>

{

"id": "33f02632-74f4-4c96-9ba1-e26945de9481",

"type": "EnvironmentObserved",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"refWeatherObserved": \[

"fae29f4c-0691-4bab-bef8-ad1cd165cc28",

"1c7a2711-ae38-4ea9-8f9f-627067067d53"

\],

"refAirQualityObserved": \[

"4b8b09c9-ce54-46de-8067-5591e02d8f29",

"08a14933-b44d-4297-b2d2-2c3f3844012e"

\],

"refWaterQualityObserved": \[

"68a83e68-61e6-4e3c-975c-5b301c184ca6",

"b01518e3-2b60-4bbd-9783-3af0d660349e"

\],

"measurand": \[

"CO, 500, M1, Carbon Monoxide"

\]

}

###  Machine

This entity contains a harmonised description of an industrial machine for example for use in CAM (Computer Aided Manufacturing). This entity provides an essentially static description of a generic automation machine. This entity is primarily associated with the industry segment in the automated manufacturing industry, including CNC (Computer Numerical Control) machines, 3D printers and all kinds of industrial robots.

&lt;Machine&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**Machine**".                                               | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Machine&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name         | Attribute Type     | Description                                                                                                                              | Mandatory/Optional | May be Null |
|------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refMachineModel        | Reference          | Refers to the machineModel that this machine is an instance of.                                                                          | M                  | N           |
| serialNumber           | Text               | The serial number assigned by the manufacturer.                                                                                          | M                  | N           |
| assetIdentifier        | Text               | An asset identifier (e.g. asset tag number) assigned by the owner.                                                                       | O                  | Y           |
| manufacturerCountry    | Text               | The country where this machine instance was manufactured.                                                                                | O                  | Y           |
| dateManufactured       | DateTime           | The ISO8601 sequence of characters at which the machine was manufactured in UTC.                                                         | M                  | N           |
| dateInstalled          | DateTime           | The ISO8601 sequence of characters at which the machine was installed in UTC.                                                            | M                  | N           |
| dateFirstUsed          | DateTime           | The ISO8601 sequence of characters at which the machine was first used in UTC.                                                           | M                  | N           |
| online                 | Boolean            | Identifies the communication status of the machine, online if set to TRUE.                                                               | O                  | Y           |
| installationNotes      | Text or URL        | Notes relating to this machine installation.                                                                                             | O                  | Y           |
| location               | geo:json           | The geo:json encoded location, of this machine.                                                                                          | M                  | N           |
| refBuilding            | Reference          | Refers to the building instance into which this machine is installed.                                                                    | O                  | Y           |
| owner                  | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s).                                    
                                                                                                                                                                                         
                                               Related to a Schema.org person or organization.                                                                                           
                                                                                                                                                                                         
                                               <https://schema.org/Person>                                                                                                               
                                                                                                                                                                                         
                                               <https://schema.org/Organization>                                                                                                         | O                  | Y           |
| refSubscriptionService | Array of Reference | An array containing a JSON encoded sequence of characters of the unique Ids of any subscription service(s) associated with this machine. | O                  | Y           |
| description            | Text               | An optional description of this machine.                                                                                                 | O                  | Y           |

#### Machine JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/aaa70bd157da04b6246d35525a7ffbcc>

{

"id": "9166c528-9c98-4579-a5d3-8068aea5d6c0",

"type": "Machine",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refMachineModel": {

"value": "00b42701-43e1-482d-aa7a-e2956cfd69c3",

"type": "Reference"

},

"serialNumber": {

"value": "123456789",

"type": "Text"

},

"assetIdentifier": {

"value": "1234567",

"type": "Text"

},

"manufacturerCountry": {

"value": "UK",

"type": "Text"

},

"dateManufactured": {

"value": "2016-08-21T10:18:16Z",

"type": "DateTime"

},

"dateInstalled": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"dateFirstUsed": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"online": {

"value": "TRUE",

"type": "Boolean"

},

"installationNotes": {

"value": "http://www.example.com/installationNote1.txt",

"type": "URL"

},

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"refBuilding": {

"value": "8683b757-649c-49e0-ac89-ad392c9a0d0c",

"type": "Reference"

},

"owner": \[

"247d402f-3e0b-4e7c-a2c0-335590c27f90",

"a7995eb7-6bec-4176-b2e8-af545e2bb3b9"

\],

"refSubscriptionService": \[

"92158a14-f6c6-4d29-85d1-5d305cc87982",

"3c6bac7b-9398-4529-8d89-766435b7490b"

\],

"description": {

"value": "Industrial machine to create plastic bottles",

"type": "Text"

}

}

<span id="_Toc456962957" class="anchor"></span>

###  MachineModel

This entity contains a harmonised description of a generic machine model. This entity is primarily associated with the industry segment and related IoT applications. The machineModel includes a hierarchical structure that allows machine models to be grouped in a flexible way.

&lt;MachineModel&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**MachineModel**".                                          | M                  | N           |
| dateCreated    | Date           | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | Date           | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;MachineModel&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name     | Attribute Type     | Description                                                                                                                                                                             | Mandatory/Optional | May be Null |
|--------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| name               | Text               | The name given to this machine model.                                                                                                                                                   | M                  | N           |
| description        | Text               | A description of this machine model.                                                                                                                                                    | O                  | Y           |
| manufacturerName   | Text               | The name of manufacturer of this machine model.                                                                                                                                         | O                  | Y           |
| brandName          | Text               | A description of this machine model brand name.                                                                                                                                         | O                  | Y           |
| version            | Text               | The manufacturer defined version number for the machine model.                                                                                                                          | O                  | Y           |
| category           | Array of Text      | An array of text based service categories which this machineModel supports. Examples include:                                                                                           
                                                                                                                                                                                                                                    
                                           **robot, cnc, 2dPrinter, 3dPrinter, 3dScanner, lathe, injectionMolding, laserCutter, millingMachine, grindingMachine, stampingMachine, oven, kiln, packaging, mixer, dryer, fan, saw.**  | O                  | Y           |
| doc                | URL                | Reference to Product Data Sheet or other manufacturers documentation about this machine.                                                                                                | O                  | Y           |
| root               | Boolean            | A logical indicator that this machineModel is the root of a machineModel hierarchy. TRUE indicates it is the root, FALSE indicates that it is not the root.                             | O                  | Y           |
| refParentModel     | Array of Reference | An array containing a JSON encoded sequence of characters referencing the ids of other machine models which this is related to.                                                         | O                  | Y           |
| processDescription | Text               | A description of the industrial process carried out by this machine.                                                                                                                    | O                  | Y           |
| standardOperations | Array of Text      | Lists the standard set of operations supported by this machineModel.                                                                                                                    | O                  | Y           |

#### MachineModel JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/10d7c9ffca1e4d1e498203f85dc0991d>

{

"id": "e01f13d1-fea4-4cc4-92c9-0d9fadb2c509",

"type": "MachineModel",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"name": {

"value": "CA1256b",

"type": "Text"

},

"description": {

"value": "Machine to screen print t-shirts",

"type": "Text"

},

"manufacturerName": {

"value": "ScreenOPrint, Inc.",

"type": "Text"

},

"brandName": {

"value": "QuickT",

"type": "Text"

},

"version": {

"value": "v1",

"type": "Text"

},

"category": \[

"2dPrinter"

\],

"doc": {

"value": "http://www.example.com",

"type": "URL"

},

"root": {

"value": "FALSE",

"type": "Boolean"

},

"refParentModel": \[

"4146335f-839f-4ff9-a575-6b4e6232b734",

"c44fc765-51a7-4f71-bf1e-22e874c35180"

\],

"processDescription": {

"value": "Industrial printer used to mass print t-shirts",

"type": "Text"

},

"standardOperations": \[

"print"

\]

}

### MachineOperation

This entity contains a harmonised description of a generic machine operation. This entity is primarily associated with the industry segment and related IoT applications. Each MachineOperation instance will be related to a specific Machine instance.

&lt;MachineOperation&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**MachineOperation**".                                      | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;MachineOperation&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name  | Attribute Type | Description                                                                                                                                      | Mandatory/Optional | May be Null |
|-----------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refMachine      | Reference      | Refers to the specific machine instance that this machineOperation record relates to.                                                            | M                  | N           |
| operationType   | Text           | Defines the type of operation conducted/ requested. This will be one of a defined list of operation types specific to the machine/ machineModel. | M                  | N           |
| description     | Text           | A description of the operation conducted or applied.                                                                                             | O                  | Y           |
| result          | Text           | A description of the results of the operation. One of (“**ok**”, “**aborted**”).                                                                 | O                  | Y           |
| startDate       | DateTime       | The planned start date for the operation.                                                                                                        | M                  | Y           |
| endDate         | DateTime       | The planned end date for the operation.                                                                                                          | M                  | Y           |
| status          | Text           | A choice from an enumerated list describing the status. One of:                                                                                  
                                                                                                                                                                                      
                                    **planned, ongoing, finished, scheduled, cancelled.**                                                                                             | O                  | Y           |
| operator        | Person         | The operator performing this action encoded as a Schema.org person.                                                                              
                                                                                                                                                                                      
                                    <https://schema.org/Person>                                                                                                                       | O                  | Y           |
| dateStarted     | DateTime       | Timestamp when the operation actually started to be performed.                                                                                   | O                  | Y           |
| dateFinished    | DateTime       | Timestamp when the operation actually finished.                                                                                                  | O                  | Y           |
| commandSequence | Text           | The command sequence executed/ requested for the machine in a representation format relevant to the machine.                                     | O                  | Y           |

#### MachineOperation JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/a2a2795c194831ac06c48222eb49e2ce>

{

"id": "27577638-bd8a-4732-b418-fc8b949a0b0f",

"type": "MachineOperation",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refMachine": {

"value": "2033a7c7-d31b-48e7-91c2-014dc426c29e",

"type": "Reference"

},

"operationType": {

"value": "tShirtPrint",

"type": "Text"

},

"description": {

"value": "Printing of 1000 T-shirts",

"type": "Text"

},

"result": {

"value": "ok",

"type": "Text"

},

"startDate": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"endDate": {

"value": "2016-08-18T14:18:16Z",

"type": "DateTime"

},

"status": {

"value": "finished",

"type": "Text"

},

"operator": {

"value": {

"name": "Fred Quimby",

"jobTitle": "Print Supervisor"

},

"type": "Person"

},

"dateStarted": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"dateFinished": {

"value": "2016-08-18T14:18:16Z",

"type": "DateTime"

},

"commandSequence": {

"value": "Select inks. Prepare print masks. Print shirts. Clean print heads and rollers ",

"type": "Text"

}

}

### PointOfInterest

<span id="_Toc437780036" class="anchor"><span id="_Toc51656806" class="anchor"><span id="_Toc74460304" class="anchor"></span></span></span>This entity contains a harmonised geographic description of a Point of Interest. This entity is used in applications that use spatial data and is applicable to Automotive, Environment, Industry and Smart City vertical segments and related IoT applications.

&lt;PointOfInterest&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**PointOfInterest**".                                       | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;PointOfInterest&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                                                                                                                                                                                                                                                      | Mandatory/Optional | May be Null |
|----------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| location       | geo:json       | The geo:json encoded map location (point or polygon), of this point of interest.                                                                                                                                                                                                                                 | M                  | N           |
| category       | Array          | A JSON encoded array of one or more sequence of characters describing categories associated with this point of interest. A choice from: **church, school, town hall, distinctiveBuilding, postOffice, shop, postBox, telephoneBox, pub, car park, lay-bye, speedCamera, restaurant, tourist attraction, other.** | M                  | Y           |
| description    | Text           | An optional description of the entity.                                                                                                                                                                                                                                                                           | O                  | Y           |
| place          | Place          | The schema.org place definition for this Point Of Interest. See <https://schema.org/Place>                                                                                                                                                                                                                       | O                  | Y           |

#### PointOfInterest JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/d9f9c492f06a96e6c6b06938002a3505>

{

"id": "44e47705-90c3-4dbc-a0ae-7810306de5e9",

"type": "PointOfInterest",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"category": \[

"school"

\],

"description": {

"value": "Learn all about mobile at the GSMA Academy",

"type": "Text"

},

"place": {

"type": "Place",

"value": {

"name": "GSMA Academy",

"address": {

"type": "PostalAddress",

"addressLocality": "London",

"postalCode": "EC4N 8AF",

"streetAddress": "25 Walbrook"

},

"telephone": "0212345678"

}

}

}

### Road

This entity contains a harmonised geographic and contextual description of a Road. Roads are made up of one or more RoadSegment entities. This entity is primarily associated with the Automotive and Smart City vertical segments and related IoT applications.

&lt;Road&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**Road**".                                                  | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Road&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                                                         | Mandatory/Optional | May be Null |
|----------------|--------------------|---------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refRoadSegment | Array of Reference | A JSON encode sequence of characters referencing the unique ids of the group of roadSegments that define this road. | M                  | Y           |
| roadClass      | Text               | The official classification of this road.                                                                           | M                  | Y           |
| name           | Text               | The official designation of this road.                                                                              | M                  | Y           |
| alternateName  | Text               | An alternative name for this road.                                                                                  | O                  | Y           |

#### Road JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/fce0066af2ef3aad51eb20a139501303>

{

"id": "19b6f4b7-a9b4-4114-8391-3133bf96aedc",

"type": "Road",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refRoadSegment": \[

"2a982120-4d98-425b-a8db-1de5563db6a8",

"43e255c7-262e-4d6d-95a1-69a53e37dcc0"

\],

"roadClass": {

"value": "Dual Carriageway",

"type": "Text"

},

"name": {

"value": "M1",

"type": "Text"

},

"alternateName": {

"value": "M1 Motorway",

"type": "Text"

}

}

### RoadSegment

This entity contains a harmonised geographic and contextual description of a RoadSegment. A collection of RoadSegments are used to describe a Road. This entity is primarily associated with the Automotive and Smart City vertical segments and related IoT applications.

&lt;RoadSegment&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**RoadSegment**".                                           | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;RoadSegment&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name     | Attribute Type     | Description                                                                                                                      | Mandatory/Optional | May be Null |
|--------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| startPoint         | geo:json           | The start point of this RoadSegment.                                                                                             | M                  | N           |
| endPoint           | geo:json           | The end point of this RoadSegment.                                                                                               | M                  | N           |
| roadClass          | Text               | The official classification of the road that this roadSegment is a part of.                                                      | M                  | Y           |
| name               | Text               | The official designation of the road that this roadSegment is a part of.                                                         | M                  | Y           |
| location           | geo:json           | A geo:json line sequence containing all the points that make up this RoadSegment.                                                | M                  | Y           |
| refPointofInterest | Array of Reference | An array containing a JSON encoded sequence of characters referencing the Ids of the points of interest along this road segment. | O                  | Y           |

#### RoadSegment JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/feebdab56255971124c8236ec8c44528>

{

"id": "27109fe0-0c60-4302-a9eb-e7065eca876e",

"type": "RoadSegment",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"startPoint": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"endPoint": {

"value": {

"type": "Point",

"coordinates": \[

-109.99404,

32.75621

\]

},

"type": "geo:json"

},

"roadClass": {

"value": "Single Carriageway",

"type": "Text"

},

"name": {

"value": "A123",

"type": "Text"

},

"location": {

"value": {

"type": "LineString",

"coordinates": \[

\[-102.98, 32.75\],

\[-103.99, 30.75\],

\[-103.99, 31.75\]

\]

},

"type": "geo:json"

},

"refPointofInterest": \[

"4d798319-22b1-4714-b847-b81dbba3357b",

"1909a43d-e5a1-46cb-bbd0-7cc16bc4fa33"

\]

}

### Subscriber

This entity contains a harmonised description of a subscriber to a service. This entity is primarily associated with the Smart Home vertical segment and related IoT applications.

&lt;Subscriber&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**Subscribe**r".                                            | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Subscriber&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name       | Attribute Type     | Description                                                                                                                                                  | Mandatory/Optional | May be Null |
|----------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| subscriptionId       | Reference          | A reference to the unique id of the subscription service.                                                                                                    | M                  | N           |
| startDate            | DateTime           | The start date time for this subscription as an ISO8601 sequence of characters in UTC.                                                                       | O                  | Y           |
| endDate              | DateTime           | The end date time for this subscription as an ISO8601 sequence of characters in UTC.                                                                         | O                  | Y           |
| duration             | Number             | The duration of the subscription in calendar months.                                                                                                         | O                  | Y           |
| category             | Array of Text      | The category of subscription. A selection from an enumerated list including:                                                                                 
                                                                                                                                                                                                           
                                             **prepay, postpay, utility, broadband, electric, gas, heat, water, landline, mobile, tv, security, financial, energy management, other.**                     | O                  | Y           |
| averageMonthly Usage | Number             | Average monthly usage of the subscription service.                                                                                                           | O                  | Y           |
| subscribed           | Array of Reference | An array containing a JSON encoded sequence of characters referencing the unique ids of those persons or organisations that have subscribed to this service. 
                                                                                                                                                                                                           
                                             Related to a Schema.org person or organization.                                                                                                               
                                                                                                                                                                                                           
                                             <https://schema.org/Person>                                                                                                                                   
                                                                                                                                                                                                           
                                             <https://schema.org/Organization>                                                                                                                             | O                  | Y           |

#### Subscriber JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/a2be9b6079309c8ea2d7a6830c31c306>

{

"id": "c1716dea-6a4d-4171-a733-916123942f09",

"type": "Subscriber",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"subscriptionId": {

"value": "65b1ccb0-ee32-41c1-9746-7ba83fb0f0f1",

"type": "Reference"

},

"startDate": {

"value": "2016-08-22T10:18:16Z",

"type": "DateTime"

},

"endDate": {

"value": "2016-08-28T10:18:16Z",

"type": "DateTime"

},

"duration": {

"value": 12,

"type": "Number"

},

"category": \[

"utility"

\],

"averageMonthlyUsage": {

"value": 28,

"type": "Number"

},

"subscribed": \[

"31dd0e29-45b6-476f-9756-a70f8141dcf3"

\]

}

### SubscriptionService

This entity contains a harmonised description of a subscription service. This entity is primarily associated with the Smart Home vertical segment and related IoT applications.

&lt;SubscriptionService&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**SubscriptionService**".                                   | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;SubscriptionService&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type | Description                      | Mandatory/Optional | May be Null |
|----------------|----------------|----------------------------------|--------------------|-------------|
| description    | Text           | The description of this service. | M                  | N           |
| offer          | Offer          | Encoded as Schema.org offer.     
                                                                     
                                   <https://schema.org/Offer>        | M                  | Y           |

#### SubscriptionService JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/1631ff51b1aa49a0422741f9b5631ecf>

{

"id": "a1e76f95-c627-4ec4-86dc-483431d25352",

"type": "SubscriptionService",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"description": {

"value": "Broadband supply service",

"type": "Text"

},

"offer": {

"type": "Offer",

"value" : {

"priceCurrency": "USD",

"price": 1000,

"description": "100 mbps fibre broadband service"

}

}

}

### Vehicle

This entity contains a harmonised description of a Vehicle. This entity is primarily associated with the Automotive vertical segment but might also be relevant to Industry, Smart City and Agriculture related IoT applications. Where practicable <https://schema.org/Vehicle> naming conventions have been adopted.

&lt;Vehicle&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**Vehicle**".                                               | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Vehicle&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name              | Attribute Type                | Description                                                                                                                                                                                                                                           | Mandatory/Optional | May be Null |
|-----------------------------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refVehicleType              | Array of Reference            | A JSON encode sequence of characters referencing the Id of the vehicleType entity which describes this vehicle in more detail.                                                                                                                        | M                  | N           |
| fuelType                    | Text                          | A choice from an enumerated list describing the power source. One of: **gasoline, petrol(unleaded), petrol(leaded), petrol, diesel, electric, hydrogen, lpg autogas, cng, biodiesel, ethanol, hybrid electric/petrol, hybrid electric/diesel, other** | M                  | N           |
| displacement                | Number                        | A number indicating the cylinder capacity of the engine in litres                                                                                                                                                                                     | O                  | Y           |
| fuelEconomy                 | Number                        | A number indicating the fuel economy index.                                                                                                                                                                                                           | O                  | Y           |
| vehicleModelDate            | DateTime                      | The ISO8601 sequence of characters indicating the year of release.                                                                                                                                                                                    | O                  | Y           |
| dateDiscontinued            | DateTime                      | The ISO8601 sequence of characters indicating the year which the vehicle was discontinued.                                                                                                                                                            | O                  | Y           |
| vechileIdentificationNumber | Text                          | The VIN (vehicle identification number) of the vehicle.                                                                                                                                                                                               | O                  | Y           |
| mileageFromOdometer         | ExtQuantitativeValue (Number) | The total distance the car has travelled according to the on-board odometer in kilometres or miles,                                                                                                                                                   
                                                                                                                                                                                                                                                                                                                      
                                                               references Schema.org Vehicle/ mileageFromOdometer.                                                                                                                                                                                                    | O                  | Y           |

#### Vehicle JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/f28833b6c5c51c3e79fa6f7dfa1a7864>

{

"id": "1fa179a6-b507-4857-ad72-eb5513ef05c6",

"type": "Vehicle",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refVehicleType": \[

"23821045-33d4-46ec-b777-98f461bf4856",

"2ff57791-ebfb-4086-ab61-60b5beed605d"

\],

"fuelType": {

"value": "Diesel",

"type": "Text"

},

"displacement": {

"value": 3,

"type": "Number"

},

"fuelEconomy": {

"value": 22,

"type": "Number"

},

"vehicleModelDate": {

"value": "2016-08-18T10:18:16Z",

"type": "DateTime"

},

"dateDiscontinued": {

"value": "2016-08-23T10:18:16Z",

"type": "DateTime"

},

"vehicleIdentificationNumber": {

"value": "2T2GK31U08C041124",

"type": "Text"

},

"mileageFromOdometer": {

"value": {

"value": 33015,

"unitCode": "NMI"

},

"type": "ExtQuantitativeValue"

}

}

### VehicleFault

This entity contains a harmonised description of a Vehicle Fault. This entity is primarily associated with the Automotive vertical segment but might also be relevant to Industry, Smart City and Agriculture related IoT applications.

&lt;VehicleFault&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**VehicleFault**".                                          | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;VehicleFault&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type     | Description                                                                                                                                                | Mandatory/Optional | May be Null |
|----------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refVehicle     | Array of Reference | A JSON encode sequence of characters referencing the Id of the vehicle in which this fault occurred.                                                       | M                  | N           |
| dateDetected   | DateTime           | An ISO8601 sequence of characters indicating the date and time the fault was detected.                                                                     | M                  | N           |
| eventType      | Text               | The event type descriptor, a choice from an enumerated list including:                                                                                     
                                                                                                                                                                                                   
                                       **collision, emergency, harshAccel, harshDecel, auxBatteryWarn, milWarn**.                                                                                  | M                  | N           |
| location       | geo:json           | The geo location where the fault was detected.                                                                                                             | M                  | Y           |
| processingType | Text               | Indicates how the fault was dealt with, e.g. **systemHandled,** or not present if the issue has not been resolved.                                         | O                  | Y           |
| dateProcessed  | DateTime           | The ISO8601 sequence of characters indicating the data and time at which the issue was solved, or not present if the issue has not been resolved.          | O                  | Y           |
| dtCode         | Text               | DTC or Diagnostic Trouble Codes are codes generated by the vehicle's computer diagnostic system. These may be manufacturer, equipment or vehicle specific. | O                  | Y           |
| faultLog       | Text               | Free text that records information about the initial fault incident, ongoing updates and fault resolution.                                                 | O                  | Y           |

#### VehicleFault JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/2e40b95654493bc44cabe360e9c3f82d>

{

"id": "4939200a-5ef5-4266-8c91-1f82ad3b543b",

"type": "VehicleFault",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refVehicle": \[

"e64a2ecb-a8ae-4f51-ab66-2e9729c02d22"

\],

"dateDetected": {

"value": "2016-08-20T10:18:16Z",

"type": "DateTime"

},

"eventType": {

"value": "emergency",

"type": "Text"

},

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"processingType": {

"value": "systemHandled",

"type": "Text"

},

"dateProcessed": {

"value": "2016-08-21T10:18:16Z",

"type": "DateTime"

},

"dtCode": {

"value": "EMERG-1234-a",

"type": "Text"

},

"faultLog": {

"value": "Emergency stop. Fault with engine",

"type": "Text"

}

}

### VehicleType

This entity contains a harmonised description of a vehicleType it forms part of the description of a Vehicle. This entity is primarily associated with the Automotive vertical segment but might also be relevant to Industry, Smart City and Agriculture related IoT applications. Where practicable <https://schema.org/Vehicle> naming conventions have been adopted.

&lt;VehicleType&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**VehicleType**".                                           | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;VehicleType&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type | Description                    | Mandatory/Optional | May be Null |
|----------------|----------------|--------------------------------|--------------------|-------------|
| model          | Text           | The vehicle model identifier.  | M                  | N           |
| category       | Text           | The vehicle class identifier.  | M                  | N           |
| manufacturer   | Text           | The manufacturer’s identifier. | M                  | N           |

#### VehicleType JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/7be3126e94779c6467fb56e1b3b0935d>

{

"id": "33253089-9cea-4227-889e-61950965f6f9",

"type": "VehicleType",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"model": {

"value": "M Class",

"type": "Text"

},

"category": {

"value": "SUV",

"type": "Text"

},

"manufacturer": {

"value": "Mercedes Benz",

"type": "Text"

}

}

### WaterQualityObserved

This entity contains a harmonised description of the water quality at a particular location and time. This entity is primarily associated with the vertical segments of agricultural and environment and related IoT applications.

&lt;WaterQualityObserved&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**WaterQualityObserved**".                                  | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;WaterQualityObserved&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name | Attribute Type                 | Description                                                                                                                         | Mandatory/Optional | May be Null |
|----------------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| refDevice      | Array of Reference             | A reference to the unique entity Ids of the devices that originated this observation data.                                          | M                  | N           |
| location       | geo:json                       | The geo:json encoded map location, that is related to this observation.                                                             | M                  | N           |
| dateObserved   | DateTime                       | The date and time of this observation in ISO8601 UTCformat.                                                                         | M                  | N           |
| measurand      | Array of Text                  | An array containing a JSON encoded sequence of characters of the measurand observed.                                                
                                                                                                                                                                                        
                                                   **measurand, valueObserved, unitcode, description.**                                                                                 
                                                                                                                                                                                        
                                                   Unitcode defined as in schema.org/QuantitativeValue                                                                                  
                                                                                                                                                                                        
                                                   The unit of measurement given using the UN/CEFACT Common Code (3 characters) – the unitcode.                                         
                                                                                                                                                                                        
                                                   <http://wiki.goodrelations-vocabulary.org/Documentation/UN/CEFACT_Common_Codes>                                                      
                                                                                                                                                                                        
                                                   see example below:                                                                                                                   
                                                                                                                                                                                        
                                                   **"O2, 50,M1,The level of free non-compound oxygen present"**                                                                        
                                                                                                                                                                                        
                                                   Possible examples of typical measurands, descriptions and unitcodes are presented below:                                             
                                                                                                                                                                                        
                                                   **O2. The level of free non-compound oxygen present. (*M1*) **                                                                       
                                                                                                                                                                                        
                                                   **CO. The level of free non-compound carbon monoxide present. (*M1*)**                                                               
                                                                                                                                                                                        
                                                   **CO2. The level of free non-compound carbon dioxide present. (*M1*)**                                                               
                                                                                                                                                                                        
                                                   **Hg. The level of compound mercury present. (*M1*)**                                                                                
                                                                                                                                                                                        
                                                   **Chla. Concentration of chlorophyll A. (*H29*)**                                                                                    
                                                                                                                                                                                        
                                                   **PE. Concentration of pigment *phycoerythrin* which can be measured to estimate cyanobacteria concentrations specifically.(H29)**   
                                                                                                                                                                                        
                                                   **PC. Concentration of pigment *phycocyanin* which can be measured to estimate cyanobacteria concentrations specifically. (*H29*)**  
                                                                                                                                                                                        
                                                   **NH4. Concentration of ammonium. (*M1*)**                                                                                           
                                                                                                                                                                                        
                                                   **NH3. Concentration of ammonia. (*M1*)**                                                                                            
                                                                                                                                                                                        
                                                   **Cl-. Concentration of chlorides. (*M1*)**                                                                                          
                                                                                                                                                                                        
                                                   **NO3-. Concentration of nitrates. (*M1*)**                                                                                          
                                                                                                                                                                                        
                                                   etc.                                                                                                                                 | O                  | Y           |
| depth          | ExtQuantitativeValue (Number)  | Depth where the observation was taken. (*m*) encoded as a ExtQuantitativeValue.                                                     | O                  | Y           |
| pressure       | ExtQuantitativeValue (Number)  | Hydrostatic pressure where the observation was taken. (Pa) encoded as a ExtQuantitativeValue.                                       | O                  | Y           |
| conductivity   | ExtQuantitativeValue (Number)  | Electrical conductivity. (*S/m*) encoded as a ExtQuantitativeValue.                                                                 | O                  | Y           |
| conductance    | ExtQuantitativeValue (Number)  | Specific conductivity / 25 ºC /. (*S/m*) encoded as a ExtQuantitativeValue.                                                         | O                  | Y           |
| temperature    | ExtQuantitativeValue (Number)  | The temperature expressed in degrees Celsius encoded as a ExtQuantitativeValue.                                                     | O                  | Y           |
| tss            | ExtQuantitativeValue (Number)r | Total suspended solids. (*M1*) encoded as a ExtQuantitativeValue                                                                    | O                  | Y           |
| tds            | ExtQuantitativeValue (Number)  | Total dissolved solids. (*M1*) encoded as a ExtQuantitativeValue.                                                                   | O                  | Y           |
| turbidity      | ExtQuantitativeValue (Number)  | Amount of light scattered by particles in the water column. (*FTU*). encoded as a ExtQuantitativeValue.                             | O                  | Y           |
| salinity       | ExtQuantitativeValue (Number)  | Derived from the conductivity measurement. (*parts per thousand, ppt*) encoded as a ExtQuantitativeValue.                           | O                  | Y           |
| pH             | ExtQuantitativeValue (Number)  | pH measurement (typically a number between *0 and 14*) encoded as a ExtQuantitativeValue.                                           | O                  | Y           |
| orp            | ExtQuantitativeValue (Number)  | Oxidation-Reduction potential (*mV*) encoded as a ExtQuantitativeValue.                                                             | O                  | Y           |
| cdom           | ExtQuantitativeValue (Number)  | Color dissolved organic matter (*RFU*) encoded as a ExtQuantitativeValue.                                                           | O                  | Y           |

#### WaterQualityObserved JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/5252d6628d7a06472c7e7fc366b7ee23>

{

"id": "72a30ca8-888e-49a2-8d8d-a5bebc19e98b",

"type": "WaterQualityObserved",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"refDevice": \[

"2033a7c7-d31b-48e7-91c2-014dc426c29e"

\],

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"dateObserved": {

"value": "2016-08-16T10:18:16Z",

"type": "DateTime"

},

"measurand": \[

"O2, 50, M1, Oxygen concentration"

\],

"depth": {

"value": {

"value": 4,

"unitCode": "MTR"

},

"type": "ExtQuantitativeValue"

},

"pressure": {

"value": {

"value": 10202,

"unitCode": "PAL"

},

"type": "ExtQuantitativeValue"

},

"conductivity": {

"value": {

"value": 10,

"unitCode": "D10"

},

"type": "ExtQuantitativeValue"

},

"conductance": {

"value": {

"value": 25,

"unitCode": "D10"

},

"type": "ExtQuantitativeValue"

},

"temperature": {

"value": {

"value": 15,

"unitCode": "CEL"

},

"type": "ExtQuantitativeValue"

},

"tss": {

"value": {

"value": 200,

"unitCode": "M1"

},

"type": "ExtQuantitativeValue"

},

"tds": {

"value": {

"value": 150,

"unitCode": "M1"

},

"type": "ExtQuantitativeValue"

},

"turbidity": {

"value": {

"value": 343,

"unitCode": "FTU"

},

"type": "ExtQuantitativeValue"

},

"salinity": {

"value": {

"value": 220

},

"type": "ExtQuantitativeValue"

},

"pH": {

"value": {

"value": 5

},

"type": "ExtQuantitativeValue"

},

"orp": {

"value": {

"value": 225,

"unitCode": "2Z"

},

"type": "ExtQuantitativeValue"

},

"cdom": {

"value": {

"value": 22,

"unitCode": "RFU"

},

"type": "ExtQuantitativeValue"

}

}

### WeatherForecast

This entity contains a harmonised description of a Weather Forecast. This entity is primarily associated with the vertical segments of the environment and agriculture but is applicable to many different applications.

&lt;WeatherForecast&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**WeatherForecast**".                                       | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;WeatherForecast&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name           | Attribute Type     | Description                                                                                                                                                                                                                                                                | Mandatory/Optional | May be Null |
|--------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| location                 | geo:json           | The geo:json encoded map location (point or polygon), of this weather forecast.                                                                                                                                                                                            | M                  | N           |
| dateRetrieved            | DateTime           | The date and time the forecast was retrieved in ISO8601 UTC format.                                                                                                                                                                                                        | M                  | N           |
| dateIssued               | DateTime           | The date and time the forecast was issued by the meteorological bureau in ISO8601 UTC format.                                                                                                                                                                              |                    |             |
| weatherType              | Text               | The weather type. A choice from an enumerated list. One of:                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                             
                                                 **notAvailable, clearNight, sunnyDay, partlyCloudy, mist, fog, cloudy, overcast, lightRainShower, drizzle, lightRain, heavy RainShower, heavyRain, sleetShower, sleet, hailShower, hail, lightSnow Shower, lightSnow, heavySnowShower,heavySnow, thunderShower, thunder.**  | M                  | N           |
| visibility               | Text               | A choice from an enumerated list. One of:                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                             
                                                 **unknown, veryPoor, poor, moderate, good, veryGood, excellent.**                                                                                                                                                                                                           | M                  | N           |
| name                     | Text               | The name of the weather forecast location.                                                                                                                                                                                                                                 | M                  | Y           |
| validity                 | Text               | Includes the validity period for this forecast as a date/time range as a textvalue.                                                                                                                                                                                        
                                                                                                                                                                                                                                                                                                                             
                                                 The **validity** is in the form of                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                                             
                                                 **validFrom/validTo**                                                                                                                                                                                                                                                       
                                                                                                                                                                                                                                                                                                                             
                                                 **validFrom** -- The date and time the forecast is valid from expressed as an ISO8601 UTC format sequence of characters.                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                             
                                                 **validTo**: The date and time the forecast is valid to expressed as an ISO8601 UTC format sequence of characters. For example:                                                                                                                                             
                                                                                                                                                                                                                                                                                                                             
                                                 **YYYY-MM-DDThh:mmZ/YYYY-MM-DDThh:mmZ**                                                                                                                                                                                                                                     | O                  | Y           |
| dayMinimum               | Array of text      | Includes the attribute, value tuples:                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                             
                                                 **temperature, feelsLikeTemperature, relativeHumidity**                                                                                                                                                                                                                     
                                                                                                                                                                                                                                                                                                                             
                                                 **temperature** -- The forecasted minimum temperature for the period in degrees Celsius.                                                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                             
                                                 **feelsLikeTemperature** – The forecasted feels like temperature for the period in degrees Celsius.                                                                                                                                                                         
                                                                                                                                                                                                                                                                                                                             
                                                 **relativeHumidity** -- The relative humidity expressed a number between 0 ≤ RelativeHumidity ≤ 1.                                                                                                                                                                          | O                  | Y           |
| dayMaximum               | Array of Text      | Includes the attribute, value tuples:                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                             
                                                 **temperature, feelsLikeTemperature, relativeHumidity**                                                                                                                                                                                                                     
                                                                                                                                                                                                                                                                                                                             
                                                 temperature -- The forecasted maximum temperature for the period in degrees Celsius.                                                                                                                                                                                        
                                                                                                                                                                                                                                                                                                                             
                                                 feelsLikeTemperature – The forecasted feels like temperature for the period in degrees Celsius.                                                                                                                                                                             
                                                                                                                                                                                                                                                                                                                             
                                                 relativeHumidity -- The relative humidity expressed a number between 0 ≤ RelativeHumidity ≤ 1.                                                                                                                                                                              | O                  | Y           |
| address                  | PostalAddress      | The weather forecast location encoded as a Schema.org PostalAddress.                                                                                                                                                                                                       
                                                                                                                                                                                                                                                                                                                             
                                                 [https://schema.org/PostalAddress](https://schema.org/Address)                                                                                                                                                                                                              | M                  | Y           |
| temperature              | Number             | The temperature expressed in degrees Celsius.                                                                                                                                                                                                                              | M                  | Y           |
| windDirection            | Number             | The wind direction expressed in degrees compared to geographic North (measured clockwise).                                                                                                                                                                                 | O                  | Y           |
| windSpeed                | Number             | The forecasted wind speed in m/s.                                                                                                                                                                                                                                          | O                  | Y           |
| uVIndexMax               | Number             | The maximum UV index for the period, based on the World Health Organization's UV Index measure.                                                                                                                                                                            | O                  | Y           |
| relativeHumidity         | Number             | The relative humidity expressed a number between                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                             
                                                 0 ≤ RelativeHumidity ≤ 1.                                                                                                                                                                                                                                                   | O                  | Y           |
| precipitationProbability | Number             | The probability of precipitation, expressed as a number between                                                                                                                                                                                                            
                                                                                                                                                                                                                                                                                                                             
                                                 0 ≤ precipitationProbability ≤ 1.                                                                                                                                                                                                                                           | O                  | Y           |
| refPointOfInterest       | Array of Reference | A JSON encode sequence of characters referencing the unique ids of the associated group of pointOfInterests.                                                                                                                                                               | O                  | Y           |

#### WeatherForecast JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/c7beae7a0e9797d2358db6cf1c190fc2>

{

"id": "7453c443-290d-44ef-a60f-d4c087010c88",

"type": "WeatherForecast",

"dateCreated": {

"value": "2016-08-08 T10:18:16Z ",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"dateRetrieved": {

"value": "2016-08-16T10:18:16Z",

"type": "DateTime"

},

"dateIssued": {

"value": "2016-08-10T10:18:16Z",

"type": "DateTime"

},

"weatherType": {

"value": "sunnyDay",

"type": "Text"

},

"visibility": {

"value": "Good",

"type": "Text"

},

"name": {

"value": "London City",

"type": "Text"

},

"validity": {

"value": "2016-08-10T10:18:16Z/2016-08-29T10:18:16Z",

"type": "Text"

},

"dayMinimum": \[

"temperature, 30, CEL",

"feelsLikeTemperature, 32, CEL",

"relativeHumidity, 0.22, P1"

\],

"dayMaximum": \[

"temperature, 33, CEL",

"feelsLikeTemperature, 328, CEL",

"relativeHumidity, 0.52, P1"

\],

"address": {

"type": "PostalAddress",

"value": {

"addressLocality": "London",

"postalCode": "EC4N 8AF",

"streetAddress": "25 Walbrook"

}

},

"temperature": {

"value": 30,

"type": "Number"

},

"windDirection": {

"value": 122,

"type": "Number"

},

"windSpeed": {

"value": 3,

"type": "Number"

},

"uVIndexMax": {

"value": 5,

"type": "Number"

},

"relativeHumidity": {

"value": 0.1,

"type": "Number"

},

"precipitationProbability": {

"value": 0.05,

"type": "Number"

},

"refPointOfInterest": \[

"d0d88168-780c-11e6-b934-2b9831af3c6f"

\]

}

### WeatherObserved

This entity contains a harmonised description of the weather at a particular location and time. This entity is primarily associated with the vertical segments of the environment and agriculture but is applicable to many different applications.

&lt;WeatherObserved&gt;&lt;Generic Attributes&gt;

| Attribute Name | Attribute Type | Description                                                                   | Mandatory/Optional | May be Null |
|----------------|----------------|-------------------------------------------------------------------------------|--------------------|-------------|
| id             | Text           | Unique id of this instance of this entity.                                    | M                  | N           |
| type           | Text           | Must be equal to "**WeatherObserved**".                                       | M                  | N           |
| dateCreated    | DateTime       | Entity creation timestamp.                                                    | M                  | N           |
| dateModified   | DateTime       | Timestamp of the last modification of the entity.                             | M                  | Y           |
| source         | Text           | A sequence of characters giving the source of the entity data as a URL.       | M                  | Y           |
| dataProvider   | Text           | A sequence of characters identifying the originator of the harmonised entity. | M                  | Y           |

&lt;Weather Observed&gt;&lt;Entity Specific Attributes&gt;

| Attribute Name      | Attribute Type                          | Description                                                                                                                                                                                                                                                                                                                            | Mandatory/Optional | May be Null |
|---------------------|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------|
| location            | geo:json                                | The geo:json encoded map location (point or polygon), of this weather observation.                                                                                                                                                                                                                                                     | M                  | N           |
| refDevice           | Array of Reference                      | Reference to the unique ids of the device(s) which captured this weather observation.                                                                                                                                                                                                                                                  | O                  | Y           |
| dateObserved        | DateTime                                | The date and time of this weather observation in ISO8601 UTCformat.                                                                                                                                                                                                                                                                    | M                  | N           |
| weatherType         | Text                                    | The weather type. A choice from an enumerated list. One of: **notAvailable, clearNight, sunnyDay, partlyCloudy, mist, fog, cloudy, overcast, lightRainShower, drizzle, lightRain, heavy RainShower, heavyRain, sleetShower, sleet, hailShower, hail, lightSnow Shower, lightSnow, heavySnowShower, heavySnow, thunderShower, thunder** | M                  | N           |
| visibility          | Text                                    | A choice from an enumerated list. One of **unknown, veryPoor, poor, moderate, good, veryGood, excellent.**                                                                                                                                                                                                                             | M                  | N           |
| name                | Text                                    | The name of the weather observed location.                                                                                                                                                                                                                                                                                             | M                  | Y           |
| address             | PostalAdresss                           | The weather observed location encoded as a Schema.org Postal Address.                                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                 [https://schema.org/PostalAddress](https://schema.org/Address)                                                                                                                                                                                                                                                                          | M                  | Y           |
| temperature         | Number Or ExtQuantitativeValue (Number) | The recorded temperature expressed in degrees Celsius, encoded as a Number OR a ExtQuantitativeValue.                                                                                                                                                                                                                                  | M                  | Y           |
| refPointOfInterest  | Array of Reference                      | A JSON encode sequence of characters referencing the unique ids of the associated group of pointOfInterests.                                                                                                                                                                                                                           | O                  | Y           |
| windDirection       | Number Or ExtQuantitativeValue (Number) | The wind direction expressed in degrees compared to geographic North (measured clockwise), encoded as a Number OR a ExtQuantitativeValue.                                                                                                                                                                                              | O                  | Y           |
| windSpeed           | Number Or ExtQuantitativeValue (Number) | The observed wind speed in m/s, encoded as a Number OR a ExtQuantitativeValue.                                                                                                                                                                                                                                                         | O                  | Y           |
| relativeHumidity    | Number Or ExtQuantitativeValue (Number) | The relative humidity expressed a number between                                                                                                                                                                                                                                                                                       
                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                 0 ≤ RelativeHumidity ≤ 1, encoded as a Number OR a ExtQuantitativeValue.                                                                                                                                                                                                                                                                | O                  | Y           |
| dewPoint            | Number Or ExtQuantitativeValue (Number) | The dew point in degrees Celsius, encoded as a Number OR a ExtQuantitativeValue.                                                                                                                                                                                                                                                       | O                  | Y           |
| atmosphericPressure | Number Or ExtQuantitativeValue (Number) | The atmospheric pressure in units of Pascal, encoded as a Number OR a ExtQuantitativeValue.                                                                                                                                                                                                                                            | O                  | Y           |
| pressureTendency    | Text Or ExtQuantitativeValue(Text)      | Is the pressure is rising or falling, encoded as Text OR a ExtQuantitativeValue. A choice from an enumerated list.                                                                                                                                                                                                                     
                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                 One of:                                                                                                                                                                                                                                                                                                                                 
                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                 **rising, falling, steady**.                                                                                                                                                                                                                                                                                                            | O                  | Y           |

#### WeatherObserved JSON

The JSON code can be downloaded from:

<https://gist.github.com/GSMADeveloper/ef466feddc874fb801b163c6c977f052>

{

"id": "adb144fb-e732-4944-a192-8690bd17de8c",

"type": "WeatherObserved",

"dateCreated": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"dateModified": {

"value": "2016-08-08T10:18:16Z",

"type": "DateTime"

},

"source": {

"value": "http://www.example.com",

"type": "URL"

},

"dataProvider": {

"value": "OperatorA",

"type": "Text"

},

"location": {

"value": {

"type": "Point",

"coordinates": \[

-104.99404,

39.75621

\]

},

"type": "geo:json"

},

"refDevice": \[

"c3e30a5a-2697-407d-908d-02a627d32730",

"08d22ce9-ce65-46a6-8e3c-12aa3a5389de"

\],

"dateObserved": {

"value": "2016-08-16T10:18:16Z",

"type": "DateTime"

},

"weatherType": {

"value": "sunnyDay",

"type": "Text"

},

"visibility": {

"value": "veryGood",

"type": "Text"

},

"name": {

"value": "London City",

"type": "Text"

},

"address": {

"type": "PostalAddress",

"value": {

"addressLocality": "London",

"postalCode": "EC4N 8AF",

"streetAddress": "25 Walbrook"

}

},

"temperature": {

"value": {

"value": 15,

"unitCode": "CEL"

},

"type": "ExtQuantitativeValue"

},

"refPointofInterest": \[

"b397c472-1ca8-4605-8d35-2fb27e85c0e8",

"e7c4d076-7eec-45b2-8982-9cd4c331e491"

\],

"windDirection": {

"value": {

"value": 122,

"unitCode": "DD"

},

"type": "ExtQuantitativeValue"

},

"windSpeed": {

"value": {

"value": 3,

"unitCode": "P87"

},

"type": "ExtQuantitativeValue"

},

"relativeHumidity": {

"value": {

"value": 0.2

},

"type": "ExtQuantitativeValue"

},

"dewPoint": {

"value": {

"value": 44,

"unitCode": "CEL"

},

"type": "ExtQuantitativeValue"

},

"atmosphericPressure": {

"value": {

"value": 101325,

"unitCode": "PAL"

},

"type": "ExtQuantitativeValue"

},

"pressureTendency": {

"value": "Rising",

"type": "Text"

}

}

1.  <span id="_Toc461716378" class="anchor"></span>ExtQuantitativeValue and NGSIv2 metadata compatibility (Informative)

The harmonized data models defined by this document make extensive use of the ExtQuantitativeValue structure. An example of the JSON formatted syntax for an attribute of type ExtQuantitativeValue is shown below:

The identical example in the equivalent NGSIv2 attribute value plus metadata, format is shown below:

Both implementation approaches are equivalent and comply with this harmonised data model.

1.  <span id="_Toc461716379" class="anchor"></span>Referenced Schema.org entities (Informative)

Some members of the project group have reported difficulties in accessing <https://schema.org/>. To provide additional clarity we provide a snapshot of the <https://schema.org/> entity definitions below. This information is informative only.

1.  <span id="_Toc461716380" class="anchor"></span>Schema.org entity descriptions: Offer

| **Property**                                                                  | **Expected Type**                                                | **Description**                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [Offer](https://schema.org/Offer)**                         |
| [**acceptedPaymentMethod**](https://schema.org/acceptedPaymentMethod)         | [LoanOrCredit](https://schema.org/LoanOrCredit)  or              
                                                                                 [PaymentMethod](https://schema.org/PaymentMethod)                 | The payment method(s) accepted by seller for this offer.                                                                                                                                                                                                                                                                                                                                   |
| [**addOn**](https://schema.org/addOn)                                         | [Offer](https://schema.org/Offer)                                | An additional offer that can only be obtained in combination with the first base offer (e.g. supplements and extensions that are available for a surcharge).                                                                                                                                                                                                                               |
| [**advanceBookingRequirement**](https://schema.org/advanceBookingRequirement) | [QuantitativeValue](https://schema.org/QuantitativeValue)        | The amount of time that is required between accepting the offer and the actual usage of the resource or service.                                                                                                                                                                                                                                                                           |
| [**aggregateRating**](https://schema.org/aggregateRating)                     | [AggregateRating](https://schema.org/AggregateRating)            | The overall rating, based on a collection of reviews or ratings, of the item.                                                                                                                                                                                                                                                                                                              |
| [**areaServed**](https://schema.org/areaServed)                               | [AdministrativeArea](https://schema.org/AdministrativeArea)  or  
                                                                                 [GeoShape](https://schema.org/GeoShape)  or                       
                                                                                 [Place](https://schema.org/Place)  or                             
                                                                                 [Text](https://schema.org/Text)                                   | The geographic area where a service or offered item is provided. Supersedes [serviceArea](https://schema.org/serviceArea).                                                                                                                                                                                                                                                                 |
| [**availability**](https://schema.org/availability)                           | [ItemAvailability](https://schema.org/ItemAvailability)          | The availability of this item—for example In stock, Out of stock, Pre-order, etc.                                                                                                                                                                                                                                                                                                          |
| [**availabilityEnds**](https://schema.org/availabilityEnds)                   | [DateTime](https://schema.org/DateTime)                          | The end of the availability of the product or service included in the offer.                                                                                                                                                                                                                                                                                                               |
| [**availabilityStarts**](https://schema.org/availabilityStarts)               | [DateTime](https://schema.org/DateTime)                          | The beginning of the availability of the product or service included in the offer.                                                                                                                                                                                                                                                                                                         |
| [**availableAtOrFrom**](https://schema.org/availableAtOrFrom)                 | [Place](https://schema.org/Place)                                | The place(s) from which the offer can be obtained (e.g. store locations).                                                                                                                                                                                                                                                                                                                  |
| [**availableDeliveryMethod**](https://schema.org/availableDeliveryMethod)     | [DeliveryMethod](https://schema.org/DeliveryMethod)              | The delivery method(s) available for this offer.                                                                                                                                                                                                                                                                                                                                           |
| [**businessFunction**](https://schema.org/businessFunction)                   | [BusinessFunction](https://schema.org/BusinessFunction)          | The business function (e.g. sell, lease, repair, dispose) of the offer or component of a bundle (TypeAndQuantityNode). The default is http://purl.org/goodrelations/v1\#Sell.                                                                                                                                                                                                              |
| [**category**](https://schema.org/category)                                   | [Text](https://schema.org/Text)  or                              
                                                                                 [Thing](https://schema.org/Thing)                                 | A category for the item. Greater signs or slashes can be used to informally indicate a category hierarchy.                                                                                                                                                                                                                                                                                 |
| [**deliveryLeadTime**](https://schema.org/deliveryLeadTime)                   | [QuantitativeValue](https://schema.org/QuantitativeValue)        | The typical delay between the receipt of the order and the goods either leaving the warehouse or being prepared for pickup, in case the delivery method is on site pickup.                                                                                                                                                                                                                 |
| [**eligibleCustomerType**](https://schema.org/eligibleCustomerType)           | [BusinessEntityType](https://schema.org/BusinessEntityType)      | The type(s) of customers for which the given offer is valid.                                                                                                                                                                                                                                                                                                                               |
| [**eligibleDuration**](https://schema.org/eligibleDuration)                   | [QuantitativeValue](https://schema.org/QuantitativeValue)        | The duration for which the given offer is valid.                                                                                                                                                                                                                                                                                                                                           |
| [**eligibleQuantity**](https://schema.org/eligibleQuantity)                   | [QuantitativeValue](https://schema.org/QuantitativeValue)        | The interval and unit of measurement of ordering quantities for which the offer or price specification is valid. This allows e.g. specifying that a certain freight charge is valid only for a certain quantity.                                                                                                                                                                           |
| [**eligibleRegion**](https://schema.org/eligibleRegion)                       | [GeoShape](https://schema.org/GeoShape)  or                      
                                                                                 [Place](https://schema.org/Place)  or                             
                                                                                 [Text](https://schema.org/Text)                                   | The ISO 3166-1 (ISO 3166-1 alpha-2) or ISO 3166-2 code, the place, or the GeoShape for the geo-political region(s) for which the offer or delivery charge specification is valid.                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    See also [ineligibleRegion](https://schema.org/ineligibleRegion).                                                                                                                                                                                                                                                                                                                           |
| [**eligibleTransactionVolume**](https://schema.org/eligibleTransactionVolume) | [PriceSpecification](https://schema.org/PriceSpecification)      | The transaction volume, in a monetary unit, for which the offer or price specification is valid, e.g. for indicating a minimal purchasing volume, to express free shipping above a certain order volume, or to limit the acceptance of credit cards to purchases to a certain minimal amount.                                                                                              |
| [**gtin12**](https://schema.org/gtin12)                                       | [Text](https://schema.org/Text)                                  | The [GTIN-12](http://apps.gs1.org/GDD/glossary/Pages/GTIN-12.aspx) code of the product, or the product to which the offer refers. The GTIN-12 is the 12-digit GS1 Identification Key composed of a U.P.C. Company Prefix, Item Reference, and Check Digit used to identify trade items. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details.        |
| [**gtin13**](https://schema.org/gtin13)                                       | [Text](https://schema.org/Text)                                  | The [GTIN-13](http://apps.gs1.org/GDD/glossary/Pages/GTIN-13.aspx) code of the product, or the product to which the offer refers. This is equivalent to 13-digit ISBN codes and EAN UCC-13. Former 12-digit UPC codes can be converted into a GTIN-13 code by simply adding a preceeding zero. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details. |
| [**gtin14**](https://schema.org/gtin14)                                       | [Text](https://schema.org/Text)                                  | The [GTIN-14](http://apps.gs1.org/GDD/glossary/Pages/GTIN-14.aspx) code of the product, or the product to which the offer refers. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details.                                                                                                                                                              |
| [**gtin8**](https://schema.org/gtin8)                                         | [Text](https://schema.org/Text)                                  | The [GTIN-8](http://apps.gs1.org/GDD/glossary/Pages/GTIN-8.aspx) code of the product, or the product to which the offer refers. This code is also known as EAN/UCC-8 or 8-digit EAN. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details.                                                                                                           |
| [**includesObject**](https://schema.org/includesObject)                       | [TypeAndQuantityNode](https://schema.org/TypeAndQuantityNode)    | This links to a node or nodes indicating the exact quantity of the products included in the offer.                                                                                                                                                                                                                                                                                         |
| [**ineligibleRegion**](https://schema.org/ineligibleRegion)                   | [GeoShape](https://schema.org/GeoShape)  or                      
                                                                                 [Place](https://schema.org/Place)  or                             
                                                                                 [Text](https://schema.org/Text)                                   | The ISO 3166-1 (ISO 3166-1 alpha-2) or ISO 3166-2 code, the place, or the GeoShape for the geo-political region(s) for which the offer or delivery charge specification is not valid, e.g. a region where the transaction is not allowed.                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    See also [eligibleRegion](https://schema.org/eligibleRegion).                                                                                                                                                                                                                                                                                                                               |
| [**inventoryLevel**](https://schema.org/inventoryLevel)                       | [QuantitativeValue](https://schema.org/QuantitativeValue)        | The current approximate inventory level for the item or items.                                                                                                                                                                                                                                                                                                                             |
| [**itemCondition**](https://schema.org/itemCondition)                         | [OfferItemCondition](https://schema.org/OfferItemCondition)      | A predefined value from OfferItemCondition or a textual description of the condition of the product or service, or the products or services included in the offer.                                                                                                                                                                                                                         |
| [**itemOffered**](https://schema.org/itemOffered)                             | [Product](https://schema.org/Product)  or                        
                                                                                 [Service](https://schema.org/Service)                             | The item being offered.                                                                                                                                                                                                                                                                                                                                                                    |
| [**mpn**](https://schema.org/mpn)                                             | [Text](https://schema.org/Text)                                  | The Manufacturer Part Number (MPN) of the product, or the product to which the offer refers.                                                                                                                                                                                                                                                                                               |
| [**offeredBy**](https://schema.org/offeredBy)                                 | [Organization](https://schema.org/Organization)  or              
                                                                                 [Person](https://schema.org/Person)                               | A pointer to the organization or person making the offer.                                                                                                                                                                                                                                                                                                                                  
                                                                                                                                                    Inverse property: [makesOffer](https://schema.org/makesOffer).                                                                                                                                                                                                                                                                                                                              |
| [**price**](https://schema.org/price)                                         | [Number](https://schema.org/Number)  or                          
                                                                                 [Text](https://schema.org/Text)                                   | The offer price of a product, or of a price component when attached to PriceSpecification and its subtypes.                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    Usage guidelines:                                                                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    -   Use the [priceCurrency](https://schema.org/priceCurrency) property (with [ISO 4217 codes](http://en.wikipedia.org/wiki/ISO_4217#Active_codes) e.g. "USD") instead of including[ambiguous symbols](http://en.wikipedia.org/wiki/Dollar_sign#Currencies_that_use_the_dollar_or_peso_sign) such as '$' in the value.                                                                       
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    -   Use '.' (Unicode 'FULL STOP' (U+002E)) rather than ',' to indicate a decimal point. Avoid using these symbols as a readability separator.                                                                                                                                                                                                                                               
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    -   Note that both [RDFa](http://www.w3.org/TR/xhtml-rdfa-primer/#using-the-content-attribute) and Microdata syntax allow the use of a "content=" attribute for publishing simple machine-readable values alongside more human-friendly formatting.                                                                                                                                         
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                    -   Use values from 0123456789 (Unicode 'DIGIT ZERO' (U+0030) to 'DIGIT NINE' (U+0039)) rather than superficially similiar Unicode symbols.                                                                                                                                                                                                                                                 |
| [**priceCurrency**](https://schema.org/priceCurrency)                         | [Text](https://schema.org/Text)                                  | The currency (in 3-letter ISO 4217 format) of the price or a price component, when attached to[PriceSpecification](https://schema.org/PriceSpecification) and its subtypes.                                                                                                                                                                                                                |
| [**priceSpecification**](https://schema.org/priceSpecification)               | [PriceSpecification](https://schema.org/PriceSpecification)      | One or more detailed price specifications, indicating the unit price and delivery or payment charges.                                                                                                                                                                                                                                                                                      |
| [**priceValidUntil**](https://schema.org/priceValidUntil)                     | [Date](https://schema.org/Date)                                  | The date after which the price is no longer available.                                                                                                                                                                                                                                                                                                                                     |
| [**review**](https://schema.org/review)                                       | [Review](https://schema.org/Review)                              | A review of the item. Supersedes [reviews](https://schema.org/reviews).                                                                                                                                                                                                                                                                                                                    |
| [**seller**](https://schema.org/seller)                                       | [Organization](https://schema.org/Organization)  or              
                                                                                 [Person](https://schema.org/Person)                               | An entity which offers (sells / leases / lends / loans) the services / goods. A seller may also be a provider. Supersedes [merchant](https://schema.org/merchant), [vendor](https://schema.org/vendor).                                                                                                                                                                                    |
| [**serialNumber**](https://schema.org/serialNumber)                           | [Text](https://schema.org/Text)                                  | The serial number or any alphanumeric identifier of a particular product. When attached to an offer, it is a shortcut for the serial number of the product included in the offer.                                                                                                                                                                                                          |
| [**sku**](https://schema.org/sku)                                             | [Text](https://schema.org/Text)                                  | The Stock Keeping Unit (SKU), i.e. a merchant-specific identifier for a product or service, or the product to which the offer refers.                                                                                                                                                                                                                                                      |
| [**validFrom**](https://schema.org/validFrom)                                 | [DateTime](https://schema.org/DateTime)                          | The date when the item becomes valid.                                                                                                                                                                                                                                                                                                                                                      |
| [**validThrough**](https://schema.org/validThrough)                           | [DateTime](https://schema.org/DateTime)                          | The date after when the item is not valid. For example the end of an offer, salary period, or a period of opening hours.                                                                                                                                                                                                                                                                   |
| [**warranty**](https://schema.org/warranty)                                   | [WarrantyPromise](https://schema.org/WarrantyPromise)            | The warranty promise(s) included in the offer. Supersedes [warrantyPromise](https://schema.org/warrantyPromise).                                                                                                                                                                                                                                                                           |

1.  <span id="_Toc461716381" class="anchor"></span>Schema.org entity descriptions: Organisation

| **Property**                                                        | **Expected Type**                                                | **Description**                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [Organization](https://schema.org/Organization)** |
| [**address**](https://schema.org/address)                           | [PostalAddress](https://schema.org/PostalAddress)  or            
                                                                       [Text](https://schema.org/Text)                                   | Physical address of the item.                                                                                                                                                                                                                                  |
| [**aggregateRating**](https://schema.org/aggregateRating)           | [AggregateRating](https://schema.org/AggregateRating)            | The overall rating, based on a collection of reviews or ratings, of the item.                                                                                                                                                                                  |
| [**alumni**](https://schema.org/alumni)                             | [Person](https://schema.org/Person)                              | Alumni of an organization.                                                                                                                                                                                                                                     
                                                                                                                                          Inverse property: [alumniOf](https://schema.org/alumniOf).                                                                                                                                                                                                      |
| [**areaServed**](https://schema.org/areaServed)                     | [AdministrativeArea](https://schema.org/AdministrativeArea)  or  
                                                                       [GeoShape](https://schema.org/GeoShape)  or                       
                                                                       [Place](https://schema.org/Place)  or                             
                                                                       [Text](https://schema.org/Text)                                   | The geographic area where a service or offered item is provided. Supersedes [serviceArea](https://schema.org/serviceArea).                                                                                                                                     |
| [**award**](https://schema.org/award)                               | [Text](https://schema.org/Text)                                  | An award won by or for this item. Supersedes [awards](https://schema.org/awards).                                                                                                                                                                              |
| [**brand**](https://schema.org/brand)                               | [Brand](https://schema.org/Brand)  or                            
                                                                       [Organization](https://schema.org/Organization)                   | The brand(s) associated with a product or service, or the brand(s) maintained by an organization or business person.                                                                                                                                           |
| [**contactPoint**](https://schema.org/contactPoint)                 | [ContactPoint](https://schema.org/ContactPoint)                  | A contact point for a person or organization. Supersedes [contactPoints](https://schema.org/contactPoints).                                                                                                                                                    |
| [**department**](https://schema.org/department)                     | [Organization](https://schema.org/Organization)                  | A relationship between an organization and a department of that organization, also described as an organization (allowing different urls, logos, opening hours). For example: a store with a pharmacy, or a bakery with a cafe.                                |
| [**dissolutionDate**](https://schema.org/dissolutionDate)           | [Date](https://schema.org/Date)                                  | The date that this organization was dissolved.                                                                                                                                                                                                                 |
| [**duns**](https://schema.org/duns)                                 | [Text](https://schema.org/Text)                                  | The Dun & Bradstreet DUNS number for identifying an organization or business person.                                                                                                                                                                           |
| [**email**](https://schema.org/email)                               | [Text](https://schema.org/Text)                                  | Email address.                                                                                                                                                                                                                                                 |
| [**employee**](https://schema.org/employee)                         | [Person](https://schema.org/Person)                              | Someone working for this organization. Supersedes [employees](https://schema.org/employees).                                                                                                                                                                   |
| [**event**](https://schema.org/event)                               | [Event](https://schema.org/Event)                                | Upcoming or past event associated with this place, organization, or action. Supersedes [events](https://schema.org/events).                                                                                                                                    |
| [**faxNumber**](https://schema.org/faxNumber)                       | [Text](https://schema.org/Text)                                  | The fax number.                                                                                                                                                                                                                                                |
| [**founder**](https://schema.org/founder)                           | [Person](https://schema.org/Person)                              | A person who founded this organization. Supersedes [founders](https://schema.org/founders).                                                                                                                                                                    |
| [**foundingDate**](https://schema.org/foundingDate)                 | [Date](https://schema.org/Date)                                  | The date that this organization was founded.                                                                                                                                                                                                                   |
| [**foundingLocation**](https://schema.org/foundingLocation)         | [Place](https://schema.org/Place)                                | The place where the Organization was founded.                                                                                                                                                                                                                  |
| [**funder**](https://schema.org/funder)                             | [Organization](https://schema.org/Organization)  or              
                                                                       [Person](https://schema.org/Person)                               | A person or organization that supports (sponsors) something through some kind of financial contribution.                                                                                                                                                       |
| [**globalLocationNumber**](https://schema.org/globalLocationNumber) | [Text](https://schema.org/Text)                                  | The [Global Location Number](http://www.gs1.org/gln) (GLN, sometimes also referred to as International Location Number or ILN) of the respective organization, person, or place. The GLN is a 13-digit number used to identify parties and physical locations. |
| [**hasOfferCatalog**](https://schema.org/hasOfferCatalog)           | [OfferCatalog](https://schema.org/OfferCatalog)                  | Indicates an OfferCatalog listing for this Organization, Person, or Service.                                                                                                                                                                                   |
| [**hasPOS**](https://schema.org/hasPOS)                             | [Place](https://schema.org/Place)                                | Points-of-Sales operated by the organization or person.                                                                                                                                                                                                        |
| [**isicV4**](https://schema.org/isicV4)                             | [Text](https://schema.org/Text)                                  | The International Standard of Industrial Classification of All Economic Activities (ISIC), Revision 4 code for a particular organization, business person, or place.                                                                                           |
| [**legalName**](https://schema.org/legalName)                       | [Text](https://schema.org/Text)                                  | The official name of the organization, e.g. the registered company name.                                                                                                                                                                                       |
| [**leiCode**](https://schema.org/leiCode)                           | [Text](https://schema.org/Text)                                  | An organization identifier that uniquely identifies a legal entity as defined in ISO 17442.                                                                                                                                                                    |
| [**location**](https://schema.org/location)                         | [Place](https://schema.org/Place)  or                            
                                                                       [PostalAddress](https://schema.org/PostalAddress)  or             
                                                                       [Text](https://schema.org/Text)                                   | The location of for example where the event is happening, an organization is located, or where an action takes place.                                                                                                                                          |
| [**logo**](https://schema.org/logo)                                 | [ImageObject](https://schema.org/ImageObject)  or                
                                                                       [URL](https://schema.org/URL)                                     | An associated logo.                                                                                                                                                                                                                                            |
| [**makesOffer**](https://schema.org/makesOffer)                     | [Offer](https://schema.org/Offer)                                | A pointer to products or services offered by the organization or person.                                                                                                                                                                                       
                                                                                                                                          Inverse property: [offeredBy](https://schema.org/offeredBy).                                                                                                                                                                                                    |
| [**member**](https://schema.org/member)                             | [Organization](https://schema.org/Organization)  or              
                                                                       [Person](https://schema.org/Person)                               | A member of an Organization or a ProgramMembership. Organizations can be members of organizations; ProgramMembership is typically for individuals. Supersedes [members](https://schema.org/members),[musicGroupMember](https://schema.org/musicGroupMember).   
                                                                                                                                          Inverse property: [memberOf](https://schema.org/memberOf).                                                                                                                                                                                                      |
| [**memberOf**](https://schema.org/memberOf)                         | [Organization](https://schema.org/Organization)  or              
                                                                       [ProgramMembership](https://schema.org/ProgramMembership)         | An Organization (or ProgramMembership) to which this Person or Organization belongs.                                                                                                                                                                           
                                                                                                                                          Inverse property: [member](https://schema.org/member).                                                                                                                                                                                                          |
| [**naics**](https://schema.org/naics)                               | [Text](https://schema.org/Text)                                  | The North American Industry Classification System (NAICS) code for a particular organization or business person.                                                                                                                                               |
| [**numberOfEmployees**](https://schema.org/numberOfEmployees)       | [QuantitativeValue](https://schema.org/QuantitativeValue)        | The number of employees in an organization e.g. business.                                                                                                                                                                                                      |
| [**owns**](https://schema.org/owns)                                 | [OwnershipInfo](https://schema.org/OwnershipInfo)  or            
                                                                       [Product](https://schema.org/Product)                             | Products owned by the organization or person.                                                                                                                                                                                                                  |
| [**parentOrganization**](https://schema.org/parentOrganization)     | [Organization](https://schema.org/Organization)                  | The larger organization that this local business is a branch of, if any. Supersedes [branchOf](https://schema.org/branchOf).                                                                                                                                   
                                                                                                                                          Inverse property: [subOrganization](https://schema.org/subOrganization).                                                                                                                                                                                        |
| [**review**](https://schema.org/review)                             | [Review](https://schema.org/Review)                              | A review of the item. Supersedes [reviews](https://schema.org/reviews).                                                                                                                                                                                        |
| [**seeks**](https://schema.org/seeks)                               | [Demand](https://schema.org/Demand)                              | A pointer to products or services sought by the organization or person (demand).                                                                                                                                                                               |
| [**sponsor**](https://schema.org/sponsor)                           | [Organization](https://schema.org/Organization)  or              
                                                                       [Person](https://schema.org/Person)                               | A person or organization that supports a thing through a pledge, promise, or financial contribution. e.g. a sponsor of a Medical Study or a corporate sponsor of an event.                                                                                     |
| [**subOrganization**](https://schema.org/subOrganization)           | [Organization](https://schema.org/Organization)                  | A relationship between two organizations where the first includes the second, e.g., as a subsidiary. See also: the more specific 'department' property.                                                                                                        
                                                                                                                                          Inverse property: [parentOrganization](https://schema.org/parentOrganization).                                                                                                                                                                                  |
| [**taxID**](https://schema.org/taxID)                               | [Text](https://schema.org/Text)                                  | The Tax / Fiscal ID of the organization or person, e.g. the TIN in the US or the CIF/NIF in Spain.                                                                                                                                                             |
| [**telephone**](https://schema.org/telephone)                       | [Text](https://schema.org/Text)                                  | The telephone number.                                                                                                                                                                                                                                          |
| [**vatID**](https://schema.org/vatID)                               | [Text](https://schema.org/Text)                                  | The Value-added Tax ID of the organization or person.                                                                                                                                                                                                          |

1.  <span id="_Toc461716382" class="anchor"></span>Schema.org entity descriptions: Person

| **Property**                                                        | **Expected Type**                                                          | **Description**                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [Person](https://schema.org/Person)**             |
| [**additionalName**](https://schema.org/additionalName)             | [Text](https://schema.org/Text)                                            | An additional name for a Person, can be used for a middle name.                                                                                                                                                                                                |
| [**address**](https://schema.org/address)                           | [PostalAddress](https://schema.org/PostalAddress)  or                      
                                                                       [Text](https://schema.org/Text)                                             | Physical address of the item.                                                                                                                                                                                                                                  |
| [**affiliation**](https://schema.org/affiliation)                   | [Organization](https://schema.org/Organization)                            | An organization that this person is affiliated with. For example, a school/university, a club, or a team.                                                                                                                                                      |
| [**alumniOf**](https://schema.org/alumniOf)                         | [EducationalOrganization](https://schema.org/EducationalOrganization)  or  
                                                                       [Organization](https://schema.org/Organization)                             | An organization that the person is an alumni of.                                                                                                                                                                                                               
                                                                                                                                                    Inverse property: [alumni](https://schema.org/alumni).                                                                                                                                                                                                          |
| [**award**](https://schema.org/award)                               | [Text](https://schema.org/Text)                                            | An award won by or for this item. Supersedes [awards](https://schema.org/awards).                                                                                                                                                                              |
| [**birthDate**](https://schema.org/birthDate)                       | [Date](https://schema.org/Date)                                            | Date of birth.                                                                                                                                                                                                                                                 |
| [**birthPlace**](https://schema.org/birthPlace)                     | [Place](https://schema.org/Place)                                          | The place where the person was born.                                                                                                                                                                                                                           |
| [**brand**](https://schema.org/brand)                               | [Brand](https://schema.org/Brand)  or                                      
                                                                       [Organization](https://schema.org/Organization)                             | The brand(s) associated with a product or service, or the brand(s) maintained by an organization or business person.                                                                                                                                           |
| [**children**](https://schema.org/children)                         | [Person](https://schema.org/Person)                                        | A child of the person.                                                                                                                                                                                                                                         |
| [**colleague**](https://schema.org/colleague)                       | [Person](https://schema.org/Person)  or                                    
                                                                       [URL](https://schema.org/URL)                                               | A colleague of the person. Supersedes [colleagues](https://schema.org/colleagues).                                                                                                                                                                             |
| [**contactPoint**](https://schema.org/contactPoint)                 | [ContactPoint](https://schema.org/ContactPoint)                            | A contact point for a person or organization. Supersedes [contactPoints](https://schema.org/contactPoints).                                                                                                                                                    |
| [**deathDate**](https://schema.org/deathDate)                       | [Date](https://schema.org/Date)                                            | Date of death.                                                                                                                                                                                                                                                 |
| [**deathPlace**](https://schema.org/deathPlace)                     | [Place](https://schema.org/Place)                                          | The place where the person died.                                                                                                                                                                                                                               |
| [**duns**](https://schema.org/duns)                                 | [Text](https://schema.org/Text)                                            | The Dun & Bradstreet DUNS number for identifying an organization or business person.                                                                                                                                                                           |
| [**email**](https://schema.org/email)                               | [Text](https://schema.org/Text)                                            | Email address.                                                                                                                                                                                                                                                 |
| [**familyName**](https://schema.org/familyName)                     | [Text](https://schema.org/Text)                                            | Family name. In the U.S., the last name of an Person. This can be used along with givenName instead of the name property.                                                                                                                                      |
| [**faxNumber**](https://schema.org/faxNumber)                       | [Text](https://schema.org/Text)                                            | The fax number.                                                                                                                                                                                                                                                |
| [**follows**](https://schema.org/follows)                           | [Person](https://schema.org/Person)                                        | The most generic uni-directional social relation.                                                                                                                                                                                                              |
| [**funder**](https://schema.org/funder)                             | [Organization](https://schema.org/Organization)  or                        
                                                                       [Person](https://schema.org/Person)                                         | A person or organization that supports (sponsors) something through some kind of financial contribution.                                                                                                                                                       |
| [**gender**](https://schema.org/gender)                             | [GenderType](https://schema.org/GenderType)  or                            
                                                                       [Text](https://schema.org/Text)                                             | Gender of the person. While http://schema.org/Male and http://schema.org/Female may be used, text strings are also acceptable for people who do not identify as a binary gender.                                                                               |
| [**givenName**](https://schema.org/givenName)                       | [Text](https://schema.org/Text)                                            | Given name. In the U.S., the first name of a Person. This can be used along with familyName instead of the name property.                                                                                                                                      |
| [**globalLocationNumber**](https://schema.org/globalLocationNumber) | [Text](https://schema.org/Text)                                            | The [Global Location Number](http://www.gs1.org/gln) (GLN, sometimes also referred to as International Location Number or ILN) of the respective organization, person, or place. The GLN is a 13-digit number used to identify parties and physical locations. |
| [**hasOfferCatalog**](https://schema.org/hasOfferCatalog)           | [OfferCatalog](https://schema.org/OfferCatalog)                            | Indicates an OfferCatalog listing for this Organization, Person, or Service.                                                                                                                                                                                   |
| [**hasPOS**](https://schema.org/hasPOS)                             | [Place](https://schema.org/Place)                                          | Points-of-Sales operated by the organization or person.                                                                                                                                                                                                        |
| [**height**](https://schema.org/height)                             | [Distance](https://schema.org/Distance)  or                                
                                                                       [QuantitativeValue](https://schema.org/QuantitativeValue)                   | The height of the item.                                                                                                                                                                                                                                        |
| [**homeLocation**](https://schema.org/homeLocation)                 | [ContactPoint](https://schema.org/ContactPoint)  or                        
                                                                       [Place](https://schema.org/Place)                                           | A contact location for a person's residence.                                                                                                                                                                                                                   |
| [**honorificPrefix**](https://schema.org/honorificPrefix)           | [Text](https://schema.org/Text)                                            | An honorific prefix preceding a Person's name such as Dr/Mrs/Mr.                                                                                                                                                                                               |
| [**honorificSuffix**](https://schema.org/honorificSuffix)           | [Text](https://schema.org/Text)                                            | An honorific suffix preceding a Person's name such as M.D. /PhD/MSCSW.                                                                                                                                                                                         |
| [**isicV4**](https://schema.org/isicV4)                             | [Text](https://schema.org/Text)                                            | The International Standard of Industrial Classification of All Economic Activities (ISIC), Revision 4 code for a particular organization, business person, or place.                                                                                           |
| [**jobTitle**](https://schema.org/jobTitle)                         | [Text](https://schema.org/Text)                                            | The job title of the person (for example, Financial Manager).                                                                                                                                                                                                  |
| [**knows**](https://schema.org/knows)                               | [Person](https://schema.org/Person)                                        | The most generic bi-directional social/work relation.                                                                                                                                                                                                          |
| [**makesOffer**](https://schema.org/makesOffer)                     | [Offer](https://schema.org/Offer)                                          | A pointer to products or services offered by the organization or person.                                                                                                                                                                                       
                                                                                                                                                    Inverse property: [offeredBy](https://schema.org/offeredBy).                                                                                                                                                                                                    |
| [**memberOf**](https://schema.org/memberOf)                         | [Organization](https://schema.org/Organization)  or                        
                                                                       [ProgramMembership](https://schema.org/ProgramMembership)                   | An Organization (or ProgramMembership) to which this Person or Organization belongs.                                                                                                                                                                           
                                                                                                                                                    Inverse property: [member](https://schema.org/member).                                                                                                                                                                                                          |
| [**naics**](https://schema.org/naics)                               | [Text](https://schema.org/Text)                                            | The North American Industry Classification System (NAICS) code for a particular organization or business person.                                                                                                                                               |
| [**nationality**](https://schema.org/nationality)                   | [Country](https://schema.org/Country)                                      | Nationality of the person.                                                                                                                                                                                                                                     |
| [**netWorth**](https://schema.org/netWorth)                         | [MonetaryAmount](https://schema.org/MonetaryAmount)  or                    
                                                                       [PriceSpecification](https://schema.org/PriceSpecification)                 | The total financial value of the person as calculated by subtracting assets from liabilities.                                                                                                                                                                  |
| [**owns**](https://schema.org/owns)                                 | [OwnershipInfo](https://schema.org/OwnershipInfo)  or                      
                                                                       [Product](https://schema.org/Product)                                       | Products owned by the organization or person.                                                                                                                                                                                                                  |
| [**parent**](https://schema.org/parent)                             | [Person](https://schema.org/Person)                                        | A parent of this person. Supersedes [parents](https://schema.org/parents).                                                                                                                                                                                     |
| [**performerIn**](https://schema.org/performerIn)                   | [Event](https://schema.org/Event)                                          | Event that this person is a performer or participant in.                                                                                                                                                                                                       |
| [**relatedTo**](https://schema.org/relatedTo)                       | [Person](https://schema.org/Person)                                        | The most generic familial relation.                                                                                                                                                                                                                            |
| [**seeks**](https://schema.org/seeks)                               | [Demand](https://schema.org/Demand)                                        | A pointer to products or services sought by the organization or person (demand).                                                                                                                                                                               |
| [**sibling**](https://schema.org/sibling)                           | [Person](https://schema.org/Person)                                        | A sibling of the person. Supersedes [siblings](https://schema.org/siblings).                                                                                                                                                                                   |
| [**sponsor**](https://schema.org/sponsor)                           | [Organization](https://schema.org/Organization)  or                        
                                                                       [Person](https://schema.org/Person)                                         | A person or organization that supports a thing through a pledge, promise, or financial contribution. e.g. a sponsor of a Medical Study or a corporate sponsor of an event.                                                                                     |
| [**spouse**](https://schema.org/spouse)                             | [Person](https://schema.org/Person)                                        | The person's spouse.                                                                                                                                                                                                                                           |
| [**taxID**](https://schema.org/taxID)                               | [Text](https://schema.org/Text)                                            | The Tax / Fiscal ID of the organization or person, e.g. the TIN in the US or the CIF/NIF in Spain.                                                                                                                                                             |
| [**telephone**](https://schema.org/telephone)                       | [Text](https://schema.org/Text)                                            | The telephone number.                                                                                                                                                                                                                                          |
| [**vatID**](https://schema.org/vatID)                               | [Text](https://schema.org/Text)                                            | The Value-added Tax ID of the organization or person.                                                                                                                                                                                                          |
| [**weight**](https://schema.org/weight)                             | [QuantitativeValue](https://schema.org/QuantitativeValue)                  | The weight of the product or person.                                                                                                                                                                                                                           |
| [**workLocation**](https://schema.org/workLocation)                 | [ContactPoint](https://schema.org/ContactPoint)  or                        
                                                                       [Place](https://schema.org/Place)                                           | A contact location for a person's place of work.                                                                                                                                                                                                               |
| [**worksFor**](https://schema.org/worksFor)                         | [Organization](https://schema.org/Organization)                            | Organizations that the person works for.                                                                                                                                                                                                                       |

**
**

1.  <span id="_Toc461716383" class="anchor"></span>Schema.org entity descriptions: PostalAddress

| **Property**                                                          | **Expected Type**                          | **Description**                                                                                                                                |
|-----------------------------------------------------------------------|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [PostalAddress](https://schema.org/PostalAddress)** |
| [**addressCountry**](https://schema.org/addressCountry)               | [Country](https://schema.org/Country)  or  
                                                                         [Text](https://schema.org/Text)             | The country. For example, USA. You can also provide the two-letter [ISO 3166-1 alpha-2 country code](http://en.wikipedia.org/wiki/ISO_3166-1). |
| [**addressLocality**](https://schema.org/addressLocality)             | [Text](https://schema.org/Text)            | The locality. For example, Mountain View.                                                                                                      |
| [**addressRegion**](https://schema.org/addressRegion)                 | [Text](https://schema.org/Text)            | The region. For example, CA.                                                                                                                   |
| [**postOfficeBoxNumber**](https://schema.org/postOfficeBoxNumber)     | [Text](https://schema.org/Text)            | The post office box number for PO box addresses.                                                                                               |
| [**postalCode**](https://schema.org/postalCode)                       | [Text](https://schema.org/Text)            | The postal code. For example, 94043.                                                                                                           |
| [**streetAddress**](https://schema.org/streetAddress)                 | [Text](https://schema.org/Text)            | The street address. For example, 1600 Amphitheatre Pkwy.                                                                                       |

1.  <span id="_Toc461716384" class="anchor"></span>Schema.org entity descriptions: Product

| **Property**                                                                  | **Expected Type**                                            | **Description**                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [Product](https://schema.org/Product)**                     |
| [**additionalProperty**](https://schema.org/additionalProperty)               | [PropertyValue](https://schema.org/PropertyValue)            | A property-value pair representing an additional characteristics of the entitity, e.g. a product feature or another characteristic for which there is no matching property in schema.org.                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            
                                                                                                                                                Note: Publishers should be aware that applications designed to use specific schema.org properties (e.g. http://schema.org/width, http://schema.org/color, http://schema.org/gtin13, ...) will typically expect such data to be provided using those properties, rather than using the generic property/value mechanism.                                                                     |
| [**aggregateRating**](https://schema.org/aggregateRating)                     | [AggregateRating](https://schema.org/AggregateRating)        | The overall rating, based on a collection of reviews or ratings, of the item.                                                                                                                                                                                                                                                                                                              |
| [**audience**](https://schema.org/audience)                                   | [Audience](https://schema.org/Audience)                      | An intended audience, i.e. a group for whom something was created. Supersedes [serviceAudience](https://schema.org/serviceAudience).                                                                                                                                                                                                                                                       |
| [**award**](https://schema.org/award)                                         | [Text](https://schema.org/Text)                              | An award won by or for this item. Supersedes [awards](https://schema.org/awards).                                                                                                                                                                                                                                                                                                          |
| [**brand**](https://schema.org/brand)                                         | [Brand](https://schema.org/Brand)  or                        
                                                                                 [Organization](https://schema.org/Organization)               | The brand(s) associated with a product or service, or the brand(s) maintained by an organization or business person.                                                                                                                                                                                                                                                                       |
| [**category**](https://schema.org/category)                                   | [Text](https://schema.org/Text)  or                          
                                                                                 [Thing](https://schema.org/Thing)                             | A category for the item. Greater signs or slashes can be used to informally indicate a category hierarchy.                                                                                                                                                                                                                                                                                 |
| [**color**](https://schema.org/color)                                         | [Text](https://schema.org/Text)                              | The color of the product.                                                                                                                                                                                                                                                                                                                                                                  |
| [**depth**](https://schema.org/depth)                                         | [Distance](https://schema.org/Distance)  or                  
                                                                                 [QuantitativeValue](https://schema.org/QuantitativeValue)     | The depth of the item.                                                                                                                                                                                                                                                                                                                                                                     |
| [**gtin12**](https://schema.org/gtin12)                                       | [Text](https://schema.org/Text)                              | The [GTIN-12](http://apps.gs1.org/GDD/glossary/Pages/GTIN-12.aspx) code of the product, or the product to which the offer refers. The GTIN-12 is the 12-digit GS1 Identification Key composed of a U.P.C. Company Prefix, Item Reference, and Check Digit used to identify trade items. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details.        |
| [**gtin13**](https://schema.org/gtin13)                                       | [Text](https://schema.org/Text)                              | The [GTIN-13](http://apps.gs1.org/GDD/glossary/Pages/GTIN-13.aspx) code of the product, or the product to which the offer refers. This is equivalent to 13-digit ISBN codes and EAN UCC-13. Former 12-digit UPC codes can be converted into a GTIN-13 code by simply adding a preceeding zero. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details. |
| [**gtin14**](https://schema.org/gtin14)                                       | [Text](https://schema.org/Text)                              | The [GTIN-14](http://apps.gs1.org/GDD/glossary/Pages/GTIN-14.aspx) code of the product, or the product to which the offer refers. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details.                                                                                                                                                              |
| [**gtin8**](https://schema.org/gtin8)                                         | [Text](https://schema.org/Text)                              | The [GTIN-8](http://apps.gs1.org/GDD/glossary/Pages/GTIN-8.aspx) code of the product, or the product to which the offer refers. This code is also known as EAN/UCC-8 or 8-digit EAN. See [GS1 GTIN Summary](http://www.gs1.org/barcodes/technical/idkeys/gtin) for more details.                                                                                                           |
| [**height**](https://schema.org/height)                                       | [Distance](https://schema.org/Distance)  or                  
                                                                                 [QuantitativeValue](https://schema.org/QuantitativeValue)     | The height of the item.                                                                                                                                                                                                                                                                                                                                                                    |
| [**isAccessoryOrSparePartFor**](https://schema.org/isAccessoryOrSparePartFor) | [Product](https://schema.org/Product)                        | A pointer to another product (or multiple products) for which this product is an accessory or spare part.                                                                                                                                                                                                                                                                                  |
| [**isConsumableFor**](https://schema.org/isConsumableFor)                     | [Product](https://schema.org/Product)                        | A pointer to another product (or multiple products) for which this product is a consumable.                                                                                                                                                                                                                                                                                                |
| [**isRelatedTo**](https://schema.org/isRelatedTo)                             | [Product](https://schema.org/Product)  or                    
                                                                                 [Service](https://schema.org/Service)                         | A pointer to another, somehow related product (or multiple products).                                                                                                                                                                                                                                                                                                                      |
| [**isSimilarTo**](https://schema.org/isSimilarTo)                             | [Product](https://schema.org/Product)  or                    
                                                                                 [Service](https://schema.org/Service)                         | A pointer to another, functionally similar product (or multiple products).                                                                                                                                                                                                                                                                                                                 |
| [**itemCondition**](https://schema.org/itemCondition)                         | [OfferItemCondition](https://schema.org/OfferItemCondition)  | A predefined value from OfferItemCondition or a textual description of the condition of the product or service, or the products or services included in the offer.                                                                                                                                                                                                                         |
| [**logo**](https://schema.org/logo)                                           | [ImageObject](https://schema.org/ImageObject)  or            
                                                                                 [URL](https://schema.org/URL)                                 | An associated logo.                                                                                                                                                                                                                                                                                                                                                                        |
| [**manufacturer**](https://schema.org/manufacturer)                           | [Organization](https://schema.org/Organization)              | The manufacturer of the product.                                                                                                                                                                                                                                                                                                                                                           |
| [**model**](https://schema.org/model)                                         | [ProductModel](https://schema.org/ProductModel)  or          
                                                                                 [Text](https://schema.org/Text)                               | The model of the product. Use with the URL of a ProductModel or a textual representation of the model identifier. The URL of the ProductModel can be from an external source. It is recommended to additionally provide strong product identifiers via the gtin8/gtin13/gtin14 and mpn properties.                                                                                         |
| [**mpn**](https://schema.org/mpn)                                             | [Text](https://schema.org/Text)                              | The Manufacturer Part Number (MPN) of the product, or the product to which the offer refers.                                                                                                                                                                                                                                                                                               |
| [**offers**](https://schema.org/offers)                                       | [Offer](https://schema.org/Offer)                            | An offer to provide this item—for example, an offer to sell a product, rent the DVD of a movie, perform a service, or give away tickets to an event.                                                                                                                                                                                                                                       |
| [**productID**](https://schema.org/productID)                                 | [Text](https://schema.org/Text)                              | The product identifier, such as ISBN. For example: meta itemprop="productID" content="isbn:123-456-789".                                                                                                                                                                                                                                                                                   |
| [**productionDate**](https://schema.org/productionDate)                       | [Date](https://schema.org/Date)                              | The date of production of the item, e.g. vehicle.                                                                                                                                                                                                                                                                                                                                          |
| [**purchaseDate**](https://schema.org/purchaseDate)                           | [Date](https://schema.org/Date)                              | The date the item e.g. vehicle was purchased by the current owner.                                                                                                                                                                                                                                                                                                                         |
| [**releaseDate**](https://schema.org/releaseDate)                             | [Date](https://schema.org/Date)                              | The release date of a product or product model. This can be used to distinguish the exact variant of a product.                                                                                                                                                                                                                                                                            |
| [**review**](https://schema.org/review)                                       | [Review](https://schema.org/Review)                          | A review of the item. Supersedes [reviews](https://schema.org/reviews).                                                                                                                                                                                                                                                                                                                    |
| [**sku**](https://schema.org/sku)                                             | [Text](https://schema.org/Text)                              | The Stock Keeping Unit (SKU), i.e. a merchant-specific identifier for a product or service, or the product to which the offer refers.                                                                                                                                                                                                                                                      |
| [**weight**](https://schema.org/weight)                                       | [QuantitativeValue](https://schema.org/QuantitativeValue)    | The weight of the product or person.                                                                                                                                                                                                                                                                                                                                                       |
| [**width**](https://schema.org/width)                                         | [Distance](https://schema.org/Distance)  or                  
                                                                                 [QuantitativeValue](https://schema.org/QuantitativeValue)     | The width of the item.                                                                                                                                                                                                                                                                                                                                                                     |

1.  <span id="_Toc461716385" class="anchor"></span>Schema.org entity descriptions: QuantitativeValue

| **Property**                                                                  | **Expected Type**                                              | **Description**                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [QuantitativeValue](https://schema.org/QuantitativeValue)** |
| [**additionalProperty**](https://schema.org/additionalProperty)               | [PropertyValue](https://schema.org/PropertyValue)              | A property-value pair representing an additional characteristics of the entitity, e.g. a product feature or another characteristic for which there is no matching property in schema.org.                                                                                                                               
                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                  Note: Publishers should be aware that applications designed to use specific schema.org properties (e.g. http://schema.org/width, http://schema.org/color, http://schema.org/gtin13, ...) will typically expect such data to be provided using those properties, rather than using the generic property/value mechanism.  |
| [**maxValue**](https://schema.org/maxValue)                                   | [Number](https://schema.org/Number)                            | The upper value of some characteristic or property.                                                                                                                                                                                                                                                                     |
| [**minValue**](https://schema.org/minValue)                                   | [Number](https://schema.org/Number)                            | The lower value of some characteristic or property.                                                                                                                                                                                                                                                                     |
| [**unitCode**](https://schema.org/unitCode)                                   | [Text](https://schema.org/Text)  or                            
                                                                                 [URL](https://schema.org/URL)                                   | The unit of measurement given using the UN/CEFACT Common Code (3 characters) or a URL. Other codes than the UN/CEFACT Common Code may be used with a prefix followed by a colon.                                                                                                                                        |
| [**unitText**](https://schema.org/unitText)                                   | [Text](https://schema.org/Text)                                | A string or text indicating the unit of measurement. Useful if you cannot provide a standard unit code for [unitCode](https://schema.org/unitCode).                                                                                                                                                                     |
| [**value**](https://schema.org/value)                                         | [Boolean](https://schema.org/Boolean)  or                      
                                                                                 [Number](https://schema.org/Number)  or                         
                                                                                 [StructuredValue](https://schema.org/StructuredValue)  or       
                                                                                 [Text](https://schema.org/Text)                                 | The value of the quantitative value or property value node.                                                                                                                                                                                                                                                             
                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                  -   For [QuantitativeValue](https://schema.org/QuantitativeValue) and [MonetaryAmount](https://schema.org/MonetaryAmount), the recommended type for values is 'Number'.                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
                                                                                                                                                  -   For [PropertyValue](https://schema.org/PropertyValue), it can be 'Text;', 'Number', 'Boolean', or 'StructuredValue'.                                                                                                                                                                                                 |
| [**valueReference**](https://schema.org/valueReference)                       | [Enumeration](https://schema.org/Enumeration)  or              
                                                                                 [PropertyValue](https://schema.org/PropertyValue)  or           
                                                                                 [QualitativeValue](https://schema.org/QualitativeValue)  or     
                                                                                 [QuantitativeValue](https://schema.org/QuantitativeValue)  or   
                                                                                 [StructuredValue](https://schema.org/StructuredValue)           | A pointer to a secondary value that provides additional information on the original value, e.g. a reference temperature.                                                                                                                                                                                                |

1.  <span id="_Toc461716386" class="anchor"></span>Schema.org entity descriptions: Vehicle

| **Property**                                                                              | **Expected Type**                                                                            | **Description**                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Properties from [Vehicle](https://pending.schema.org/Vehicle)**                         |
| [**cargoVolume**](https://pending.schema.org/cargoVolume)                                 | [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                            | The available volume for cargo or luggage. For automobiles, this is usually the trunk volume.                                                                                                                                                                               
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): LTR for liters, FTQ for cubic foot/feet                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Note: You can use [minValue](https://pending.schema.org/minValue) and [maxValue](https://pending.schema.org/maxValue) to indicate ranges.                                                                                                                                    |
| [**dateVehicleFirstRegistered**](https://pending.schema.org/dateVehicleFirstRegistered)   | [Date](https://pending.schema.org/Date)                                                      | The date of the first registration of the vehicle with the respective public authorities.                                                                                                                                                                                   |
| [**driveWheelConfiguration**](https://pending.schema.org/driveWheelConfiguration)         | [DriveWheelConfigurationValue](https://pending.schema.org/DriveWheelConfigurationValue)  or  
                                                                                             [Text](https://pending.schema.org/Text)                                                       | The drive wheel configuration, i.e. which roadwheels will receive torque from the vehicle's engine via the drivetrain.                                                                                                                                                      |
| [**fuelConsumption**](https://pending.schema.org/fuelConsumption)                         | [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                            | The amount of fuel consumed for traveling a particular distance or temporal duration with the given vehicle (e.g. lites per 100 km).                                                                                                                                        
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            -   Note 1: There are unfortunately no standard unit codes for liters per 100 km. Use [unitText](https://pending.schema.org/unitText) to indicate the unit of measurement, e.g. L/100 km.                                                                                    
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            -   Note 2: There are two ways of indicating the fuel consumption, [fuelConsumption](https://pending.schema.org/fuelConsumption)(e.g. 8 liters per 100 km) and [fuelEfficiency](https://pending.schema.org/fuelEfficiency) (e.g. 30 miles per gallon). They are reciprocal.  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            -   Note 3: Often, the absolute value is useful only when related to driving speed ("at 80 km/h") or usage pattern ("city traffic"). You can use [valueReference](https://pending.schema.org/valueReference) to link the value for the fuel consumption to another value.    |
| [**fuelEfficiency**](https://pending.schema.org/fuelEfficiency)                           | [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                            | The distance traveled per unit of fuel used; most commonly miles per gallon (mpg) or kilometers per liter (km/L).                                                                                                                                                           
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            -   Note 1: There are unfortunately no standard unit codes for miles per gallon or kilometers per liter. Use [unitText](https://pending.schema.org/unitText) to indicate the unit of measurement, e.g. mpg or km/L.                                                          
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            -   Note 2: There are two ways of indicating the fuel consumption, [fuelConsumption](https://pending.schema.org/fuelConsumption)(e.g. 8 liters per 100 km) and [fuelEfficiency](https://pending.schema.org/fuelEfficiency) (e.g. 30 miles per gallon). They are reciprocal.  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            -   Note 3: Often, the absolute value is useful only when related to driving speed ("at 80 km/h") or usage pattern ("city traffic"). You can use [valueReference](https://pending.schema.org/valueReference) to link the value for the fuel economy to another value.        |
| [**fuelType**](https://pending.schema.org/fuelType)                                       | [QualitativeValue](https://pending.schema.org/QualitativeValue)  or                          
                                                                                             [Text](https://pending.schema.org/Text)  or                                                   
                                                                                             [URL](https://pending.schema.org/URL)                                                         | The type of fuel suitable for the engine or engines of the vehicle. If the vehicle has only one engine, this property can be attached directly to the vehicle.                                                                                                              |
| [**knownVehicleDamages**](https://pending.schema.org/knownVehicleDamages)                 | [Text](https://pending.schema.org/Text)                                                      | A textual description of known damages, both repaired and unrepaired.                                                                                                                                                                                                       |
| [**mileageFromOdometer**](https://pending.schema.org/mileageFromOdometer)                 | [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                            | The total distance travelled by the particular vehicle since its initial production, as read from its odometer.                                                                                                                                                             
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): KMT for kilometers, SMI for statute miles                                                                                                                                                                                                              |
| [**numberOfAirbags**](https://pending.schema.org/numberOfAirbags)                         | [Number](https://pending.schema.org/Number)  or                                              
                                                                                             [Text](https://pending.schema.org/Text)                                                       | The number or type of airbags in the vehicle.                                                                                                                                                                                                                               |
| [**numberOfAxles**](https://pending.schema.org/numberOfAxles)                             | [Number](https://pending.schema.org/Number)  or                                              
                                                                                             [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                             | The number of axles.                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): C62                                                                                                                                                                                                                                                    |
| [**numberOfDoors**](https://pending.schema.org/numberOfDoors)                             | [Number](https://pending.schema.org/Number)  or                                              
                                                                                             [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                             | The number of doors.                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): C62                                                                                                                                                                                                                                                    |
| [**numberOfForwardGears**](https://pending.schema.org/numberOfForwardGears)               | [Number](https://pending.schema.org/Number)  or                                              
                                                                                             [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                             | The total number of forward gears available for the transmission system of the vehicle.                                                                                                                                                                                     
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): C62                                                                                                                                                                                                                                                    |
| [**numberOfPreviousOwners**](https://pending.schema.org/numberOfPreviousOwners)           | [Number](https://pending.schema.org/Number)  or                                              
                                                                                             [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                             | The number of owners of the vehicle, including the current one.                                                                                                                                                                                                             
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): C62                                                                                                                                                                                                                                                    |
| [**productionDate**](https://pending.schema.org/productionDate)                           | [Date](https://pending.schema.org/Date)                                                      | The date of production of the item, e.g. vehicle.                                                                                                                                                                                                                           |
| [**purchaseDate**](https://pending.schema.org/purchaseDate)                               | [Date](https://pending.schema.org/Date)                                                      | The date the item e.g. vehicle was purchased by the current owner.                                                                                                                                                                                                          |
| [**steeringPosition**](https://pending.schema.org/steeringPosition)                       | [SteeringPositionValue](https://pending.schema.org/SteeringPositionValue)                    | The position of the steering wheel or similar device (mostly for cars).                                                                                                                                                                                                     |
| [**vehicleConfiguration**](https://pending.schema.org/vehicleConfiguration)               | [Text](https://pending.schema.org/Text)                                                      | A short text indicating the configuration of the vehicle, e.g. '5dr hatchback ST 2.5 MT 225 hp' or 'limited edition'.                                                                                                                                                       |
| [**vehicleEngine**](https://pending.schema.org/vehicleEngine)                             | [EngineSpecification](https://pending.schema.org/EngineSpecification)                        | Information about the engine or engines of the vehicle.                                                                                                                                                                                                                     |
| [**vehicleIdentificationNumber**](https://pending.schema.org/vehicleIdentificationNumber) | [Text](https://pending.schema.org/Text)                                                      | The Vehicle Identification Number (VIN) is a unique serial number used by the automotive industry to identify individual motor vehicles.                                                                                                                                    |
| [**vehicleInteriorColor**](https://pending.schema.org/vehicleInteriorColor)               | [Text](https://pending.schema.org/Text)                                                      | The color or color combination of the interior of the vehicle.                                                                                                                                                                                                              |
| [**vehicleInteriorType**](https://pending.schema.org/vehicleInteriorType)                 | [Text](https://pending.schema.org/Text)                                                      | The type or material of the interior of the vehicle (e.g. synthetic fabric, leather, wood, etc.). While most interior types are characterized by the material used, an interior type can also be based on vehicle usage or target audience.                                 |
| [**vehicleModelDate**](https://pending.schema.org/vehicleModelDate)                       | [Date](https://pending.schema.org/Date)                                                      | The release date of a vehicle model (often used to differentiate versions of the same make and model).                                                                                                                                                                      |
| [**vehicleSeatingCapacity**](https://pending.schema.org/vehicleSeatingCapacity)           | [Number](https://pending.schema.org/Number)  or                                              
                                                                                             [QuantitativeValue](https://pending.schema.org/QuantitativeValue)                             | The number of passengers that can be seated in the vehicle, both in terms of the physical space available, and in terms of limitations set by law.                                                                                                                          
                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                            Typical unit code(s): C62 for persons.                                                                                                                                                                                                                                       |
| [**vehicleSpecialUsage**](https://auto.schema.org/vehicleSpecialUsage)                    | [Text](https://pending.schema.org/Text)                                                      | Indicates whether the vehicle has been used for special purposes, like commercial rental, driving school, or as a taxi. The legislation in many countries requires this information to be revealed when offering a car for sale.                                            |
| [**vehicleTransmission**](https://pending.schema.org/vehicleTransmission)                 | [QualitativeValue](https://pending.schema.org/QualitativeValue)  or                          
                                                                                             [Text](https://pending.schema.org/Text)  or                                                   
                                                                                             [URL](https://pending.schema.org/URL)                                                         | The type of component used for transmitting the power from a rotating power source to the wheels or other relevant component(s) ("gearbox" for cars).                                                                                                                       |

1.  <span id="_Toc209948274" class="anchor"><span id="_Toc327548013" class="anchor"><span id="_Toc327548213" class="anchor"><span id="_Ref329687100" class="anchor"><span id="_Toc461716387" class="anchor"></span></span></span></span></span>Document Management

2.  <span id="_Toc327548014" class="anchor"><span id="_Toc327548214" class="anchor"><span id="_Toc461716388" class="anchor"></span></span></span>Document History

| Version | Date      | Brief Description of Change | Approval Authority | Editor / Company      |
|---------|-----------|-----------------------------|--------------------|-----------------------|
| 0.10    | 8 Sept 16 | New PRD - first draft       | PSMC               | Allan Bartlett / GSMA |
|         |           |                             |                    |                       |

1.  <span id="_Toc327548015" class="anchor"><span id="_Toc327548215" class="anchor"><span id="_Toc461716389" class="anchor"></span></span></span>Other Information

| Type             | Description                             |
|------------------|-----------------------------------------|
| Document Owner   | Connected Living – IoT Big Data Project |
| Editor / Company | GSMA                                    |

It is our intention to provide a quality product for your use. If you find any errors or omissions, please contact us with your comments. You may notify us at <prd@gsma.com>

Your comments or suggestions & questions are always welcome.
