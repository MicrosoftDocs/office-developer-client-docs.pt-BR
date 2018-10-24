---
title: Copiar um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564931"
---
# <a name="copying-a-profile"></a><span data-ttu-id="217a5-103">Copiar um perfil</span><span class="sxs-lookup"><span data-stu-id="217a5-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="217a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="217a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="217a5-105">Uma maneira para criar um perfil é a cópia de um perfil existente e alterar os serviços de mensagem necessárias e os provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="217a5-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="217a5-106">Copiar um perfil envolve o uso de um objeto de administração de perfil, fornecido pelo MAPI por meio da função [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="217a5-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="217a5-107">**Para copiar um perfil**</span><span class="sxs-lookup"><span data-stu-id="217a5-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="217a5-108">Chame **MAPIAdminProfiles** para recuperar um ponteiro de interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="217a5-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="217a5-109">Chame [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para acessar a tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="217a5-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="217a5-110">Construa uma restrição de propriedade com uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="217a5-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="217a5-111">Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha apropriada na tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="217a5-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="217a5-112">Chame [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passando o valor da coluna **PR_DISPLAY_NAME** como o parâmetro _lpszOldProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="217a5-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

