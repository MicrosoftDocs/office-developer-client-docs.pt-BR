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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412685"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="a03bf-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="a03bf-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="a03bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a03bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a03bf-105">Retorna a sessão MAPI na qual a mensagem atual foi criada ou aberta.</span><span class="sxs-lookup"><span data-stu-id="a03bf-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="a03bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a03bf-106">Parameters</span></span>

 <span data-ttu-id="a03bf-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="a03bf-107">_ppSession_</span></span>
  
> <span data-ttu-id="a03bf-108">[out] Um ponteiro para um ponteiro para o objeto de sessão retornado.</span><span class="sxs-lookup"><span data-stu-id="a03bf-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a03bf-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a03bf-109">Return value</span></span>

<span data-ttu-id="a03bf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a03bf-110">S_OK</span></span> 
  
> <span data-ttu-id="a03bf-111">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a03bf-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a03bf-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a03bf-112">S_FALSE</span></span> 
  
> <span data-ttu-id="a03bf-113">Não há sessão para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="a03bf-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a03bf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a03bf-114">Remarks</span></span>

<span data-ttu-id="a03bf-115">Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a03bf-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a03bf-116">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a03bf-116">MFCMAPI reference</span></span>

<span data-ttu-id="a03bf-117">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a03bf-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a03bf-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a03bf-118">**File**</span></span>|<span data-ttu-id="a03bf-119">**Função**</span><span class="sxs-lookup"><span data-stu-id="a03bf-119">**Function**</span></span>|<span data-ttu-id="a03bf-120">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="a03bf-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a03bf-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a03bf-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a03bf-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="a03bf-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="a03bf-123">MFCMAPI usa o método **IMAPIMessageSite::GetSession** para retornar o ponteiro de sessão atualmente armazenado em cache, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="a03bf-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a03bf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a03bf-124">See also</span></span>



[<span data-ttu-id="a03bf-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a03bf-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a03bf-126">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a03bf-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

