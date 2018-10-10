---
title: Propriedade Recordset2.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 204b66b120405522707da23bf093a311ca8c2625
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463764"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="a1dd4-102">Propriedade Recordset2.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1dd4-102">Recordset2.BatchCollisions Property (DAO)</span></span>


<span data-ttu-id="a1dd4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1dd4-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a1dd4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1dd4-104">Syntax</span></span>

<span data-ttu-id="a1dd4-105">*expressão* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="a1dd4-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="a1dd4-106">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a1dd4-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1dd4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1dd4-107">Remarks</span></span>

<span data-ttu-id="a1dd4-p101">Essa propriedade contém uma matriz de indicadores para as linhas que se encontram em colisão durante a última tentativa de chamada **[Update](recordset2-update-method-dao.md)** em lotes. A propriedade **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indica o número dos elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="a1dd4-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call. The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="a1dd4-110">Se você definir a propriedade [**Bookmark**](recordset2-bookmark-property-dao.md) do objeto **Recordset** em funcionamento como valores de indicador na matriz **BatchCollisions**, poderá mover cada registro com falha para concluir a operação de Atualização no modo de lotes mais recente.</span><span class="sxs-lookup"><span data-stu-id="a1dd4-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="a1dd4-p102">Depois que os registros de colisão forem corrigidos, você poderá chamar o método **Update** do modo de lotes novamente. Nesse ponto, o DAO tentará outra atualização em lotes e a propriedade **BatchCollisions** refletirá novamente o conjunto de registros que falharam na segunda tentativa. Qualquer registro que foi bem-sucedido na tentativa anterior não será enviado para a tentativa atual porque agora possui a propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)** de dbRecordUnmodified. Esse processo poderá continuar enquanto ocorrem colisões ou até que você desista das atualizações e feche o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="a1dd4-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="a1dd4-115">Essa matriz é recriada sempre que você executar um método **Update** no modo em lote.</span><span class="sxs-lookup"><span data-stu-id="a1dd4-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

