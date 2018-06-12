---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767188"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="07888-103">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="07888-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="07888-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07888-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07888-105">Cria um token numérico que o método [IMAPISession:: ShowForm](imapisession-showform.md) usa para acessar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="07888-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="07888-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="07888-106">Parameters</span></span>

 <span data-ttu-id="07888-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="07888-107">_lpInterface_</span></span>
  
> <span data-ttu-id="07888-108">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="07888-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="07888-109">Passando **Nulo** resultados na interface padrão ou [IMessage](imessageimapiprop.md), sendo usados.</span><span class="sxs-lookup"><span data-stu-id="07888-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="07888-110">O parâmetro _lpInterface_ deve ser **nula** ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="07888-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="07888-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="07888-111">_lpMessage_</span></span>
  
> <span data-ttu-id="07888-112">[in] Um ponteiro para a mensagem a ser exibido no formulário.</span><span class="sxs-lookup"><span data-stu-id="07888-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="07888-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="07888-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="07888-114">[out] Um ponteiro para um token de mensagem, que é usado pelo método **IMAPISession:: ShowForm** para acessar a mensagem apontada pela _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="07888-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07888-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="07888-115">Return value</span></span>

<span data-ttu-id="07888-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="07888-116">S_OK</span></span> 
  
> <span data-ttu-id="07888-117">A preparação de formulário foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="07888-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07888-118">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="07888-118">Remarks</span></span>

<span data-ttu-id="07888-119">O método **PrepareForm** cria um token de mensagem para a mensagem apontado pelo parâmetro _lpMessage_ e chama o método de [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="07888-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="07888-120">Este token é passada no parâmetro _ulMessageToken_ para **IMAPISession:: ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="07888-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="07888-121">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="07888-121">Notes to callers</span></span>

<span data-ttu-id="07888-122">Se a chamada para **PrepareForm** for bem sucedido, libere a mensagem apontada pela _lpMessage_ chamando seu método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) antes de chamar **ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="07888-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="07888-123">Falha ao liberar a mensagem antes de chamar **ShowForm** pode causar vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="07888-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="07888-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="07888-124">MFCMAPI reference</span></span>

<span data-ttu-id="07888-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="07888-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="07888-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="07888-126">**File**</span></span>|<span data-ttu-id="07888-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="07888-127">**Function**</span></span>|<span data-ttu-id="07888-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="07888-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="07888-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="07888-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="07888-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="07888-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="07888-131">MFCMAPI usa o método **PrepareForm** , juntamente com **IMAPISession:: ShowForm**, exiba uma mensagem em um formulário restrito.</span><span class="sxs-lookup"><span data-stu-id="07888-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07888-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="07888-132">See also</span></span>



[<span data-ttu-id="07888-133">IMAPISession:: ShowForm</span><span class="sxs-lookup"><span data-stu-id="07888-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="07888-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="07888-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="07888-135">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="07888-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

