---
title: Seção MapiSvc.inf [Serviços padrão]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768018"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="4c54a-103">Seção MapiSvc.inf [Serviços padrão]</span><span class="sxs-lookup"><span data-stu-id="4c54a-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="4c54a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c54a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c54a-105">A seção **[Padrão serviços]** lista todos os serviços de mensagem que são selecionados como serviços de mensagem padrão.</span><span class="sxs-lookup"><span data-stu-id="4c54a-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="4c54a-106">Esses serviços de mensagem padrão são um subconjunto dos serviços de mensagem listadas na seção **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="4c54a-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="4c54a-107">Quando um programa de configuração do perfil cria um perfil padrão, os serviços de mensagem nesta seção são incluídos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4c54a-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="4c54a-108">As entradas de usam o mesmo formato como entradas na seção **[Services]** , como mostrado seguinte:</span><span class="sxs-lookup"><span data-stu-id="4c54a-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="4c54a-109">**[Padrão Services]**</span><span class="sxs-lookup"><span data-stu-id="4c54a-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="4c54a-110">_nome da seção do serviço de mensagem_ =  _nome do serviço de mensagem_</span><span class="sxs-lookup"><span data-stu-id="4c54a-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="4c54a-111">As entradas a seguir seriam incluídas na seção **[Services Default]** para o Mapisvc mostrado na ilustração anterior:</span><span class="sxs-lookup"><span data-stu-id="4c54a-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


