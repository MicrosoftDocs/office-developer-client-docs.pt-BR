---
title: Contando linhas (referência de banco de dados da área de trabalho do Access)
TOCTitle: Counting Rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 664e7022d3a49f7c4c7c1fa6122b05a230b6e297
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889648"
---
# <a name="counting-rows"></a><span data-ttu-id="8e11a-102">Contagem de linhas</span><span class="sxs-lookup"><span data-stu-id="8e11a-102">Counting Rows</span></span>


<span data-ttu-id="8e11a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e11a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e11a-p101">A propriedade **RecordCount** retorna um valor **Long** que indica o número de registros no **Recordset**. Use a propriedade **RecordCount** para descobrir quantos registros existem em um objeto **Recordset**. A propriedade retorna -1 quando o ADO não pode determinar o número de registros ou se o tipo de cursor ou provedor não oferecer suporte à propriedade **RecordCount**. Ler a propriedade **RecordCount** em um objeto **Recordset** fechado produz um erro.</span><span class="sxs-lookup"><span data-stu-id="8e11a-p101">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**. Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="8e11a-p102">A propriedade **RecordCount** depende dos recursos do provedor e do tipo de cursor. A propriedade **RecordCount** retornará -1 para um cursor apenas de avanço, a contagem real para um cursor estático ou de conjunto de chaves e -1 ou a contagem real para um cursor dinâmico, dependendo da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="8e11a-p102">The **RecordCount** property depends on the capabilities of the provider and the type of cursor. The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="8e11a-110">O exemplo de **Recordset** introduzidas no [Examinando dados](chapter-3-examining-data.md) retornaria – 1 porque um cursor somente de encaminhamento foi aberto.</span><span class="sxs-lookup"><span data-stu-id="8e11a-110">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened.</span></span> <span data-ttu-id="8e11a-111">Para usar a propriedade **RecordCount**, você precisaria abrir o **Recordset** com um cursor mais sofisticado (estático ou de conjunto de chaves).</span><span class="sxs-lookup"><span data-stu-id="8e11a-111">In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="8e11a-p104">Em alguns casos, o provedor ou o cursor talvez não seja capaz de fornecer o valor **RecordCount** sem primeiro buscar todos os registros na fonte de dados. Para forçar esse tipo de busca, chame o método **MoveLast** do objeto **Recordset** antes de chamar **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="8e11a-p104">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source. To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="8e11a-114">Se você estivava para substituir a linha de código que chama o método **Open** do objeto **Recordset** por:</span><span class="sxs-lookup"><span data-stu-id="8e11a-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="8e11a-p105">você poderia usar a propriedade **RecordCount** porque os cursores estáticos com [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) oferecem suporte à propriedade **RecordCount**. Por exemplo, o código a seguir imprimiria o número de registros retornados pelo comando para a janela de depuração, assumindo que o cursor oferecesse suporte à propriedade **RecordCount**:</span><span class="sxs-lookup"><span data-stu-id="8e11a-p105">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**. For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="8e11a-117">Deste ponto em diante, considere que essas configurações de tipo de bloqueio e cursor com mais recursos (mas mais caras) são usadas.</span><span class="sxs-lookup"><span data-stu-id="8e11a-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>

