---
title: Propriedade Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c151868e349621d964f61058cfe82458764cf443
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929087"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="fcef2-102">Propriedade Recordset.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="fcef2-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="fcef2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcef2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="fcef2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcef2-104">Syntax</span></span>

<span data-ttu-id="fcef2-105">*expressão* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="fcef2-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="fcef2-106">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="fcef2-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcef2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcef2-107">Remarks</span></span>

<span data-ttu-id="fcef2-p101">Essa propriedade contém uma matriz de indicadores para linhas que encontraram uma colisão durante a última tentativa de chamada de **[Update](recordset-update-method-dao.md)** em lote. A propriedade **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indica o número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="fcef2-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call. The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="fcef2-110">Se você definir trabalhar com a propriedade **[Bookmark](recordset-object-dao.md)** do objeto **[Recordset](recordset-bookmark-property-dao.md)** para indicar valores na matriz **BatchCollisions**, poderá mover-se para cada registro com falha para concluir a operação de atualização mais recente no modo em lote.</span><span class="sxs-lookup"><span data-stu-id="fcef2-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="fcef2-p102">Depois que os registros de colisão são corrigidos, você pode chamar novamente o método **Update** no modo em lote. Nesse momento, o DAO tenta outra atualização em lote, e a propriedade **BatchCollisions** reflete novamente o conjunto de registros que falharam na segunda tentativa. Os registros bem-sucedidos na tentativa anterior não são enviados para a tentativa atual, pois eles têm agora uma propriedade **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Esse processo pode continuar até não haver mais colisões ou até você parar as atualizações e fechar a definição de resultados.</span><span class="sxs-lookup"><span data-stu-id="fcef2-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="fcef2-115">Essa matriz é recriada sempre que você executar um método **Update** no modo em lote.</span><span class="sxs-lookup"><span data-stu-id="fcef2-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

