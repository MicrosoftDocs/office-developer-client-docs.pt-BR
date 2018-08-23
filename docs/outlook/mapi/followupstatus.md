---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568515"
---
# <a name="followupstatus"></a><span data-ttu-id="bc32e-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="bc32e-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="bc32e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc32e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc32e-105">Especifica os status de acompanhamento diferentes para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc32e-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bc32e-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bc32e-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="bc32e-107">Members</span><span class="sxs-lookup"><span data-stu-id="bc32e-107">Members</span></span>

 <span data-ttu-id="bc32e-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="bc32e-108">_flwupNone_</span></span>
  
> <span data-ttu-id="bc32e-109">Nenhum acompanhamento foi especificado.</span><span class="sxs-lookup"><span data-stu-id="bc32e-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="bc32e-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="bc32e-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="bc32e-111">A mensagem foi concluída.</span><span class="sxs-lookup"><span data-stu-id="bc32e-111">The message is complete.</span></span>
    
 <span data-ttu-id="bc32e-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="bc32e-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="bc32e-113">A mensagem é marcada para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="bc32e-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="bc32e-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="bc32e-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="bc32e-115">O número de status diferentes com suporte para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="bc32e-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc32e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc32e-116">See also</span></span>



[<span data-ttu-id="bc32e-117">Propriedade canônica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="bc32e-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

