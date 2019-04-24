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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321543"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="fcfd5-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="fcfd5-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="fcfd5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcfd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcfd5-105">Copia a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="fcfd5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcfd5-106">Parameters</span></span>

 <span data-ttu-id="fcfd5-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="fcfd5-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="fcfd5-108">no Um ponteiro para a pasta onde a mensagem deve ser copiada.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcfd5-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fcfd5-109">Return value</span></span>

<span data-ttu-id="fcfd5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcfd5-110">S_OK</span></span> 
  
> <span data-ttu-id="fcfd5-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fcfd5-112">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="fcfd5-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="fcfd5-113">A operação não é suportada por este site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcfd5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcfd5-114">Remarks</span></span>

<span data-ttu-id="fcfd5-115">Os objetos Form chamam o método **IMAPIMessageSite:: CopyMessage** para copiar a mensagem atual para uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="fcfd5-116">**CopyMessage** não altera a mensagem que está sendo exibida para o usuário e nenhuma interface para a mensagem recém-criada é retornada ao formulário.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fcfd5-117">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="fcfd5-117">Notes to implementers</span></span>

<span data-ttu-id="fcfd5-118">Uma implementação típica do método **CopyMessage** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="fcfd5-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="fcfd5-119">Cria uma nova mensagem para a mensagem atual a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="fcfd5-120">Chama o método [IPersistMessage:: Save](ipersistmessage-save.md) com um ponteiro para a nova mensagem no parâmetro _PMessage_ e false no parâmetro _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="fcfd5-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="fcfd5-121">Chama o método [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) , passando NULL no parâmetro _PMessage_ .</span><span class="sxs-lookup"><span data-stu-id="fcfd5-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="fcfd5-122">Chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="fcfd5-123">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulários MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="fcfd5-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fcfd5-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fcfd5-124">MFCMAPI reference</span></span>

<span data-ttu-id="fcfd5-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fcfd5-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fcfd5-126">**File**</span></span>|<span data-ttu-id="fcfd5-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="fcfd5-127">**Function**</span></span>|<span data-ttu-id="fcfd5-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="fcfd5-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcfd5-129">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="fcfd5-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="fcfd5-130">CMyMAPIFormViewer:: CopyMessage</span><span class="sxs-lookup"><span data-stu-id="fcfd5-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="fcfd5-131">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="fcfd5-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcfd5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcfd5-132">See also</span></span>



[<span data-ttu-id="fcfd5-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="fcfd5-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="fcfd5-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="fcfd5-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="fcfd5-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="fcfd5-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="fcfd5-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcfd5-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="fcfd5-137">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fcfd5-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fcfd5-138">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="fcfd5-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

