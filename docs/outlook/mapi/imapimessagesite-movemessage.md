---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382369"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="08f77-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="08f77-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="08f77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08f77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08f77-105">Move a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="08f77-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="08f77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08f77-106">Parameters</span></span>

 <span data-ttu-id="08f77-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="08f77-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="08f77-108">[in] Um ponteiro para a pasta onde a mensagem deve ser movido.</span><span class="sxs-lookup"><span data-stu-id="08f77-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="08f77-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="08f77-109">_pViewContext_</span></span>
  
> <span data-ttu-id="08f77-110">[in] Um ponteiro para um objeto de contexto do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="08f77-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="08f77-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="08f77-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="08f77-112">[in] Um ponteiro para uma estrutura de [Retangular](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho da janela e a posição atual do formulário.</span><span class="sxs-lookup"><span data-stu-id="08f77-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="08f77-113">A próxima forma exibida também usa esse retângulo de janela.</span><span class="sxs-lookup"><span data-stu-id="08f77-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08f77-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="08f77-114">Return value</span></span>

<span data-ttu-id="08f77-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="08f77-115">S_OK</span></span> 
  
> <span data-ttu-id="08f77-116">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="08f77-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="08f77-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="08f77-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="08f77-118">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="08f77-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08f77-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="08f77-119">Remarks</span></span>

<span data-ttu-id="08f77-120">Objetos de formulário chame o método **IMAPIMessageSite::MoveMessage** para mover a mensagem atual para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="08f77-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="08f77-121">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="08f77-121">Notes to implementers</span></span>

<span data-ttu-id="08f77-122">A implementação do Visualizador de um formulário de **MoveMessage** deve chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , passando o sinalizador VCDIR_MOVE, antes de realmente mover a mensagem para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="08f77-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="08f77-123">Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função do Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="08f77-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="08f77-124">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="08f77-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="08f77-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="08f77-125">Notes to callers</span></span>

<span data-ttu-id="08f77-126">Após o retorno de **MoveMessage**, formulários devem verificar se há uma mensagem atual e, em seguida, descartar sozinhos, se não houver nenhum.</span><span class="sxs-lookup"><span data-stu-id="08f77-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="08f77-127">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="08f77-127">MFCMAPI reference</span></span>

<span data-ttu-id="08f77-128">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="08f77-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="08f77-129">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="08f77-129">**File**</span></span>|<span data-ttu-id="08f77-130">**Função**</span><span class="sxs-lookup"><span data-stu-id="08f77-130">**Function**</span></span>|<span data-ttu-id="08f77-131">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="08f77-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="08f77-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="08f77-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="08f77-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="08f77-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="08f77-134">Não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="08f77-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08f77-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="08f77-135">See also</span></span>



[<span data-ttu-id="08f77-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="08f77-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="08f77-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08f77-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="08f77-138">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="08f77-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="08f77-139">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="08f77-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

