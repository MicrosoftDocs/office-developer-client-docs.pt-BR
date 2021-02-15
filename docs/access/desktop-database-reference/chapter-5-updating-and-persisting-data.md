---
title: 'Capítulo 5: Atualização e dados persistentes'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18dd63acd733624fba522ee7382f305d34019905
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296427"
---
# <a name="chapter-5-updating-and-persisting-data"></a><span data-ttu-id="f7a91-102">Capítulo 5: Atualização e dados persistentes</span><span class="sxs-lookup"><span data-stu-id="f7a91-102">Chapter 5: Updating and persisting data</span></span>

<span data-ttu-id="f7a91-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7a91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7a91-p101">Os capítulos anteriores abordavam como usar o ADO para obter dados em uma fonte de dados, como mover-se nos dados e até mesmo como editá-los. Obviamente, se o objetivo do aplicativo for permitir que os usuários façam alterações nos dados, você precisará entender como salvar essas alterações. Você pode manter as alterações do **Recordset** em um arquivo usando o método **Save** ou enviar as alterações de volta para a fonte de dados para armazenamento, usando os métodos **Update** ou **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="f7a91-p101">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data. Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes. You can either persist the **Recordset** changes to a file using the **Save** method, or you can send the changes back to the data source for storage using the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="f7a91-p102">Nos capítulos anteriores, você alterou os dados em várias linhas do **Recordset**. O ADO oferece suporte a duas noções básicas relacionadas à adição, exclusão e modificação de linhas de dados.</span><span class="sxs-lookup"><span data-stu-id="f7a91-p102">In the preceding chapters, you changed the data in several rows of the **Recordset**. ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</span></span>

<span data-ttu-id="f7a91-p103">A primeira noção é de que as alterações não são feitas imediatamente no **Recordset**; elas são feitas em um *buffer de cópia* interno. Se você decidir que não deseja as alterações, as modificações no buffer de cópia serão descartadas. Se você decidir mantê-las, as alterações no buffer de cópia serão aplicadas ao **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f7a91-p103">The first notion is that changes aren't immediately made to the **Recordset**; instead, they are made to an internal *copy buffer*. If you decide you don't want the changes, the modifications in the copy buffer are discarded. If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.</span></span>

<span data-ttu-id="f7a91-p104">A segunda noção é que as alterações são propagadas para a fonte de dados assim que você declarar o trabalho em uma linha completa (ou seja, modo *imediato*) ou todas as alterações em um conjunto de linhas serão coletadas até que você declare o trabalho para o conjunto completo (ou seja, modo *batch*). A propriedade **LockType** determina quando as alterações são feitas na fonte de dados subjacente. **adLockOptimistic** ou **adLockPessimistic** especifica o modo imediato, enquanto **adLockBatchOptimistic** especifica o modo de lote. A propriedade **CursorLocation** pode afetar quais configurações **LockType** estão disponíveis. Por exemplo, não há suporte para a configuração **adLockPessimistic** se a propriedade **CursorLocation** estiver definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="f7a91-p104">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, *immediate* mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, *batch* mode). The **LockType** property determines when the changes are made to the underlying data source. **adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode. The **CursorLocation** property can affect which **LockType** settings are available. For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.</span></span>

<span data-ttu-id="f7a91-p105">No modo imediato, cada invocação do método **Update** propaga as alterações na fonte de dados. No modo de lote, cada invocação de **Update** ou movimento da posição da linha atual salva as alterações no buffer de cópia, mas apenas o método **UpdateBatch** propaga as alterações para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="f7a91-p105">In immediate mode, each invocation of the **Update** method propagates the changes to the data source. In batch mode, each invocation of **Update** or movement of the current row position saves the changes to the copy buffer, but only the **UpdateBatch** method propagates the changes to the data source.</span></span>

<span data-ttu-id="f7a91-119">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f7a91-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="f7a91-120">Atualizando dados (ADO)</span><span class="sxs-lookup"><span data-stu-id="f7a91-120">Updating data (ADO)</span></span>](updating-data.md)
- [<span data-ttu-id="f7a91-121">Dados persistentes (ADO)</span><span class="sxs-lookup"><span data-stu-id="f7a91-121">Persisting data (ADO)</span></span>](persisting-data.md)
