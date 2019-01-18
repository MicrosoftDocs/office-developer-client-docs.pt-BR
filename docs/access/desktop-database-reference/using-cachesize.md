---
title: Usando CacheSize (referência de banco de dados da área de trabalho do Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718956"
---
# <a name="using-cachesize"></a><span data-ttu-id="cbd18-102">Uso de CacheSize</span><span class="sxs-lookup"><span data-stu-id="cbd18-102">Using CacheSize</span></span>

<span data-ttu-id="cbd18-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbd18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbd18-p101">Use a propriedade **CacheSize** para controlar a quantidade de registros a serem recuperados de uma vez, do provedor para a memória local. Por exemplo, se **CacheSize** for 10, após a abertura inicial do objeto **Recordset**, o provedor irá recuperar os 10 primeiros registros para a memória local. À medida que você se movimentar pelo objeto **Recordset**, o provedor retornará os dados do buffer de memória local. Assim que você passar pelo último registro armazenado em cache, o provedor irá recuperar os 10 registros seguintes da fonte de dados para o cache.</span><span class="sxs-lookup"><span data-stu-id="cbd18-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="cbd18-p102">[!OBSERVAçãO] A propriedade **CacheSize** baseia-se na propriedade **Maximum Open Rows** específica do provedor (na coleção **Properties** do objeto **Recordset** ). Não é possível definir **CacheSize** como um valor maior do que **Maximum Open Rows**. Para modificar o número de linhas que podem ser abertas pelo provedor, defina **Maximum Open Rows**.</span><span class="sxs-lookup"><span data-stu-id="cbd18-p102">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="cbd18-p103">O valor de **CacheSize** pode ser ajustado durante a vida do objeto **Recordset**, mas a alteração desse valor afeta apenas o número de registros do cache após recuperações subsequentes da fonte de dados. Alterar apenas o valor da propriedade não irá alterar o conteúdo atual do cache.</span><span class="sxs-lookup"><span data-stu-id="cbd18-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="cbd18-113">Se o número de registros a serem recuperados for menor do que o especificado em **CacheSize**, o provedor retornará os registros restantes e não ocorrerá erros.</span><span class="sxs-lookup"><span data-stu-id="cbd18-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="cbd18-114">A configuração de **CacheSize** como zero não é permitida e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cbd18-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="cbd18-p104">Os registros recuperados do cache não refletem as alterações simultâneas feitas por outros usuários na fonte de dados. Para forçar uma atualização de todos os dados armazenados em cache, use o método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cbd18-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="cbd18-p105">Se **CacheSize** for definido como um valor maior do que 1, os métodos de navegação ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext e MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) poderão resultar na navegação para um registro excluído, se a exclusão ocorrer após a recuperação dos registros. Depois da busca inicial, as exclusões subsequentes não serão refletidas no cache de dados, até que você tente acessar um valor de dados de uma linha excluída. No entanto, a definição de **CacheSize** como 1 elimina esse problema, pois as linhas excluídas não podem ser buscadas.</span><span class="sxs-lookup"><span data-stu-id="cbd18-p105">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

