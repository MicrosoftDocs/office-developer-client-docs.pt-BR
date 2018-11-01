---
title: Propriedade IsolationLevel (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76978d33fc5f82c9b1f8137b64a663e7e95f2204
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883054"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="4134b-102">Propriedade IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="4134b-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="4134b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4134b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4134b-104">Indica o nível de isolamento de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4134b-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4134b-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="4134b-105">Settings and return values</span></span>

<span data-ttu-id="4134b-p101">Define ou retorna um valor [IsolationLevelEnum](isolationlevelenum.md). O padrão é **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="4134b-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4134b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4134b-108">Remarks</span></span>

<span data-ttu-id="4134b-p102">Use a propriedade **IsolationLevel** para definir o nível de isolamento de um objeto **Connection**. A configuração só entrará em vigor na próxima vez em que você chamar o método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se o nível de isolamento solicitado estiver indisponível, o provedor poderá retornar o maior nível seguinte de isolamento.</span><span class="sxs-lookup"><span data-stu-id="4134b-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="4134b-112">A propriedade **IsolationLevel** é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4134b-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="4134b-113">**Uso de serviço de dados remotos** Quando usado em um objeto de Conexão do cliente, a propriedade **IsolationLevel** pode ser definida somente para **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="4134b-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="4134b-p103">Como os usuários estão trabalhando com objetos **Recordset** desconectados em um cache do lado do cliente, pode haver problemas com vários usuários. Por exemplo, quando dois usuários diferentes tentam atualizar o mesmo registro, o Remote Data Service simplesmente permite que o usuário que atualizar o registro primeiro "ganhe". A solicitação de atualização do segundo usuário falhará, apresentando um erro.</span><span class="sxs-lookup"><span data-stu-id="4134b-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

