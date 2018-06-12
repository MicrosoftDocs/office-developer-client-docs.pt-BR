---
title: IMAPIFormInfoOpenFormContainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f6461a1e47437c5d0c2c422d727e2b00819629b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767028"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="0a8bc-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="0a8bc-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="0a8bc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a8bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a8bc-105">Retorna um ponteiro para o contêiner de formulário na qual um determinado formulário está instalado.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="0a8bc-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0a8bc-106">Parameters</span></span>

 <span data-ttu-id="0a8bc-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="0a8bc-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="0a8bc-108">[out] Um ponteiro para um ponteiro para o objeto de contêiner do formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0a8bc-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0a8bc-109">Return value</span></span>

<span data-ttu-id="0a8bc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a8bc-110">S_OK</span></span> 
  
> <span data-ttu-id="0a8bc-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a8bc-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a8bc-112">See also</span></span>



[<span data-ttu-id="0a8bc-113">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0a8bc-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

