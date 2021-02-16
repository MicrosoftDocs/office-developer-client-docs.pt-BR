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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340974"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="9b3d0-103">Propriedade canônica PidTagOriginalSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="9b3d0-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="9b3d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b3d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b3d0-105">Contém a chave de pesquisa do usuário de mensagens em cujo nome a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b3d0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9b3d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b3d0-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9b3d0-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="9b3d0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b3d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b3d0-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="9b3d0-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="9b3d0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9b3d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b3d0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9b3d0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9b3d0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b3d0-112">Area:</span></span>  <br/> |<span data-ttu-id="9b3d0-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="9b3d0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b3d0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b3d0-114">Remarks</span></span>

<span data-ttu-id="9b3d0-115">Essa propriedade é uma das propriedades de endereço do remetente original representado de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="9b3d0-116">Ele é usado em um thread de conversa.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="9b3d0-117">Um aplicativo cliente enviando uma mensagem em nome de outro cliente deve definir essa propriedade como o valor da propriedade **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="9b3d0-118">Uma vez definido, ele nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9b3d0-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b3d0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b3d0-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b3d0-120">Protocol specifications</span></span>

<span data-ttu-id="9b3d0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b3d0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b3d0-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b3d0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b3d0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b3d0-124">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b3d0-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9b3d0-125">Header files</span></span>

<span data-ttu-id="9b3d0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b3d0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b3d0-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b3d0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b3d0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9b3d0-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9b3d0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b3d0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b3d0-130">See also</span></span>



[<span data-ttu-id="9b3d0-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b3d0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b3d0-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9b3d0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b3d0-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b3d0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b3d0-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9b3d0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

