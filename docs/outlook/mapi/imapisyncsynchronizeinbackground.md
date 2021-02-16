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
description: 'Última modificação: 26 de junho de 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426853"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="20953-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="20953-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="20953-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20953-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="20953-105">Inicia uma sincronização.</span><span class="sxs-lookup"><span data-stu-id="20953-105">Initiates a synchronization.</span></span> <span data-ttu-id="20953-106">Esse método é chamado pelo Microsoft Outlook 2010 e pelo Microsoft Outlook 2013 e implementado pelos provedores de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="20953-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="20953-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20953-107">Parameters</span></span>

 <span data-ttu-id="20953-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="20953-108">_psibpb_</span></span>
  
> <span data-ttu-id="20953-109">Informa o provedor sobre o que será sincronizado e dá acesso a interfaces que podem ser usadas durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="20953-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="20953-110">É uma estrutura [MAPISIB.](mapisib.md)</span><span class="sxs-lookup"><span data-stu-id="20953-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20953-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20953-111">Return value</span></span>

<span data-ttu-id="20953-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="20953-112">S_OK</span></span> 
  
> <span data-ttu-id="20953-113">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="20953-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20953-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="20953-114">See also</span></span>



[<span data-ttu-id="20953-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20953-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="20953-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="20953-116">MAPISIB</span></span>](mapisib.md)

