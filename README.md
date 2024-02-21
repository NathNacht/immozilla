# immozilla
[![forthebadge made-with-python](https://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

##  Description
This Python project employs web scraping techniques to compile a dataset of real estate properties in Belgium. Specifically, we utilized Immoweb to gather information on 10,000 houses and apartments available for sale across the country.

The outcome of this project provides us with the following headers in our files:

<li>
    <ul>Property ID</ul>
    <ul>Locality name</ul>
    <ul>Postal code</ul>
    <ul>Price</ul>
    <ul>Type of property (house or apartment)</ul>
    <ul>Subtype of property (bungalow, chalet, mansion, ...)</ul>
    <ul>Type of sale (note: exclude life sales)</ul>
    <ul>Number of rooms</ul>
    <ul>Living area (area in m²)</ul>
    <ul>Equipped kitchen (0/1)</ul>
    <ul>Furnished (0/1)</ul>
    <ul>Open fire (0/1)</ul>
    <ul>Terrace (area in m² or null if no terrace)</ul>
    <ul>Garden (area in m² or null if no garden)</ul>
    <ul>Surface of good</ul>
    <ul>Number of facades</ul>
    <ul>Swimming pool (0/1)</ul>
    <ul>State of building (new, to be renovated, ...)</ul>
</li>
##  Installation

* clone the repo
* Install all the libraries in requirements.txt

```bash
$ python3 main.py
```

* everything wil be stored in ./data/csvdump.csv. 

##  Workflow

### threathimmolinks
```mermaid
graph TD;
    A["immo_pagelinks(n)"]-->B[n is the amount of pages];
    B-->C["multiWeblinks()"];
    C-->D["write_json(weblinks)"];
```

### scraper
```mermaid
graph TD;
    A["immo_pagelinks(n)"]-->B[fetch_all_info_from_property()];
    B-->C["check_sale(property_dict)"];
    C-->D["data_to_insert_in_dataframe"];
```

### main
```mermaid
graph TD;
    A["multiWeblinks()"]-->B[ write_json(webklinks)];
    B-->C[" df.to_csv()"];
```

##  Usage

## Visuals

##  Contributors

##  Timeline