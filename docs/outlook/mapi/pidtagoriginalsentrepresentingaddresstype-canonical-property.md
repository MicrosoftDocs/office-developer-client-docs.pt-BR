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
ms.openlocfilehash: ce3678c5137caec2e9f80c7fc15cde0ae99441ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572526"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="50754-103">Propriedade canônica PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="50754-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="50754-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50754-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50754-105">Contém o tipo de endereço do usuário mensagens em nome do qual a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="50754-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50754-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="50754-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50754-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="50754-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="50754-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="50754-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50754-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="50754-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="50754-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="50754-110">Data type:</span></span>  <br/> |<span data-ttu-id="50754-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50754-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="50754-112">Área:</span><span class="sxs-lookup"><span data-stu-id="50754-112">Area:</span></span>  <br/> |<span data-ttu-id="50754-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="50754-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50754-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="50754-114">Remarks</span></span>

<span data-ttu-id="50754-115">Essas propriedades são o tipo de remetente original representado de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="50754-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="50754-116">Eles são usados em um segmento de conversação.</span><span class="sxs-lookup"><span data-stu-id="50754-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="50754-117">Um aplicativo cliente enviar uma mensagem em nome de outro cliente deve definir essas propriedades com o valor da propriedade **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="50754-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="50754-118">Depois de definido, ela nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="50754-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50754-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="50754-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50754-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="50754-120">Protocol specifications</span></span>

<span data-ttu-id="50754-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50754-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50754-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="50754-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50754-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50754-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50754-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="50754-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50754-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="50754-125">Header files</span></span>

<span data-ttu-id="50754-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50754-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="50754-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="50754-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="50754-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="50754-128">Mapitags.h</span></span>
  
> <span data-ttu-id="50754-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="50754-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50754-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="50754-130">See also</span></span>



[<span data-ttu-id="50754-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="50754-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50754-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="50754-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50754-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="50754-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50754-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="50754-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

