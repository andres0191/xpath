# XPATH

XPath is a query language used to select nodes from an XML document. Since HTML pages can be expressed as well formed XML  documents, XPath could be used to extract relevant data from web pages of interest. This is one of the most used techniques by web scraping tools.

## Exercise 1 - Extracting item information from Auction web pages
* Goal:
Define XPath expressions inside an XLST file to extract information from given HTML pages
- Given the following XSLT template:
```
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
    <xsl:template match="/">
        <items>
            <!--Use "select" attr to write the XPath expression that will select ALL items -->
            <!--Example: html[1]/body[1]/div[@id='auctions'] -->
            <xsl:for-each select="{Enter here the XPath expr to select all items}">
                <item>
                    <id>
                        <xsl:value-of select="{Relative XPath to fetch the id}"/>
                    </id>
                    <name>
                        <xsl:value-of select="{Relative XPath to fetch the name}"/>
                    </name>
                    <location>
                        <xsl:value-of select="{Relative XPath to fetch the location}"/>
                    </location>
                    <url>
                        <xsl:value-of select="{Relative XPath to fetch the URL}"/>
                    </url>
                    <img>
                        <xsl:value-of select="{Relative XPath to fetch the img URL}"/>
                    </img>
                    <price>
                        <xsl:value-of select="{Relative XPath to fetch the price}"/>
                    </price>
                    <end-date>
                        <xsl:value-of select="{Relative XPath to fetch the end date}"/>
                    </end-date>
                </item>
            </xsl:for-each>
        </items>
    </xsl:template>
</xsl:stylesheet>
```

Develop the proper XPath expressions inside XSLT files (using the above template) to fully extract the item information (id, name, description, location, url, image url, price and end date) listed in the following HTML pages:

● Exercise_1.html
● Exercise_2.html
● Exercise_3.html
● Exercise_4.html
● Exercise_5.html

All the above HTML files contain auction information. Each one of them has a very different structure, so the XPath expressions needed to extract the information will vary from one HTML file to another. You need to provide the XPath expression that will match every node containing auctions (the XPath expression inside the “select” attribute of the xsl:for-each element in the XSLT template), and then you will provide the relative XPath expressions to grab each value
into the corresponding field (id, name, etc).

### For each one of these HTML files, you must provide:

● The XSLT file containing the proper XPath expressions that fully extracts all auctions
and its fields from the HTML file. File name should be “Exercise_<number>.xslt”.
● The resulting XML file with all the auctions extracted, with its fields. Filename should be
“Exercise_<number>_results.xml”.
Tools you will need:
● Text editor
● Web browser
● XPath reference manual
○ [xpath w3school](https://www.w3schools.com/xml/xpath_intro.asp)
○ [xpath developer mozilla](https://developer.mozilla.org/en-US/docs/Web/XPath)
● XPath evaluation tool. Mozilla Firefox and Google Chrome browsers provide built-in
functionality to evaluate XPath expressions (inside Developer Tools).
● An XSLT transformation engine. There are some tools online such as:
○ [transformer xsl](https://www.freeformatter.com/xsl-transformer.html)
○ [xsltransformation](http://www.utilities-online.info/xsltransformation/)
Guidelines
● Keep XPath expressions as simple as possible.