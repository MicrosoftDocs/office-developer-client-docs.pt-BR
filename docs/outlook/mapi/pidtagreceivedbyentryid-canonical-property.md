---
title: Propriedade canônica PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7d457c898a1b8c733913de0fbb2fbfe9542dc9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769741"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="bd084-103">Propriedade canônica PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="bd084-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bd084-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd084-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd084-105">Contém o identificador de entrada do usuário mensagens que recebe a mensagem de fato.</span><span class="sxs-lookup"><span data-stu-id="bd084-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd084-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bd084-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd084-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bd084-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bd084-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bd084-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd084-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="bd084-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="bd084-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bd084-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd084-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd084-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bd084-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bd084-112">Area:</span></span>  <br/> |<span data-ttu-id="bd084-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="bd084-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd084-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd084-114">Remarks</span></span>

<span data-ttu-id="bd084-115">Essa propriedade é uma das propriedades de endereço para o usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bd084-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="bd084-116">Ele deve ser definido pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="bd084-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="bd084-117">Essa propriedade corresponde a um atributo MH_T_ x. 400 entrega envelope-message.</span><span class="sxs-lookup"><span data-stu-id="bd084-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd084-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd084-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd084-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bd084-119">Protocol specifications</span></span>

<span data-ttu-id="bd084-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd084-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd084-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bd084-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd084-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd084-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd084-123">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="bd084-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="bd084-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd084-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd084-125">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="bd084-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="bd084-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd084-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd084-127">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e itens de reunião.</span><span class="sxs-lookup"><span data-stu-id="bd084-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="bd084-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd084-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd084-129">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="bd084-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="bd084-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd084-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd084-131">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="bd084-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd084-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd084-132">Header files</span></span>

<span data-ttu-id="bd084-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd084-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd084-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd084-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd084-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd084-135">Mapitags.h</span></span>
  
> <span data-ttu-id="bd084-136">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="bd084-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd084-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd084-137">See also</span></span>



[<span data-ttu-id="bd084-138">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="bd084-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="bd084-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bd084-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd084-140">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bd084-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd084-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bd084-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd084-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bd084-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

