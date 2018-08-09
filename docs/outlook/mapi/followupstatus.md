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
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766576"
---
# <a name="followupstatus"></a><span data-ttu-id="c6e42-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="c6e42-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="c6e42-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6e42-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6e42-105">Especifica os status de acompanhamento diferentes para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c6e42-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c6e42-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c6e42-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="c6e42-107">Members</span><span class="sxs-lookup"><span data-stu-id="c6e42-107">Members</span></span>

 <span data-ttu-id="c6e42-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="c6e42-108">_flwupNone_</span></span>
  
> <span data-ttu-id="c6e42-109">Nenhum acompanhamento foi especificado.</span><span class="sxs-lookup"><span data-stu-id="c6e42-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="c6e42-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="c6e42-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="c6e42-111">A mensagem foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c6e42-111">The message is complete.</span></span>
    
 <span data-ttu-id="c6e42-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="c6e42-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="c6e42-113">A mensagem é marcada para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="c6e42-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="c6e42-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="c6e42-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="c6e42-115">O número de status diferentes com suporte para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="c6e42-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6e42-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6e42-116">See also</span></span>



[<span data-ttu-id="c6e42-117">Propriedade canônica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="c6e42-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

