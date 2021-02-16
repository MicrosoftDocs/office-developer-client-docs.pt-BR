---
title: Propriedade canônica PidTagOriginalSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bfb768b774b1fa3d4b65ad2122f49a8ffe11a7b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341220"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="1799a-103">Propriedade canônica PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="1799a-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="1799a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1799a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1799a-105">Contém o tipo de endereço do usuário de mensagens em cujo nome a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="1799a-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1799a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1799a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1799a-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1799a-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="1799a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1799a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1799a-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="1799a-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="1799a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1799a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1799a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1799a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1799a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1799a-112">Area:</span></span>  <br/> |<span data-ttu-id="1799a-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="1799a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1799a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1799a-114">Remarks</span></span>

<span data-ttu-id="1799a-115">Essas propriedades são do tipo do remetente original representado de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1799a-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="1799a-116">Eles são usados em um thread de conversa.</span><span class="sxs-lookup"><span data-stu-id="1799a-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="1799a-117">Um aplicativo cliente enviando uma mensagem em nome de outro cliente deve definir essas propriedades como o valor da propriedade **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1799a-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="1799a-118">Uma vez definido, ele nunca deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="1799a-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1799a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1799a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1799a-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1799a-120">Protocol specifications</span></span>

<span data-ttu-id="1799a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1799a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1799a-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1799a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1799a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1799a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1799a-124">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1799a-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1799a-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1799a-125">Header files</span></span>

<span data-ttu-id="1799a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1799a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1799a-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1799a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1799a-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1799a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1799a-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1799a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1799a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1799a-130">See also</span></span>



[<span data-ttu-id="1799a-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1799a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1799a-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1799a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1799a-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1799a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1799a-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1799a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

