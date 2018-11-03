---
title: Informações sobre erros relacionados a Recordsets
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b0dc56ba591263cd834e26ca4e89a371f272d5a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946465"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="4f93c-102">Informações sobre erros relacionados a Recordsets</span><span class="sxs-lookup"><span data-stu-id="4f93c-102">Recordset-related error information</span></span>

<span data-ttu-id="4f93c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f93c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f93c-104">Durante o processamento em lote, a propriedade **Status** do objeto **Recordset** fornece informações sobre os registros individuais no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4f93c-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="4f93c-105">Antes de ocorrer uma atualização em lote, a propriedade **Status** do **Recordset** reflete informações sobre os registros a serem adicionados, alterados e excluídos.</span><span class="sxs-lookup"><span data-stu-id="4f93c-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="4f93c-106">Depois que **UpdateBatch** tiver sido chamado, a propriedade **Status** indicará o êxito ou a falha da operação.</span><span class="sxs-lookup"><span data-stu-id="4f93c-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="4f93c-107">Conforme você se move de registro em registro no **Recordset,** o valor da propriedade **Status** é alterado para descrever o status do registro atual.</span><span class="sxs-lookup"><span data-stu-id="4f93c-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

