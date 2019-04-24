---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349249"
---
# <a name="imessageopenattach"></a><span data-ttu-id="887d7-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="887d7-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="887d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="887d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="887d7-105">Abre um anexo.</span><span class="sxs-lookup"><span data-stu-id="887d7-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="887d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="887d7-106">Parameters</span></span>

 <span data-ttu-id="887d7-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="887d7-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="887d7-108">no Número de índice do anexo a ser aberto, conforme armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="887d7-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="887d7-109">Esse número de índice identifica exclusivamente o anexo na mensagem e é válido somente no contexto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="887d7-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="887d7-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="887d7-110">_lpInterface_</span></span>
  
> <span data-ttu-id="887d7-111">no Ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o anexo.</span><span class="sxs-lookup"><span data-stu-id="887d7-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="887d7-112">Passar resultados nulos na interface padrão do anexo ou **IAttach**, sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="887d7-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="887d7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="887d7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="887d7-114">no Bitmask de sinalizadores que controla como o anexo é aberto.</span><span class="sxs-lookup"><span data-stu-id="887d7-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="887d7-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="887d7-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="887d7-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="887d7-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="887d7-117">Solicita que o anexo seja aberto com as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="887d7-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="887d7-118">Por exemplo, se o cliente tiver permissão de leitura/gravação, o anexo deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o anexo deverá ser aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="887d7-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="887d7-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="887d7-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="887d7-120">Permite que o **OpenAttach** seja retornado com êxito, possivelmente antes que o anexo esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="887d7-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="887d7-121">Se o anexo não estiver disponível, fazer uma chamada subsequente para ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="887d7-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="887d7-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="887d7-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="887d7-123">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="887d7-123">Requests read/write permission.</span></span> <span data-ttu-id="887d7-124">Por padrão, os anexos são abertos com acesso somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="887d7-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="887d7-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="887d7-125">_lppAttach_</span></span>
  
> <span data-ttu-id="887d7-126">bota Ponteiro para um ponteiro para o anexo aberto.</span><span class="sxs-lookup"><span data-stu-id="887d7-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="887d7-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="887d7-127">Return value</span></span>

<span data-ttu-id="887d7-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="887d7-128">S_OK</span></span> 
  
> <span data-ttu-id="887d7-129">O anexo foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="887d7-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="887d7-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="887d7-130">Remarks</span></span>

<span data-ttu-id="887d7-131">O método **IMessage:: OpenAttach** abre o anexo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="887d7-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="887d7-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="887d7-132">Notes to callers</span></span>

<span data-ttu-id="887d7-133">Para abrir um anexo, você deve ter acesso ao número de anexo ou à propriedade **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="887d7-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="887d7-134">Chame [IMessage::](imessage-getattachmenttable.md) GetAttachmentTable para recuperar a tabela de anexos da mensagem e localizar a linha que representa o anexo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="887d7-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="887d7-135">ConFira como [abrir um anexo](opening-an-attachment.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="887d7-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="887d7-136">Não tente abrir um anexo várias vezes; os resultados são indefinidos e dependentes do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="887d7-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="887d7-137">Você pode solicitar que o anexo seja aberto no modo de leitura/gravação, em vez do modo somente leitura padrão.</span><span class="sxs-lookup"><span data-stu-id="887d7-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="887d7-138">No enTanto, se o anexo será realmente aberto no modo de leitura/gravação está no provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="887d7-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="887d7-139">Você pode tentar modificar o anexo, se preparar para lidar com uma possível falha ou verificar o nível de acesso que foi concedido ao recuperar a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) do anexo, se estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="887d7-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="887d7-140">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="887d7-140">MFCMAPI reference</span></span>

<span data-ttu-id="887d7-141">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="887d7-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="887d7-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="887d7-142">**File**</span></span>|<span data-ttu-id="887d7-143">**Função**</span><span class="sxs-lookup"><span data-stu-id="887d7-143">**Function**</span></span>|<span data-ttu-id="887d7-144">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="887d7-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="887d7-145">AttachmentsDlg. cpp usado para</span><span class="sxs-lookup"><span data-stu-id="887d7-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="887d7-146">CAttachmentsDlg:: OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="887d7-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="887d7-147">MFCMAPI usa o método **IMessage:: OpenAttach** para abrir objetos Attachment,</span><span class="sxs-lookup"><span data-stu-id="887d7-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="887d7-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="887d7-148">See also</span></span>



[<span data-ttu-id="887d7-149">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="887d7-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="887d7-150">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="887d7-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

