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
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594982"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="10599-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="10599-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="10599-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10599-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10599-105">Fornece detalhes que são exibidos na caixa de diálogo Enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="10599-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="10599-106">Se forem encontrados erros durante a sincronização, o provedor de armazenamento chama essa função.</span><span class="sxs-lookup"><span data-stu-id="10599-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="10599-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10599-107">Parameters</span></span>

 <span data-ttu-id="10599-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="10599-108">**hResult**</span></span>
  
> <span data-ttu-id="10599-109">O HRESULT do erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="10599-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="10599-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="10599-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="10599-111">Um ponteiro para a cadeia de caracteres associada ao erro a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="10599-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10599-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="10599-112">Return value</span></span>

<span data-ttu-id="10599-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="10599-113">S_OK</span></span> 
  
> <span data-ttu-id="10599-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="10599-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10599-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="10599-115">See also</span></span>



[<span data-ttu-id="10599-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10599-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

