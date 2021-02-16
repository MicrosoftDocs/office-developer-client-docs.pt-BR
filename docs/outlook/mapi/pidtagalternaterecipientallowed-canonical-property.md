---
title: Propriedade canônica PidTagAlternateRecipientAllowed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipientAllowed
api_type:
- HeaderDef
ms.assetid: dbbdeb54-3d14-4601-a77b-55ee31f33416
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327983"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="e224d-103">Propriedade canônica PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="e224d-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="e224d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e224d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e224d-105">Contém TRUE se o remetente permitir o encaminhamento automático dessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e224d-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e224d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e224d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e224d-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="e224d-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="e224d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e224d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e224d-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="e224d-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="e224d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e224d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e224d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e224d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e224d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e224d-112">Area:</span></span>  <br/> |<span data-ttu-id="e224d-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="e224d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e224d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e224d-114">Remarks</span></span>

<span data-ttu-id="e224d-115">Se o encaminhamento automático não for permitido ou se nenhum destinatário alternativo tiver sido designado, um relatório de não entrega deverá ser gerado.</span><span class="sxs-lookup"><span data-stu-id="e224d-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e224d-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e224d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e224d-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e224d-117">Protocol specifications</span></span>

<span data-ttu-id="e224d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e224d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e224d-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e224d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e224d-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e224d-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e224d-121">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="e224d-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e224d-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e224d-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e224d-123">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="e224d-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e224d-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e224d-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e224d-125">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e224d-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e224d-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e224d-126">Header files</span></span>

<span data-ttu-id="e224d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e224d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e224d-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e224d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e224d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e224d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e224d-130">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e224d-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e224d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e224d-131">See also</span></span>



[<span data-ttu-id="e224d-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e224d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e224d-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e224d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e224d-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e224d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e224d-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e224d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

