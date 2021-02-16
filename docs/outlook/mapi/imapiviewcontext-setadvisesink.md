---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419391"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="ad288-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ad288-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="ad288-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad288-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad288-105">Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador.</span><span class="sxs-lookup"><span data-stu-id="ad288-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="ad288-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad288-106">Parameters</span></span>

 <span data-ttu-id="ad288-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="ad288-107">_pmvns_</span></span>
  
> <span data-ttu-id="ad288-108">[in] Ponteiro para um objeto sink de aconselhmento de formulário ou NULL.</span><span class="sxs-lookup"><span data-stu-id="ad288-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad288-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ad288-109">Return value</span></span>

<span data-ttu-id="ad288-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad288-110">S_OK</span></span> 
  
> <span data-ttu-id="ad288-111">O registro ou cancelamento para notificação de formulário foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ad288-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad288-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad288-112">Remarks</span></span>

<span data-ttu-id="ad288-113">Objetos de formulário chamam o método **IMAPIViewContext::SetAdviseSink** para se registrar para saber mais sobre alterações no visualizador de formulário ou cancelar um registro anterior.</span><span class="sxs-lookup"><span data-stu-id="ad288-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="ad288-114">Quando  _pmvns_ é definido como NULL, o formulário deseja cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="ad288-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="ad288-115">Quando  _pmvns aponta_ para um sink de aviso de formulário válido, o formulário deseja se registrar para notificações futuras.</span><span class="sxs-lookup"><span data-stu-id="ad288-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ad288-116">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ad288-116">Notes to implementers</span></span>

<span data-ttu-id="ad288-117">Quando **SetAdviseSink** inclui um ponteiro de pia de aviso de formulário, mantenha uma referência a ele até que outra chamada **SetAdviseSink** seja feita para cancelar a notificação.</span><span class="sxs-lookup"><span data-stu-id="ad288-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="ad288-118">Envie uma notificação quando ocorrer uma alteração no visualizador e quando você estiver carregando uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="ad288-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="ad288-119">Para obter mais informações, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="ad288-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad288-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ad288-120">MFCMAPI reference</span></span>

<span data-ttu-id="ad288-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad288-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad288-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ad288-122">**File**</span></span>|<span data-ttu-id="ad288-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="ad288-123">**Function**</span></span>|<span data-ttu-id="ad288-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ad288-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad288-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ad288-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ad288-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ad288-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="ad288-127">MFCMAPI implementa o **método IMAPIViewContext::SetAdviseSink** nesta função.</span><span class="sxs-lookup"><span data-stu-id="ad288-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad288-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad288-128">See also</span></span>



[<span data-ttu-id="ad288-129">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ad288-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

