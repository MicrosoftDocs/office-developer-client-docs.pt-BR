---
title: Definindo um perfil padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439811"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="5511a-103">Definindo um perfil padrão</span><span class="sxs-lookup"><span data-stu-id="5511a-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="5511a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5511a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5511a-105">O perfil padrão é o perfil que será usado se você não especificar explicitamente um na chamada para [MAPILogonEx](mapilogonex.md), definindo, em vez disso, o MAPI_USE_DEFAULT sinalizador.</span><span class="sxs-lookup"><span data-stu-id="5511a-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="5511a-106">**Para estabelecer um perfil padrão**</span><span class="sxs-lookup"><span data-stu-id="5511a-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="5511a-107">Chame a [função MAPIAdminProfiles](mapiadminprofiles.md) para recuperar um ponteiro da interface **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="5511a-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="5511a-108">Chame [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="5511a-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="5511a-109">**SetDefaultProfile** define a **propriedade PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para o novo perfil padrão e remove a configuração do perfil padrão anterior.</span><span class="sxs-lookup"><span data-stu-id="5511a-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

