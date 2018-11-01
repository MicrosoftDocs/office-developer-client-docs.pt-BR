---
title: Formato de persistência XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 201ea2b46ad2bb08e631882cebd5419b6b301179
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867745"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="72843-102">Formato de persistência XML</span><span class="sxs-lookup"><span data-stu-id="72843-102">XML Persistence Format</span></span>

<span data-ttu-id="72843-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="72843-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="72843-104">Formato de persistência XML</span><span class="sxs-lookup"><span data-stu-id="72843-104">XML Persistence Format</span></span>

<span data-ttu-id="72843-105">O ADO usa a codificação UTF-para o fluxo XML que ele mantém.</span><span class="sxs-lookup"><span data-stu-id="72843-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="72843-p101">O formato XML do ADO está dividido em duas seções, uma seção de esquema seguida pela seção de dados. A seguir está um arquivo XML de exemplo para a tabela Transportadoras a partir do banco de dados Northwind. Diversas partes do XML são discutidas seguindo o exemplo.</span><span class="sxs-lookup"><span data-stu-id="72843-p101">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="72843-p102">O esquema mostra as declarações de espaços de nomes, a seção de esquema e a seção de dados. A seção de esquema contém definições para a linha, ShipperID, CompanyName e Phone.</span><span class="sxs-lookup"><span data-stu-id="72843-p102">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="72843-p103">As definições de esquema estão em conformidade com a especificação de Dados XML e são capazes de ser totalmente validadas (embora a validação não ocorrerá no Internet Explorer 5). Você pode visualizar essa especificação em [Nota W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). Os Dados XML são o único formato de esquema suportado para a persistência **Recordset** no momento.</span><span class="sxs-lookup"><span data-stu-id="72843-p103">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="72843-114">A seção de dados possui três linhas que contêm informações sobre as transportadoras.</span><span class="sxs-lookup"><span data-stu-id="72843-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="72843-115">Para um conjunto de linhas vazio, a seção de dados pode estar vazia, mas o `<rs:data>` marcas devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="72843-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="72843-116">Sem dados, você poderia escrever simplesmente como a forma abreviada de marca `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="72843-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="72843-117">Qualquer marca com o prefixo "rs" indica que estamos no namespace definido por urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="72843-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="72843-118">A definição completa desse esquema está definida no apêndice desse documento.</span><span class="sxs-lookup"><span data-stu-id="72843-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="72843-119">Formato de persistência XML</span><span class="sxs-lookup"><span data-stu-id="72843-119">XML Persistence Format</span></span>

<span data-ttu-id="72843-120">O ADO usa a codificação UTF-para o fluxo XML que ele mantém.</span><span class="sxs-lookup"><span data-stu-id="72843-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="72843-p105">O formato XML do ADO está dividido em duas seções, uma seção de esquema seguida pela seção de dados. A seguir está um arquivo XML de exemplo para a tabela Transportadoras a partir do banco de dados Northwind. Diversas partes do XML são discutidas seguindo o exemplo.</span><span class="sxs-lookup"><span data-stu-id="72843-p105">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="72843-p106">O esquema mostra as declarações de espaços de nomes, a seção de esquema e a seção de dados. A seção de esquema contém definições para a linha, ShipperID, CompanyName e Phone.</span><span class="sxs-lookup"><span data-stu-id="72843-p106">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="72843-p107">As definições de esquema estão em conformidade com a especificação de Dados XML e são capazes de ser totalmente validadas (embora a validação não ocorrerá no Internet Explorer 5). Você pode visualizar essa especificação em [Nota W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). Os Dados XML são o único formato de esquema suportado para a persistência **Recordset** no momento.</span><span class="sxs-lookup"><span data-stu-id="72843-p107">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="72843-129">A seção de dados possui três linhas que contêm informações sobre as transportadoras.</span><span class="sxs-lookup"><span data-stu-id="72843-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="72843-130">Para um conjunto de linhas vazio, a seção de dados pode estar vazia, mas o `<rs:data>` marcas devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="72843-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="72843-131">Sem dados, você poderia escrever simplesmente como a forma abreviada de marca `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="72843-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="72843-132">Qualquer marca com o prefixo "rs" indica que estamos no namespace definido por urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="72843-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="72843-133">A definição completa desse esquema está definida no apêndice desse documento.</span><span class="sxs-lookup"><span data-stu-id="72843-133">The full definition of this schema is defined in the appendix to this document.</span></span>

