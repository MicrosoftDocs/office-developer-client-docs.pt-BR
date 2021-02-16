---
title: Propriedade canônica PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342676"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="95c65-103">Propriedade canônica PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="95c65-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="95c65-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95c65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95c65-105">Contém o tipo de endereço do remetente da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="95c65-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95c65-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="95c65-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95c65-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="95c65-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="95c65-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="95c65-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95c65-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="95c65-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="95c65-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="95c65-110">Data type:</span></span>  <br/> |<span data-ttu-id="95c65-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95c65-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="95c65-112">Área:</span><span class="sxs-lookup"><span data-stu-id="95c65-112">Area:</span></span>  <br/> |<span data-ttu-id="95c65-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="95c65-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95c65-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="95c65-114">Remarks</span></span>

<span data-ttu-id="95c65-115">Essas propriedades são exemplos das propriedades de endereço do remetente original de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="95c65-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="95c65-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essas propriedades como o valor de **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95c65-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="95c65-117">Ela nunca é alterada quando a mensagem é encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="95c65-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95c65-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="95c65-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95c65-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="95c65-119">Protocol specifications</span></span>

<span data-ttu-id="95c65-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95c65-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95c65-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="95c65-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95c65-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95c65-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95c65-123">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="95c65-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95c65-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="95c65-124">Header files</span></span>

<span data-ttu-id="95c65-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95c65-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="95c65-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="95c65-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="95c65-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95c65-127">Mapitags.h</span></span>
  
> <span data-ttu-id="95c65-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="95c65-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95c65-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="95c65-129">See also</span></span>



[<span data-ttu-id="95c65-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="95c65-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95c65-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="95c65-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95c65-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="95c65-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95c65-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="95c65-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

