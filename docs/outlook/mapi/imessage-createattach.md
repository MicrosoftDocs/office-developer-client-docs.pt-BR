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
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417665"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="6e235-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="6e235-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="6e235-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e235-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e235-105">Cria um novo anexo.</span><span class="sxs-lookup"><span data-stu-id="6e235-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="6e235-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e235-106">Parameters</span></span>

 <span data-ttu-id="6e235-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6e235-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6e235-108">[in] Ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e235-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="6e235-109">Passar resultados NULL na interface padrão da mensagem ou **IMessage**, sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="6e235-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="6e235-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6e235-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6e235-111">[in] Bitmask de sinalizadores que controla como o anexo é criado.</span><span class="sxs-lookup"><span data-stu-id="6e235-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="6e235-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6e235-112">The following flag can be set:</span></span>
    
<span data-ttu-id="6e235-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6e235-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6e235-114">Permite que **CreateAttach** retorne com êxito, possivelmente antes que o anexo seja totalmente acessível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="6e235-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="6e235-115">Se o anexo não estiver acessível, fazer uma chamada subsequente pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="6e235-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="6e235-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="6e235-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="6e235-117">[out] Ponteiro para um número de índice que identifica o anexo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="6e235-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="6e235-118">Esse número é válido somente quando a mensagem está aberta e é a base para a propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="6e235-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="6e235-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="6e235-119">_lppAttach_</span></span>
  
> <span data-ttu-id="6e235-120">[out] Ponteiro para um ponteiro para o objeto de anexo aberto.</span><span class="sxs-lookup"><span data-stu-id="6e235-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e235-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6e235-121">Return value</span></span>

<span data-ttu-id="6e235-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e235-122">S_OK</span></span> 
  
> <span data-ttu-id="6e235-123">O anexo foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6e235-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e235-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e235-124">Remarks</span></span>

<span data-ttu-id="6e235-125">O **método IMessage::CreateAttach** cria um novo anexo em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e235-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="6e235-126">O novo anexo e todas as propriedades definidas para ele não estarão disponíveis até que um cliente tenha chamado o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do anexo e o método **IMAPIProp::SaveChanges** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e235-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="6e235-127">O número do anexo apontado por  _lpulAttachmentNum_ é exclusivo e válido somente no contexto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e235-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="6e235-128">Ou seja, dois anexos em duas mensagens diferentes podem ter o mesmo número, enquanto dois anexos na mesma mensagem não podem.</span><span class="sxs-lookup"><span data-stu-id="6e235-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e235-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e235-129">See also</span></span>



[<span data-ttu-id="6e235-130">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6e235-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

