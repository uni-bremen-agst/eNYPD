```xml
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" 
targetNamespace="..." 
xmlns:tns="..." 
elementFormDefault="qualified">
<xs:element name="classesType">
		<xs:complexType>
			<xs:sequence>
				<xs:element name="class" type="tns:classType"></xs:element>
			</xs:sequence>
		</xs:complexType>
	</xs:element>

	<xs:complexType name="classType">
		<xs:sequence>
			<xs:element name="attributeOrMethod"
				type="tns:attributeOrMethodType"></xs:element>
		</xs:sequence>
		<xs:attribute name="name" use="required"></xs:attribute>
		<xs:attribute name="scope" default="unknown"></xs:attribute>
		
		<xs:attribute name="package" type="xs:string" default="No Package"></xs:attribute>
	</xs:complexType>


	<xs:complexType name="attributeType">
		<xs:sequence>
			<xs:element name="attributeOrMethod"
				type="tns:attributeOrMethodType"></xs:element>
		</xs:sequence>
		<xs:attribute name="name" use="required"></xs:attribute>

	</xs:complexType>


	<xs:complexType name="methodType">
		<xs:sequence>
			<xs:element name="parameter" type="xs:string"
				minOccurs="0" maxOccurs="unbounded"></xs:element>
		</xs:sequence>
		<xs:attribute name="name" use="required"></xs:attribute>
		<xs:attribute name="return" type="xs:string"
			 default="unknown" ></xs:attribute>
	</xs:complexType>

	<xs:complexType name="attributeOrMethodType">

		<xs:choice>
			<xs:element name="attribute" type="tns:attributeType">
			</xs:element>
			<xs:element name="method" type="tns:methodType"
				maxOccurs="1"></xs:element>
		</xs:choice>
	</xs:complexType>
</xs:schema>
```

