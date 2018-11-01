---
title: A coleção Fields
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67f16c9c4dd27fdbd57a2c082580ead0606298e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874871"
---
# <a name="the-fields-collection"></a><span data-ttu-id="4caf4-102">A coleção Fields</span><span class="sxs-lookup"><span data-stu-id="4caf4-102">The Fields Collection</span></span>


<span data-ttu-id="4caf4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4caf4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4caf4-p101">A coleção **Fields** é uma das coleções intrínsecas do ADO. Uma coleção é um conjunto ordenado de itens ao qual podemos nos referir como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="4caf4-p101">The **Fields** collection is one of ADO's intrinsic collections. A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="4caf4-p102">A coleção **Fields** contém um objeto **Field** para cada campo (coluna) no **Recordset**. Como todas as coleções do ADO, ela possui as propriedades **Count** e **Item**, além dos métodos **Append** e **Refresh**. Ela também possui métodos **CancelUpdate**, **Delete**, **Resync** e **Update**, que não estão disponíveis para outras coleções da ADO.</span><span class="sxs-lookup"><span data-stu-id="4caf4-p102">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**. Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods. It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="4caf4-109">Examinando a coleção Fields</span><span class="sxs-lookup"><span data-stu-id="4caf4-109">Examining the Fields Collection</span></span>

<span data-ttu-id="4caf4-p103">Considere a coleção **Fields** do **Recordset** de exemplo apresentado neste capítulo. O **Recordset** de exemplo foi derivado da instrução SQL</span><span class="sxs-lookup"><span data-stu-id="4caf4-p103">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter. The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="4caf4-112">Assim, você descobrirá que a coleção **Fields** do **Recordset** contém três campos.</span><span class="sxs-lookup"><span data-stu-id="4caf4-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

<span data-ttu-id="4caf4-p104">Esse código determina simplesmente o número de objetos **Field** na coleção **Fields** usando a propriedade **Count** e os loops pela coleção, retornando o valor da propriedade **Name** de cada objeto **Field**. Você pode usar muitas outras propriedades de **Field** para obter informações sobre um campo. Para obter mais informações sobre como consultar um **campo**, consulte [O objeto Field](the-field-object.md).</span><span class="sxs-lookup"><span data-stu-id="4caf4-p104">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object. You can use many more **Field** properties to get information about a field. For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="4caf4-116">Contando colunas</span><span class="sxs-lookup"><span data-stu-id="4caf4-116">Counting Columns</span></span>

<span data-ttu-id="4caf4-p105">Como você deve esperar, a propriedade **Count** retorna o número real de objetos **Field** na coleção **Fields**. Como a numeração dos participantes de uma coleção começa com zero, você sempre deve codificar os loops começando com o participante zero e terminado com o valor da propriedade **Count** menos 1. Se estiver usando o Microsoft Visual Basic e desejar fazer um loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="4caf4-p105">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection. Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="4caf4-120">Se a propriedade **Count** for zero, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="4caf4-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="4caf4-121">Chegando ao Field</span><span class="sxs-lookup"><span data-stu-id="4caf4-121">Getting to the Field</span></span>

<span data-ttu-id="4caf4-p106">Como em qualquer coleção do ADO, a propriedade **Item** é a propriedade padrão da coleção. Ela retorna o objeto **Field** individual especificado pelo nome ou índice passado para ela. Portanto, as instruções a seguir são equivalentes para o **Recordset** de exemplo:</span><span class="sxs-lookup"><span data-stu-id="4caf4-p106">As with any ADO collection, the **Item** property is the default property of the collection. It returns the individual **Field** object specified by the name or index passed to it. Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="4caf4-p107">Se esses métodos são equivalentes, qual é o melhor? Depende. Usar um índice para recuperar um **campo** da coleção é mais rápido porque ele acessa o **campo** diretamente, sem precisar executar uma busca de sequência. Por outro lado, a ordem de **campos** na coleção deve ser conhecida e, se a ordem for alterada, a referência ao índice de **campos** deverá ser alterado, onde quer que ocorra. Apesar de um pouco mais lenta, a utilização do nome do **campo** é mais flexível porque não depende da ordem dos **campos** na coleção.</span><span class="sxs-lookup"><span data-stu-id="4caf4-p107">If these methods are equivalent, which is best? It depends. Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup. On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs. Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="4caf4-130">Usando o método Refresh</span><span class="sxs-lookup"><span data-stu-id="4caf4-130">Using the Refresh Method</span></span>

<span data-ttu-id="4caf4-p108">Diferente de algumas outras coleções do ADO, a utilização do método **Refresh** na coleção **Fields** não tem nenhum efeito visível. Para recuperar alterações da estrutura do banco de dados de base, você deve usar o método **Requery** ou, se o objeto **Recordset** não oferecer suporte a indicadores, o método **MoveFirst**, que fará o comando ser executado contra o provedor novamente.</span><span class="sxs-lookup"><span data-stu-id="4caf4-p108">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="4caf4-133">Adicionando campos a um Recordset</span><span class="sxs-lookup"><span data-stu-id="4caf4-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="4caf4-134">O método **Append** é usado para adicionar campos a um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4caf4-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="4caf4-p109">Você pode usar o método **Append** para fabricar um **Recordset** por programação, sem abrir uma conexão com uma origem de dados. Ocorrerá um erro em tempo de execução se o método **Append** for chamado na coleção **Fields** de um **Recordset** aberto ou em um **Recordset** onde a propriedade **ActiveConnection** tiver sido definida. Você pode acrescentar campos apenas a um **Recordset** que não esteja aberto e ainda não esteja conectado a uma origem de dados. Contudo, para especificar valores para os **campos** recém-acrescentados, o **Recordset** deverá ser aberto primeiro.</span><span class="sxs-lookup"><span data-stu-id="4caf4-p109">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source. A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set. You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source. However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="4caf4-p110">Frequentemente os desenvolvedores precisam de um lugar para armazenar alguns dados temporariamente ou desejam que alguns dados atuem como se viessem de um servidor de forma que possam participar na ligação de dados em uma interface do usuário. O ADO (em conjunto com o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) permite que o desenvolvedor crie um objeto **Recordset** vazio especificando informações de coluna e chamando **Open**. No exemplo a seguir, três novos campos são acrescentados a um objeto **Recordset** novo. Em seguida, o **Recordset** é aberto, dois registros novos são adicionados e o **Recordset** é mantido em um arquivo. (Para obter mais informações sobre a manutenção do **Recordset**, consulte o [Capítulo 5: Atualizando e mantendo dados](chapter-5-updating-and-persisting-data.md).)</span><span class="sxs-lookup"><span data-stu-id="4caf4-p110">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface. ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**. In the following example, three new fields are appended to a new **Recordset** object. Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file. (For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

<span data-ttu-id="4caf4-p111">O uso do método **Append** dos **campos** difere entre o objeto **Recordset** e o objeto **Record**. Para obter mais informações sobre o objeto **Record**, consulte o [Capítulo 10: Registros e fluxos](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="4caf4-p111">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object. For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

