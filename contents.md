# DHIS2 in 120 minutes

---

## Disclaimer

- This is not a practical tranining
- This is not an alternative to the academy

Anyone in your team that is going to use WISN/POA and/or interact with the UDSM team on the features should do the academy - "now" (15-20 hours of content)

---

## Goals

- Give you an idea of what DHIS2 can do "out of the box"
- Give you the vocabulary associated so you can recognise it

---

## Agenda

- Intro
- Data Model & Data Entry
- Quality
- Reporting & Analysis
- Administration
- API

--

## Intro

---

## Quick about

- 10+ years of history
- Built by UiO
- Funding from Norad and others
- Open Source

---

## In a nutshell

A datawarehouse allowing to follow the full cycle of data management: 

- Collection of data ("Data Entry")
- Validation/Quality control ("Validation Rules", Quality checks)
- Analysis ("Pivot Table", "GIS", Reports, Reporting Rates)

---

Includes supporting use cases:

- Data administration
- User/permissions
- + API for integration

While sold as a health database, nothing there is actually health specific.

--

## Data Model & Data Entry

---

## Data model

How to work with "any" data in a generic system?

![Aggregate](https://yuml.me/mva/DHIS2_Aggregate_Model.png)

---

### Organisation Unit

A tree of structures, typically geographically organized:

- Country
- Region
- District
- Health Center

All data in DHIS2 are linked to an org unit (can be any level)

---

### Data Element

What is the value collected? Examples:

- number of consultations
- number of vaccines doses given

---

### Category

Disaggregation inside a Data Element, Example:

- Male/Female
- Age ranges

Sum of categories should make sense

---

### Period

Montly, Quarterly, Yearly + some other weird ones

---

### Does it fit ?

Yes if the data can be linked to:

- Org Unit ("where")
- Data Element ("what")
- Period ("when")

---

### Data Sets

You don't encode data individually - "group" of data elements
Specify Org Units and Data Elements

---

## Tracker

There is another (new) data model in DHIS2:

![Aggregate](https://yuml.me/mva/DHIS2_Tracker_Model.png)

(that's for another day)

---

## In practice: Data Entry

---

## Mobile data collection

Android based apps to enter data in DHIS2 ("Data Capture"), possibly offline

---

## 2. Quality control

---

### Quality control

- Starts with Data Element type
- Validation rules

Very important ("shit in, shit out")
Many programs with a lot of -bad- data

---

### Reporting Rates

- Did Baoma CHP report its quality data for September 2018?
- How many health centers in Kansai provinces reported their data for last quarter?

--

## Reporting & Analysis

---

### Indicators

- Formulas applied on values
- Ratios:
  - Number of premature births / Number of births
  - Number of vaccines / Target population

Can be used in analysis after

---

### Pivot table

As in XLS:

- Org Unit
- Data Elements
- Periods

---

### Same in (basic) charts

---

### Secret weapon

Download as XLS and work from there

---

### Favorites & Dashboard

Create the needed tables & charts
Share them

---

### In practice: Analysis

--

## Administration

---

### Creating/Updating Meta Data

Org Units, Data Elements, etc

---

### User Management

Roles + sub pyramid

---

### Keep it simple!

- Groups
- Never assign specific permissions to specific user

---

### Import / Export

- Meta data: XML/JSON/CSV
- Data

--

## API

---

For "machine to machine" communication

---

Examples:

- Importing data from an external system
- Exporting data to an internal system
- Batch processing

---

Three good things:

- It exists
- It's complete
- It works

It's even documented

---

Everything that is possible throught the interface is possible through the API

---

## Q/A