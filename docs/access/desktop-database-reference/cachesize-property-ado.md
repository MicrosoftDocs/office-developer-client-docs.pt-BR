---
title: Propriedade CacheSize (ADO)
TOCTitle: CacheSize Property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed4d104dcd6d0b90e6011a305cd3502cf671175b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464610"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="37935-102">Propriedade CacheSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="37935-102">CacheSize Property (ADO)</span></span>


<span data-ttu-id="37935-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37935-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37935-104">Indica o número de registros de um objeto [Recordset](recordset-object-ado.md) que ficam armazenados em cache localmente na memória.</span><span class="sxs-lookup"><span data-stu-id="37935-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="37935-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="37935-105">Settings and Return Values</span></span>

<span data-ttu-id="37935-p101">Define ou retorna um valor **Long** que deve ser maior do que 0. O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="37935-p101">Sets or returns a **Long** value that must be greater than 0. Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="37935-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="37935-108">Remarks</span></span>

<span data-ttu-id="37935-p102">Use a propriedade **CacheSize** para controlar a quantidade de registros a serem recuperados de uma vez, do provedor para a memória local. Por exemplo, se **CacheSize** for 10, após a abertura inicial do objeto **Recordset**, o provedor irá recuperar os 10 primeiros registros para a memória local. À medida que você se movimentar pelo objeto **Recordset**, o provedor retornará os dados do buffer de memória local. Assim que você passar pelo último registro armazenado em cache, o provedor irá recuperar os 10 registros seguintes da fonte de dados para o cache.</span><span class="sxs-lookup"><span data-stu-id="37935-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="37935-p103">[!OBSERVAçãO] <STRONG>CacheSize</STRONG> baseia-se na propriedade <STRONG>Maximum Open Rows</STRONG> específica do provedor (na coleção <STRONG>Properties</STRONG> do objeto <STRONG>Recordset</STRONG> ). Não é possível definir <STRONG>CacheSize</STRONG> para um valor maior do que <STRONG>Maximum Open Rows</STRONG>. Para modificar o número de linhas que podem ser abertas pelo provedor, defina <STRONG>Maximum Open Rows</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="37935-p103"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows which can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="37935-p104">O valor de **CacheSize** pode ser ajustado enquanto o objeto **Recordset** durar, mas a alteração desse valor afetará apenas o número de registros no cache após recuperações subsequentes da fonte de dados. A alteração do valor da propriedade apenas não alterará o conteúdo atual do cache.</span><span class="sxs-lookup"><span data-stu-id="37935-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="37935-118">Se o número de registros a serem recuperados for menor do que o especificado em **CacheSize**, o provedor retornará os registros restantes e não ocorrerá erros.</span><span class="sxs-lookup"><span data-stu-id="37935-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="37935-119">Não é permitido definir **CacheSize** como zero e isso provocará um erro.</span><span class="sxs-lookup"><span data-stu-id="37935-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="37935-p105">Os registros recuperados do cache não refletem alterações simultâneas feitas por outros usuários na fonte de dados. Para forçar uma atualização de todos os dados armazenados em cache, use o método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37935-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="37935-p106">Se **CacheSize** for definida com um valor maior do que um, os métodos de navegação ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext e MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) poderão resultar na navegação para um registro excluído, caso a exclusão ocorra depois que os registros forem recuperados. Após a busca inicial, as exclusões seguintes não serão refletidas no cache de dados até que você tente acessar um valor de dados de uma linha excluída. Contudo, a definição de **CacheSize** como um elimina esse problema, uma vez que as linhas excluídas não poderão ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="37935-p106">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

