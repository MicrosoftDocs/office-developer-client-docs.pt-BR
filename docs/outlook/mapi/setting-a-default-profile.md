---
title: Configurar um perfil padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591769"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="969d6-103">Configurar um perfil padrão</span><span class="sxs-lookup"><span data-stu-id="969d6-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="969d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="969d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="969d6-105">O perfil padrão será o que é usado se você não especificar explicitamente um na chamada a [MAPILogonEx](mapilogonex.md), em vez disso, definindo o sinalizador MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="969d6-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="969d6-106">**Para estabelecer um perfil padrão**</span><span class="sxs-lookup"><span data-stu-id="969d6-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="969d6-107">Chame a função [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro de interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="969d6-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="969d6-108">Chame [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="969d6-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="969d6-109">**SetDefaultProfile** define a propriedade **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para o novo perfil padrão e remove a configuração de perfil padrão anterior.</span><span class="sxs-lookup"><span data-stu-id="969d6-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

