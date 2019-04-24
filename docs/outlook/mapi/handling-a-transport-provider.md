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
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299493"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="013f2-103">Manipular um provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="013f2-103">Handling a transport provider</span></span>
  
<span data-ttu-id="013f2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="013f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="013f2-105">Os clientes se comunicam com provedores de transporte por meio de objetos de status fornecidos por provedores de transporte e pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="013f2-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="013f2-106">Os clientes acessam objetos de status chamando [IMAPISession::](imapisession-getstatustable.md) getstatustable para recuperar a tabela status.</span><span class="sxs-lookup"><span data-stu-id="013f2-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="013f2-107">Os objetos de status implementam a interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) , que tem métodos para configurar provedores, liberar filas de mensagens de entrada e de saída, definir senhas e validação de estado.</span><span class="sxs-lookup"><span data-stu-id="013f2-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="013f2-108">Para obter mais informações sobre objetos de status, consulte [tabela de status e objetos de status](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="013f2-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="013f2-109">[Enviando ou recebendo uma mensagem sob demanda](sending-or-receiving-a-message-on-demand.md): descreve como enviar ou receber uma mensagem sob demanda.</span><span class="sxs-lookup"><span data-stu-id="013f2-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="013f2-110">[Configuração da ordem de transporte](setting-transport-order.md): descreve como definir a ordem de transporte.</span><span class="sxs-lookup"><span data-stu-id="013f2-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="013f2-111">[Reconfiguração de um provedor de transporte](reconfiguring-a-transport-provider.md): descreve como reconfigurar um provedor de transporte e quais propriedades estão disponíveis para definir.</span><span class="sxs-lookup"><span data-stu-id="013f2-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

