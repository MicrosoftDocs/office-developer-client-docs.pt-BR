---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572079"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="f6302-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="f6302-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="f6302-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6302-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6302-105">Cria um novo anexo.</span><span class="sxs-lookup"><span data-stu-id="f6302-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="f6302-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6302-106">Parameters</span></span>

 <span data-ttu-id="f6302-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f6302-107">_lpInterface_</span></span>
  
> <span data-ttu-id="f6302-108">[in] Ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6302-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="f6302-109">Passagem nula resulta em interface padrão ou **IMessage**, a mensagem que está sendo retornada.</span><span class="sxs-lookup"><span data-stu-id="f6302-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="f6302-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6302-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f6302-111">[in] Bitmask dos sinalizadores que controla como o anexo é criado.</span><span class="sxs-lookup"><span data-stu-id="f6302-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="f6302-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f6302-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f6302-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f6302-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f6302-114">Permite que **CreateAttach** retornar com êxito, possivelmente antes que o anexo seja totalmente acessível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="f6302-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="f6302-115">Se o anexo não está acessível, fazendo uma chamada subsequente a ele pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="f6302-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="f6302-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="f6302-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="f6302-117">[out] Ponteiro para um número de índice que identifica o anexo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="f6302-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="f6302-118">Esse número é válido somente quando a mensagem é aberta e é a base para a propriedade de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="f6302-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="f6302-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="f6302-119">_lppAttach_</span></span>
  
> <span data-ttu-id="f6302-120">[out] Ponteiro para um ponteiro para o objeto de abrir anexo.</span><span class="sxs-lookup"><span data-stu-id="f6302-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6302-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f6302-121">Return value</span></span>

<span data-ttu-id="f6302-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6302-122">S_OK</span></span> 
  
> <span data-ttu-id="f6302-123">O anexo foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f6302-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6302-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6302-124">Remarks</span></span>

<span data-ttu-id="f6302-125">O método **IMessage::CreateAttach** cria um novo anexo em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6302-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="f6302-126">O novo anexo e as propriedades que são definidas para ele, não estão disponíveis até que um cliente tenha chamado o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do anexo e o método de **IMAPIProp::SaveChanges** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6302-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="f6302-127">O número de anexo apontado pela _lpulAttachmentNum_ é exclusivo e válido somente dentro do contexto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6302-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="f6302-128">Ou seja, dois anexos em duas mensagens diferentes podem ter o mesmo número enquanto dois anexos na mesma mensagem não é possível.</span><span class="sxs-lookup"><span data-stu-id="f6302-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6302-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6302-129">See also</span></span>



[<span data-ttu-id="f6302-130">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f6302-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

