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
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321438"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="f29c7-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="f29c7-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="f29c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f29c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f29c7-105">Retorna a sessão MAPI na qual a mensagem atual foi criada ou aberta.</span><span class="sxs-lookup"><span data-stu-id="f29c7-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="f29c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f29c7-106">Parameters</span></span>

 <span data-ttu-id="f29c7-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="f29c7-107">_ppSession_</span></span>
  
> <span data-ttu-id="f29c7-108">bota Um ponteiro para um ponteiro para o objeto Session retornado.</span><span class="sxs-lookup"><span data-stu-id="f29c7-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f29c7-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f29c7-109">Return value</span></span>

<span data-ttu-id="f29c7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f29c7-110">S_OK</span></span> 
  
> <span data-ttu-id="f29c7-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f29c7-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f29c7-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f29c7-112">S_FALSE</span></span> 
  
> <span data-ttu-id="f29c7-113">Nenhuma sessão existe para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="f29c7-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f29c7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f29c7-114">Remarks</span></span>

<span data-ttu-id="f29c7-115">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulários MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f29c7-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f29c7-116">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f29c7-116">MFCMAPI reference</span></span>

<span data-ttu-id="f29c7-117">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f29c7-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f29c7-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f29c7-118">**File**</span></span>|<span data-ttu-id="f29c7-119">**Função**</span><span class="sxs-lookup"><span data-stu-id="f29c7-119">**Function**</span></span>|<span data-ttu-id="f29c7-120">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f29c7-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f29c7-121">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="f29c7-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f29c7-122">CMyMAPIFormViewer:: GetSession</span><span class="sxs-lookup"><span data-stu-id="f29c7-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="f29c7-123">MFCMAPI usa o método **IMAPIMessageSite:: GetSession** para retornar o ponteiro de sessão atualmente em cache, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="f29c7-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f29c7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f29c7-124">See also</span></span>



[<span data-ttu-id="f29c7-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f29c7-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f29c7-126">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f29c7-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

