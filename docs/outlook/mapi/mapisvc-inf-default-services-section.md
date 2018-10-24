---
title: Seção MapiSvc.inf [Serviços padrão]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573142"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="2d124-103">Seção MapiSvc.inf [Serviços padrão]</span><span class="sxs-lookup"><span data-stu-id="2d124-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="2d124-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d124-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d124-105">A seção **[Padrão serviços]** lista todos os serviços de mensagem que são selecionados como serviços de mensagem padrão.</span><span class="sxs-lookup"><span data-stu-id="2d124-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="2d124-106">Esses serviços de mensagem padrão são um subconjunto dos serviços de mensagem listadas na seção **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="2d124-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="2d124-107">Quando um programa de configuração do perfil cria um perfil padrão, os serviços de mensagem nesta seção são incluídos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2d124-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="2d124-108">As entradas de usam o mesmo formato como entradas na seção **[Services]** , como mostrado seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d124-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="2d124-109">**[Padrão Services]**</span><span class="sxs-lookup"><span data-stu-id="2d124-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="2d124-110">_nome da seção do serviço de mensagem_ =  _nome do serviço de mensagem_</span><span class="sxs-lookup"><span data-stu-id="2d124-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="2d124-111">As entradas a seguir seriam incluídas na seção **[Services Default]** para o Mapisvc mostrado na ilustração anterior:</span><span class="sxs-lookup"><span data-stu-id="2d124-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


