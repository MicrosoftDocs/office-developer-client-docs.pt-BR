---
title: Excluindo um serviço de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766392"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="77836-103">Excluindo um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="77836-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="77836-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77836-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="77836-105">**Para excluir um serviço de mensagem de um perfil**</span><span class="sxs-lookup"><span data-stu-id="77836-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="77836-106">Chame **IMAPISession::GetMsgServiceTable** para acessar a tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="77836-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="77836-107">Localize a linha para o serviço de mensagem e passar uma coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) no parâmetro _lpuid_ para [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="77836-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="77836-108">**DeleteMsgService** chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="77836-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="77836-109">Serviços de mensagem executam qualquer tarefas de limpeza neste momento antes de serem removidos do perfil.</span><span class="sxs-lookup"><span data-stu-id="77836-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

