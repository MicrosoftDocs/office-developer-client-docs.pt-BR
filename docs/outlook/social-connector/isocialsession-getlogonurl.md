---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtém uma cadeia de caracteres que representa uma URL que é usada para apresentar um formulário baseado em navegador para o usuário durante a autenticação da Web.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427910"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="e227a-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="e227a-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="e227a-104">Obtém uma cadeia de caracteres que representa uma URL que é usada para apresentar um formulário baseado em navegador para o usuário durante a autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="e227a-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="e227a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e227a-105">Parameters</span></span>

<span data-ttu-id="e227a-106">_url_</span><span class="sxs-lookup"><span data-stu-id="e227a-106">_url_</span></span>
  
> <span data-ttu-id="e227a-107">[out] Uma cadeia de caracteres que contém uma URL para o formulário usado na autenticação da Web.</span><span class="sxs-lookup"><span data-stu-id="e227a-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e227a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e227a-108">Remarks</span></span>

<span data-ttu-id="e227a-109">Depois que o formulário é apresentado ao usuário, o método [ISocialSession::LogonWeb](isocialsession-logonweb.md) é chamado com uma cadeia de caracteres vazia para _o parâmetro connectIn._</span><span class="sxs-lookup"><span data-stu-id="e227a-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e227a-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="e227a-110">See also</span></span>

- [<span data-ttu-id="e227a-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e227a-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

