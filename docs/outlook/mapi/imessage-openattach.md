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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767384"
---
# <a name="imessageopenattach"></a><span data-ttu-id="aa3ab-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="aa3ab-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="aa3ab-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa3ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa3ab-105">Abre um anexo.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="aa3ab-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="aa3ab-106">Parameters</span></span>

 <span data-ttu-id="aa3ab-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="aa3ab-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="aa3ab-108">[in] Número de índice do anexo seja aberto, conforme armazenado na propriedade de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="aa3ab-109">Esse número de índice exclusivamente identifica o anexo na mensagem e é válido apenas no contexto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="aa3ab-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="aa3ab-110">_lpInterface_</span></span>
  
> <span data-ttu-id="aa3ab-111">[in] Ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o anexo.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="aa3ab-112">Passagem nula resulta na interface padrão do anexo ou **IAttach**, sendo retornados.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="aa3ab-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa3ab-113">_ulFlags_</span></span>
  
> <span data-ttu-id="aa3ab-114">[in] Bitmask dos sinalizadores que controla como o anexo é aberto.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="aa3ab-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="aa3ab-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="aa3ab-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="aa3ab-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="aa3ab-117">Solicita que o anexo seja aberto com as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="aa3ab-118">Por exemplo, se o cliente tem a permissão de leitura/gravação, o anexo deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o anexo deve ser aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="aa3ab-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="aa3ab-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="aa3ab-120">Permite que **OpenAttach** retornar com êxito, possivelmente antes que o anexo seja totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="aa3ab-121">Se o anexo não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="aa3ab-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="aa3ab-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="aa3ab-123">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-123">Requests read/write permission.</span></span> <span data-ttu-id="aa3ab-124">Por padrão, anexos abertos com acesso somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="aa3ab-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="aa3ab-125">_lppAttach_</span></span>
  
> <span data-ttu-id="aa3ab-126">[out] Ponteiro para um ponteiro para abrir o anexo.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa3ab-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aa3ab-127">Return value</span></span>

<span data-ttu-id="aa3ab-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa3ab-128">S_OK</span></span> 
  
> <span data-ttu-id="aa3ab-129">O anexo foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa3ab-130">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="aa3ab-130">Remarks</span></span>

<span data-ttu-id="aa3ab-131">O método **IMessage::OpenAttach** abre o anexo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa3ab-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="aa3ab-132">Notes to callers</span></span>

<span data-ttu-id="aa3ab-133">Para abrir um anexo, você deve ter acesso ao seu número de anexos ou a propriedade **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="aa3ab-134">Chame [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) para recuperar a tabela de anexos da mensagem e localize a linha que representa o anexo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="aa3ab-135">Para obter mais informações, consulte [abertura de um anexo](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="aa3ab-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="aa3ab-136">Não tente abrir um anexo várias vezes; os resultados são indefinido e dependentes de provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="aa3ab-137">Você pode solicitar que o anexo seja aberto no modo de leitura/gravação, em vez do modo padrão de somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="aa3ab-138">No entanto, se o anexo realmente será aberto no modo leitura/gravação é do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="aa3ab-139">Você pode tentar modificar o anexo, preparando para lidar com falhas ou marque o nível de acesso que foi concedido Recuperando a propriedade de **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) do anexo, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa3ab-140">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aa3ab-140">MFCMAPI reference</span></span>

<span data-ttu-id="aa3ab-141">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa3ab-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa3ab-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="aa3ab-142">**File**</span></span>|<span data-ttu-id="aa3ab-143">**Function**</span><span class="sxs-lookup"><span data-stu-id="aa3ab-143">**Function**</span></span>|<span data-ttu-id="aa3ab-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="aa3ab-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa3ab-145">AttachmentsDlg.cpp usado para</span><span class="sxs-lookup"><span data-stu-id="aa3ab-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="aa3ab-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="aa3ab-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="aa3ab-147">MFCMAPI usa o método **IMessage::OpenAttach** para abrir a objetos de anexo</span><span class="sxs-lookup"><span data-stu-id="aa3ab-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa3ab-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa3ab-148">See also</span></span>



[<span data-ttu-id="aa3ab-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa3ab-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="aa3ab-150">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="aa3ab-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

