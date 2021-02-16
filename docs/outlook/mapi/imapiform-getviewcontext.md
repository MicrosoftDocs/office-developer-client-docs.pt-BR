---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430900"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="2fa76-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="2fa76-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="2fa76-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fa76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fa76-105">Retorna o contexto de exibição atual do formulário.</span><span class="sxs-lookup"><span data-stu-id="2fa76-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="2fa76-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fa76-106">Parameters</span></span>

 <span data-ttu-id="2fa76-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="2fa76-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="2fa76-108">[out] Um ponteiro para um ponteiro para o contexto de exibição do formulário.</span><span class="sxs-lookup"><span data-stu-id="2fa76-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2fa76-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2fa76-109">Return value</span></span>

<span data-ttu-id="2fa76-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fa76-110">S_OK</span></span> 
  
> <span data-ttu-id="2fa76-111">O contexto de exibição atual do formulário foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="2fa76-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="2fa76-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2fa76-112">S_FALSE</span></span> 
  
> <span data-ttu-id="2fa76-113">Não há contexto de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="2fa76-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2fa76-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fa76-114">Remarks</span></span>

<span data-ttu-id="2fa76-115">Visualizadores de formulário chamam **GetViewContext** para obter um ponteiro para o contexto de exibição estabelecido em uma chamada anterior para [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="2fa76-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="2fa76-116">Se nenhuma chamada anterior tiver sido feita para **SetViewContext**, **GetViewContext**  _definirá ppViewContext_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="2fa76-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2fa76-117">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="2fa76-117">Notes to implementers</span></span>

<span data-ttu-id="2fa76-118">Copie o ponteiro de contexto de exibição do formulário para o ponteiro passado pelo visualizador do formulário de chamada no _parâmetro ppViewContext._</span><span class="sxs-lookup"><span data-stu-id="2fa76-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="2fa76-119">Se o formulário não tiver um contexto de exibição, de definida  _ppViewContext_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="2fa76-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2fa76-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2fa76-120">MFCMAPI reference</span></span>

<span data-ttu-id="2fa76-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2fa76-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2fa76-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2fa76-122">**File**</span></span>|<span data-ttu-id="2fa76-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="2fa76-123">**Function**</span></span>|<span data-ttu-id="2fa76-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="2fa76-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2fa76-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2fa76-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2fa76-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="2fa76-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2fa76-127">MFCMAPI usa o **método IMAPIForm::GetViewContext** para verificar se um formulário tem um contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="2fa76-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2fa76-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fa76-128">See also</span></span>



[<span data-ttu-id="2fa76-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fa76-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="2fa76-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fa76-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="2fa76-131">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="2fa76-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

