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
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341108"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="4d621-103">Propriedade canônica PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="4d621-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="4d621-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d621-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d621-105">Especifica se a adição de destinatários adicionais, ao encaminhar a mensagem, é proibida para a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4d621-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d621-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4d621-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d621-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="4d621-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="4d621-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4d621-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d621-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="4d621-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="4d621-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4d621-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d621-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4d621-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4d621-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4d621-112">Area:</span></span>  <br/> |<span data-ttu-id="4d621-113">MAPI Envelope</span><span class="sxs-lookup"><span data-stu-id="4d621-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d621-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d621-114">Remarks</span></span>

<span data-ttu-id="4d621-115">Essa propriedade é definida com base no valor de PR_SENSITIVITY **(** [PidTagSensitivity](pidtagsensitivity-canonical-property.md)) da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4d621-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="4d621-116">Se **PR_SENSITIVITY** for definido como "0x00000000" (normal) ou "0x00000003" (confidencial), essa propriedade deverá ser definida como "0x00" ou ausente, o que significa que é permitido adicionar destinatários adicionais ou diferentes à mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4d621-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="4d621-117">Se o PR_SENSITIVITY  do objeto de email estiver definido como "0x00000001" (pessoal) ou "0x00000002" (privado), essa propriedade deverá ser definida como "0x01" para impedir a adição de destinatários adicionais ou diferentes desse email por meio do encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4d621-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d621-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d621-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d621-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4d621-119">Protocol specifications</span></span>

<span data-ttu-id="4d621-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d621-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d621-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4d621-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d621-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d621-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d621-123">Especifica as propriedades e operações permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="4d621-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d621-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="4d621-124">Header files</span></span>

<span data-ttu-id="4d621-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d621-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d621-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4d621-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d621-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d621-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4d621-128">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="4d621-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d621-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d621-129">See also</span></span>



[<span data-ttu-id="4d621-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d621-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d621-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4d621-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d621-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4d621-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d621-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4d621-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

