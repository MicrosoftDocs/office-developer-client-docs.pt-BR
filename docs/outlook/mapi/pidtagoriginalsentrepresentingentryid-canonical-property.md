---
title: Propriedade canônica PidTagOriginalSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 92300733d32f021bb0ab8ab29a9676b740eeda12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769595"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="e06c1-103">Propriedade canônica PidTagOriginalSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="e06c1-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e06c1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e06c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e06c1-105">Contém o identificador de entrada do usuário mensagens em nome do qual a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="e06c1-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e06c1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e06c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e06c1-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e06c1-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e06c1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e06c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e06c1-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="e06c1-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="e06c1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e06c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="e06c1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e06c1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e06c1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e06c1-112">Area:</span></span>  <br/> |<span data-ttu-id="e06c1-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="e06c1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e06c1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e06c1-114">Remarks</span></span>

<span data-ttu-id="e06c1-115">Essa propriedade é uma das propriedades de endereço de remetente de uma mensagem original representado.</span><span class="sxs-lookup"><span data-stu-id="e06c1-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="e06c1-116">Ele é usado em um segmento de conversação.</span><span class="sxs-lookup"><span data-stu-id="e06c1-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="e06c1-117">Um aplicativo cliente enviar uma mensagem em nome de outro cliente deve definir essa propriedade como o valor da propriedade **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e06c1-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="e06c1-118">Depois de definido, ela nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="e06c1-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e06c1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e06c1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e06c1-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e06c1-120">Protocol specifications</span></span>

<span data-ttu-id="e06c1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e06c1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e06c1-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e06c1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e06c1-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e06c1-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e06c1-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e06c1-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e06c1-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e06c1-125">Header files</span></span>

<span data-ttu-id="e06c1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e06c1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e06c1-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e06c1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e06c1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e06c1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e06c1-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e06c1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e06c1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e06c1-130">See also</span></span>



[<span data-ttu-id="e06c1-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e06c1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e06c1-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e06c1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e06c1-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e06c1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e06c1-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e06c1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

