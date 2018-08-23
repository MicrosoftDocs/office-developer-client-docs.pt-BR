---
title: Tabelas de perfis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571476"
---
# <a name="profile-tables"></a><span data-ttu-id="b75ff-103">Tabelas de perfis</span><span class="sxs-lookup"><span data-stu-id="b75ff-103">Profile Tables</span></span>

  
  
<span data-ttu-id="b75ff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b75ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b75ff-105">A tabela de perfil lista informações sobre todos os perfis associados com um aplicativo cliente específico.</span><span class="sxs-lookup"><span data-stu-id="b75ff-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="b75ff-106">Há uma tabela de perfil para cada sessão, implementadas pelo MAPI para uso por clientes.</span><span class="sxs-lookup"><span data-stu-id="b75ff-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="b75ff-107">Os clientes de acessar a tabela de perfil chamando o método [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) .</span><span class="sxs-lookup"><span data-stu-id="b75ff-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="b75ff-108">A tabela de perfil é uma tabela estática.</span><span class="sxs-lookup"><span data-stu-id="b75ff-108">The profile table is a static table.</span></span> <span data-ttu-id="b75ff-109">Perfis que foram marcados para exclusão não são incluídos na tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="b75ff-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="b75ff-110">Como com a maioria das implementações de tabela, se **GetProfileTable** é chamado e não existem perfis disponíveis para o cliente, a tabela é criada com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="b75ff-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="b75ff-111">As seguintes propriedades compõem a coluna necessária definida nas tabelas de perfil:</span><span class="sxs-lookup"><span data-stu-id="b75ff-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="b75ff-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b75ff-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="b75ff-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b75ff-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b75ff-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="b75ff-114">See also</span></span>



[<span data-ttu-id="b75ff-115">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="b75ff-115">MAPI Tables</span></span>](mapi-tables.md)

