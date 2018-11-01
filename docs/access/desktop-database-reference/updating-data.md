---
title: Atualizando dados (referência de banco de dados da área de trabalho do Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9202a81617f253477c9788055738eaa64e73322
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880478"
---
# <a name="updating-data"></a><span data-ttu-id="8e44c-102">Atualização de dados</span><span class="sxs-lookup"><span data-stu-id="8e44c-102">Updating Data</span></span>


<span data-ttu-id="8e44c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e44c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e44c-104">A atualização do comportamento e do recurso depende amplamente do modo Atualização (tipo de bloqueio), tipo de cursor e local do cursor.</span><span class="sxs-lookup"><span data-stu-id="8e44c-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="8e44c-p101">Use o método **Update** para salvar quaisquer alterações feitas no registro atual de um objeto **Recordset** desde a chamada do método **AddNew** ou desde a alteração de quaisquer valores de campo em um registro existente. O objeto **Recordset** deve oferecer suporte às atualizações.</span><span class="sxs-lookup"><span data-stu-id="8e44c-p101">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="8e44c-p102">Se o objeto **Recordset** oferecer suporte à atualização do lote, você poderá armazenar em cache várias alterações em um ou mais registros localmente até que você chame o método **UpdateBatch**. Se você estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método **Update** para salvar quaisquer alterações pendentes no registro atual antes de transmitir as alterações em lote para o provedor.</span><span class="sxs-lookup"><span data-stu-id="8e44c-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="8e44c-109">O registro atual permanece atual depois que você chama os métodos **Update** ou **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="8e44c-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="8e44c-110">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="8e44c-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="8e44c-111">Modo Imediato</span><span class="sxs-lookup"><span data-stu-id="8e44c-111">Immediate Mode</span></span>](immediate-mode.md)

- [<span data-ttu-id="8e44c-112">Processamento de transações</span><span class="sxs-lookup"><span data-stu-id="8e44c-112">Transaction Processing</span></span>](transaction-processing.md)

- [<span data-ttu-id="8e44c-113">Modo de lotes (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e44c-113">Batch Mode (ADO)</span></span>](batch-mode.md)

