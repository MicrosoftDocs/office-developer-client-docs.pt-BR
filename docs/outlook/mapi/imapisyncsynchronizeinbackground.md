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
ms.openlocfilehash: ee6fe07df894213331ab51f9abaa4008247dac07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568774"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="f4132-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="f4132-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="f4132-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4132-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f4132-105">Inicia uma sincronização.</span><span class="sxs-lookup"><span data-stu-id="f4132-105">Initiates a synchronization.</span></span> <span data-ttu-id="f4132-106">Esse método é chamado pelo Microsoft Outlook 2010 e o Microsoft Outlook 2013 e implementado por provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f4132-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="f4132-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4132-107">Parameters</span></span>

 <span data-ttu-id="f4132-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="f4132-108">_psibpb_</span></span>
  
> <span data-ttu-id="f4132-109">Informa o provedor do qual será sincronizado e fornece acesso a interfaces que podem ser usadas durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="f4132-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="f4132-110">Ele é uma estrutura [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="f4132-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4132-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f4132-111">Return value</span></span>

<span data-ttu-id="f4132-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4132-112">S_OK</span></span> 
  
> <span data-ttu-id="f4132-113">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f4132-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4132-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4132-114">See also</span></span>



[<span data-ttu-id="f4132-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4132-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="f4132-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="f4132-116">MAPISIB</span></span>](mapisib.md)

