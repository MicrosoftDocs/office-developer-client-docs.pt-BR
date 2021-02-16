---
title: Propriedade canônica PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355647"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="85ed8-103">Propriedade canônica PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="85ed8-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="85ed8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85ed8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85ed8-105">Contém a soma, em bytes, dos tamanhos de todas as propriedades em um objeto message.</span><span class="sxs-lookup"><span data-stu-id="85ed8-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85ed8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="85ed8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85ed8-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="85ed8-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="85ed8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="85ed8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85ed8-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="85ed8-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="85ed8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="85ed8-110">Data type:</span></span>  <br/> |<span data-ttu-id="85ed8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="85ed8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="85ed8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="85ed8-112">Area:</span></span>  <br/> |<span data-ttu-id="85ed8-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="85ed8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85ed8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="85ed8-114">Remarks</span></span>

<span data-ttu-id="85ed8-115">É recomendável que os objetos de mensagem exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="85ed8-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="85ed8-116">O tamanho da mensagem indica o número aproximado de bytes transferidos quando a mensagem é movida de um armazenamento de mensagens para outro.</span><span class="sxs-lookup"><span data-stu-id="85ed8-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="85ed8-117">Sendo a soma dos tamanhos de todas as propriedades no objeto de mensagem, geralmente é consideravelmente maior do que o texto da mensagem sozinho.</span><span class="sxs-lookup"><span data-stu-id="85ed8-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="85ed8-118">A maioria dos provedores de armazenamento de mensagens calcula essa propriedade para mensagens que eles lidam.</span><span class="sxs-lookup"><span data-stu-id="85ed8-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="85ed8-119">No entanto, alguns provedores de armazenamento de mensagens não suportam essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="85ed8-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="85ed8-120">De qualquer forma, essa propriedade não estará disponível até que o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMessage::SubmitMessage](imessage-submitmessage.md) tenha sido chamado.</span><span class="sxs-lookup"><span data-stu-id="85ed8-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="85ed8-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="85ed8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85ed8-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="85ed8-122">Protocol specifications</span></span>

<span data-ttu-id="85ed8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85ed8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85ed8-124">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="85ed8-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85ed8-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85ed8-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85ed8-126">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="85ed8-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="85ed8-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85ed8-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85ed8-128">Lida com operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="85ed8-128">Handles folder operations.</span></span>
    
<span data-ttu-id="85ed8-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85ed8-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85ed8-130">Especifica operações permitidas para os objetos principais do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="85ed8-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85ed8-131">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="85ed8-131">Header files</span></span>

<span data-ttu-id="85ed8-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85ed8-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="85ed8-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="85ed8-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="85ed8-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="85ed8-134">Mapitags.h</span></span>
  
> <span data-ttu-id="85ed8-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="85ed8-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85ed8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="85ed8-136">See also</span></span>



[<span data-ttu-id="85ed8-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="85ed8-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85ed8-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="85ed8-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85ed8-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="85ed8-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85ed8-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="85ed8-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

