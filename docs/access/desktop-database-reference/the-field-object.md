---
title: O objeto Field (referência de banco de dados da área de trabalho do Access)
TOCTitle: The Field Object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b01232e7afd4f32411a53dec6ae233c786c1c08
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873401"
---
# <a name="field-object"></a><span data-ttu-id="d8501-102">Objeto Field</span><span class="sxs-lookup"><span data-stu-id="d8501-102">Field Object</span></span>


<span data-ttu-id="d8501-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8501-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8501-p101">Cada objeto **Field** normalmente corresponde a uma coluna em uma tabela de banco de dados. No entanto, um **Field** também pode representar um ponteiro para outro **Recordset**, chamado de capítulo. Exceções, como colunas de capítulo, serão abordadas posteriormente neste guia.</span><span class="sxs-lookup"><span data-stu-id="d8501-p101">Each **Field** object usually corresponds to a column in a database table. However, a **Field** can also represent a pointer to another **Recordset**, called a chapter. Exceptions, such as chapter columns, will be covered later in this guide.</span></span>

<span data-ttu-id="d8501-p102">Use a propriedade **Value** de objetos **Field** para definir ou retornar dados do registro atual. Dependendo da funcionalidade apresentada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Field** talvez não estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d8501-p102">Use the **Value** property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="d8501-109">Com as coleções, os métodos e as propriedades de um objeto **Field**, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d8501-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="d8501-110">Retornar o nome de um campo usando a propriedade **Name**.</span><span class="sxs-lookup"><span data-stu-id="d8501-110">Return the name of a field by using the **Name** property.</span></span>

  - <span data-ttu-id="d8501-p103">Exibir ou alterar os dados do campo usando a propriedade **Value**. **Value** é a propriedade padrão do objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p103">View or change the data in the field by using the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="d8501-113">Retorne as características básicas de um campo usando as propriedades **Type**, **Precision** e **NumericScale**.</span><span class="sxs-lookup"><span data-stu-id="d8501-113">Return the basic characteristics of a field by using the **Type**, **Precision**, and **NumericScale** properties.</span></span>

  - <span data-ttu-id="d8501-114">Retorne um tamanho declarada de um campo usando a propriedade **DefinedSize**.</span><span class="sxs-lookup"><span data-stu-id="d8501-114">Return the declared size of a field by using the **DefinedSize** property.</span></span>

  - <span data-ttu-id="d8501-115">Retorne o tamanho real dos dados em determinado campo usando a propriedade **ActualSize**.</span><span class="sxs-lookup"><span data-stu-id="d8501-115">Return the actual size of the data in a given field by using the **ActualSize** property.</span></span>

  - <span data-ttu-id="d8501-116">Determine a quais tipos de funcionalidade há suporte em determinado campo, usando a propriedade **Attributes** e a coleção **Properties**.</span><span class="sxs-lookup"><span data-stu-id="d8501-116">Determine what types of functionality are supported for a given field by using the **Attributes** property and **Properties** collection.</span></span>

  - <span data-ttu-id="d8501-117">Manipule os valores dos campos que contêm dados binários longos e de caracteres longos, usando os métodos **AppendChunk** e **GetChunk**.</span><span class="sxs-lookup"><span data-stu-id="d8501-117">Manipulate the values of fields containing long binary or long character data by using the **AppendChunk** and **GetChunk** methods.</span></span>

<span data-ttu-id="d8501-118">Resolva discrepâncias nos valores dos campos durante as atualizações em lotes, usando as propriedades **OriginalValue** e **UnderlyingValue**, se o provedor oferecer suporte a essas atualizações.</span><span class="sxs-lookup"><span data-stu-id="d8501-118">Resolve discrepancies in field values during batch updating by using the **OriginalValue** and **UnderlyingValue** properties, if the provider supports batch updates.</span></span>

## <a name="describing-a-field"></a><span data-ttu-id="d8501-119">Descrevendo um campo</span><span class="sxs-lookup"><span data-stu-id="d8501-119">Describing a Field</span></span>

<span data-ttu-id="d8501-p104">Os tópicos a seguir abordarão as propriedades do objeto [Field](field-object-ado.md) que representam informações descritivas do próprio objeto **Field**, isto é, metadados sobre o campo. É possível usar essas informações para determinar vários aspectos sobre o esquema do **Recordset**. Essas propriedades incluem **Type**, **DefinedSize** e **ActualSize**, bem como **Name**, **NumericScale** e **Precision**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p104">The topics that follow will discuss properties of the [Field](field-object-ado.md) object that represent information that describes the **Field** object itself — that is, metadata about the field. This information can be used to determine much about the schema of the **Recordset**. These properties include **Type**, **DefinedSize** and **ActualSize**, **Name**, and **NumericScale** and **Precision**.</span></span>

