---
title: Informações sobre erros relacionados a recordsets
TOCTitle: Recordset-Related Error Information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62f9a6d235b6c06ad8e7fa49d7b89960fd1ad2b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464269"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="f30c8-102">Informações sobre erros relacionados a recordsets</span><span class="sxs-lookup"><span data-stu-id="f30c8-102">Recordset-Related Error Information</span></span>


<span data-ttu-id="f30c8-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f30c8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f30c8-104">Durante o processamento em lote, a propriedade **Status** do objeto **Recordset** fornece informações sobre os registros individuais no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f30c8-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="f30c8-105">Antes de ocorrer uma atualização em lote, a propriedade **Status** do **Recordset** reflete informações sobre os registros a serem adicionados, alterados e excluídos.</span><span class="sxs-lookup"><span data-stu-id="f30c8-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="f30c8-106">Depois que **UpdateBatch** tiver sido chamado, a propriedade **Status** indicará o êxito ou a falha da operação.</span><span class="sxs-lookup"><span data-stu-id="f30c8-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="f30c8-107">Conforme você se move de registro em registro no **Recordset,** o valor da propriedade **Status** é alterado para descrever o status do registro atual.</span><span class="sxs-lookup"><span data-stu-id="f30c8-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

