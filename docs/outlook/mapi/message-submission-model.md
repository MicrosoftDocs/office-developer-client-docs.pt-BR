---
title: Modelo de envio de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768146"
---
# <a name="message-submission-model"></a><span data-ttu-id="e7de1-103">Modelo de envio de mensagens</span><span class="sxs-lookup"><span data-stu-id="e7de1-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="e7de1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7de1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7de1-105">Envio de mensagem é realizado através de uma série de chamadas do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e7de1-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="e7de1-106">As chamadas são sequenciadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e7de1-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="e7de1-107">O MAPI spooler chama [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passando um [IMessage: IMAPIProp](imessageimapiprop.md) instância, para começar o processo.</span><span class="sxs-lookup"><span data-stu-id="e7de1-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="e7de1-108">O provedor de transporte, em seguida, coloca um valor de referência — um identificador definido pelo transporte usada em futuras referências a esta mensagem — no local referenciado na **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="e7de1-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="e7de1-109">O provedor de transporte acessa os dados de mensagem usando a instância **IMessage** passada.</span><span class="sxs-lookup"><span data-stu-id="e7de1-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="e7de1-110">Para cada destinatário no passado **IMessage** para o qual ela aceita a responsabilidade, o provedor de transporte define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) e, em seguida, retorna.</span><span class="sxs-lookup"><span data-stu-id="e7de1-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="e7de1-111">Provedor de transporte que pode usar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar se ele reconhece quaisquer destinatários que não possam ser entregues, ou para criar um relatório de entrega padrão.</span><span class="sxs-lookup"><span data-stu-id="e7de1-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="e7de1-112">**StatusRecips** é uma conveniência para provedores de transporte que determinou que alguns dos destinatários não podem ser entregues em ou que tenha recebido informações de entrega de seu sistema de mensagens subjacente que talvez o aplicativo cliente ou de usuário Encontre útil.</span><span class="sxs-lookup"><span data-stu-id="e7de1-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="e7de1-113">Chamada do spooler MAPI para [IXPLogon::EndMessage](ixplogon-endmessage.md) é o final responsabilidade início da mensagem do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e7de1-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="e7de1-114">O MAPI spooler pode usar [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para cancelar durante as chamadas **SubmitMessage** ou **EndMessage** de processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e7de1-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

