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
# <a name="followupstatus"></a><span data-ttu-id="f12da-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="f12da-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="f12da-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f12da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f12da-105">Especifica os status de acompanhamento diferentes para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f12da-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f12da-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f12da-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="f12da-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f12da-107">Members</span></span>

 <span data-ttu-id="f12da-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="f12da-108">_flwupNone_</span></span>
  
> <span data-ttu-id="f12da-109">Nenhum acompanhamento foi especificado.</span><span class="sxs-lookup"><span data-stu-id="f12da-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="f12da-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="f12da-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="f12da-111">A mensagem foi concluída.</span><span class="sxs-lookup"><span data-stu-id="f12da-111">The message is complete.</span></span>
    
 <span data-ttu-id="f12da-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="f12da-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="f12da-113">A mensagem é marcada para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="f12da-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="f12da-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="f12da-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="f12da-115">O número de status diferentes com suporte para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="f12da-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f12da-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f12da-116">See also</span></span>



[<span data-ttu-id="f12da-117">Propriedade canônico de PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="f12da-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

