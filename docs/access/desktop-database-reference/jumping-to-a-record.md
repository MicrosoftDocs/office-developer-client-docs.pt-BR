---
title: Alternância para um registro
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290783"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="a74d2-102">Alternância para um registro</span><span class="sxs-lookup"><span data-stu-id="a74d2-102">Jumping to a record</span></span>


<span data-ttu-id="a74d2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a74d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a74d2-104">O método [Move](move-method-ado.md) permite que você avance ou retroceda um número específico de registros no **Recordset** usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="a74d2-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="a74d2-105">Há suporte no método **Move** para todos os objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a74d2-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="a74d2-p101">Se o argumento *NumRecords* for maior que zero, a posição de registro atual é movida para frente (em direção ao final do **Recordset**). Se *NumRecords* for menor que zero, a posição de registro atual será movida para trás (em direção ao início do **Recordset**).</span><span class="sxs-lookup"><span data-stu-id="a74d2-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="a74d2-p102">Se a chamada de **Move** mover a posição de registro atual para um ponto antes do primeiro registro, o ADO define o registro atual para a posição antes do primeiro registro no **Recordset** (**BOF** é **True**). Uma tentativa em mover para trás quando a propriedade **BOF** já é **True** gera um erro.</span><span class="sxs-lookup"><span data-stu-id="a74d2-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a74d2-p103">Se a chamada de **Move** mover a posição do registro atual para um ponto depois do último registro, o ADO define o registro atual para a posição depois do último registro no **Recordset** (**EOF** é **True**). Uma tentativa em mover para frente quando a propriedade **EOF** já é **True** gera um erro.</span><span class="sxs-lookup"><span data-stu-id="a74d2-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a74d2-112">Chamar o método **Move** a partir de um objeto **Recordset** vazio gera um erro.</span><span class="sxs-lookup"><span data-stu-id="a74d2-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="a74d2-p104">Se você passar um indicador no argumento *Start*, o movimento será relativo ao registro com esse indicador, assumindo que o objeto **Recordset** suporte indicadores. Um indicador é obtido usando a propriedade [Bookmark](bookmark-property-ado.md). Se não for especificado, o movimento será relativo ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="a74d2-p104">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="a74d2-p105">Se estiver utilizando a propriedade **CacheSize** para armazenar localmente em cache os registros do provedor, passar um argumento *NumRecords* que mova a posição do registro atual para fora do grupo atual de registros em cache força o ADO a recuperar um novo grupo de registros, iniciando pelo registro de destino. A propriedade **CacheSize** determina o tamanho do grupo recém-recuperado e o registro de destino é o primeiro registro recuperado.</span><span class="sxs-lookup"><span data-stu-id="a74d2-p105">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

