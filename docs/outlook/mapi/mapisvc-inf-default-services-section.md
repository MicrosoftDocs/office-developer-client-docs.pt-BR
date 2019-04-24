---
title: Seção MapiSvc. inf [serviços padrão]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270067"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="82244-103">Seção MapiSvc. inf [serviços padrão]</span><span class="sxs-lookup"><span data-stu-id="82244-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="82244-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82244-105">A seção **[default Services]** lista todos os serviços de mensagem selecionados como serviços de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="82244-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="82244-106">Esses serviços de mensagens padrão são um subconjunto dos serviços de mensagens listados na seção **[serviços]** .</span><span class="sxs-lookup"><span data-stu-id="82244-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="82244-107">Quando um programa de configuração de perfil cria um perfil padrão, os serviços de mensagem nesta seção são incluídos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="82244-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="82244-108">As entradas usam o mesmo formato que as entradas na seção **[serviços]** , conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="82244-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="82244-109">**[Serviços padrão]**</span><span class="sxs-lookup"><span data-stu-id="82244-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="82244-110">__ =  nome da seção do serviço de mensagens nome do_serviço_</span><span class="sxs-lookup"><span data-stu-id="82244-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="82244-111">As entradas a seguir seriam incluídas na seção **[default Services]** para o MAPISVC. inf mostrado na ilustração anterior:</span><span class="sxs-lookup"><span data-stu-id="82244-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


