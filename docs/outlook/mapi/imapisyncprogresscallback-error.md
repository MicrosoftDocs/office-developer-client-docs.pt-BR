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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767295"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="17154-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="17154-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="17154-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17154-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17154-105">Fornece detalhes que são exibidos na caixa de diálogo Enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="17154-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="17154-106">Se forem encontrados erros durante a sincronização, o provedor de armazenamento chama essa função.</span><span class="sxs-lookup"><span data-stu-id="17154-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="17154-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17154-107">Parameters</span></span>

 <span data-ttu-id="17154-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="17154-108">**hResult**</span></span>
  
> <span data-ttu-id="17154-109">O HRESULT do erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="17154-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="17154-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="17154-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="17154-111">Um ponteiro para a cadeia de caracteres associada ao erro a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="17154-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17154-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="17154-112">Return value</span></span>

<span data-ttu-id="17154-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="17154-113">S_OK</span></span> 
  
> <span data-ttu-id="17154-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="17154-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17154-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="17154-115">See also</span></span>



[<span data-ttu-id="17154-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17154-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

