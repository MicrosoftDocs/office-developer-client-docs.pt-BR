---
title: Modelo de envio de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356872"
---
# <a name="message-submission-model"></a><span data-ttu-id="ad211-103">Modelo de envio de mensagens</span><span class="sxs-lookup"><span data-stu-id="ad211-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="ad211-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad211-105">O envio da mensagem é realizado por uma série de chamadas do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ad211-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="ad211-106">As chamadas são sequenciadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ad211-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="ad211-107">O spooler MAPI chama [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), passando uma instância de [IMessage: IMAPIProp](imessageimapiprop.md) , para iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="ad211-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="ad211-108">O provedor de transporte, em seguida, coloca um valor de referência — um identificador definido pelo transporte usado em referências futuras a essa mensagem, no local mencionado no **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="ad211-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="ad211-109">O provedor de transporte acessa os dados da mensagem usando a instância do **IMessage** aprovada.</span><span class="sxs-lookup"><span data-stu-id="ad211-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="ad211-110">Para cada destinatário no **IMessage** passado para o qual ele aceita responsabilidades, o provedor de transporte define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) e, em seguida, retorna.</span><span class="sxs-lookup"><span data-stu-id="ad211-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="ad211-111">O provedor de transporte pode usar o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para indicar se ele reconhece qualquer destinatário que não possa ser entregue ou para criar um relatório de entrega padrão.</span><span class="sxs-lookup"><span data-stu-id="ad211-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="ad211-112">**StatusRecips** é uma conveniência para provedores de transporte que determinaram que alguns dos destinatários não podem ser entregues ou que receberam informações de entrega de seu sistema de mensagens subjacente que o usuário ou aplicativo cliente pode ser útil.</span><span class="sxs-lookup"><span data-stu-id="ad211-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="ad211-113">A chamada do spooler MAPI para [IXPLogon:: endmessage](ixplogon-endmessage.md) é a responsabilidade final da entrega da mensagem do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ad211-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="ad211-114">O MAPI spooler pode usar [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) para cancelar o processamento de mensagens durante as chamadas de **SubmitMessage** ou endmessage. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ad211-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

