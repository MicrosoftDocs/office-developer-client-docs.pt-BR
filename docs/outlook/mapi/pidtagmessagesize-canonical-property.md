---
title: Propriedade canônico de PidTagMessageSize
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769488"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="58a5e-103">Propriedade canônico de PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="58a5e-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="58a5e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58a5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58a5e-105">Contém a soma, em bytes, dos tamanhos de todas as propriedades em um objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="58a5e-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58a5e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="58a5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58a5e-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="58a5e-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="58a5e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="58a5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58a5e-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="58a5e-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="58a5e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="58a5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="58a5e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="58a5e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="58a5e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="58a5e-112">Area:</span></span>  <br/> |<span data-ttu-id="58a5e-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="58a5e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58a5e-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="58a5e-114">Remarks</span></span>

<span data-ttu-id="58a5e-115">É recomendável que os objetos de mensagem exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="58a5e-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="58a5e-116">O tamanho da mensagem indica o número aproximado de bytes são transferidos quando a mensagem é movida do repositório de uma mensagem para outro.</span><span class="sxs-lookup"><span data-stu-id="58a5e-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="58a5e-117">Sendo a soma dos tamanhos de todas as propriedades no objeto de mensagem, normalmente é consideravelmente maior do que o texto da mensagem sozinho.</span><span class="sxs-lookup"><span data-stu-id="58a5e-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="58a5e-118">A maioria das mensagens armazenar provedores compute essa propriedade para mensagens que eles conduzem.</span><span class="sxs-lookup"><span data-stu-id="58a5e-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="58a5e-119">No entanto, alguns provedores de armazenamento de mensagem não têm suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="58a5e-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="58a5e-120">Em qualquer caso, essa propriedade não está disponível até que o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMessage::SubmitMessage](imessage-submitmessage.md) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="58a5e-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="58a5e-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="58a5e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58a5e-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="58a5e-122">Protocol specifications</span></span>

<span data-ttu-id="58a5e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58a5e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58a5e-124">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="58a5e-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58a5e-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58a5e-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58a5e-126">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="58a5e-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="58a5e-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58a5e-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58a5e-128">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="58a5e-128">Handles folder operations.</span></span>
    
<span data-ttu-id="58a5e-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58a5e-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58a5e-130">Especifica as operações permitidas para os objetos do repositório de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="58a5e-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58a5e-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="58a5e-131">Header files</span></span>

<span data-ttu-id="58a5e-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58a5e-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="58a5e-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="58a5e-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="58a5e-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58a5e-134">Mapitags.h</span></span>
  
> <span data-ttu-id="58a5e-135">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="58a5e-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58a5e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="58a5e-136">See also</span></span>



[<span data-ttu-id="58a5e-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="58a5e-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58a5e-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="58a5e-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58a5e-139">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="58a5e-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58a5e-140">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="58a5e-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

