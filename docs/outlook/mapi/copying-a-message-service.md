---
title: Copiar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333051"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="a5371-103">Copiar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="a5371-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="a5371-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5371-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a5371-105">**Para copiar um serviço de mensagens para um perfil**</span><span class="sxs-lookup"><span data-stu-id="a5371-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="a5371-106">Chamar [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a5371-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="a5371-107">Quando um serviço de mensagens é copiado, a nova instância do serviço é configurada exatamente da mesma maneira que o original.</span><span class="sxs-lookup"><span data-stu-id="a5371-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="a5371-108">Às vezes **CopyMsgService** retorna o erro MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="a5371-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="a5371-109">A causa mais comum desse retorno de erro é um serviço de mensagens que não permite que ele próprio seja duplicado.</span><span class="sxs-lookup"><span data-stu-id="a5371-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

