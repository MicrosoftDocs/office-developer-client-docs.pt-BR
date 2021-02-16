---
title: Excluindo um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428120"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="40ddb-103">Excluindo um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="40ddb-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="40ddb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="40ddb-105">**Para excluir um serviço de mensagens de um perfil**</span><span class="sxs-lookup"><span data-stu-id="40ddb-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="40ddb-106">Chame **IMAPISession::GetMsgServiceTable** para acessar a tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="40ddb-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="40ddb-107">Localize a linha para o serviço de mensagens e passe sua coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) no parâmetro  _lpuid_ para [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="40ddb-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="40ddb-108">**DeleteMsgService** chama a função de ponto de entrada do serviço de mensagens com o  _parâmetro ulContext_ definido como MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="40ddb-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="40ddb-109">Os serviços de mensagens executam qualquer tarefa de limpeza neste momento antes que elas sejam removidas do perfil.</span><span class="sxs-lookup"><span data-stu-id="40ddb-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

