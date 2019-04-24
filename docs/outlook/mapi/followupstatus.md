---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327521"
---
# <a name="followupstatus"></a><span data-ttu-id="3aa2f-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="3aa2f-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="3aa2f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3aa2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3aa2f-105">Especifica os diferentes status de acompanhamento de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3aa2f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3aa2f-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="3aa2f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3aa2f-107">Members</span></span>

 <span data-ttu-id="3aa2f-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="3aa2f-108">_flwupNone_</span></span>
  
> <span data-ttu-id="3aa2f-109">Nenhum acompanhamento foi especificado.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="3aa2f-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="3aa2f-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="3aa2f-111">A mensagem está concluída.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-111">The message is complete.</span></span>
    
 <span data-ttu-id="3aa2f-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="3aa2f-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="3aa2f-113">A mensagem está marcada para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="3aa2f-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="3aa2f-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="3aa2f-115">O número de status diferentes suportados para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="3aa2f-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3aa2f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aa2f-116">See also</span></span>



[<span data-ttu-id="3aa2f-117">Propriedade canônica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="3aa2f-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