## <a name="discovering-the-data-type"></a><span data-ttu-id="d8501-123">Descobrindo o tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d8501-123">Discovering the Data Type</span></span>

<span data-ttu-id="d8501-p105">A propriedade **Type** indica o tipo de dados do campo. As constantes enumeradas do tipo de dados às quais o ADO oferece suporte estão descritas em [DataTypeEnum](datatypeenum.md) na *Referência do programador do ADO* (ADO Programmer's Reference).</span><span class="sxs-lookup"><span data-stu-id="d8501-p105">The **Type** property indicates the data type of the field. The data type enumerated constants that are supported by ADO are described in [DataTypeEnum](datatypeenum.md) in the *ADO Programmer's Reference*.</span></span>

<span data-ttu-id="d8501-p106">É possível obter mais informações sobre os tipos numéricos de ponto flutuante, como **adNumeric**. A propriedade **NumericScale** indica quantos dígitos à direita do ponto decimal serão usados para representar valores do **Field**. A propriedade **Precision** especifica o número máximo de dígitos usados para representar valores do **Field**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p106">For floating point numeric types such **adNumeric**, you can obtain more information. The **NumericScale** property indicates how many digits to the right of the decimal point will be used to represent values for the **Field**. The **Precision** property specifies the maximum number of digits used to represent values for the **Field**.</span></span>

## <a name="determining-field-size"></a><span data-ttu-id="d8501-129">Determinando o tamanho do campo</span><span class="sxs-lookup"><span data-stu-id="d8501-129">Determining Field Size</span></span>

<span data-ttu-id="d8501-130">Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="d8501-130">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="d8501-p107">Use a propriedade **ActualSize** para retornar o valor real de um objeto **Field**. Em todos os campos, a propriedade **ActualSize** é somente leitura. Se o ADO não puder determinar o valor do objeto **Field**, a propriedade **ActualSize** retornará **adUnknown**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p107">Use the **ActualSize** property to return the actual length of a **Field** object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="d8501-p108">As propriedades **DefinedSize** e **ActualSize** tem finalidades diferentes. Por exemplo, considere um objeto **Field** com o tipo declarado **adVarChar** e o valor 50 da propriedade **DefinedSize**, contendo um único caractere. O valor da propriedade **ActualSize** retornado por ele é o tamanho em bytes do caractere único.</span><span class="sxs-lookup"><span data-stu-id="d8501-p108">The **DefinedSize** and **ActualSize** properties have different purposes. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

## <a name="determining-field-contents"></a><span data-ttu-id="d8501-137">Determinando o conteúdo do campo</span><span class="sxs-lookup"><span data-stu-id="d8501-137">Determining Field Contents</span></span>

<span data-ttu-id="d8501-p109">O identificador da coluna da fonte de dados é representado pela propriedade **Name** do **Field**. A propriedade **Value** do objeto **Field** retorna ou define o conteúdo real dos dados do campo. Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="d8501-p109">The identifier of the column from the data source is represented by the **Name** property of the **Field**. The **Value** property of the **Field** object returns or sets the actual data content of the field. This is the default property.</span></span>

<span data-ttu-id="d8501-p110">Para alterar os dados em um campo, defina a propriedade **Value** como um novo valor do tipo correto. O tipo de seu cursor deve oferecer suporte a atualizações para que o conteúdo de um campo seja alterado. A validação do banco de dados não é feita aqui no modo em lotes; portanto, você precisará verificar os erros quando chamar **UpdateBatch** nesse caso. Alguns provedores também oferecem suporte às propriedades **UnderlyingValue** e **OriginalValue** do objeto **Field** do ADO para ajudá-lo a solucionar conflitos quando você tentar realizar atualizações em lotes. Para obter detalhes sobre como solucionar esses conflitos, consulte o [Capítulo 4: Editando dados](chapter-4-editing-data.md).</span><span class="sxs-lookup"><span data-stu-id="d8501-p110">To change the data in a field, set the **Value** property equal to a new value of the correct type. Your cursor type must support updates to change the contents of a field. Database validation is not done here in batch mode, so you will need to check for errors when you call **UpdateBatch** in such a case. Some providers also support the ADO **Field** object's **UnderlyingValue** and **OriginalValue** properties to assist you with resolving conflicts when you attempt to perform batch updates. For details about how to resolve such conflicts, see [Chapter 4: Editing Data](chapter-4-editing-data.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="d8501-p111">[!OBSERVAçãO] Não é possível definir os valores do campo <STRONG>Recordset</STRONG> durante o acréscimo de novos objetos <STRONG>Field</STRONG> a um <STRONG>Recordset</STRONG>. Em vez disso, é possível acrescentar novos objetos <STRONG>Field</STRONG> a um <STRONG>Recordset</STRONG> fechado. Em seguida, o <STRONG>Recordset</STRONG> deverá ser aberto, e só então valores poderão ser atribuídos a esses objetos <STRONG>Field</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d8501-p111"><STRONG>Recordset Field</STRONG> values cannot be set when appending new <STRONG>Fields</STRONG> to a <STRONG>Recordset</STRONG>. Rather, new <STRONG>Fields</STRONG> can be appended to a closed <STRONG>Recordset</STRONG>. Then the <STRONG>Recordset</STRONG> must be opened, and only then can values be assigned to these <STRONG>Fields</STRONG>.</span></span></P>



## <a name="getting-more-field-information"></a><span data-ttu-id="d8501-149">Obtendo mais informações sobre campos</span><span class="sxs-lookup"><span data-stu-id="d8501-149">Getting More Field Information</span></span>

<span data-ttu-id="d8501-p112">Os objetos do ADO têm dois tipos de propriedades: internas e dinâmicas. Até esse ponto, foram abordadas somente as propriedades internas do objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p112">ADO objects have two types of properties: built-in and dynamic. To this point, only the built-in properties of the **Field** object have been discussed.</span></span>

<span data-ttu-id="d8501-152">As propriedades internas são aquelas propriedades implementadas no ADO e estão disponíveis para qualquer novo objeto, usando a sintaxe imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d8501-152">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="d8501-153">Elas não são exibidas como objetos **Property** na coleção **Properties** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="d8501-153">They do not appear as **Property** objects in an object's **Properties** collection.</span></span>

<span data-ttu-id="d8501-154">As propriedades dinâmicas são definidas pelo provedor de dados subjacentes e aparecem na coleção **Properties** referente ao objeto ADO adequado.</span><span class="sxs-lookup"><span data-stu-id="d8501-154">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="d8501-155">Por exemplo, uma propriedade específica do provedor pode indicar se um objeto **Recordset** oferece suporte a transações ou à atualização.</span><span class="sxs-lookup"><span data-stu-id="d8501-155">For example, a property specific to the provider may indicate if a **Recordset** object supports transactions or updating.</span></span> <span data-ttu-id="d8501-156">Essas propriedades adicionais serão exibidas como objetos **Property** na coleção **Properties** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d8501-156">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="d8501-157">Propriedades dinâmicas podem ser referenciadas somente através da coleção, usando a sintaxe MyObject.Properties(0) ou ou MyObject.Properties("Name").</span><span class="sxs-lookup"><span data-stu-id="d8501-157">Dynamic properties can be referenced only through the collection, using the syntax MyObject.Properties(0) or or MyObject.Properties("Name") .</span></span>

<span data-ttu-id="d8501-158">Não é possível excluir nenhum tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d8501-158">You cannot delete either kind of property.</span></span>

<span data-ttu-id="d8501-159">Um objeto **Property** dinâmico tem quatro propriedades internas próprias:</span><span class="sxs-lookup"><span data-stu-id="d8501-159">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="d8501-160">A propriedade **Name** é uma cadeia de caracteres que identifica a propriedade.</span><span class="sxs-lookup"><span data-stu-id="d8501-160">The **Name** property is a string that identifies the property.</span></span>

  - <span data-ttu-id="d8501-161">A propriedade **Type** é um número inteiro que especifica o tipo de dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d8501-161">The **Type** property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="d8501-p115">A propriedade **Value** é uma variante que contém a definição da propriedade. **Value** é a propriedade padrão de um objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p115">The **Value** property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="d8501-164">A propriedade **Attributes** é um valor **Long** que indica características da propriedade específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="d8501-164">The **Attributes** property is a **Long** value that indicates characteristics of the property specific to the provider.</span></span>

<span data-ttu-id="d8501-p116">A coleção **Properties** do objeto **Field** contém metadados adicionais sobre o campo. O conteúdo dessa coleção varia de acordo com o provedor. O exemplo de código a seguir examina a coleção **Properties** do **Recordset** de exemplo apresentado no início deste capítulo. Primeiro, ele observa o conteúdo da coleção. Esse código usa o [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), de modo que a coleção **Properties** contenha informações relevantes a esse provedor.</span><span class="sxs-lookup"><span data-stu-id="d8501-p116">The **Properties** collection for the **Field** object contains additional metadata about the field. The contents of this collection vary depending upon the provider. The following code example examines the **Properties** collection of the sample **Recordset** introduced at the beginning of this chapter. It first looks at the contents of the collection. This code uses the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), so the **Properties** collection contains information relevant to that provider.</span></span>

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a><span data-ttu-id="d8501-170">Lidando com dados binários</span><span class="sxs-lookup"><span data-stu-id="d8501-170">Dealing with Binary Data</span></span>

