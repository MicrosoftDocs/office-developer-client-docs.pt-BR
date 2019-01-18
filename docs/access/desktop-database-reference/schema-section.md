---
title: Seção Schema (referência de banco de dados da área de trabalho do Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709863"
---
# <a name="schema-section"></a><span data-ttu-id="49582-102">Seção de esquema</span><span class="sxs-lookup"><span data-stu-id="49582-102">Schema section</span></span>

<span data-ttu-id="49582-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="49582-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="49582-104">Seção schema</span><span class="sxs-lookup"><span data-stu-id="49582-104">Schema Section</span></span>

<span data-ttu-id="49582-p101">A seção schema é obrigatória. Como os exemplos anteriores mostraram, o ADO grava metadados detalhados sobre cada coluna para preservar a semântica dos valores de dados o máximo possível visando as atualizações. Contudo, para ser carregado no XML, o ADO só necessita dos nomes das colunas e do conjunto de linhas ao qual elas pertencem. Aqui está um exemplo de seção schema mínima:</span><span class="sxs-lookup"><span data-stu-id="49582-p101">The schema section is required. As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating. However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong. Here is an example of a minimal schema:</span></span>

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

<span data-ttu-id="49582-109">No caso acima, o ADO tratará os dados como sequências de caracteres de comprimento variável porque nenhuma informação de tipo foi incluída na seção schema.</span><span class="sxs-lookup"><span data-stu-id="49582-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="49582-110">Criando aliases para nomes de colunas</span><span class="sxs-lookup"><span data-stu-id="49582-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="49582-p102">O atributo **rs:name** permite que você crie um alias para uma coluna de forma que um nome amigável possa aparecer nas informações sobre a coluna expostas pelo conjunto de linhas e um nome abreviado possa ser usado na seção de dados. Por exemplo, a seção schema acima poderia ser modificada para mapear ShipperID como s1, CompanyName como s2 and Phone como s3 da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="49582-p102">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section. For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

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

<span data-ttu-id="49582-113">Em seguida, na seção de dados, a linha usaria o atributo **name** (em vez do atributo **rs:name**) para referir-se àquela coluna:</span><span class="sxs-lookup"><span data-stu-id="49582-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="49582-p103">É necessário criar aliases para nomes de colunas sempre que um nome de coluna não é um atributo legal ou um nome de marca no XML. Por exemplo, "Last Name" deve ter um alias porque os nomes com espaços incorporados são atributos ilegais. A linha a seguir não será tratada de forma correta pelo analisador XML. Portanto, você deve criar um alias para os outros nomes que não contenham espaços incorporados:</span><span class="sxs-lookup"><span data-stu-id="49582-p103">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML. For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes. The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="49582-p104">Seja qual for o valor usado para o atributo **name**, ele deve ser usado de forma consistente em cada local em que for feita uma referência à coluna tanto na seção schema como na seção data do documento em XML. O exemplo a seguir mostra o uso consistente de s1:</span><span class="sxs-lookup"><span data-stu-id="49582-p104">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document. The following example shows the consistent use of s1:</span></span>

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

<span data-ttu-id="49582-119">Do mesmo modo, como não há um alias definido para CompanyName no exemplo acima, CompanyName deve ser usado de forma consistente em todo o documento.</span><span class="sxs-lookup"><span data-stu-id="49582-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="49582-120">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="49582-120">Data Types</span></span>

<span data-ttu-id="49582-p105">Você pode aplicar um tipo de dados a uma coluna com o atributo **dt:type**. Pode-se especificar um tipo de dados de duas maneiras: especificando o atributo **dt:type** diretamente na própria definição da coluna ou usar a construção **s:datatype** como um elemento aninhado da definição da coluna. Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="49582-p105">You can apply a data type to a column with the **dt:type** attribute. You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition. For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="49582-124">é equivalente a</span><span class="sxs-lookup"><span data-stu-id="49582-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="49582-125">Se você omitir o atributo **dt:type** totalmente da definição de linha, por padrão, o tipo da coluna será uma sequência de caracteres de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="49582-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="49582-p106">Se você tiver outras informações de tipo além do nome de tipo (por exemplo, **dt:maxLength**), elas tornarão o uso do elemento filho **s:datatype** mais legível. Contudo, isso é meramente uma convenção, não um requisito.</span><span class="sxs-lookup"><span data-stu-id="49582-p106">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element. This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="49582-128">Os exemplos a seguir mostram como incluir as informações de tipo na seção schema:</span><span class="sxs-lookup"><span data-stu-id="49582-128">The following examples show further how to include type information in your schema:</span></span>

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

<span data-ttu-id="49582-129">Há um uso sutil do atributo **rs:fixedlength** no segundo exemplo.</span><span class="sxs-lookup"><span data-stu-id="49582-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="49582-130">Uma coluna com o atributo **rs:fixedlength** definida como true significa que os dados devem ter o comprimento definido na seção schema.</span><span class="sxs-lookup"><span data-stu-id="49582-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="49582-131">Nesse caso, um departamento jurídico valor para o título\_id é "123456", como "123".</span><span class="sxs-lookup"><span data-stu-id="49582-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="49582-132">Contudo, "123" não seria válido porque seu comprimento é 3, e não 6.</span><span class="sxs-lookup"><span data-stu-id="49582-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="49582-133">Consulte o OLE DB Programmer's Guide para obter uma descrição mais completa da propriedade **fixedlength**.</span><span class="sxs-lookup"><span data-stu-id="49582-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="49582-134">Tratando valores nulos</span><span class="sxs-lookup"><span data-stu-id="49582-134">Handling Nulls</span></span>

<span data-ttu-id="49582-p108">Os valores nulos são tratados pelo atributo **rs:maybenull**. Se esse atributo estiver definido como true, o conteúdo da coluna poderá conter um valor nulo. Além disso, se a coluna não for encontrada em uma linha de dados, o usuário que estiver lendo os dados do conjunto de linhas receberá um status nulo de **IRowset::GetData()**. Considere as seguintes definições de coluna a seguir da tabela Shippers:</span><span class="sxs-lookup"><span data-stu-id="49582-p108">Null values are handled by the **rs:maybenull** attribute. If this attribute is set to true, the contents of the column may contain a null value. Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**. Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="49582-139">A definição permite que CompanyName seja nulo, mas ShipperID não pode conter um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="49582-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="49582-140">Se a seção de dados contidos na linha seguinte, Persistence Provider definirá o status dos dados da coluna CompanyName para a constante de status do OLE DB DBSTATUS\_S\_ISNULL:</span><span class="sxs-lookup"><span data-stu-id="49582-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="49582-141">Se a linha estivesse totalmente vazia, da seguinte maneira, o Persistence Provider retornaria um status de OLE DB da DBSTATUS\_f\_INDISPONÍVEL para ShipperID e DBSTATUS\_S\_ISNULL para CompanyName.</span><span class="sxs-lookup"><span data-stu-id="49582-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="49582-142">Observe que uma sequência de caracteres de comprimento igual a zero não é nula.</span><span class="sxs-lookup"><span data-stu-id="49582-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="49582-143">Para a linha anterior, o Persistence Provider retornará um status de OLE DB da DBSTATUS\_S\_Okey para ambas as colunas.</span><span class="sxs-lookup"><span data-stu-id="49582-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="49582-144">Nesse caso, CompanyName é simplesmente "" (uma sequência de caracteres de comprimento zero).</span><span class="sxs-lookup"><span data-stu-id="49582-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="49582-145">Para obter mais informações sobre construções de banco de dados OLE disponíveis para uso dentro da seção schema de um documento em XML do banco de dados OLE, consulte a definição de "urn:schemas-microsoft-com:rowset" e o OLE DB Programmer's Guide.</span><span class="sxs-lookup"><span data-stu-id="49582-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>

