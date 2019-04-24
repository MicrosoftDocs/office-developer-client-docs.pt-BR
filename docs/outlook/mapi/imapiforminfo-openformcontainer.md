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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342088"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="69ed5-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="69ed5-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="69ed5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69ed5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69ed5-105">Retorna um ponteiro para o contêiner de formulários no qual um determinado formulário é instalado.</span><span class="sxs-lookup"><span data-stu-id="69ed5-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="69ed5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69ed5-106">Parameters</span></span>

 <span data-ttu-id="69ed5-107">_ppformcontainer_</span><span class="sxs-lookup"><span data-stu-id="69ed5-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="69ed5-108">bota Um ponteiro para um ponteiro para o objeto contêiner Form retornado.</span><span class="sxs-lookup"><span data-stu-id="69ed5-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69ed5-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="69ed5-109">Return value</span></span>

<span data-ttu-id="69ed5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="69ed5-110">S_OK</span></span> 
  
> <span data-ttu-id="69ed5-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="69ed5-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69ed5-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ed5-112">See also</span></span>



[<span data-ttu-id="69ed5-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="69ed5-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

