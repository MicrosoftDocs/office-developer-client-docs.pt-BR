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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767089"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="f6c8f-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="f6c8f-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="f6c8f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6c8f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6c8f-105">Move a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="f6c8f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f6c8f-106">Parameters</span></span>

 <span data-ttu-id="f6c8f-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="f6c8f-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="f6c8f-108">[in] Um ponteiro para a pasta onde a mensagem deve ser movido.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="f6c8f-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="f6c8f-109">_pViewContext_</span></span>
  
> <span data-ttu-id="f6c8f-110">[in] Um ponteiro para um objeto de contexto do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="f6c8f-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="f6c8f-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="f6c8f-112">[in] Um ponteiro para uma estrutura de [Retangular](http://msdn.microsoft.com/pt-br/library/dd162897%28VS.85%29.aspx) que contém o tamanho da janela e a posição atual do formulário.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-112">[in] A pointer to a [RECT](http://msdn.microsoft.com/pt-br/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="f6c8f-113">A próxima forma exibida também usa esse retângulo de janela.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6c8f-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f6c8f-114">Return value</span></span>

<span data-ttu-id="f6c8f-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6c8f-115">S_OK</span></span> 
  
> <span data-ttu-id="f6c8f-116">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f6c8f-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f6c8f-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f6c8f-118">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6c8f-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="f6c8f-119">Remarks</span></span>

<span data-ttu-id="f6c8f-120">Objetos de formulário chame o método **IMAPIMessageSite::MoveMessage** para mover a mensagem atual para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f6c8f-121">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="f6c8f-121">Notes to implementers</span></span>

<span data-ttu-id="f6c8f-122">A implementação do Visualizador de um formulário de **MoveMessage** deve chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , passando o sinalizador VCDIR_MOVE, antes de realmente mover a mensagem para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="f6c8f-123">Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função do Windows [GetWindowRect](http://msdn.microsoft.com/pt-br/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="f6c8f-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/pt-br/library/ms633519) function.</span></span> 
  
<span data-ttu-id="f6c8f-124">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f6c8f-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6c8f-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f6c8f-125">Notes to callers</span></span>

<span data-ttu-id="f6c8f-126">Após o retorno de **MoveMessage**, formulários devem verificar se há uma mensagem atual e, em seguida, descartar sozinhos, se não houver nenhum.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6c8f-127">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6c8f-127">MFCMAPI reference</span></span>

<span data-ttu-id="f6c8f-128">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6c8f-129">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f6c8f-129">**File**</span></span>|<span data-ttu-id="f6c8f-130">**Function**</span><span class="sxs-lookup"><span data-stu-id="f6c8f-130">**Function**</span></span>|<span data-ttu-id="f6c8f-131">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f6c8f-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6c8f-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f6c8f-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f6c8f-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="f6c8f-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="f6c8f-134">Não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="f6c8f-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6c8f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6c8f-135">See also</span></span>



[<span data-ttu-id="f6c8f-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f6c8f-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="f6c8f-137">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6c8f-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f6c8f-138">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f6c8f-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f6c8f-139">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="f6c8f-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

