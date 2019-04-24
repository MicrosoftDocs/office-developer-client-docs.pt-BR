---
title: Seção Schema (referência do banco de dados de área de trabalho do Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308936"
---
# <a name="schema-section"></a>Seção de esquema

**Aplica-se ao:** Access 2013, Office 2013

## <a name="schema-section"></a>Seção schema

A seção schema é obrigatória. Como os exemplos anteriores mostraram, o ADO grava metadados detalhados sobre cada coluna para preservar a semântica dos valores de dados o máximo possível visando as atualizações. Contudo, para ser carregado no XML, o ADO só necessita dos nomes das colunas e do conjunto de linhas ao qual elas pertencem. Aqui está um exemplo de seção schema mínima:

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

No caso acima, o ADO tratará os dados como sequências de caracteres de comprimento variável porque nenhuma informação de tipo foi incluída na seção schema.

## <a name="creating-aliases-for-column-names"></a>Criando aliases para nomes de colunas

O atributo **rs:name** permite que você crie um alias para uma coluna de forma que um nome amigável possa aparecer nas informações sobre a coluna expostas pelo conjunto de linhas e um nome abreviado possa ser usado na seção de dados. Por exemplo, a seção schema acima poderia ser modificada para mapear ShipperID como s1, CompanyName como s2 and Phone como s3 da seguinte forma:

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

Em seguida, na seção de dados, a linha usaria o atributo **name** (em vez do atributo **rs:name**) para referir-se àquela coluna:

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

É necessário criar aliases para nomes de colunas sempre que um nome de coluna não é um atributo legal ou um nome de marca no XML. Por exemplo, "Last Name" deve ter um alias porque os nomes com espaços incorporados são atributos ilegais. A linha a seguir não será tratada de forma correta pelo analisador XML. Portanto, você deve criar um alias para os outros nomes que não contenham espaços incorporados:

```xml 
 
<row last name="Jones"/> 
```

Seja qual for o valor usado para o atributo **name**, ele deve ser usado de forma consistente em cada local em que for feita uma referência à coluna tanto na seção schema como na seção data do documento em XML. O exemplo a seguir mostra o uso consistente de s1:

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

Do mesmo modo, como não há um alias definido para CompanyName no exemplo acima, CompanyName deve ser usado de forma consistente em todo o documento.

## <a name="data-types"></a>Tipos de dados

Você pode aplicar um tipo de dados a uma coluna com o atributo **dt:type**. Pode-se especificar um tipo de dados de duas maneiras: especificando o atributo **dt:type** diretamente na própria definição da coluna ou usar a construção **s:datatype** como um elemento aninhado da definição da coluna. Por exemplo,

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

é equivalente a

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Se você omitir o atributo **dt:type** totalmente da definição de linha, por padrão, o tipo da coluna será uma sequência de caracteres de comprimento variável.

Se você tiver outras informações de tipo além do nome de tipo (por exemplo, **dt:maxLength**), elas tornarão o uso do elemento filho **s:datatype** mais legível. Contudo, isso é meramente uma convenção, não um requisito.

Os exemplos a seguir mostram como incluir as informações de tipo na seção schema:

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

Há um uso sutil do atributo **rs:fixedlength** no segundo exemplo. Uma coluna com o atributo **rs:fixedlength** definida como true significa que os dados devem ter o comprimento definido na seção schema. Nesse caso, um valor legal para ID de\_título é "123456", como é "123". Contudo, "123" não seria válido porque seu comprimento é 3, e não 6. Consulte o OLE DB Programmer's Guide para obter uma descrição mais completa da propriedade **fixedlength**.

## <a name="handling-nulls"></a>Tratando valores nulos

Os valores nulos são tratados pelo atributo **rs:maybenull**. Se esse atributo estiver definido como true, o conteúdo da coluna poderá conter um valor nulo. Além disso, se a coluna não for encontrada em uma linha de dados, o usuário que estiver lendo os dados do conjunto de linhas receberá um status nulo de **IRowset::GetData()**. Considere as seguintes definições de coluna a seguir da tabela Shippers:

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

A definição permite que CompanyName seja nulo, mas ShipperID não pode conter um valor nulo. Se a seção de dados contiver a seguinte linha, o provedor de persistência definiria o status dos dados da coluna CompanyName para a constante de status do\_OLE\_DB DBSTATUS S IsNull:

```xml 
 
<z:row ShipperID="1"/> 
```

Se a linha estava totalmente vazia, como a seguir, o provedor de persistência retornaria um status de OLE\_DB\_de DBSTATUS e indisponível para transportador e DBSTATUS\_S\_IsNull para CompanyName.

```xml 
 
<z:row/>  
```

Observe que uma sequência de caracteres de comprimento igual a zero não é nula.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Para a linha anterior, o provedor de persistência retornará um status do OLE DB DBSTATUS\_S\_OK para ambas as colunas. Nesse caso, CompanyName é simplesmente "" (uma sequência de caracteres de comprimento zero).

Para obter mais informações sobre construções de banco de dados OLE disponíveis para uso dentro da seção schema de um documento em XML do banco de dados OLE, consulte a definição de "urn:schemas-microsoft-com:rowset" e o OLE DB Programmer's Guide.

