---
title: Modo em lotes (referência do banco de dados da área de trabalho do Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296875"
---
# <a name="batch-mode"></a><span data-ttu-id="b6d12-102">Modo em Lote</span><span class="sxs-lookup"><span data-stu-id="b6d12-102">Batch mode</span></span>

<span data-ttu-id="b6d12-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6d12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6d12-p101">O modo de processamento em lotes é efetivo quando a propriedade **LockType** está definida como **adLockBatchOptimistic** e a atualização em lotes tem o suporte do provedor. Certas configurações de tipo de bloqueio não estão disponíveis, dependendo do local do cursor. Por exemplo, um tipo de bloqueio pessimista não está disponível quando **CursorLocation** está definido como **adUseClient**. Por outro lado, um provedor pode não oferecer suporte para um bloqueio otimista em lotes quando o local do cursor é no servidor. Você deve usar a atualização em lotes somente com um cursor de conjunto de chaves ou estático.</span><span class="sxs-lookup"><span data-stu-id="b6d12-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="b6d12-p102">O método **UpdateBatch** é usado para enviar ao servidor as alterações de **Recordset** retidas no buffer de cópia, a fim de atualizar a fonte de dados. Na próxima seção, abriremos um **Recordset** no modo de processamento em lotes, faremos alterações no buffer de cópia e, em seguida, enviaremos as alterações para a fonte de dados usando uma chamada para **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="b6d12-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="b6d12-111">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b6d12-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="b6d12-112">Envio de atualizações: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="b6d12-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="b6d12-113">Filtragem de registros atualizados</span><span class="sxs-lookup"><span data-stu-id="b6d12-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="b6d12-114">Como lidar com atualizações com falhas</span><span class="sxs-lookup"><span data-stu-id="b6d12-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="b6d12-115">Detecção e solução de conflitos</span><span class="sxs-lookup"><span data-stu-id="b6d12-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="b6d12-116">Desconexão e reconexão do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="b6d12-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="b6d12-117">Atualização de resultados JOINed: tabela exclusiva</span><span class="sxs-lookup"><span data-stu-id="b6d12-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

