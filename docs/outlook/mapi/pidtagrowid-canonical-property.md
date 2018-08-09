---
title: Propriedade canônica PidTagRowid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8d0e79e01040c1cc3d46e73a7e6a456a915a67f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769855"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="d541d-103">Propriedade canônica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="d541d-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="d541d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d541d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d541d-105">Contém um identificador exclusivo para um destinatário em uma tabela de destinatários ou a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="d541d-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d541d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d541d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d541d-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="d541d-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="d541d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d541d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d541d-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="d541d-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="d541d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d541d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d541d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d541d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d541d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d541d-112">Area:</span></span>  <br/> |<span data-ttu-id="d541d-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="d541d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d541d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d541d-114">Remarks</span></span>

<span data-ttu-id="d541d-115">Esta propriedade é um valor temporário que é válido apenas para a vida útil do objeto que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="d541d-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="d541d-116">Ele é exibido como uma coluna da tabela, mas não está armazenado.</span><span class="sxs-lookup"><span data-stu-id="d541d-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d541d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d541d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d541d-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d541d-118">Protocol specifications</span></span>

<span data-ttu-id="d541d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d541d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d541d-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d541d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d541d-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d541d-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d541d-122">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="d541d-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d541d-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d541d-123">Header files</span></span>

<span data-ttu-id="d541d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d541d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d541d-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d541d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d541d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d541d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d541d-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d541d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d541d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d541d-128">See also</span></span>



[<span data-ttu-id="d541d-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="d541d-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="d541d-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="d541d-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="d541d-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d541d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d541d-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d541d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d541d-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d541d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d541d-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d541d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

