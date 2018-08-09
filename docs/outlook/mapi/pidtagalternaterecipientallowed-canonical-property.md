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
ms.openlocfilehash: dc77f9c7b58fc925048d6dec2bee2ff96a8723b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768939"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="8ba0c-103">Propriedade canônica PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="8ba0c-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="8ba0c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ba0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ba0c-105">Conterá TRUE se o remetente permite o encaminhamento automático desta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ba0c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8ba0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ba0c-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="8ba0c-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="8ba0c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8ba0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ba0c-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="8ba0c-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="8ba0c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8ba0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ba0c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8ba0c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8ba0c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8ba0c-112">Area:</span></span>  <br/> |<span data-ttu-id="8ba0c-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="8ba0c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ba0c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ba0c-114">Remarks</span></span>

<span data-ttu-id="8ba0c-115">Se o encaminhamento automático não é permitido ou nenhum destinatário alternativo foi designado, um relatório de não entrega deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ba0c-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ba0c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ba0c-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8ba0c-117">Protocol specifications</span></span>

<span data-ttu-id="8ba0c-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba0c-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ba0c-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ba0c-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba0c-120">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ba0c-121">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8ba0c-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba0c-122">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ba0c-123">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8ba0c-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba0c-124">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ba0c-125">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ba0c-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8ba0c-126">Header files</span></span>

<span data-ttu-id="8ba0c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ba0c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ba0c-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ba0c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ba0c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8ba0c-130">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ba0c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ba0c-131">See also</span></span>



[<span data-ttu-id="8ba0c-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8ba0c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ba0c-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8ba0c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ba0c-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8ba0c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ba0c-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8ba0c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

