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
ms.openlocfilehash: 9f09f29d67bff6588c826b92d93aead491510cef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574815"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="e1553-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="e1553-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="e1553-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1553-105">Retorna o contexto de modo de exibição atual para o formulário.</span><span class="sxs-lookup"><span data-stu-id="e1553-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="e1553-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1553-106">Parameters</span></span>

 <span data-ttu-id="e1553-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="e1553-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="e1553-108">[out] Um ponteiro para um ponteiro para o contexto de exibição do formulário.</span><span class="sxs-lookup"><span data-stu-id="e1553-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1553-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e1553-109">Return value</span></span>

<span data-ttu-id="e1553-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1553-110">S_OK</span></span> 
  
> <span data-ttu-id="e1553-111">Contexto de modo de exibição atual do formulário foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e1553-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="e1553-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e1553-112">S_FALSE</span></span> 
  
> <span data-ttu-id="e1553-113">Não há nenhum contexto de modo de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="e1553-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1553-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1553-114">Remarks</span></span>

<span data-ttu-id="e1553-115">Visualizadores de formulário chame **GetViewContext** para obter um ponteiro para o contexto de modo de exibição estabelecido em uma chamada anterior para [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="e1553-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="e1553-116">Se nenhuma chamada anterior foi feita para **SetViewContext**, **GetViewContext** define _ppViewContext_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="e1553-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e1553-117">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="e1553-117">Notes to implementers</span></span>

<span data-ttu-id="e1553-118">Copie o ponteiro de contexto do modo de exibição do formulário para o ponteiro transmitido pelo Visualizador formulário chamada no parâmetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="e1553-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="e1553-119">Se o formulário não terá um contexto de modo de exibição, defina _ppViewContext_ como NULL.</span><span class="sxs-lookup"><span data-stu-id="e1553-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1553-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1553-120">MFCMAPI reference</span></span>

<span data-ttu-id="e1553-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1553-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1553-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e1553-122">**File**</span></span>|<span data-ttu-id="e1553-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="e1553-123">**Function**</span></span>|<span data-ttu-id="e1553-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e1553-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1553-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e1553-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e1553-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="e1553-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="e1553-127">MFCMAPI usa o método **IMAPIForm::GetViewContext** para verificar se um formulário tem um contexto de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="e1553-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1553-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1553-128">See also</span></span>



[<span data-ttu-id="e1553-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1553-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="e1553-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1553-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="e1553-131">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e1553-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

