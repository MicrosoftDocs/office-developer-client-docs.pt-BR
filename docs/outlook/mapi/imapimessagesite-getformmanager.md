---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767094"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="7cf37-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="7cf37-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="7cf37-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cf37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cf37-105">Retorna uma interface de Gerenciador de formulário, que um servidor de formulário pode usar para abrir o outro servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="7cf37-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="7cf37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cf37-106">Parameters</span></span>

 <span data-ttu-id="7cf37-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="7cf37-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="7cf37-108">[out] Um ponteiro para um ponteiro para a interface do Gerenciador de formulário retornado.</span><span class="sxs-lookup"><span data-stu-id="7cf37-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7cf37-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7cf37-109">Return value</span></span>

<span data-ttu-id="7cf37-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cf37-110">S_OK</span></span> 
  
> <span data-ttu-id="7cf37-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7cf37-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cf37-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cf37-112">Remarks</span></span>

<span data-ttu-id="7cf37-113">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7cf37-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7cf37-114">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7cf37-114">MFCMAPI reference</span></span>

<span data-ttu-id="7cf37-115">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cf37-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7cf37-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7cf37-116">**File**</span></span>|<span data-ttu-id="7cf37-117">**Function**</span><span class="sxs-lookup"><span data-stu-id="7cf37-117">**Function**</span></span>|<span data-ttu-id="7cf37-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7cf37-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cf37-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7cf37-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7cf37-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="7cf37-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="7cf37-121">MFCMAPI usa o método **IMAPIMessageSite::GetFormManager** para chamar [MAPIOpenFormMgr](mapiopenformmgr.md) e apresentar os resultados dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="7cf37-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cf37-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cf37-122">See also</span></span>



[<span data-ttu-id="7cf37-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="7cf37-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="7cf37-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7cf37-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="7cf37-125">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7cf37-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7cf37-126">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="7cf37-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

