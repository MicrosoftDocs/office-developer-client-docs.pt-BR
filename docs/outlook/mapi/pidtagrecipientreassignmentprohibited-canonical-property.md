---
title: Propriedade canônica PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769783"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="92584-103">Propriedade canônica PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="92584-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="92584-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92584-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92584-105">Especifica se a adição de destinatários adicionais, quando o encaminhamento da mensagem, é proibida para a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="92584-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92584-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="92584-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92584-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="92584-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="92584-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="92584-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92584-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="92584-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="92584-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="92584-110">Data type:</span></span>  <br/> |<span data-ttu-id="92584-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="92584-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="92584-112">Área:</span><span class="sxs-lookup"><span data-stu-id="92584-112">Area:</span></span>  <br/> |<span data-ttu-id="92584-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="92584-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92584-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="92584-114">Remarks</span></span>

<span data-ttu-id="92584-115">Essa propriedade é definida com base no valor de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="92584-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="92584-116">Se **PR_SENSITIVITY** for definido como "0x00000000" (normal) ou "0x00000003" (confidencial), essa propriedade deve ser definida como "0x00" ou absent o que significa que adicionar destinatários diferentes ou adicionais de mensagem de email é permitido.</span><span class="sxs-lookup"><span data-stu-id="92584-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="92584-117">Se o email **PR_SENSITIVITY do objeto** é definido como "0x00000001" (pessoais) ou "0x00000002" (privada), essa propriedade deverá ser definida "0x01" para impedir a adição de destinatários diferentes ou adicionais deste email por meio de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="92584-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="92584-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="92584-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92584-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="92584-119">Protocol specifications</span></span>

<span data-ttu-id="92584-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92584-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92584-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="92584-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92584-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92584-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92584-123">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="92584-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92584-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="92584-124">Header files</span></span>

<span data-ttu-id="92584-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92584-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="92584-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="92584-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="92584-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92584-127">Mapitags.h</span></span>
  
> <span data-ttu-id="92584-128">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="92584-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92584-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="92584-129">See also</span></span>



[<span data-ttu-id="92584-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="92584-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92584-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="92584-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92584-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="92584-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92584-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="92584-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

