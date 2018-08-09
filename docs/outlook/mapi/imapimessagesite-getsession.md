---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d5d0f465ecdf4865ca86448448c56d54d5df4505
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767090"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="b2fc5-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="b2fc5-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="b2fc5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2fc5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2fc5-105">Retorna a sessão MAPI em que a mensagem atual foi criada ou aberta.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="b2fc5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2fc5-106">Parameters</span></span>

 <span data-ttu-id="b2fc5-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="b2fc5-107">_ppSession_</span></span>
  
> <span data-ttu-id="b2fc5-108">[out] Um ponteiro para um ponteiro para o objeto retornado de sessão.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2fc5-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b2fc5-109">Return value</span></span>

<span data-ttu-id="b2fc5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2fc5-110">S_OK</span></span> 
  
> <span data-ttu-id="b2fc5-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b2fc5-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b2fc5-112">S_FALSE</span></span> 
  
> <span data-ttu-id="b2fc5-113">Nenhuma sessão existe para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2fc5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2fc5-114">Remarks</span></span>

<span data-ttu-id="b2fc5-115">Para obter uma lista das interfaces que estão relacionados aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b2fc5-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b2fc5-116">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b2fc5-116">MFCMAPI reference</span></span>

<span data-ttu-id="b2fc5-117">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b2fc5-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-118">**File**</span></span>|<span data-ttu-id="b2fc5-119">**Function**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-119">**Function**</span></span>|<span data-ttu-id="b2fc5-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b2fc5-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2fc5-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b2fc5-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b2fc5-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="b2fc5-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="b2fc5-123">MFCMAPI usa o método **IMAPIMessageSite::GetSession** para retornar o ponteiro de sessão atualmente em cache, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="b2fc5-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2fc5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2fc5-124">See also</span></span>



[<span data-ttu-id="b2fc5-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2fc5-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="b2fc5-126">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b2fc5-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

