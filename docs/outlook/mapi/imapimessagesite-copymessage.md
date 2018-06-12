---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5bf2ff74f6cda01608efd4b372aa4b03468c820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767073"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="0122c-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="0122c-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="0122c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0122c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0122c-105">Copia a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="0122c-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="0122c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0122c-106">Parameters</span></span>

 <span data-ttu-id="0122c-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="0122c-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="0122c-108">[in] Um ponteiro para a pasta onde a mensagem deve ser copiado.</span><span class="sxs-lookup"><span data-stu-id="0122c-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0122c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0122c-109">Return value</span></span>

<span data-ttu-id="0122c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0122c-110">S_OK</span></span> 
  
> <span data-ttu-id="0122c-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="0122c-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0122c-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0122c-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0122c-113">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0122c-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0122c-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0122c-114">Remarks</span></span>

<span data-ttu-id="0122c-115">Objetos de formulário chame o método **IMAPIMessageSite::CopyMessage** para copiar a mensagem atual para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="0122c-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="0122c-116">**CopyMessage** não altera a mensagem atualmente estiver sendo exibida ao usuário e nenhuma interface para a mensagem recém-criado é retornado ao formulário.</span><span class="sxs-lookup"><span data-stu-id="0122c-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0122c-117">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="0122c-117">Notes to implementers</span></span>

<span data-ttu-id="0122c-118">Uma implementação típica do método **CopyMessage** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0122c-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="0122c-119">Cria uma nova mensagem para a mensagem atual deve ser copiado para.</span><span class="sxs-lookup"><span data-stu-id="0122c-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="0122c-120">Chama o método [IPersistMessage::Save](ipersistmessage-save.md) com um ponteiro para a nova mensagem no parâmetro _pMessage_ e FALSE no parâmetro _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="0122c-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="0122c-121">Chama o método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) , passando NULL no parâmetro _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="0122c-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="0122c-122">Chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="0122c-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="0122c-123">Para obter uma lista das interfaces que estão relacionados aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0122c-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0122c-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0122c-124">MFCMAPI reference</span></span>

<span data-ttu-id="0122c-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0122c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0122c-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0122c-126">**File**</span></span>|<span data-ttu-id="0122c-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="0122c-127">**Function**</span></span>|<span data-ttu-id="0122c-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0122c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0122c-129">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0122c-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0122c-130">CMyMAPIFormViewer::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="0122c-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="0122c-131">Não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="0122c-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0122c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0122c-132">See also</span></span>



[<span data-ttu-id="0122c-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0122c-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="0122c-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="0122c-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="0122c-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="0122c-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="0122c-136">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0122c-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="0122c-137">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0122c-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0122c-138">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="0122c-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

