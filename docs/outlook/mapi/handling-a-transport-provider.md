---
title: Manipular um provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567948"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="9af13-103">Manipular um provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="9af13-103">Handling a transport provider</span></span>
  
<span data-ttu-id="9af13-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9af13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9af13-105">Os clientes se comuniquem com provedores de transporte por meio de objetos de status fornecidos por provedores de transporte e o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="9af13-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="9af13-106">Clientes acessam objetos de status chamando [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="9af13-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="9af13-107">Objetos de status implementar o [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface, que tem métodos para configurando provedores, liberação de entrada e saída da mensagem filas, senhas de configuração e validação de estado.</span><span class="sxs-lookup"><span data-stu-id="9af13-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="9af13-108">Para obter mais informações sobre objetos de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9af13-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="9af13-109">[Enviar ou receber uma mensagem sob demanda](sending-or-receiving-a-message-on-demand.md): descreve como enviar ou receber uma mensagem sob demanda.</span><span class="sxs-lookup"><span data-stu-id="9af13-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="9af13-110">[Ordem de transporte de configuração](setting-transport-order.md): descreve como definir a ordem de transporte.</span><span class="sxs-lookup"><span data-stu-id="9af13-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="9af13-111">[Reconfiguração de um provedor de transporte](reconfiguring-a-transport-provider.md): descreve como reconfigurar um provedor de transporte e as propriedades que estão disponíveis para definir.</span><span class="sxs-lookup"><span data-stu-id="9af13-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

