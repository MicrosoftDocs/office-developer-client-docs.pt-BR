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
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321363"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="32cc7-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="32cc7-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="32cc7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32cc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32cc7-105">Retorna uma interface de Gerenciador de formulários, que um servidor de formulário pode usar para abrir outro servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="32cc7-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="32cc7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32cc7-106">Parameters</span></span>

 <span data-ttu-id="32cc7-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="32cc7-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="32cc7-108">bota Um ponteiro para um ponteiro para a interface do Gerenciador de formulários retornado.</span><span class="sxs-lookup"><span data-stu-id="32cc7-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32cc7-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="32cc7-109">Return value</span></span>

<span data-ttu-id="32cc7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="32cc7-110">S_OK</span></span> 
  
> <span data-ttu-id="32cc7-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="32cc7-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32cc7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="32cc7-112">Remarks</span></span>

<span data-ttu-id="32cc7-113">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="32cc7-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="32cc7-114">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="32cc7-114">MFCMAPI reference</span></span>

<span data-ttu-id="32cc7-115">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="32cc7-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="32cc7-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="32cc7-116">**File**</span></span>|<span data-ttu-id="32cc7-117">**Função**</span><span class="sxs-lookup"><span data-stu-id="32cc7-117">**Function**</span></span>|<span data-ttu-id="32cc7-118">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="32cc7-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32cc7-119">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="32cc7-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="32cc7-120">CMyMAPIFormViewer:: getFormmanager</span><span class="sxs-lookup"><span data-stu-id="32cc7-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="32cc7-121">MFCMAPI usa o método **IMAPIMessageSite::** getformmanager para chamar [MAPIOpenFormMgr](mapiopenformmgr.md) e retornar os resultados da chamada.</span><span class="sxs-lookup"><span data-stu-id="32cc7-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32cc7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="32cc7-122">See also</span></span>



[<span data-ttu-id="32cc7-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="32cc7-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="32cc7-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32cc7-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="32cc7-125">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="32cc7-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="32cc7-126">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="32cc7-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

