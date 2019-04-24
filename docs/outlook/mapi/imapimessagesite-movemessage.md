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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321361"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="d1765-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="d1765-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="d1765-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1765-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1765-105">Move a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="d1765-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="d1765-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1765-106">Parameters</span></span>

 <span data-ttu-id="d1765-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="d1765-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="d1765-108">no Um ponteiro para a pasta onde a mensagem deve ser movida.</span><span class="sxs-lookup"><span data-stu-id="d1765-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="d1765-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="d1765-109">_pViewContext_</span></span>
  
> <span data-ttu-id="d1765-110">no Um ponteiro para um objeto de contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="d1765-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="d1765-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="d1765-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="d1765-112">no Um ponteiro para uma estrutura de [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário atual.</span><span class="sxs-lookup"><span data-stu-id="d1765-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="d1765-113">O próximo formulário também usa este retângulo de janela.</span><span class="sxs-lookup"><span data-stu-id="d1765-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d1765-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d1765-114">Return value</span></span>

<span data-ttu-id="d1765-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1765-115">S_OK</span></span> 
  
> <span data-ttu-id="d1765-116">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d1765-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d1765-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d1765-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d1765-118">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d1765-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1765-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1765-119">Remarks</span></span>

<span data-ttu-id="d1765-120">Os objetos Form chamam o método **IMAPIMessageSite:: MoveMessage** para mover a mensagem atual para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="d1765-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d1765-121">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="d1765-121">Notes to implementers</span></span>

<span data-ttu-id="d1765-122">A implementação de um visualizador de formulários do **MoveMessage** deve chamar o método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) , passando o sinalizador VCDIR_MOVE, antes de mover a mensagem para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="d1765-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="d1765-123">Para obter a estrutura do **Rect** usada pela janela de um formulário, chame a função [GetWindowRect](https://msdn.microsoft.com/library/ms633519) do Windows.</span><span class="sxs-lookup"><span data-stu-id="d1765-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="d1765-124">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d1765-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1765-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d1765-125">Notes to callers</span></span>

<span data-ttu-id="d1765-126">Após o retorno de **MoveMessage**, os formulários devem verificar uma mensagem atual e, em seguida, descartar-se não existir nenhum.</span><span class="sxs-lookup"><span data-stu-id="d1765-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d1765-127">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d1765-127">MFCMAPI reference</span></span>

<span data-ttu-id="d1765-128">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1765-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d1765-129">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d1765-129">**File**</span></span>|<span data-ttu-id="d1765-130">**Função**</span><span class="sxs-lookup"><span data-stu-id="d1765-130">**Function**</span></span>|<span data-ttu-id="d1765-131">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="d1765-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1765-132">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="d1765-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d1765-133">CMyMAPIFormViewer:: MoveMessage</span><span class="sxs-lookup"><span data-stu-id="d1765-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="d1765-134">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="d1765-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1765-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1765-135">See also</span></span>



[<span data-ttu-id="d1765-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d1765-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="d1765-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1765-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d1765-138">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d1765-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d1765-139">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="d1765-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

