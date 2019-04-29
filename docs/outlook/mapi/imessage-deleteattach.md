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
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430704"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="f6e23-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="f6e23-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="f6e23-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6e23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6e23-105">Exclui um anexo.</span><span class="sxs-lookup"><span data-stu-id="f6e23-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f6e23-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6e23-106">Parameters</span></span>

 <span data-ttu-id="f6e23-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="f6e23-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="f6e23-108">no Número de índice do anexo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f6e23-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="f6e23-109">Este é o valor da propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="f6e23-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="f6e23-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f6e23-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="f6e23-111">no Manipulador para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.</span><span class="sxs-lookup"><span data-stu-id="f6e23-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="f6e23-112">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador ATTACH_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="f6e23-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f6e23-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f6e23-113">_lpProgress_</span></span>
  
> <span data-ttu-id="f6e23-114">no Ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="f6e23-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f6e23-115">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6e23-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="f6e23-116">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador ATTACH_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="f6e23-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="f6e23-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6e23-117">_ulFlags_</span></span>
  
> <span data-ttu-id="f6e23-118">no Bitmask de sinalizadores que controla a exibição de uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="f6e23-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="f6e23-119">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f6e23-119">The following flag can be set:</span></span>
    
<span data-ttu-id="f6e23-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f6e23-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="f6e23-121">Solicita a exibição de um indicador de progresso à medida que a operação prossegue.</span><span class="sxs-lookup"><span data-stu-id="f6e23-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6e23-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f6e23-122">Return value</span></span>

<span data-ttu-id="f6e23-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6e23-123">S_OK</span></span> 
  
> <span data-ttu-id="f6e23-124">O anexo foi excluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="f6e23-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6e23-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6e23-125">Remarks</span></span>

<span data-ttu-id="f6e23-126">O método **IMessage::D eleteattach** exclui um anexo de dentro de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6e23-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="f6e23-127">Um anexo excluído não é excluído permanentemente até que o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f6e23-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6e23-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f6e23-128">Notes to callers</span></span>

<span data-ttu-id="f6e23-129">Antes de chamar **DeleteAttach**, chame o método **IUnknown:: Release** para o anexo e cada um de seus fluxos.</span><span class="sxs-lookup"><span data-stu-id="f6e23-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="f6e23-130">Como a exclusão de um anexo pode ser um processo demorado, o **DeleteAttach** fornece o mecanismo que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="f6e23-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="f6e23-131">Você pode solicitar a exibição de um indicador de progresso passando um ponteiro para sua implementação [método imapiprogress: IUnknown](imapiprogressiunknown.md) ou nulo se não tiver uma implementação.</span><span class="sxs-lookup"><span data-stu-id="f6e23-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="f6e23-132">Você também deve especificar um identificador de janela no parâmetro _ulUIParam_ e o sinalizador ATTACH_DIALOG no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="f6e23-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6e23-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6e23-133">MFCMAPI reference</span></span>

<span data-ttu-id="f6e23-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6e23-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6e23-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f6e23-135">**File**</span></span>|<span data-ttu-id="f6e23-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="f6e23-136">**Function**</span></span>|<span data-ttu-id="f6e23-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f6e23-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6e23-138">AttachmentsDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="f6e23-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="f6e23-139">CAttachmentsDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="f6e23-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="f6e23-140">MFCMAPI usa o método **IMessage::D eleteattach** para excluir o anexo selecionado.</span><span class="sxs-lookup"><span data-stu-id="f6e23-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6e23-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6e23-141">See also</span></span>



[<span data-ttu-id="f6e23-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f6e23-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="f6e23-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f6e23-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="f6e23-144">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f6e23-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

