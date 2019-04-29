---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424928"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="7b2cc-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="7b2cc-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="7b2cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b2cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b2cc-105">Fornece detalhes que são exibidos na caixa de diálogo enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="7b2cc-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="7b2cc-106">Se forem encontrados erros durante a sincronização, o provedor de repositório chamará essa função.</span><span class="sxs-lookup"><span data-stu-id="7b2cc-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="7b2cc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b2cc-107">Parameters</span></span>

 <span data-ttu-id="7b2cc-108">**And**</span><span class="sxs-lookup"><span data-stu-id="7b2cc-108">**hResult**</span></span>
  
> <span data-ttu-id="7b2cc-109">O HRESULT do erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="7b2cc-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="7b2cc-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="7b2cc-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="7b2cc-111">Um ponteiro para a cadeia de caracteres associada ao erro a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="7b2cc-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b2cc-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7b2cc-112">Return value</span></span>

<span data-ttu-id="7b2cc-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b2cc-113">S_OK</span></span> 
  
> <span data-ttu-id="7b2cc-114">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="7b2cc-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b2cc-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b2cc-115">See also</span></span>



[<span data-ttu-id="7b2cc-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b2cc-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

