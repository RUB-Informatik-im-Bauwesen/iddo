Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# The Interconnected Data Dictionary Ontology (IDDO)

## Metadata
* **IRI**
  * `http://icdd.vm.rub.de/ontology/iddo`
* **Publisher(s)**
  * [Chair of Computing in Engineering, Ruhr University Bochum](https://www.inf.bi.rub.de)
* **Creators(s)**
  * [Sven Zentgraf](https://orcid.org/0000-0001-6058-7614)
    [[ORCID]](https://orcid.org/0000-0001-6058-7614)
    (<sven.zentgraf@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/sven_zentgraf.html.en)
* **Contributor(s)**
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Created**
  * 2019-01-01
* **Modified**
  * 2021-12-20
* **Issued**
  * 2021-12-06
* **Version Information**
  * v0.2
* **License**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
* **Ontology RDF**
  * RDF ([iddo-schema.ttl](turtle))
* **Code Repository**
  * [https://git.inf.bi.ruhr-uni-bochum.de/semweb-ontology/iddo](https://git.inf.bi.ruhr-uni-bochum.de/semweb-ontology/iddo)
### Description
<p>The interconnected data dictionary ontology maps the data model of the ISO 23386 for the describing, creating, and maintenance of properties in interconnected data dictionaries. <br>
The namespace for IDDO terms is <a href="http://icdd.vm.rub.de/ontology/iddo#">http://icdd.vm.rub.de/ontology/iddo#</a> <br>
The preferred prefix for the IDDO namespace is <code>iddo</code>.</p>
* **History Note:** <p>v0.2: ontology update 
 v0.1: initial ontology for BIMSTRUCT project </p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Annotation Properties](#annotationproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Beziehung des Merkmalsbezeichners in den miteinander verbundenen Datenkatalogen](#BeziehungdesMerkmalsbezeichnersindenmiteinanderverbundenenDatenkatalogen),
[Boundary value item](#Boundaryvalueitem),
[Boundary values list](#Boundaryvalueslist),
[Definierender Wert-Item](#DefinierenderWert-Item),
[Digital format item](#Digitalformatitem),
[Group of properties](#Groupofproperties),
[Liste definierender Werte](#ListedefinierenderWerte),
[Liste moeglicher Werte in Sprache N](#PossibleValueInLanguageN),
[Merkmal](#Merkmal),
[Relation of the group of properties identifier in the interconnected data dictionaries](#Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries),
[Symbol of the property in a given property group](#Symbolofthepropertyinagivenpropertygroup),
[Text Format Item](#TextFormatItem),
[Zugewiesenes Merkmal](#ZugewiesenesMerkmal),
### Zugewiesenes Merkmal
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#AssignedProperty`
Description | <p>Repraesentiert die Zweisung eines Merkmals und einer Merkmalszustandes an ein Feature of Interest (FOI)</p>
Super-classes |[http://www.w3id.org/opm#Property](http://www.w3id.org/opm#Property) (c)<br />
Restrictions |[iddo:hasPropertyReference](hasPropertyReference) (op) **exactly** 1<br />[http://www.w3id.org/opm#hasPropertyState](http://www.w3id.org/opm#hasPropertyState) **min** 1<br />
In domain of |[iddo:hasPropertyReference](hasPropertyReference) (op)<br />
In range of |[iddo:hasProperty](hasproperty) (op)<br />
### Boundary value item
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#BoundaryValueItem`
Description | <p>Boundary value interval consisting of the lower(minValue) and the upper(maxValue) interval boundary</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:minValue](https://schema.org/minValue) **exactly** 1<br />[sdo:maxValue](https://schema.org/maxValue) **exactly** 1<br />
In range of |[iddo:BoundaryValue](Boundaryvalue) (op)<br />
### Boundary values list
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#BoundaryValuesList`
Description | <p>Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)</p>
Usage Note | PA040
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:BoundaryValue](Boundaryvalue) (op) **min** 1 [iddo:BoundaryValueItem](Boundaryvalueitem) (c)<br />[iddo:Unit](Unit) (op) **exactly** 1<br />
In domain of |[iddo:BoundaryValue](Boundaryvalue) (op)<br />
In range of |[iddo:BoundaryValues](Boundaryvalues) (op)<br />
### Definierender Wert-Item
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DefiningValueItem`
Description | <p>Enthaelt einen definierenden Wert eines Arrays in Form eines Literals</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:DefiningValue](DefinierenderWert) (op)<br />
### Liste definierender Werte
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DefiningValuesList`
Description | <p>Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben</p>
Usage Note | PA035
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:DefiningValueItem](DefinierenderWert-Item) **min** 1<br />
In domain of |[iddo:DefiningValue](DefinierenderWert) (op)<br />
In range of |[iddo:DefiningValues](Definingvalues) (op)<br />
### Digital format item
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DigitalFormatItem`
Description | <p>Paar fuer den digitalen Texttyp (Praezision, Masseinheit) Praezision ist die Anzahl signifikanter Stellen</p>
Usage Note | PA037
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Unit](Unit) (op) **exactly** 1<br />[iddo:Precision](Toleranz) (dp) **exactly** 1<br />
In domain of |[iddo:Unit](Unit) (op)<br />[iddo:Precision](Toleranz) (dp)<br />
In range of |[iddo:DigitalFormat](DigitalesFormat) (op)<br />
### Group of properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#GroupOfProperties`
Description | <p>Collection enabling the properties to be prearranged or organized</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **min** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:CountryOfUse](CountryOfUse) (dp) **min** 1<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[iddo:DefinitionInLanguage](Definitionoftheproperty/groupofpropertiesinlanguageN) (dp) **min** 1<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:CategoryOfGroupOfProperties](Categoryofgroupofproperties) (dp) **exactly** 1<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op) **min** 0 [iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 1<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op) **min** 0 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op) **max** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />
In domain of |[iddo:DeprecationExplanation](DeprecationExplanation) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp)<br />[iddo:DefinitionInLanguage](Definitionoftheproperty/groupofpropertiesinlanguageN) (dp)<br />[iddo:RevisionNumber](Revisionnumber) (dp)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:CountryOfUse](CountryOfUse) (dp)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:Status](Status) (dp)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:DateOfVersion](Dateofversion) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:CategoryOfGroupOfProperties](Categoryofgroupofproperties) (dp)<br />
In range of |[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op)<br />[iddo:ParentGroupOfProperties](uebergeordneteMerkmalsgruppe) (op)<br />[iddo:ListOfReplacingGroupsOfProperties](Listofreplacinggroupsofproperties) (op)<br />[iddo:ListOfReplacedGroupsOfProperties](Listofreplacedgroupsofproperties) (op)<br />
### Liste moeglicher Werte in Sprache N
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#PossibleValueInLanguageN`
Description | <p>Moeglicher Wert fuer das Merkmal und Sprache Werte koennen String oder Zahlen sein</p>
Usage Note | PA039
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />[sdo:PropertyValue](https://schema.org/PropertyValue) (c)<br />
Restrictions |[sdo:value](https://schema.org/value) **exactly** 1<br />
In range of |[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />
### Merkmal
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Property`
Description | <p>Inherent or acquired feature of an item</p>
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:Units](Units) (op) **min** 0<br />[iddo:DateOfRevision](Dateofrevision) (dp) **exactly** 1<br />[iddo:NameInLanguage](NameinSpracheN) (dp) **min** 1<br />[iddo:DateOfCreation](Dateofcreation) (dp) **exactly** 1<br />[iddo:DigitalFormat](DigitalesFormat) (op) **min** 0 [iddo:DigitalFormatItem](Digitalformatitem) (c)<br />[iddo:TextFormat](Textformat) (op) **min** 0 [iddo:TextFormatItem](TextFormatItem) (c)<br />[iddo:Dimension](Dimension) (dp) **max** 1<br />[iddo:DateOfActivation](DatumderAktivierung) (dp) **min** 0<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op) **min** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp) **max** 1<br />[iddo:Status](Status) (dp) **exactly** 1<br />[iddo:NameOfTheDefiningValues](Namesofthedefiningvalues) (dp) **min** 0<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **min** 0<br />[iddo:VersionNumber](Versionsnummer) (dp) **exactly** 1<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp) **min** 0<br />[iddo:RevisionNumber](Revisionnumber) (dp) **exactly** 1<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0 [iddo:PossibleValueInLanguageN](PossibleValueInLanguageN) (c)<br />[iddo:DataType](Datatype) (dp) **exactly** 1<br />[iddo:PhysicalQuantity](PhysikalischeGroesse) (dp) **min** 1<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op) **min** 0 [iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />[iddo:ExampleInLanguage](BeispieldesMerkmalsinSpracheN) (dp) **min** 0<br />[iddo:DateOfLastChange](Dateoflastchange) (dp) **min** 0<br />[iddo:CountryOfOrigin](Countryoforigin) (dp) **min** 0<br />[iddo:DefiningValues](Definingvalues) (op) **min** 0 [iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp) **exactly** 1<br />[iddo:ListOfReplacingProperties](Listofreplacingproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp) **min** 0<br />[iddo:BoundaryValues](Boundaryvalues) (op) **exactly** 1 [iddo:BoundaryValuesList](Boundaryvalueslist) (c)<br />[iddo:ConnectedProperties](Connectedproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op) **min** 0 [iddo:RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries](BeziehungdesMerkmalsbezeichnersindenmiteinanderverbundenenDatenkatalogen) (c)<br />[iddo:CountryOfUse](CountryOfUse) (dp) **min** 1<br />[iddo:DateOfVersion](Dateofversion) (dp) **exactly** 1<br />[iddo:Dimension](Dimension) (dp) **min** 0<br />[iddo:DescriptionInLanguage](DescriptionofthepropertyinlanguageN) (dp) **min** 0<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp) **min** 0<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp) **min** 0<br />[iddo:Tolerance](Tolerance) (dp) **min** 0<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op) **min** 0<br />[iddo:DefinitionInLanguage](Definitionoftheproperty/groupofpropertiesinlanguageN) (dp) **min** 1<br />[iddo:DynamicProperty](DynamicProperty) (dp) **exactly** 1<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp) **max** 1<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op) **min** 0 [iddo:Property](Merkmal) (c)<br />
In domain of |[iddo:Status](Status) (dp)<br />[iddo:DateOfDeactivation](DatumderDeaktivierung) (dp)<br />[iddo:VisualRepresentation](Visualrepresentation) (dp)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op)<br />[iddo:Tolerance](Tolerance) (dp)<br />[iddo:DateOfVersion](Dateofversion) (dp)<br />[iddo:DateOfRevision](Dateofrevision) (dp)<br />[iddo:Units](Units) (op)<br />[iddo:ExampleInLanguage](BeispieldesMerkmalsinSpracheN) (dp)<br />[iddo:DeprecationExplanation](DeprecationExplanation) (dp)<br />[iddo:BoundaryValues](Boundaryvalues) (op)<br />[iddo:DefinitionInLanguage](Definitionoftheproperty/groupofpropertiesinlanguageN) (dp)<br />[iddo:CreatorsLanguage](ErlaeuterungfuerdieAblehnung) (dp)<br />[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />[iddo:CountryOfOrigin](Countryoforigin) (dp)<br />[iddo:MethodOfMeasurement](Methodofmeasurement) (dp)<br />[iddo:RevisionNumber](Revisionnumber) (dp)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:DateOfCreation](Dateofcreation) (dp)<br />[iddo:ListOfReplacingProperties](Listofreplacingproperties) (op)<br />[iddo:Dimension](Dimension) (dp)<br />[iddo:CountryOfUse](CountryOfUse) (dp)<br />[iddo:SubdivisionOfUse](Subdivisionofuse) (dp)<br />[iddo:VersionNumber](Versionsnummer) (dp)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />[iddo:DateOfLastChange](Dateoflastchange) (dp)<br />[iddo:ListOfPossibleValuesInLanguageN](ListemoeglicherWerteinSpracheN) (op)<br />[iddo:DateOfActivation](DatumderAktivierung) (dp)<br />[iddo:DefiningValues](Definingvalues) (op)<br />[iddo:GroupsOfProperties](Merkmalsgruppe(n)) (op)<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp)<br />[iddo:ConnectedProperties](Connectedproperties) (op)<br />[iddo:PhysicalQuantity](PhysikalischeGroesse) (dp)<br />[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op)<br />[iddo:DataType](Datatype) (dp)<br />[iddo:NameInLanguage](NameinSpracheN) (dp)<br />[iddo:DigitalFormat](DigitalesFormat) (op)<br />[iddo:TextFormat](Textformat) (op)<br />
In range of |[iddo:hasPropertyReference](hasPropertyReference) (op)<br />[iddo:ListOfReplacedProperties](Listofreplacedproperties) (op)<br />[iddo:ConnectedProperties](Connectedproperties) (op)<br />[iddo:ListOfReplacingProperties](Listofreplacingproperties) (op)<br />[iddo:ParametersOfTheDynamicProperty](Parametersofthedynamicproperty) (op)<br />
### Beziehung des Merkmalsbezeichners in den miteinander verbundenen Datenkatalogen
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries`
Description | <p>Pair (property internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing properties</p>
Usage Note | PA014
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />
In domain of |[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp)<br />
### Relation of the group of properties identifier in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | <p>Pair (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties</p>
Usage Note | GA014
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:GloballyUniqueIdentifier](GlobaleindeutigerBezeichner(GUID)) (dp) **exactly** 1<br />[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp) **exactly** 1<br />[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp) **exactly** 1<br />
In domain of |[iddo:InterConDictID](InterconnectedDataDictionaryID) (dp)<br />
In range of |[iddo:RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen) (op)<br />[iddo:RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries) (op)<br />
### Symbol of the property in a given property group
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#SymbolOfTheProperty`
Description | <p>Pair (symbol of the property, globally unique identifier of the group of properties (attribute GA001))</p>
Usage Note | PA022
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:GivenGroupsOfProperties](Givengroupofproperties) (op) **exactly** 1 [iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Symbol](Symbol) (dp) **exactly** 1<br />
In domain of |[iddo:Symbol](Symbol) (dp)<br />
In range of |[iddo:SymbolsOfTheProperty](Symbolsofthepropertyinagivenpropertygroup) (op)<br />
### Text Format Item
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#TextFormatItem`
Description | <p>Paar fuer den Texttyp (Verschluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt</p>
Usage Note | PA038
Super-classes |[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
Restrictions |[iddo:NumberOfCharacters](NumberofCharacters) (dp) **exactly** 1<br />[iddo:Encoding](Encoding) (dp) **exactly** 1<br />
In domain of |[iddo:Encoding](Encoding) (dp)<br />[iddo:NumberOfCharacters](NumberofCharacters) (dp)<br />
In range of |[iddo:TextFormat](Textformat) (op)<br />

## Object Properties
[Boundary value](#Boundaryvalue),
[Boundary values](#Boundaryvalues),
[Connected properties](#Connectedproperties),
[Definierender Wert](#DefinierenderWert),
[Defining values](#Definingvalues),
[Digitales Format](#DigitalesFormat),
[Given group of properties](#Givengroupofproperties),
[Merkmalsgruppe(n)](#Merkmalsgruppe(n)),
[Liste moeglicher Werte in Sprache N](#ListemoeglicherWerteinSpracheN),
[List of replaced groups of properties](#Listofreplacedgroupsofproperties),
[List of replaced properties](#Listofreplacedproperties),
[List of replacing groups of properties](#Listofreplacinggroupsofproperties),
[List of replacing properties](#Listofreplacingproperties),
[Parameters of the dynamic property](#Parametersofthedynamicproperty),
[uebergeordnete Merkmalsgruppe](#uebergeordneteMerkmalsgruppe),
[Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen](#BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen),
[Relations of the property identifiers in the interconnected data dictionaries](#Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries),
[Symbols of the property in a given property group](#Symbolsofthepropertyinagivenpropertygroup),
[Textformat](#Textformat),
[Unit](#Unit),
[Units](#Units),
[has property](#hasproperty),
[has Property Reference](#hasPropertyReference),
[](Boundaryvalue)
### Boundary value
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#BoundaryValue`
Description | Single Boundary value interval
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:BoundaryValuesList](Boundaryvalueslist) (c)<br />
Range(s) |[iddo:BoundaryValueItem](Boundaryvalueitem) (c)<br />
[](Boundaryvalues)
### Boundary values
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#BoundaryValues`
Description | Paar (Liste von Grenzwert-Intervallen moeglicher Werte fuer das Merkmal, Einheit)
Usage Note | PA040
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:BoundaryValuesList](Boundaryvalueslist) (c)<br />
[](Connectedproperties)
### Connected properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ConnectedProperties`
Description | List of the globally unique identifier of the connected properties (attribute PA001); the value of one property is related to the values of the other ones. For example, a sound absorption coefficient is given for a specific frequency, in this case sound absorption and frequency are connected properties
Usage Note | PA020
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](DefinierenderWert)
### Definierender Wert
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DefiningValue`
Description | Enthaelt einen definierenden Wert eines Arrays
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
Range(s) |[iddo:DefiningValueItem](DefinierenderWert-Item) (c)<br />
[](Definingvalues)
### Defining values
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DefiningValues`
Description | Im Falle eines Feldes liefert dieses Attribut die definierenden Werte, sofern zutreffend, der Datentyp wird durch das Attribut PA030 angegeben
Usage Note | PA035
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DefiningValuesList](ListedefinierenderWerte) (c)<br />
[](DigitalesFormat)
### Digitales Format
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DigitalFormat`
Description | Pair for digital text type (precision, unit) Precision is the number of significant digits
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
[](Givengroupofproperties)
### Given group of properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#GivenGroupsOfProperties`
Description | Globally unique identifier of a group of properties (attribute GA001) for the symbol assigned to the property.
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Merkmalsgruppe(n))
### Merkmalsgruppe(n)
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#GroupsOfProperties`
Description | List of globally unique identifiers of groups of properties (attribute GA001) to which the property is attached
Usage Note | PA021
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](ListemoeglicherWerteinSpracheN)
### Liste moeglicher Werte in Sprache N
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ListOfPossibleValuesInLanguageN`
Description | Liste von Paaren (moeglicher Wert fuer das Merkmal und Sprache) Werte koennen String oder Zahlen sein
Usage Note | PA039
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:PossibleValueInLanguageN](PossibleValueInLanguageN) (c)<br />
[](Listofreplacedgroupsofproperties)
### List of replaced groups of properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ListOfReplacedGroupsOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzten Merk-malsgruppen
Usage Note | GA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Listofreplacedproperties)
### List of replaced properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ListOfReplacedProperties`
Description | Globally unique identifier of the replaced property (or properties)
Usage Note | PA011
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](Listofreplacinggroupsofproperties)
### List of replacing groups of properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ListOfReplacingGroupsOfProperties`
Description | Liste von globalen Bezeichnern fuer die ersetzenden Merkmalsgruppen
Usage Note | GA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Listofreplacingproperties)
### List of replacing properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ListOfReplacingProperties`
Description | global eindeutiger Bezeichner (Attribut PA001) des ersetzenden Merkmals (oder der Merkmale)
Usage Note | PA012
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](Parametersofthedynamicproperty)
### Parameters of the dynamic property
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ParametersOfTheDynamicProperty`
Description | List of GUIDS of properties which are parameters of the function for a dynamic property
Usage Note | PA032
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />
[](uebergeordneteMerkmalsgruppe)
### uebergeordnete Merkmalsgruppe
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ParentGroupOfProperties`
Description | Enables a sub-group to be linked to a parent group via their globally unique identifiers (attribute GA001) Any property attached to a group is inherited by the sub-group(s)
Usage Note | GA023
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](BeziehungderBezeichnerderMerkmalsgruppeindenmiteinanderverbundenenDatenkatalogen)
### Beziehung der Bezeichner der Merkmalsgruppe in den miteinander verbundenen Datenkatalogen
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#RelationsOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries`
Description | List of pairs (group of properties internal identifier, corresponding data dictionary identifier) This attribute should be used for compatibility between already existing groups of properties
Usage Note | GA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
[](Relationsofthepropertyidentifiersintheinterconnecteddatadictionaries)
### Relations of the property identifiers in the interconnected data dictionaries
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#RelationsOfThePropertyIdentifiersInTheInterconnectedDataDictionaries`
Description | Liste von Paaren (interner Merk-malsbezeichner, entsprechender Datenkatalog-Bezeichner) dieses Attribut sollte fuer die Vertraeglichkeit zwischen bereits vorhandenen Merkmalen verwendet werden
Usage Note | PA014
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
[](Symbolsofthepropertyinagivenpropertygroup)
### Symbols of the property in a given property group
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#SymbolsOfTheProperty`
Description | List of pairs (symbol of the property, globally unique identifier of the group of properties (attribute GA001))
Usage Note | PA022
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
[](Textformat)
### Textformat
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#TextFormat`
Description | Paar fuer den Texttyp (Ver-schluesselung, Anzahl der Zeichen) die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[iddo:TextFormatItem](TextFormatItem) (c)<br />
[](Unit)
### Unit
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Unit`
Description | Masseinheit fuer den digitalen Texttyp
Usage Note | PA037
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](Units)
### Units
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Units`
Description | A unit to represent a scale that enables a value to be measured It is possible to use this attribute to explain there is no unit attached to the property by using unitless
Usage Note | PA033
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[http://qudt.org/schema/qudt/Unit](http://qudt.org/schema/qudt/Unit) (c)<br />
[](hasproperty)
### has property
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#hasProperty`
Description | Fuegt ein Merkmal zu einem Feature of Interest (FOI) hinzu
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Range(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
[](hasPropertyReference)
### has Property Reference
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#hasPropertyReference`
Description | Attaches a property reference to a property assignment
Super-properties |[owl:topObjectProperty](http://www.w3.org/2002/07/owl#topObjectProperty)<br />
Domain(s) |[iddo:AssignedProperty](ZugewiesenesMerkmal) (c)<br />
Range(s) |[iddo:Property](Merkmal) (c)<br />

## Datatype Properties
[Category of group of properties](#Categoryofgroupofproperties),
[Country of origin](#Countryoforigin),
[Country of origin](#CountryOfUse),
[Erlaeuterung fuer die Ablehnung](#ErlaeuterungfuerdieAblehnung),
[Data type](#Datatype),
[Datum der Aktivierung](#DatumderAktivierung),
[Date of creation](#Dateofcreation),
[Datum der Deaktivierung](#DatumderDeaktivierung),
[Date of last change](#Dateoflastchange),
[Date of revision](#Dateofrevision),
[Date of version](#Dateofversion),
[Definition of the property/group of properties in language N](#Definitionoftheproperty/groupofpropertiesinlanguageN),
[Erlaeuterung fuer die Ablehnung](#DeprecationExplanation),
[Description of the property in language N](#DescriptionofthepropertyinlanguageN),
[Dimension](#Dimension),
[Dynamic Property](#DynamicProperty),
[Encoding](#Encoding),
[Beispiel des Merkmals in Sprache N](#BeispieldesMerkmalsinSpracheN),
[Global eindeutiger Bezeichner (GUID)](#GlobaleindeutigerBezeichner(GUID)),
[Interconnected Data Dictionary ID](#InterconnectedDataDictionaryID),
[Method of measurement](#Methodofmeasurement),
[Name in Sprache N](#NameinSpracheN),
[Names of the defining values](#Namesofthedefiningvalues),
[Number of Characters](#NumberofCharacters),
[Physikalische Groesse](#PhysikalischeGroesse),
[Toleranz](#Toleranz),
[Revision number](#Revisionnumber),
[Status](#Status),
[Subdivision of use](#Subdivisionofuse),
[Symbol](#Symbol),
[Toleranz](#Tolerance),
[Versionsnummer](#Versionsnummer),
[Visual representation](#Visualrepresentation),
[](Categoryofgroupofproperties)
### Category of group of properties
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#CategoryOfGroupOfProperties`
Description | Gibt die Kategorie der erstellten Merkmalsgruppe an
Usage Note | GA022
Example | ````Reference document`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Countryoforigin)
### Country of origin
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#CountryOfOrigin`
Description | Country from where the requirement for this property/group of properties originated
Usage Note | PA026/GA021
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](CountryOfUse)
### Country of origin
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#CountryOfUse`
Description | Country from where the requirement for this property/group of properties originated
Usage Note | PA024/GA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](ErlaeuterungfuerdieAblehnung)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#CreatorsLanguage`
Description | Sentence explaining the reason of the deprecation, which can explain how to convert values to conform to the new property; this explanation has to be written in international English (EN)
Usage Note | PA015/GA015
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Datatype)
### Data type
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DataType`
Description | Format for expressing the value of the property This can be understood as the storage type from a software perspective In case of a dynamic property the value of this attribute is the datatype of the result of the calculation by the formula
Usage Note | PA030
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DatumderAktivierung)
### Datum der Aktivierung
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DateOfActivation`
Description | Date after when the property can be used
Usage Note | PA04/GA04
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofcreation)
### Date of creation
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DateOfCreation`
Description | Datum der Validierung der An-frage zur Erstellung des Merkmals durch Sachverstaendige
Usage Note | PA003/GA003
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](DatumderDeaktivierung)
### Datum der Deaktivierung
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DateOfDeactivation`
Description | Date of deactivation
Usage Note | PA008/GA008
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateoflastchange)
### Date of last change
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DateOfLastChange`
Description | Datum der Validierung der letzten Aenderungsanfrage durch Sachverstaendige
Usage Note | PA005/GA005
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofrevision)
### Date of revision
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DateOfRevision`
Description | Datum der Ueberarbeitung
Usage Note | PA006/GA006
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Dateofversion)
### Date of version
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DateOfVersion`
Description | Date of version
Usage Note | PA007/GA007
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime) (c)<br />
[](Definitionoftheproperty/groupofpropertiesinlanguageN)
### Definition of the property/group of properties in language N
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DefinitionInLanguage`
Description | Liste von Paaren (Definition des Merkmals/der Merkmalsgruppe, Sprache)
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DeprecationExplanation)
### Erlaeuterung fuer die Ablehnung
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DeprecationExplanation`
Description | Satz, der den Grund fuer die Ablehnung erlaeutert, der erklaeren kann, wie Werte umzurechnen sind, damit sie dem neuen Merkmal/der neuen Merkmalsgruppe entsprechen; diese Erlaeuterung muss in internationalem Englisch (EN) geschrieben werden
Usage Note | PA013/GA013
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DescriptionofthepropertyinlanguageN)
### Description of the property in language N
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DescriptionInLanguage`
Description | Liste von Paaren (Beschreibung des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Dimension)
### Dimension
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Dimension`
Description | In case of a physical quantity, dimension according to ISO 80000 (all parts) This attribute allows the dimension to be machine readable; as all physical quantities are derived from 7 base quantities, it is provided with the power (as a rational number) attached to a basic dimension in the following order and with one space between each
Usage Note | PA028
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](DynamicProperty)
### Dynamic Property
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#DynamicProperty`
Description | Wenn es sich um ein dynamisches Merkmal handelt, haengt der Wert von den im Attribut PA032 bereitgestellten Parametern ab
Usage Note | PA031
Example | ````yes`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
[](Encoding)
### Encoding
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Encoding`
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](TextFormatItem) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](BeispieldesMerkmalsinSpracheN)
### Beispiel des Merkmals in Sprache N
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#ExampleInLanguage`
Description | Liste von Paaren (Beispiel des Merkmals, Sprache)
Usage Note | PA019
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](GlobaleindeutigerBezeichner(GUID))
### Global eindeutiger Bezeichner (GUID)
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#GloballyUniqueIdentifier`
Description | Eindeutiger Bezeichner, der mit dem in RFC 4122 beschriebenen Algorithmus erzeugt wird
Usage Note | PA001/GA001
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](InterconnectedDataDictionaryID)
### Interconnected Data Dictionary ID
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#InterConDictID`
Description | Entsprechender Daten-katalog-Bezeichner
Usage Note | PA014
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:RelationOfPropertiyIdentifiersInTheInterconnectedDataDictionaries](BeziehungdesMerkmalsbezeichnersindenmiteinanderverbundenenDatenkatalogen) (c)<br />[iddo:RelationOfTheGroupOfPropertiesIdentifiersInTheInterconnectedDataDictionaries](Relationofthegroupofpropertiesidentifierintheinterconnecteddatadictionaries) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Methodofmeasurement)
### Method of measurement
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#MethodOfMeasurement`
Description | Beurteilung von Bauprodukten, um ihre Tauglichkeit entsprechend den Anforderungen in harmonisierten technischen Spezifikationen sicherzustellen
Usage Note | PA029
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NameinSpracheN)
### Name in Sprache N
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#NameInLanguage`
Description | Liste von Paaren (Name des Merkmals und Sprache) Dieses Attribut kann verwendet werden, um Synonyme fuer verschiedene Domaenen hinzuzufuegen
Usage Note | PA016/GA016
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Namesofthedefiningvalues)
### Names of the defining values
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#NameOfTheDefiningValues`
Description | In case of an array, this attribute provides the names of the column headers defined as a list of pairs (name, language)
Usage Note | PA034
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](NumberofCharacters)
### Number of Characters
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#NumberOfCharacters`
Description | Die Verschluesselung wird nach Name der Codierungsnorm von IANA, RFC 2978 festgelegt
Usage Note | PA038
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:TextFormatItem](TextFormatItem) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](PhysikalischeGroesse)
### Physikalische Groesse
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#PhysicalQuantity`
Description | List of pairs (physical quantity | language) Physical quantities are expressed in International System (SI) units Non-physical quantities such as text are expressed with the value "without" This is equivalent to a measure in ISO 16739-1 and ISO 10303 Only one physical quantity can be attached to a property. This attribute is used to provide the quantity in plain text with all the needed translations
Usage Note | PA027
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Toleranz)
### Toleranz
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Precision`
Description | Praezision ist die Anzahl signifi-kanter Stellen
Usage Note | PA037
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:DigitalFormatItem](Digitalformatitem) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Revisionnumber)
### Revision number
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#RevisionNumber`
Description | Diese Nummer der ueberarbeitung ermoeglicht die Verfolgung kleinerer aenderungen, z. B. neue uebersetzung, Korrekturen von Tippfehlern: wenn sich die Versionsnummer aendert, beginnt die Nummer der ueberarbeitung wieder bei 1. Sachverstaendige entscheiden, ob eine neue Nummer der ueberarbeitung angewendet werden kann oder ob eine neue ueberarbeitung erforderlich ist.
Usage Note | PA010/GA010
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Status)
### Status
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Status`
Description | Status des Merkmals waehrend seines Lebenszyklus
Usage Note | PA002/GA002
Example | ````inactive`<br />```
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />[iddo:GroupOfProperties](Groupofproperties) (c)<br />
[](Subdivisionofuse)
### Subdivision of use
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#SubdivisionOfUse`
Description | Dokumentierte geographische Region, in der das Merkmal/ die Merkmalsgruppe verwendet wird
Usage Note | PA025/GA020
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Symbol)
### Symbol
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Symbol`
Usage Note | PA022
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:SymbolOfTheProperty](Symbolofthepropertyinagivenpropertygroup) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](Tolerance)
### Toleranz
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#Tolerance`
Description | Fuer numerische Werte; der Gesamtbetrag, um den eine be-stimmte Einheit schwanken darf; sie ist die Differenz zwischen dem Hoechstwert und dem Mindestwert fuer die Einheit
Usage Note | PA036
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:decimal](http://www.w3.org/2001/XMLSchema#decimal) (c)<br />
[](Versionsnummer)
### Versionsnummer
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#VersionNumber`
Description | This version number allows tracking of major changes. Experts decide if a new version number must be applied
Usage Note | PA009/GA009
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](Visualrepresentation)
### Visual representation
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#VisualRepresentation`
Description | Visual representation of the group of properties through sketches, photos, videos or other multimedia objects
Usage Note | PA023/GA018
Super-properties |[owl:topDataProperty](http://www.w3.org/2002/07/owl#topDataProperty)<br />
Domain(s) |[iddo:GroupOfProperties](Groupofproperties) (c)<br />[iddo:Property](Merkmal) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Annotation Properties
[Code](#Code),
[](Code)
### Code
Property | Value
--- | ---
IRI | `http://icdd.vm.rub.de/ontology/iddo#code`
Is Defined By | http://www.w3.org/2000/01/rdf-schema#
Description | Code, der zur Identifizierung des Attributs verwendet werden kann
Domain(s) |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Range(s) |[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#Literal) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `http://icdd.vm.rub.de/ontology/iddo#`
* **dc**
  * `http://purl.org/dc/terms/`
* **iddo**
  * `http://icdd.vm.rub.de/ontology/iddo#`
* **opm**
  * `https://w3id.org/opm#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **unit**
  * `http://qudt.org/vocab/unit/`
* **vann**
  * `http://purl.org/vocab/vann/`
* **voaf**
  * `http://purl.org/vocommons/voaf#`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni