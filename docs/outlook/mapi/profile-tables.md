---
title: Tabelas de Perfis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424347"
---
# <a name="profile-tables"></a><span data-ttu-id="4dd46-103">Tabelas de Perfis</span><span class="sxs-lookup"><span data-stu-id="4dd46-103">Profile Tables</span></span>

  
  
<span data-ttu-id="4dd46-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dd46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dd46-105">A tabela de perfil lista informações sobre todos os perfis associados a um aplicativo cliente específico.</span><span class="sxs-lookup"><span data-stu-id="4dd46-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="4dd46-106">Há uma tabela de perfil para cada sessão, implementada pelo MAPI para uso por clientes.</span><span class="sxs-lookup"><span data-stu-id="4dd46-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="4dd46-107">Os clientes acessam a tabela de perfil chamando o [método IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md)</span><span class="sxs-lookup"><span data-stu-id="4dd46-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="4dd46-108">A tabela de perfil é uma tabela estática.</span><span class="sxs-lookup"><span data-stu-id="4dd46-108">The profile table is a static table.</span></span> <span data-ttu-id="4dd46-109">Perfis que foram marcados para exclusão não estão incluídos na tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="4dd46-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="4dd46-110">Assim como na maioria das implementações de tabela, se **GetProfileTable** for chamado e não houver perfis disponíveis para o cliente, a tabela será criada com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="4dd46-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="4dd46-111">As propriedades a seguir compom o conjunto de colunas necessário nas tabelas de perfil:</span><span class="sxs-lookup"><span data-stu-id="4dd46-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="4dd46-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4dd46-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="4dd46-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4dd46-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dd46-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dd46-114">See also</span></span>



[<span data-ttu-id="4dd46-115">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="4dd46-115">MAPI Tables</span></span>](mapi-tables.md)

