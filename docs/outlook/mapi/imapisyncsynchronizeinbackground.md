---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Modificado pela última vez: 26 de junho de 2012'
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767311"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="ffb49-103">IMAPISync: SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="ffb49-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="ffb49-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffb49-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="ffb49-105">Inicia uma sincronização.</span><span class="sxs-lookup"><span data-stu-id="ffb49-105">Initiates a synchronization.</span></span> <span data-ttu-id="ffb49-106">Esse método é chamado pelo Microsoft Outlook 2010 e o Microsoft Outlook 2013 e implementado por provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ffb49-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="ffb49-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ffb49-107">Parameters</span></span>

 <span data-ttu-id="ffb49-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="ffb49-108">_psibpb_</span></span>
  
> <span data-ttu-id="ffb49-109">Informa o provedor do qual será sincronizado e fornece acesso a interfaces que podem ser usadas durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="ffb49-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="ffb49-110">Ele é uma estrutura [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb49-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ffb49-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ffb49-111">Return value</span></span>

<span data-ttu-id="ffb49-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ffb49-112">S_OK</span></span> 
  
> <span data-ttu-id="ffb49-113">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ffb49-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffb49-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffb49-114">See also</span></span>



[<span data-ttu-id="ffb49-115">IMAPISync: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ffb49-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="ffb49-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="ffb49-116">MAPISIB</span></span>](mapisib.md)

