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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385953"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="485a8-103">Propriedade canônica PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="485a8-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="485a8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="485a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="485a8-105">Conterá TRUE se o remetente permite o encaminhamento automático desta mensagem.</span><span class="sxs-lookup"><span data-stu-id="485a8-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="485a8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="485a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="485a8-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="485a8-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="485a8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="485a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="485a8-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="485a8-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="485a8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="485a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="485a8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="485a8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="485a8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="485a8-112">Area:</span></span>  <br/> |<span data-ttu-id="485a8-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="485a8-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="485a8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="485a8-114">Remarks</span></span>

<span data-ttu-id="485a8-115">Se o encaminhamento automático não é permitido ou nenhum destinatário alternativo foi designado, um relatório de não entrega deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="485a8-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="485a8-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="485a8-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="485a8-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="485a8-117">Protocol specifications</span></span>

<span data-ttu-id="485a8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="485a8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="485a8-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="485a8-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="485a8-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="485a8-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="485a8-121">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="485a8-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="485a8-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="485a8-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="485a8-123">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="485a8-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="485a8-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="485a8-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="485a8-125">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="485a8-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="485a8-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="485a8-126">Header files</span></span>

<span data-ttu-id="485a8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="485a8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="485a8-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="485a8-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="485a8-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="485a8-129">Mapitags.h</span></span>
  
> <span data-ttu-id="485a8-130">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="485a8-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="485a8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="485a8-131">See also</span></span>



[<span data-ttu-id="485a8-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="485a8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="485a8-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="485a8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="485a8-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="485a8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="485a8-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="485a8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

