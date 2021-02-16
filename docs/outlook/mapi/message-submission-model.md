---
title: Modelo de envio de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421120"
---
# <a name="message-submission-model"></a><span data-ttu-id="9de4c-103">Modelo de envio de mensagem</span><span class="sxs-lookup"><span data-stu-id="9de4c-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="9de4c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9de4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9de4c-105">O envio de mensagens é realizado por uma série de chamadas do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9de4c-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="9de4c-106">As chamadas são sequenciadas da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="9de4c-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="9de4c-107">O spooler MAPI chama [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passando uma [IMessage : instância IMAPIProp,](imessageimapiprop.md) para iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="9de4c-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="9de4c-108">Em seguida, o provedor de transporte coloca um valor de referência — um identificador definido por transporte usado em referências futuras a essa mensagem — no local referenciado em **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="9de4c-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="9de4c-109">O provedor de transporte acessa os dados da mensagem usando a **instância IMessage** passada.</span><span class="sxs-lookup"><span data-stu-id="9de4c-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="9de4c-110">Para cada destinatário no **IMessage** passado para o qual ele aceita responsabilidade, o provedor de transporte define a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) e retorna.</span><span class="sxs-lookup"><span data-stu-id="9de4c-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="9de4c-111">O provedor de transporte pode usar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar se reconhece destinatários que não podem ser entregues ou para criar um relatório de entrega padrão.</span><span class="sxs-lookup"><span data-stu-id="9de4c-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="9de4c-112">**StatusRecips** é uma conveniência para provedores de transporte que determinaram que alguns dos destinatários não podem ser entregues ou que receberam informações de entrega de seu sistema de mensagens subjacente que o usuário ou aplicativo cliente pode achar útil.</span><span class="sxs-lookup"><span data-stu-id="9de4c-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="9de4c-113">A chamada do spooler MAPI para [IXPLogon::EndMessage](ixplogon-endmessage.md) é a entrega de responsabilidade final da mensagem do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9de4c-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="9de4c-114">O spooler MAPI pode usar [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para cancelar o processamento de mensagens durante as chamadas **SubmitMessage** ou **EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="9de4c-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

