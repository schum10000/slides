> Semantic

![](media/image1.png){width="2.5083333333333333in" height="7.5in"}Web
=====================================================================

Block II
--------

### Themenblock II 

**Serialisierung von RDF ( Turtle, **

**N-Triples) **

> **\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--**

![](media/image1.png){width="0.35in" height="7.5in"}8.12.2017
**RDF/XML**

> **\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--**

**Wissensorganisation mit **

**Vokabularen**

> **\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--**
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther
>
> **Serialisierung von RDF **
>
> ![](media/image3.png){width="2.5033344269466316in"
> height="7.5in"}**(Turtle, N-Triples) **
>
> Hochschule Hannover - BIB - WS 2017/2018 Walther

3

#### RDF Wiederholung

**Tripelstruktur (= RDF-Triple) -\> **

> **\<Subjekt\>\<Prädikat\>\<Objekt\>**

**Jedes Triple -- eine Aussage (RDF-Statement)**

**Subjekt und Prädikat werden durch URI bezeichnet, Objekt **

> **-- durch einen URI oder ein RDF-Literal**

![](media/image12.png){width="0.35in" height="7.5in"}Ausnahme: **Blank
Nodes -- Leere Knoten zur Beschreibung von unbenannten Ressourcen** Vgl.
Hitzler u. a.(2008), S.40

> ![](media/image4.png){width="5.906667760279965in"
> height="3.1366666666666667in"}
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

### RDF-Serialisierung

