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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335757"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="f38de-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="f38de-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="f38de-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f38de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f38de-105">Cria um token numérico que o método [IMAPISession:: @ Form](imapisession-showform.md) usa para acessar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f38de-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="f38de-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f38de-106">Parameters</span></span>

 <span data-ttu-id="f38de-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f38de-107">_lpInterface_</span></span>
  
> <span data-ttu-id="f38de-108">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f38de-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="f38de-109">Passar \*\*\*\* resultados nulos na interface padrão ou [IMessage](imessageimapiprop.md), sendo usado.</span><span class="sxs-lookup"><span data-stu-id="f38de-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="f38de-110">O parâmetro _lpInterface_ deve ser **nulo** ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="f38de-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="f38de-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f38de-111">_lpMessage_</span></span>
  
> <span data-ttu-id="f38de-112">no Um ponteiro para a mensagem a ser exibida no formulário.</span><span class="sxs-lookup"><span data-stu-id="f38de-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="f38de-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="f38de-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="f38de-114">bota Um ponteiro para um token de mensagem, que é usado pelo método **IMAPISession:: Form** para acessar a mensagem indicada por _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="f38de-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f38de-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f38de-115">Return value</span></span>

<span data-ttu-id="f38de-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f38de-116">S_OK</span></span> 
  
> <span data-ttu-id="f38de-117">A preparação do formulário foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f38de-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f38de-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f38de-118">Remarks</span></span>

<span data-ttu-id="f38de-119">O método **IMAPISession::P repareform** cria um token de mensagem para a mensagem indicada pelo parâmetro _lpMessage_ e chama o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f38de-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="f38de-120">Esse token é passado no parâmetro _ulMessageToken_ para **IMAPISession:: conform**.</span><span class="sxs-lookup"><span data-stu-id="f38de-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f38de-121">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f38de-121">Notes to callers</span></span>

<span data-ttu-id="f38de-122">Se a chamada para **PrepareForm** tiver êxito, libere a mensagem indicada por _lpMessage_ chamando seu método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) antes de chamar o **formulário**.</span><span class="sxs-lookup"><span data-stu-id="f38de-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="f38de-123">Falha ao liberar a mensagem antes de chamar o **formulário** pode causar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="f38de-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f38de-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f38de-124">MFCMAPI reference</span></span>

<span data-ttu-id="f38de-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f38de-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f38de-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f38de-126">**File**</span></span>|<span data-ttu-id="f38de-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="f38de-127">**Function**</span></span>|<span data-ttu-id="f38de-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f38de-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f38de-129">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f38de-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f38de-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="f38de-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="f38de-131">MFCMAPI usa o método **IMAPISession::P repareform** , juntamente com **IMAPISession::**, para exibir uma mensagem em um formulário de janela restrita.</span><span class="sxs-lookup"><span data-stu-id="f38de-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f38de-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f38de-132">See also</span></span>



[<span data-ttu-id="f38de-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="f38de-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="f38de-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f38de-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f38de-135">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f38de-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

