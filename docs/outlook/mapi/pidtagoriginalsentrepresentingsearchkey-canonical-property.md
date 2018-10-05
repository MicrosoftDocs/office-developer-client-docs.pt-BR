---
title: Propriedade canônica PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388494"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="c16e5-103">Propriedade canônica PidTagOriginalSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="c16e5-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="c16e5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c16e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c16e5-105">Contém a chave de pesquisa do usuário mensagens em nome do qual a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="c16e5-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c16e5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c16e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c16e5-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="c16e5-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="c16e5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c16e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c16e5-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="c16e5-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="c16e5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c16e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="c16e5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c16e5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c16e5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c16e5-112">Area:</span></span>  <br/> |<span data-ttu-id="c16e5-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="c16e5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c16e5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c16e5-114">Remarks</span></span>

<span data-ttu-id="c16e5-115">Essa propriedade é uma das propriedades de endereço de remetente de uma mensagem original representado.</span><span class="sxs-lookup"><span data-stu-id="c16e5-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="c16e5-116">Ele é usado em um segmento de conversação.</span><span class="sxs-lookup"><span data-stu-id="c16e5-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="c16e5-117">Um aplicativo cliente enviar uma mensagem em nome de outro cliente deve definir essa propriedade como o valor da propriedade **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c16e5-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="c16e5-118">Depois de definido, ela nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="c16e5-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c16e5-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c16e5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c16e5-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c16e5-120">Protocol specifications</span></span>

<span data-ttu-id="c16e5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c16e5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c16e5-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c16e5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c16e5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c16e5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c16e5-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c16e5-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c16e5-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c16e5-125">Header files</span></span>

<span data-ttu-id="c16e5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c16e5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c16e5-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c16e5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c16e5-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c16e5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c16e5-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c16e5-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c16e5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c16e5-130">See also</span></span>



[<span data-ttu-id="c16e5-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c16e5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c16e5-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c16e5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c16e5-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c16e5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c16e5-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c16e5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

