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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: abee768dd29cc807b605a7d13570a579cb271b2c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767365"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="451b5-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="451b5-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="451b5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="451b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="451b5-105">Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador.</span><span class="sxs-lookup"><span data-stu-id="451b5-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="451b5-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="451b5-106">Parameters</span></span>

 <span data-ttu-id="451b5-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="451b5-107">_pmvns_</span></span>
  
> <span data-ttu-id="451b5-108">[in] Ponteiro para um formulário avise o objeto coletor de eventos ou nulo.</span><span class="sxs-lookup"><span data-stu-id="451b5-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="451b5-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="451b5-109">Return value</span></span>

<span data-ttu-id="451b5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="451b5-110">S_OK</span></span> 
  
> <span data-ttu-id="451b5-111">O registro ou cancelamento de notificação de formulário foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="451b5-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="451b5-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="451b5-112">Remarks</span></span>

<span data-ttu-id="451b5-113">Objetos de formulário chame o método de **IMAPIViewContext::SetAdviseSink** para registrar-se para aprender sobre alterações no Visualizador do formulário ou cancelar um registro prévio.</span><span class="sxs-lookup"><span data-stu-id="451b5-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="451b5-114">Quando _pmvns_ estiver definido como nulo, o formulário deseja cancelar um registro.</span><span class="sxs-lookup"><span data-stu-id="451b5-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="451b5-115">Quando o coletor de eventos de aviso de pontos de _pmvns_ para um formulário válido, o formulário quer registrar para notificações futuras.</span><span class="sxs-lookup"><span data-stu-id="451b5-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="451b5-116">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="451b5-116">Notes to implementers</span></span>

<span data-ttu-id="451b5-117">Quando o **SetAdviseSink** inclui um formulário ponteiro coletor de eventos de aviso, mantenha uma referência a ele até que a outra chamada **SetAdviseSink** é feita de cancelar a notificação.</span><span class="sxs-lookup"><span data-stu-id="451b5-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="451b5-118">Envie uma notificação quando ocorre uma alteração no seu visualizador e ao carregar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="451b5-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="451b5-119">Para obter mais informações, consulte [enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="451b5-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="451b5-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="451b5-120">MFCMAPI reference</span></span>

<span data-ttu-id="451b5-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="451b5-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="451b5-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="451b5-122">**File**</span></span>|<span data-ttu-id="451b5-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="451b5-123">**Function**</span></span>|<span data-ttu-id="451b5-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="451b5-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="451b5-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="451b5-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="451b5-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="451b5-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="451b5-127">MFCMAPI implementa o método **IMAPIViewContext::SetAdviseSink** nessa função.</span><span class="sxs-lookup"><span data-stu-id="451b5-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="451b5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="451b5-128">See also</span></span>



[<span data-ttu-id="451b5-129">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="451b5-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

