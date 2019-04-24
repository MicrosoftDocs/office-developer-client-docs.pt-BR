---
title: Formato de persistência XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7825d55c6f0c2f900f61a325265dce048f965e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308278"
---
# <a name="xml-persistence-format"></a>Formato de persistência de XML

**Aplica-se ao:** Access 2013, Office 2013

## <a name="xml-persistence-format"></a>Formato de persistência XML

O ADO usa a codificação UTF-para o fluxo XML que ele mantém.

O formato XML do ADO está dividido em duas seções, uma seção de esquema seguida pela seção de dados. A seguir está um arquivo XML de exemplo para a tabela Transportadoras a partir do banco de dados Northwind. Diversas partes do XML são discutidas seguindo o exemplo.

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

O esquema mostra as declarações de espaços de nomes, a seção de esquema e a seção de dados. A seção de esquema contém definições para a linha, ShipperID, CompanyName e Phone.

As definições de esquema estão em conformidade com a especificação de Dados XML e são capazes de ser totalmente validadas (embora a validação não ocorrerá no Internet Explorer 5). Você pode visualizar essa especificação em [Nota W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). Os Dados XML são o único formato de esquema suportado para a persistência **Recordset** no momento.

A seção de dados possui três linhas que contêm informações sobre as transportadoras. Para um conjunto de linhas vazio, a seção de dados pode estar vazia `<rs:data>` , mas as marcas devem estar presentes. Sem dados, você pode escrever a marca de forma abreviada `<rs:data>`como simples. Qualquer marca com o prefixo "rs" indica que estamos no namespace definido por urn:schemas-microsoft-com:rowset. A definição completa desse esquema está definida no apêndice desse documento.

## <a name="xml-persistence-format"></a>Formato de persistência XML

O ADO usa a codificação UTF-para o fluxo XML que ele mantém.

O formato XML do ADO está dividido em duas seções, uma seção de esquema seguida pela seção de dados. A seguir está um arquivo XML de exemplo para a tabela Transportadoras a partir do banco de dados Northwind. Diversas partes do XML são discutidas seguindo o exemplo.

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

O esquema mostra as declarações de espaços de nomes, a seção de esquema e a seção de dados. A seção de esquema contém definições para a linha, ShipperID, CompanyName e Phone.

As definições de esquema estão em conformidade com a especificação de Dados XML e são capazes de ser totalmente validadas (embora a validação não ocorrerá no Internet Explorer 5). Você pode visualizar essa especificação em [Nota W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). Os Dados XML são o único formato de esquema suportado para a persistência **Recordset** no momento.

A seção de dados possui três linhas que contêm informações sobre as transportadoras. Para um conjunto de linhas vazio, a seção de dados pode estar vazia `<rs:data>` , mas as marcas devem estar presentes. Sem dados, você pode escrever a marca de forma abreviada `<rs:data>`como simples. Qualquer marca com o prefixo "rs" indica que estamos no namespace definido por urn:schemas-microsoft-com:rowset. A definição completa desse esquema está definida no apêndice desse documento.

