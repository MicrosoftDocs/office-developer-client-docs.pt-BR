---
title: Propriedade canônica PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411369"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="e0da1-103">Propriedade canônica PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e0da1-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="e0da1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0da1-105">Contém o endereço de email do destinatário originalmente pretendido de uma mensagem com origem automática.</span><span class="sxs-lookup"><span data-stu-id="e0da1-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0da1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e0da1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0da1-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="e0da1-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="e0da1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e0da1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0da1-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="e0da1-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="e0da1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e0da1-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0da1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e0da1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e0da1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e0da1-112">Area:</span></span>  <br/> |<span data-ttu-id="e0da1-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="e0da1-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0da1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0da1-114">Remarks</span></span>

<span data-ttu-id="e0da1-115">Essas propriedades são exemplos das propriedades de endereço do destinatário da mensagem originalmente pretendido.</span><span class="sxs-lookup"><span data-stu-id="e0da1-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="e0da1-116">Eles devem ser definidos pelo agente automático que encaminhou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0da1-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="e0da1-117">Essas propriedades correspondem ao atributo de relatório X.400 por destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0da1-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0da1-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0da1-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e0da1-119">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e0da1-119">Header files</span></span>

<span data-ttu-id="e0da1-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0da1-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0da1-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e0da1-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0da1-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0da1-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e0da1-123">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e0da1-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0da1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0da1-124">See also</span></span>



[<span data-ttu-id="e0da1-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e0da1-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0da1-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e0da1-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0da1-127">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e0da1-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0da1-128">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e0da1-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

