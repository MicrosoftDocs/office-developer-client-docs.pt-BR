---
title: Copiar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766300"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="6f402-103">Copiar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="6f402-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="6f402-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f402-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="6f402-105">**Para copiar um serviço de mensagem para um perfil**</span><span class="sxs-lookup"><span data-stu-id="6f402-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="6f402-106">Chame [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="6f402-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="6f402-107">Quando um serviço de mensagem é copiado, a nova instância do serviço é configurada exatamente da mesma maneira que o original.</span><span class="sxs-lookup"><span data-stu-id="6f402-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="6f402-108">Em alguns casos, **CopyMsgService** retorna o erro MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="6f402-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="6f402-109">A causa mais comum de retorno este erro é um serviço de mensagem que não permita a mesmo a ser duplicado.</span><span class="sxs-lookup"><span data-stu-id="6f402-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