<span data-ttu-id="d8501-p117">Use o método [AppendChunk](appendchunk-method-ado.md) em um objeto **Field** para preenchê-lo com dados binários ou de caracteres longos. Em situações em que a memória do sistema é limitada, você pode usar o método **AppendChunk** para manipular valores longos em partes, e não em sua totalidade.</span><span class="sxs-lookup"><span data-stu-id="d8501-p117">Use the [AppendChunk](appendchunk-method-ado.md) method on a **Field** object to fill it with long binary or character data. In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="d8501-173">Se o bit **adFldLong** na propriedade **Attributes** de um objeto **Field** for definido como **True**, você poderá usar o método **AppendChunk** nesse campo.</span><span class="sxs-lookup"><span data-stu-id="d8501-173">If the **adFldLong** bit in the **Attributes** property of a **Field** object is set to **True**, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="d8501-p118">A primeira chamada de **AppendChunk** em um objeto **Field** grava dados no campo, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** fazem adições aos dados existentes. Se você estiver acrescentando dados a um campo e, depois, definir ou ler o valor de outro campo no registro atual, o ADO presumirá que o acréscimo de dados ao primeiro campo foi concluído. Se você chamar o método **AppendChunk** no primeiro campo novamente, o ADO interpretará a chamada como uma nova operação de **AppendChunk** e substituirá os dados existentes. O acesso a campos em outros objetos **Recordset** que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **AppendChunk**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p118">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other **Recordset** objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="d8501-p119">Use o método **GetChunk** em um objeto **Field** para recuperar parte ou todos os seus dados binários ou de caracteres longos. Em situações em que a memória do sistema é limitada, você pode usar o método **GetChunk** para manipular valores longos em partes, e não em sua totalidade.</span><span class="sxs-lookup"><span data-stu-id="d8501-p119">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="d8501-p120">Os dados retornados por **GetChunk** são atribuídos a *variable*. Se *Size* for maior que os dados restantes, o método **GetChunk** retornará somente esses dados sem preencher *variable* com espaços vazios. Se o campo estiver vazio, o método **GetChunk** retornará um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="d8501-p120">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="d8501-p121">Cada chamada subsequente de **GetChunk** recupera dados a partir do ponto em que a chamada anterior de **GetChunk** foi interrompida. Contudo, se você estiver recuperando dados de um campo e, em seguida, definir ou ler o valor de outro campo do registro atual, o ADO presumirá que foi concluída a recuperação de dados no primeiro campo. Se você chamar o método **GetChunk** no primeiro campo novamente, o ADO interpretará a chamada como uma nova operação de **GetChunk** e iniciará a leitura desde o início dos dados. O acesso a campos em outros objetos **Recordset** que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **GetChunk**.</span><span class="sxs-lookup"><span data-stu-id="d8501-p121">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other **Recordset** objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="d8501-188">Se o bit **adFldLong** na propriedade **Attributes** de um objeto **Field** for definido como **True**, será possível utilizar o método **GetChunk** nesse campo.</span><span class="sxs-lookup"><span data-stu-id="d8501-188">If the **adFldLong** bit in the **Attributes** property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="d8501-189">Se não houver um registro atual quando você usar o método **GetChunk** ou **AppendChunk** em um objeto **Field**, ocorrerá o erro 3021 (sem registro atual).</span><span class="sxs-lookup"><span data-stu-id="d8501-189">If there is no current record when you use the **GetChunk** or **AppendChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>

<span data-ttu-id="d8501-190">Para obter um exemplo de como usar esses métodos para manipular dados binários, consulte os exemplos do [Método AppendChunk](appendchunk-method-ado.md) e [Método GetChunk](getchunk-method-ado.md) na *Referência do programador do ADO* (ADO Programmer's Reference).</span><span class="sxs-lookup"><span data-stu-id="d8501-190">For an example of using these methods to manipulate binary data, see the [AppendChunk Method](appendchunk-method-ado.md) and [GetChunk Method](getchunk-method-ado.md) examples in the *ADO Programmer's Reference*.</span></span>

