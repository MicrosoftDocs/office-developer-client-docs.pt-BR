---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592511"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="a77fc-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="a77fc-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="a77fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a77fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a77fc-105">Exclui um anexo.</span><span class="sxs-lookup"><span data-stu-id="a77fc-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a77fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a77fc-106">Parameters</span></span>

 <span data-ttu-id="a77fc-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="a77fc-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="a77fc-108">[in] Número de índice do anexo para excluir.</span><span class="sxs-lookup"><span data-stu-id="a77fc-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="a77fc-109">Esse é o valor da propriedade de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="a77fc-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="a77fc-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a77fc-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="a77fc-111">[in] Identificador da janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="a77fc-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="a77fc-112">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador ATTACH_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a77fc-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a77fc-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a77fc-113">_lpProgress_</span></span>
  
> <span data-ttu-id="a77fc-114">[in] Ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a77fc-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a77fc-115">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="a77fc-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="a77fc-116">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador ATTACH_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="a77fc-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a77fc-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a77fc-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a77fc-118">[in] Bitmask dos sinalizadores que controla a exibição de uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a77fc-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="a77fc-119">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="a77fc-119">The following flag can be set:</span></span>
    
<span data-ttu-id="a77fc-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a77fc-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="a77fc-121">Solicita a exibição de um indicador de progresso conforme continua a operação.</span><span class="sxs-lookup"><span data-stu-id="a77fc-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a77fc-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a77fc-122">Return value</span></span>

<span data-ttu-id="a77fc-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a77fc-123">S_OK</span></span> 
  
> <span data-ttu-id="a77fc-124">O anexo foi excluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="a77fc-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a77fc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a77fc-125">Remarks</span></span>

<span data-ttu-id="a77fc-126">O método **IMessage::DeleteAttach** exclui um anexo de dentro de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a77fc-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="a77fc-127">Um anexo excluído não é permanentemente excluído até que o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem foi chamado.</span><span class="sxs-lookup"><span data-stu-id="a77fc-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a77fc-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a77fc-128">Notes to callers</span></span>

<span data-ttu-id="a77fc-129">Antes de chamar **DeleteAttach**, chame o método de **IUnknown:: Release** para o anexo e cada um dos seus fluxos.</span><span class="sxs-lookup"><span data-stu-id="a77fc-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="a77fc-130">Como a exclusão de um anexo pode ser um processo demorado, **DeleteAttach** fornece o mecanismo que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a77fc-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="a77fc-131">Você pode solicitar a exibição de um indicador de progresso ao passar um ponteiro para sua [IMAPIProgress: IUnknown](imapiprogressiunknown.md) implementação ou NULL se você não tiver uma implementação.</span><span class="sxs-lookup"><span data-stu-id="a77fc-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="a77fc-132">Você também deve especificar um identificador de janela no parâmetro _ulUIParam_ e o sinalizador ATTACH_DIALOG no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a77fc-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a77fc-133">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a77fc-133">MFCMAPI reference</span></span>

<span data-ttu-id="a77fc-134">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a77fc-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a77fc-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a77fc-135">**File**</span></span>|<span data-ttu-id="a77fc-136">**Function**</span><span class="sxs-lookup"><span data-stu-id="a77fc-136">**Function**</span></span>|<span data-ttu-id="a77fc-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a77fc-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a77fc-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a77fc-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="a77fc-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a77fc-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a77fc-140">MFCMAPI usa o método **IMessage::DeleteAttach** para excluir o anexo selecionado.</span><span class="sxs-lookup"><span data-stu-id="a77fc-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a77fc-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a77fc-141">See also</span></span>



[<span data-ttu-id="a77fc-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a77fc-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a77fc-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a77fc-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="a77fc-144">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a77fc-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