Für maschinelle Verarbeitung von Informationen -\> **Serialisierung**
(„Umwandlung komplexer Objekte in lineare Zeichenketten") ebd.

Verschiedene Serialisierungsvarianten sind vollkommen äquivalent.

![](media/image12.png){width="0.35in" height="7.5in"}Inhalte können
ohne Informationsverlust vom einem in das andere Format übersetzt werden

-   [[http://www.w3.org/RDF/Validator/]{.underline}](http://www.w3.org/RDF/Validator/)

-   [[http://rdf-translator.appspot.com/]{.underline}](http://rdf-translator.appspot.com/)

-   [<http://ttl.summerofcode.be/>]{.underline} - Validierung von Turtle

N3 (Notation N3), **N-Triples, Turtle, RDF/XML**, RDFa, JASON LD

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

### RDF-Serialisierung

> **N3** (Notation N3)- die älteste
>
> Serialisierungsart von RDF, entwickelt 1998
>
> komplexe Regeln
>
> **N-Triples** und **Turtle** -- Teile von **N3**
>
> ![](media/image12.png){width="0.35in" height="7.5in"}**N-Triples** -
> Grundform
>
> **Turtle**
>
> Kürzer
>
> Verständlich für Menschen und Maschinen
>
> Am meisten verbreitet

**RDF/XML** - XML-Syntax Vgl. ebd~.~

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### RDF-Serialisierung N-Triples

**N-Triples** Bsp.:

\<http://ik.hsh/id/\#JojoMoyes\>

> ![](media/image12.png){width="0.35in"
> height="7.5in"}\<http://ik.hsh/ont/\#istAutorinVon\>
> \<http://ik.hsh/id/\#MeBeforeYou\> .

\<http://ik.hsh/id/\#JojoMoyes\>

> \<http://ik.hsh/ont/\#hatNamen\> „Jojo Moyes" .

\<http://ik.hsh/id/\#MeBeforeYou\>

> \<http://ik.hsh/ont/\#hatTitel\> „Me Before You" .
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

\@prefixhsho:
\<[[http://ik.hsh/ont/\#]{.underline}\>](http://ik.hsh/ont/).
\@prefixhshi: \<http://ik.hsh/id/\#\> .

**hshi:JojoMoyes** hsho:istAutorinVon hshi:MeBeforeYou

> hsho:hatNamen „Jojo Moyes" **[.]{.underline}**

#### RDF-Serialisierung Turtle

![](media/image12.png){width="0.35in" height="7.5in"}Deklaration von
Namensräumen, übernommen aus XML Vgl.

> ebd., S. 41

**[;]{.underline}**Triple mit dem gleichen Subjekt werden
zusammengefasst

**;** - Verbindet die Aussagen, die sich auf dasselbe Subjekt beziehen

**.** -- Beendet die Aussagen.

Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### RDF-Serialisierung

\@prefixhsho:
\<[[http://ik.hsh/ont/\#]{.underline}\>](http://ik.hsh/ont/) .

\@prefixhshi: \<http://ik.hsh/id/\#\> .

**hshi:MeBeforeYou hsho:hatTitel**

„Me Before You"**[,]{.underline}**

„Das ganze halbe Jahr" **[.]{.underline}**

**,** - verbindet zwei oder mehrere Objekte die sich auf dasselbe
Subjekt-Prädikat-Paar beziehen

#### ![](media/image12.png){width="0.35in" height="7.5in"}Turtle

Triple mit den gleichen Subjekt und Prädikat werden ebenfalls
zusammengefasst

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Blank Nodes in N-Triples

> In N-Triples werden leere Knoten mithilfe eines Unterstrichs anstelle
> eines Namensraum-Präfixes (**\_:jA145**) dargestellt:
>
> \<http://www.w3.org/TR/rdf-syntax-grammar\>
>
> \<http://example.org/stuff/1.0/editor\> **\_:jA145** .
>
> **\_:jA145**
>
> ![](media/image12.png){width="0.35in"
> height="7.5in"}\<http://example.org/stuff/1.0/fullName\> \"Dave
> Beckett\" .
>
> **\_:jA145** könnte auch **\_:re4672** heißen, die Bedeutung würde
> unverändert bleiben, da **\_:jA145** -- nur lokal gültig ist.
>
> Viele Anwendungen bevorzugen statt Blank Nodes Hilfs-URIs
>
> **-** bessere Wiederverwendbarkeit von Daten

Vgl. ebd., S. 57ff

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

##### Blank Nodes in N3 und Turtle

> Schreibweise in Turtle für Blank Node -- ähnlich wie in NTriples
>
> **\@prefix ex: \<http://example.org/\> . ex:MeBeforeYou
> ex:hatVerfilmung \_:id1 .**
>
> ![](media/image12.png){width="0.35in" height="7.5in"}**\_:id1
> ex:besatzung ex:EmiliaClark; ex:dateTime «2016» .**
>
> Weglassung von Blank-Node-Angabe durch die geschachtelte
>
> Darstellung -- Abgekürzte Schreibweise
>
> **\@prefix** hsh: **\<http://ik.hsh.org/Beispiel/\> .**
>
> **\@prefix** rdf: **\<http://www.w3.org/1999/02/22-rdf-syntax-ns\#\> .
> hsh:Tom hsh:faengt \[ a hsh:Maus \] .** = Tom fängt eine Maus.
>
> Vgl. ebd.
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Reifizierung

\@prefix example: \<http://example\#\>.

\@prefix rdf: \<http://www.w3.org/1999/02/22rdf-syntax-ns\#\>.

![](media/image12.png){width="0.35in" height="7.5in"}**example:Wikipedia
example:says \_:bnode197.**

**\_:bnode197 rdf:type rdf:Statement; rdf:subject example:Tolkien;
rdf:predicate example:wrote; rdf:object example:LordOfTheRings.**

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### RDF Type

> **rdf:type** ist ein in RDF-Vokabularsprache definiertes Prädikat
>
> Bezeichnet die Zugehörigkeit der Ressource zu einer
>
> ![](media/image1.png){width="0.35in" height="7.5in"}Klasse / einem Typ
> von Dingen Vgl. ebd., S. 60
>
> \_:**bnode197 rdf:type rdf:Statement**
>
> **= **
>
> \_:**bnode197 a rdf:Statement** .
>
> „**a**" -- abgekürzte Schreibweise für **rdf:type** im **Turtle**
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Datentypen

> Literale können einen Datentyp haben,
>
> Datentypen werden am Wert angefügt und mit „**\^\^**" getrennt.
>
> In N-Triple wird die Datentyp-URI ausgeschrieben
>
> ...**\^\^[\<http://www.w3.org/2001/XMLSchema\#string\>](http://www.w3.org/2001/XMLSchema#string)**
>
> In Turtle -- abgekürzte Schreibweise, wenn der Namensraum deklariert
> ist
>
> ![](media/image1.png){width="0.35in" height="7.5in"}**\@prefix xsd:
> ...**
>
> ...**\^\^xsd:string** Bsp.:
>
> **\@prefix xsd: \<http://www.w3.org/2001/XMLSchema\#\> .**
>
> **\<http://springer.com/Verlag\>**
>
> **\<http://example.org/Name\> \"Springer-Verlag\"\^\^xsd:string ;**
>
> **\<http://example.org/Gründungstag\> \"1842-05-10\"\^\^xsd:date .**

Vgl. ebd., S. 53ff

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Sprachangaben

> Sprachangaben können ebenfalls an Literale angehängt werden.
>
> Sprachbezeichnung nach dem Trennungszeichen:
>
> ![](media/image1.png){width="0.35in" height="7.5in"}**\@de, \@en,
> ...**
>
> Bsp.: \"Springer-Verlag\"\@de
>
> Sprachangaben sind **nur für ungetypte Literale** möglich!
>
> „Springer-Verlag"\@de **≠** „Springer-Verlag"\^\^xsd:string

Vgl. ebd

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### zu N-Triples und Turtle

> ![](media/image1.png){width="0.35in" height="7.5in"}**Analysieren Sie
> folgenden N-Triple-Ausschnitt. Welche Aussagen können Sie darin
> erkennen?**
>
> \<http://hsh.ik.org/Beispiel/RDA\>
> \<http://www.w3.org/1999/02/22-rdf-syntaxns\#type\>
> \<http://hsh.ik.org/Beispiel/Regelwerk\> .
>
> \<http://hsh.ik.org/Beispiel/Petra\>
> \<http://hsh.ik.org/Beispiel/istAnwenderVon\>
> \<http://hsh.ik.org/Beispiel/RDA\> .
>
> \<http://hsh.ik.org/Beispiel/Petra\>
> \<http://www.w3.org/1999/02/22-rdf-syntaxns\#type\>
> \<http://hsh.ik.org/Beispiel/Bibliothekar\> .

#### zu N-Triples und Turtle

**Welche Aussagen können Sie in diesem Turtle-Ausschnitt erkennen?**

![](media/image1.png){width="0.35in" height="7.5in"}**hsh:DNB** a
hsh:Bibliothek ; hsh:hatNamen „Deutsche Nationalbibliothek\"\@de ;
hsh:hatBestand hsh:Buch12 ; hsh:hatNutzer hsh:LeeW .

**hsh:LeeW** a hsh:Nutzer ; hsh:hatNamen „Lee Wang\" ; hsh:ausleihen
hsh:Buch12.

**hsh:Buch12** hsh:hatTitel „Semantic macht Spaß" .

#### zu N-Triples und Turtle

![](media/image1.png){width="0.35in" height="7.5in"}**Welche Aussagen
können Sie in diesem Turtle-Ausschnitt erkennen?**

**hsh:DNB** a hsh:Bibliothek ; hsh:hatBestand hsh:Buch12 ; hsh:hatNamen
\"Deutsche Nationalbibliothek\"\@de ; hsh:hatNutzer hsh:LeeW .
**hsh:LeeW** a hsh:Nutzer ; hsh:hatNamen \"Lee Wang\" ; hsh:ausleihen \[
hsh:hatTitel \"Semantic macht Spaß\" \] .

#### zu N-Triples und Turtle

> Stellen Sie folgende Aussagen erst in N-Triples und dann in Turtle
> dar:

1.  Die Erde umkreist die Sonne.

2.  Die Katze fängt die Maus.

3.  ![](media/image12.png){width="0.35in" height="7.5in"}Jan studiert.

4.  Helga heiratet Jan in Paris am 16.08.2017.

5.  Jörg schenkt Lina ein Buch, das von einer Schriftstellerin namens
    Jojo Moyes geschrieben wurde.

6.  Das Buch „Das ganze halbe Jahr" wurde verfilmt von Thea Sharrock im
    Jahr 2016.

7.  Jenni glaubt, dass Michel ihre italienische Tasche gestohlen hat.

#### Übungsaufgaben RDF-Turtle

Für die Turtle-Darstellung deklarieren Sie da, wo es notwendig ist, in
dem Datei-Kopf folgende Namensräume:

\@prefix rdf: \<http://www.w3.org/1999/02/22-rdf-syntax-ns\#\> .

![](media/image12.png){width="0.35in" height="7.5in"}\@prefix hsh:
\<http://ik.hsh.org/Beispiel/\> .

\@prefix xsd: \<http://www.w3.org/2001/XMLSchema\#\> .

Verwenden Sie den Präfix **hsh:** für die Bezeichnung der Ressourcen in
Ihrer Datei.

Bsp.: hsh:Lina hsh:naehtKleid hsh:Kleid1 ; a hsh:Schneiderin .

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Übungsaufgaben RDF-Turtle

![](media/image12.png){width="0.35in" height="7.5in"}Benutzen Sie
**Datentypen, Sprachangaben, Reifizierung, rdf:type und Blank Nodes,
falls erforderlich**

Sie können die Turtle in einer Datei mit der Endung - **.ttl (Turtle)**
speichern und unter **[<http://ttl.summerofcode.be/>]{.underline}**
validieren.

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

### ![](media/image3.png){width="2.5033344269466316in" height="7.5in"}RDF/XML

> Hochschule Hannover - BIB - WS 2017/2018 -

Walther

22

#### RDF/XML

> Warum RDF/XML, wenn es auch Turtle gibt?
>
> ![](media/image12.png){width="0.35in" height="7.5in"}Turtle ist
> genauso verbreitet wie RDF/XML
>
> RDF/XML ist ein Standard-Format
>
> RDF/XML - häufig als Import/Export-Format bei Semantic-
>
> Web-Anwendungen
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

##### RDF/XML

**\<rdf:RDFWurzelelement**
xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\"**mit
Deklaration **

![](media/image12.png){width="0.35in" height="7.5in"}xmlns:ex
=\"http://example.org/\"\>**^der\ Namensräume^**

**\<rdf:Description rdf:about=\"http://example.org/Wolkenatlas\"\>
Subjekt**

\<**ex:VerlegtBei**\> **Prädikat **

> **\<rdf:Description rdf:about=\"http://rowohlt.com/Verlag\"\> Objekt
> \</rdf:Description\>**
>
> **\</ex:VerlegtBei\>**
>
> **\</rdf:Description\>**

**\</rdf:RDF\>**

##### RDF/XML

**\<rdf:RDFWurzelelement**
xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\"**mit
Deklaration **

xmlns:ex =\"http://example.org/\"\>**^der\ Namensräume^**

![](media/image12.png){width="0.35in" height="7.5in"}**\<rdf:Description
rdf:about=\"http://example.org/Wolkenatlas\"\> **

**\<ex:Titel\>Wolkenatlas\</ex:Titel\> ^Subjekt^**

**\<ex:VerlegtBei\> Prädikat **

> **\<rdf:Description rdf:about=\"http://rowohlt.com/Verlag\"\>**

**\<ex:Name\>Rowohlt-Verlag\</ex:Name\> Objekt**

> **\</rdf:Description\>**

**\</ex:VerlegtBei\> Literal als Objekt**

**\</rdf:Description\>**

**\</rdf:RDF\>**

> **\<rdf:RDF**
>
> xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\" xmlns:ex
> =\"http://example.org/\"\>
>
> **\<rdf:Description rdf:about=\"http://example.org/Wolkenatlas**\"
> **ex:Titel**= „**Wolkenatlas**\"\>
>
> \<**ex:VerlegtBei rdf:resource=**\"**http://rowohlt.com/Verlag**\" /\>
> **\</rdf:Description\>**
>
> ![](media/image12.png){width="0.35in"
> height="7.5in"}**\<rdf:Description
> rdf:about=\"http://rowohlt.com/Verlag**\"
> **ex:Name**=„**Rowohlt-Verlag**\" /\>
>
> **\</rdf:RDF\>**

-   **ex:predicate=**„**Literal**" -- nur für Literal zulässig -\>
    Interpretation als Zeichenkette!

-   **rdf:resource=**„**URI**"- nur für URIs zulässig-\> Interpretation
    als URI!

-   rdf:about=\"**ex:Wolkenatlas**\" -- **so eine Abkürzung der URI im
    Attributwert ist nicht zulässig!**

rdf:resource=„**&ex;Wolkenatlas**" - zulässig, wenn die URIs zusätzlich
im Element **Entity** deklariert wurden.

-   ![](media/image12.png){width="0.35in" height="7.5in"}**\<!Entity ex
    „http://exampl.org/"\>**

**xml:base -** definiert eine Art Basis-URI für ein RDF/XMLDokument.

Relative URIs in Attributen werden jetzt relativ zum Basis-URI
interpretiert.

Vgl. ebd., S. 45-47

**\<?xml version=\"1.0\"?\>**

**\<!DOCTYPE rdf:RDF \[ **

**\<!ENTITY ex \"http://example.org/\" \>**

**\<!ENTITY row \"http://rowohlt.org/\" \> **

**\<!ENTITY xsd \"http://www.w3.org/2001/XMLSchema\#\" \> **

**\<!ENTITY rdf \"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\" \>
\]\>**

**\<rdf:RDF xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\"
xmlns:ex=\"http://example.org\" **

> **xml:base=\"http://example.org\" **
>
> ![](media/image12.png){width="0.35in"
> height="7.5in"}**xmlns:xsd=\"http://www.w3.org/2001/XMLSchema\#\"
> xmlns:row=\"http://rowohlt.com/\"\>**

**\<rdf:Description rdf:about=\"&ex;Wolkenatlas\"\> **

**\<ex:Titel rdf:datatype=\"&xsd;string\"\>Wolkenatlas\</ex:Titel\>**

> **\<ex:VerlegtBei rdf:resource=\"&row;Verlag\"/\>**

**\</rdf:Description\>**

**\<rdf:Description rdf:about=\"&row;Verlag\"\>**

**\<ex:Name rdf:datatype=\"&xsd;string\"\>Rowohlt-Verlag\</ex:Name\>**

**\</rdf:Description\>**

**\</rdf:RDF\>**

#### RDF/XML rdf:ID

> ![](media/image1.png){width="0.35in" height="7.5in"}**rdf:ID
> =\"Name\" -- URI bezieht sich immer auf BasisURI, vollständige
> URI-Angabe nicht zulässig**
>
> **rdf:ID=\"Name\"** = **rdf:about =„\#Name\" **
>
> rdf:ID darf für eine URI nur ein mal verwendet werden

Vgl. ebd., S.47

#### Blank Nodes

Statt rdf:resource und rdf:about verwenden wir **rdf:nodeID**.

> Lokaler Identifier
>
> ![](media/image1.png){width="0.35in" height="7.5in"}\<rdf:Description
> **rdf:nodeID**=\"**f121065a922b8461580a24096c5e0fc45b10**\"\>
>
> \<hsh:hatAutor
> **rdf:nodeID**=\"**f121065a922b8461580a24096c5e0fc45b11**\"/\>
>
> \<rdf:type rdf:resource=\"http://ik.hsh.org/Beispiel/Buch\"/\>
>
> \</rdf:Description\>

Vgl. ebd., S. 57-58

#### Blank Nodes

> Auslassen des **rdf:about-**Attributes im
> **rdf:Description**-Element!
>
> \<rdf:Description
> rdf:about=\"http://www.w3.org/TR/rdf-syntax-grammar\"
> dc:title=\"RDF/XML Syntax Specification (Revised)\"\>
>
> ![](media/image1.png){width="0.35in" height="7.5in"}\<ex:editor\>

+------------------------------------------------------------------------+
| **\<rdf:Description\> **                                               |
|                                                                        |
| > \<ex:homePage rdf:resource=\"http://purl.org/net/dajobe/\"/\>        |
| >                                                                      |
| > \<ex:fullName\>Dave Beckett\</ex:fullName\> **\</rdf:Description\>** |
+------------------------------------------------------------------------+

> \</ex:editor\>
>
> \</rdf:Description\> \</rdf:RDF\>

#### RDF Type

> Option 1:
>
> **\<rdf:Description rdf:about=„ex:Wolkenatlas\"\>**
>
> ![](media/image1.png){width="0.35in" height="7.5in"}**\<rdf:type
> rdf:resource=„ex:Buch\"/\> . . . **
>
> **\</rdf:Description\>**
>
> Option 2:
>
> **\<ex:Buch rdf:about=„ex:Wolkenatlas"\>**
>
> **...**
>
> **\</ex:Buch\>**

#### Reifizierung

> \<?xml version=\"1.0\"?\>
>
> \<rdf:RDF xmlns:rdf=\"http://www.w3.org/1999/02/22-rdfsyntax-ns\#\"
> xmlns:example=\"http://example\#\"\>
>
> \<rdf:Description rdf:about=\"http://example\#Wikipedia\"\>
>
> ![](media/image1.png){width="0.35in" height="7.5in"}\<example:says\>

+-----------------------------------------------------------------------+
| **\<rdf:Statement\>**                                                 |
|                                                                       |
| > \<rdf:subject rdf:resource=\"http://example\#Tolkien\" /\>          |
| >                                                                     |
| > \<rdf:predicate rdf:resource=\"http://example\#wrote\" /\>          |
|                                                                       |
| \<rdf:object rdf:resource=\"http://example\#LordOfTheRings\" /\>      |
| **\</rdf:Statement\>**                                                |
+-----------------------------------------------------------------------+

> \</example:says\>
>
> \</rdf:Description\> \</rdf:RDF\>

#### Übung RDF/XML

> **Extrahieren Sie die Tripel aus folgenden RDF-XML-Abschnitten.
> Schreiben Sie die Triples in N-3 und in Turtle.**
>
> \<rdf:Description
> rdf:about=\"http://ik.hsh.org/Beispiel/EmiliaClark\"\>
>
> \<hsh:hatNamen\>Emilia Clark\</hsh:hatNamen\>
>
> ![](media/image1.png){width="0.35in"
> height="7.5in"}\<hsh:hatHauptrolle\>

\<rdf:Description rdf:about=\"http://ik.hsh.org/Beispiel/MeBeforeYou\"\>
\<hsh:hatTitel xml:lang=\"de\"\>Das ganze halbe Jahr\</hsh:hatTitel\>

> \<rdf:type rdf:resource=\"http://ik.hsh.org/Beispiel/Film\"/\>
> \</rdf:Description\>
>
> \</hsh:hatHauptrolle\>
>
> \</rdf:Description\>
>
> \</rdf:RDF\>
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

##### Übung

> \<?xml version=\"1.0\" encoding=\"UTF-8\"?\> \<rdf:RDF

xmlns:hsh=\"http://ik.hsh.org/Beispiel/\" **RDF/XML**

> xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\" \>
>
> \<rdf:Description rdf:nodeID=\"N9543„/\>
>
> \<rdf:type rdf:resource=\"http://ik.hsh.org/Beispiel/Fahrt\"/\>
>
> \<hsh:hatZiel rdf:resource=\"http://ik.hsh.org/Beispiel/Wien\"/\>
>
> ![](media/image1.png){width="0.35in"
> height="7.5in"}\<hsh:hatDatum\>31.01.2016\</hsh:hatDatum\>
>
> \<hsh:hatAnlass rdf:nodeID=\"N59c57\"/\>
>
> \<hsh:hatReisenden
>
> rdf:resource=\"http://ik.hsh.org/Beispiel/Michael\"/\>
> \</rdf:Description\>
>
> \<rdf:Description rdf:nodeID=\"N59c57\"\> \<rdf:type
> rdf:resource=\"http://ik.hsh.org/Beispiel/Feier\"/\>
> \</rdf:Description\>
>
> \</rdf:RDF\>

##### Übung RDF/XML

\<rdf:Description rdf:about=\"http://ik.hsh.org/Beispiel/Klara\"\>

> \<hsh:vorschlagen\>
>
> \<rdf:Statement\>

\<rdf:subject rdf:resource=\"http://ik.hsh.org/Beispiel/Klaus\"/\>

> ![](media/image1.png){width="0.35in" height="7.5in"}\<rdf:property
> rdf:resource=\"http://ik.hsh.org/Beispiel/erzaehlen\"/\>
> \<rdf:object\>
>
> \<rdf:Description\>
>
> \<rdf:type rdf:resource=\"http://ik.hsh.org/Beispiel/Geschichte\"/\>
> \</rdf:Description\>
>
> \</rdf:object\>
>
> \</rdf:Statement\>
>
> \</hsh:vorschlagen\>

\</rdf:Description\>

##### Übung RDF/XML

> \<?xml version=\"1.0\" encoding=\"UTF-8\"?\>
>
> \<rdf:RDF
>
> xmlns:hsh=\"http://ik.hsh.org/Beispiel/\"
>
> xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns\#\"\>
>
> \<hsh:Dozent\>
>
> \<hsh:empfiehlt\>
>
> \<hsh:Buch\>
>
> ![](media/image1.png){width="0.35in" height="7.5in"}\<hsh:autor\>
>
> \<hsh:Wissenschaftler\>
>
> \<hsh:namens\>Hitzler\</hsh:namens\>
>
> \</hsh:Wissenschaftler\>
>
> \</hsh:autor\>
>
> \</hsh:Buch\>
>
> \</hsh:empfiehlt\>
>
> \</hsh:Dozent\> \</rdf:RDF\>
>
> ![](media/image1.png){width="0.35in" height="7.5in"}Lesen Sie Hitzler
> et al., Kap. 3.2.2, 3.2.3, 3.2.4, 3.2.5, 3.3.1, 3.3.2

![](media/image3.png){width="9.859997812773404in"
height="7.499998906386701in"}

##### ![](media/image12.png){width="0.35in" height="7.5in"}Wissensorganisation mit Vokabularen

> ![](media/image7.jpg){width="7.255in" height="5.443333333333333in"}

Vernetzte Daten aus Wikidata über Deutschland

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

-   Linked Data -- vernetzte Daten in Datensets, in Triple Stores, in
    > Webdokumenten

-   Annotiert mit semantischen Angaben - Kombination aus faktischem u.
    > terminologischen Wissen

-   Was sind die Träger der semantischen Informationen und wo kommen sie
    > her?

-   ![](media/image12.png){width="0.35in" height="7.5in"}Assertionales
    > (faktisches) Wissen -- Fakten über konkrete Individuen -\>
    > Beziehungen der Entitäten zu anderen Entitäten, Zugehörigkeit der
    > Entitäten zu Typen von Dingen.

> Bsp.: \_:Goethe \_:geborenIn \_:Deutschland .
>
> \_:Steinmeier \_:regierungschefVon \_:Deutschland .
>
> \_:HochschuleHannover \_:hatLand \_:Deutschland .

\_:Deutschland a \_:Land .

Vgl. ebd.

-   Terminologisches Wissen -- das allgemeine Wissen über alle für die

> Domäne relevanten Begriffe (Bsp.: Mütter sind Frauen; Mütter haben
> Kinder)

-   ![](media/image12.png){width="0.35in" height="7.5in"}Definition der
    > Typen von Dingen und ihrer Eigenschaften -\> in Vokabularen
    > definierte Bezeichner

-   Bsp.: Bezeichner für die Klasse „Person" in Friend of a Friend
    > (FOAF) Vokabular -
    > [\<[http://xmlns.com/foaf/0.1/Person\>]{.underline}](http://xmlns.com/foaf/0.1/Person)

> ![](media/image8.jpg){width="8.186666666666667in"
> height="2.243333333333333in"}

-   Art und Eigenschaften der Beziehungen -\> in Vokabularen definierte

> ![](media/image12.png){width="0.35in" height="7.5in"}Bezeichner

-   Bsp.: Bezeichner für die Beziehung „kennt" in FOAF Ontology -

> \<[[http://xmlns.com/foaf/0.1/knows]{.underline}
> \>](http://xmlns.com/foaf/0.1/)
>
> ![](media/image9.jpg){width="8.425in" height="2.605in"}

Vokabular -- eine Zusammenstellung von Bezeichnern mit klar

> definierter Bedeutung. Vgl. Hitzler u. a.(2008), S. ~48~

![](media/image12.png){width="0.35in" height="7.5in"}Vokabulare in
Semantic Web -- wohldefiniert und idealerweise ausgestattet mit im Web
verfügbaren Spezifikationen, wo die Bezeichner abgelegt sind.

-   Bsp.: [[GND
    > Ontology](https://d-nb.info/standards/elementset/gnd)]{.underline}
    > , [[DCMI Metadata](http://dublincore.org/documents/dcmi-terms/)
    > [Terms
    > ](http://dublincore.org/documents/dcmi-terms/)]{.underline},
    > [[Friend of](http://xmlns.com/foaf/spec/) [a
    > Friend](http://xmlns.com/foaf/spec/)]{.underline}

Vgl. ebd.

#### ![](media/image12.png){width="0.35in" height="7.5in"}Vokabulare: das Spektrum

![](media/image11.png){width="8.958055555555555in"
height="5.478194444444444in"}

> Überblicksartikel: [Towards a Taxonomy of KOS : Dimensions for
> Classifying Knowledge Organization Systems.]{.underline} Souza, Renato
> R.; Tudhope, Douglas; Almeida, Mauricio B. In: Knowledge Organization,
> Vol. 39, No. 3, 2012, p. 179-192
>
> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Vokabulare: das Spektrum

**Glossar**: Liste von Begriffen, ggfs. mit Definitionen und weiteren
Informationen \[linear\]

**Taxonomie**: Begriffe sind durch Ober-

> /Unterbegriffsrelationen hierarchisch geordnet
>
> \[Baumstruktur\]

![](media/image12.png){width="0.35in" height="7.5in"}**Thesaurus**:
(idealerweise) Trennung in Konzepte und Terme; weitere Relationen wie
Synonymie und andere semantische Bezüge \[Baumstruktur oder
Netzstruktur, Polyhierarchie\]

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-- *natürlichsprachige
Grenze* \-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

**(Heavy-Weight-)Ontologie**: Klassen, Relationen und Eigenschaften
plus logische Schlussregeln

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

#### Grundlagen der natürlichsprachigen Vokabulare

**Konzept ≈ Begriff** (von lat. con + capere, "zusammen-fassen")

-   Das abstrakte Ding, sprachunabhängig

**Term ≈ Label **

-   Natürlichsprachige Bezeichnung für ein Konzept, z.B. "Schimmel",

> ![](media/image12.png){width="0.35in" height="7.5in"}"weißes Pferd",
> "white horse", ...

**Relation**

-   Semantische (oder andere) Beziehung zwischen Einheiten, kann
    zwischen Konzepten, zwischen Termen und zwischen Konzepten und
    Termen bestehen z.B. "ist Unterbegriff von", "ist Abkürzung von",
    "ist altertümliche Bezeichnung für"

> Hochschule Hannover - BIB - WS 2017/2018 Walther

Thesaurus
---------

**Anwendung**:

-   Inhaltliche Erschließung in Bibliotheken, Archiven, Museen,
    Unternehmen, auf Webseiten ...

-   Zur Unterstützung von Indexierung und Retrieval

**Themenbezug**:

-   ![](media/image12.png){width="0.35in"
    height="7.5in"}**Universalthesaurus --** fächerübergreifend
    /**Fachthesaurus -** fachspezifisch **Beziehungen: Konzepte \<-\>
    Konzepte**:

-   Konzepte sind keine Klassen!

-   Hierarchie: Hypernyme, Hyponyme, Meronyme, Holonyme

-   Nicht-Hierarchie: Synonyme, Antonyme, Assoziationen
    ^Vgl.\ Dengel u.\ a., S.\ 92^

**Beziehungen: Konzepte \<-\> Terme**:

-   Bevorzugte Bezeichnungen, alternative Bezeichnungen, Abkürzungen,
    Benennungen in anderen Sprachen

Beispiele Thesauri: STW, EUROVOC, Unesco Thesaurus, Agrovoc etc.

> Hochschule Hannover - BIB - WS 2016/2017 - Walther

### ![](media/image12.png){width="0.35in" height="7.5in"}Beispiel: EuroVoc Thesaurus

![](media/image12.jpg){width="7.096666666666667in"
height="6.213333333333333in"}

> Hochschule Hannover - BIB - WS 2017/2018 - Walther

Formalisierte Ontologie
-----------------------

> Ontologie -- aus dem Griechischen „die Lehre vom Sein",
>
> Wissensgebiet und Begriff aus Philosophie

![](media/image12.png){width="0.35in" height="7.5in"}Vgl.
[[https://gi.de/service/informatiklexikon/detail/ontologien/]{.underline}](https://gi.de/service/informatiklexikon/detail/ontologien/)

> In Semantic Web **- Ein in RDF(S) und OWL modellierte **
>
> **Wissensbasis, welche das Wissen eines oder mehrerer **
>
> **Gegenstandsbereiche abbildet.** Vgl. Hitzler, S. 12
>
> Hochschule Hannover - BIB - WS 2016/2017 - Walther

Formalisierte Ontologie
-----------------------

> **Definitionen von Klassen und Instanzen**
>
> ![](media/image12.png){width="0.35in" height="7.5in"}**Definition von
> Relationen und Hierarchien **
>
> Statt einfacher Hierarchien Ober-/Unterbegriff -- **vielfältige **
>
> **Beziehungen zwischen den Klassen und Instanzen**
>
> Komplexe Beziehungsarten mit expliziter Semantik (reflexiv,
> symmetrisch, inverse, disjunkt etc.)
>
> Formalisiert -- (enthält formale Ableitungsregeln, kann neue Axiome
> implizieren)

### Formalisierte Ontologien

![](media/image12.png){width="0.35in" height="7.5in"}**Klassen**
(„Person", „Publikation") sind **Mengen von einzelnen Ressourcen
(Individuen) mit gewissen Gemeinsamkeiten**

**Individuen** („Jojo Moyes", „Me before You"), die zu einer Klasse
gehören, werden **Instanzen** dieser Klasse genannt.

Vgl. Hitzler u. a.(2008), S. 68

> Hochschule Hannover - BIB - WS 2017/2018 Walther

### OWL-Ontologien

**FOAF** - Friend of a Friend **Beispiele**

> **vCARD**
>
> **BIBO** - Bibliographic Ontology
>
> **FaBiO**, the FRBR-aligned Bibliographic
>
> Ontology
>
> ![](media/image12.png){width="0.35in" height="7.5in"}**VIVO** -- VIVO
> Core Ontology
>
> **SWRC** - Semantic Web for Research
>
> Communities
>
> **AIISO** - Academic Institution Internal
>
> Structure Ontology
>
> **FRAPO -** Funding, Research Administration and Projects Ontology
>
> **GND Ontology**

FOAF
----

> **FOAF: Friend of a Friend**
>
> ![](media/image12.png){width="0.35in" height="7.5in"}Relationen zur
> Darstellung sozialer Netzwerke.
>
> Personen, Adressen, Webseiten, usw.
>
> Personen werden durch persönliche E-MailAdressen identifiziert.

Namespace:
[[http://xmlns.com/foaf/0.1/]{.underline}](http://xmlns.com/foaf/0.1/)

vCard
-----

**vCard Ontology** -- for describing People and

> ![](media/image12.png){width="0.35in" height="7.5in"}Organizations

-   RDFS/OWL-basierte Ontologie

-   Beschreibt Personen und Organisationen (Adresse, Kontakt,
    Beziehungs-Informationen)

Namespace:
[[http://www.w3.org/2006/vcard/ns]{.underline}](http://www.w3.org/2006/vcard/ns)

BIBO
----

**BIBO - Bibliographic Ontology**

Beschreibt bibliographische Ressourcen für Semantic Web in RDF.

![](media/image12.png){width="0.35in" height="7.5in"}Bedient sich der
Elemente von DCMI Terms (Dublin Core Metadata Initiative Metadata Terms)

Nutzung durch DNB und andere große Bibliotheken und Bibliotheksverbünde
[[http://hub.culturegraph.org/statistics/overview]{.underline}](http://hub.culturegraph.org/statistics/overview)

Namensraum:
[**[http://bibliontology.com/]{.underline}**](http://bibliontology.com/)

Vgl. D'Arcus u. a. (2009)

Hochschule Hannover - BIB - WS 2016/2017 - Walther 56

VIVO Ontology
-------------

**VIVO-ISF Ontology**

Beschreibt akademische und forschungsbezogene

> ![](media/image12.png){width="0.35in" height="7.5in"}Einrichtungen und
> Aktivitäten

Bedient sich Klassen und Beziehungen einiger Ontologien, u. A. aus
FOAF, OBO Foundary usw.

Namensraum:
[[http://vivoweb.org/ontology/core\#]{.underline}](http://vivoweb.org/ontology/core)

Hochschule Hannover - BIB - WS 2016/2017 - Walther 57

### Nachnutzung der Vokabulare

"vocabularies provide the semantic glue enabling Data to

> become meaningful Data" Linked Open Vocabularies (~o.J.)~

**Nachnutzung der Bezeichner aus wohldefinierten, etablierten
Vokabularen**

Bsp.: statt hsh:Person - foaf:Person,

![](media/image12.png){width="0.35in" height="7.5in"}statt hsh:hatNamen
- foaf:firstName, foaf:lastName statt hsh:hatThema -
vivo:associatedConcept, vivo:subjectedArea

**Gemeinsames Verständnis der Aussagen**

**Interoperabilität der Daten**

[**[Linked]{.underline}**](http://lov.okfn.org/dataset/lov) [** [Open
Vocabularies](http://lov.okfn.org/dataset/lov) **]{.underline}--
Sammlung von Linked Open Data Vokabularen

Vgl. ebd.

Hochschule Hannover - BIB - WS 2016/2017 - Walther 58

### Aufgabe

-   Erstellen Sie aus folgenden Elementen einen Entwurf einer Ontologie:

Musik, CD, Rock, Oberton, Belting, Beyonce, Sun Rise Avenue, Samu Haber,

![](media/image12.png){width="0.35in" height="7.5in"}Interpret,
Finnland, USA, 2. April 1976, Natascha Nikeprelevic, Sibirien, Sanna
Haber, „Towards the Light"

-   Überlegen Sie sich anhand der vorhanden Entitäten, welche Klassen,
    Beziehungen und Hierarchien Ihre Ontologie enthalten soll.

-   Nutzen Sie die Bezeichner aus bestehenden, etablierten Vokabularen.
    Browsen Sie nach Bezeichnern in
    [[Linked](http://lov.okfn.org/dataset/lov/vocabs) [Open
    Vocabularies](http://lov.okfn.org/dataset/lov/vocabs)]{.underline}.

Hochschule Hannover - BIB - WS 2017/2018 - Walther 59







#HSLIDE

# Semantic Web
## Block II

Hochschule H,
[@im_hsh](https://twitter.com/im_hsh)

#HSLIDE

 # **Themenblock II**
 

   Serialisierung von RDF ( Turtle, N-Triples) 

   -------------------------------------------- 
   RDF/XML

   -------------------------------------------- 
   Wissensorganisation mit Vokabularen

   -------------------------------------------- 


#HSLIDE
   
   
## Serialisierung von RDF 
##      (Turtle, N-Triples) 

---?image=/pics/bild1.png&size= 25%&position= bottom 75% right 10%
## RDF Wiederholung ##
--------------------------------------------
  * Tripelstruktur (= RDF-Triple) -&gt;  
  *   **&lt;Subjekt&gt;&lt;Prädikat&gt;&lt;Objekt&gt;**
   
  * Jedes Triple – eine Aussage (RDF-Statement)
   
  * Subjekt und Prädikat werden durch URI bezeichnet, Objekt – durch einen URI oder ein RDF-Literal
   
  * Ausnahme: Blank Nodes – Leere Knoten zur Beschreibung von unbenannten Ressourcen  
  ###### Vgl. Hitzler u. a.(2008), S.40 ######
#VSLIDE
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

