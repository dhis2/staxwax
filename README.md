# StaxWax

StaxWax is a light-weight convenience framework for high-performance StAX XML writing and parsing.

## Reading XML

To read XML, instantiate an XmlReader from an InputStream.

```java
XmlReader reader = XMLFactory.getXMLReader( inputStream );
reader.moveToStartElement( "dataValue" );
reader.getAttributeValue( "period" );
reader.getElementValue( "dataElement" );
```

## Writing XML

To write XML, instantiate an XmlReader from an OutputStream.

```java
XmlWriter writer = XmlFactory.getXmlWriter( outputStream );
writer.openDocument();
writer.openElement( "dataValues" );
writer.writeAttribute( "period", period );
writer.writeElement( "dataElement", dataElement );
writer.closeElement();
writer.closeDocument();
```
