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
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387717"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="be0a2-103">Propriedade canônica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="be0a2-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="be0a2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be0a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be0a2-105">Contém um identificador exclusivo para um destinatário em uma tabela de destinatários ou a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="be0a2-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be0a2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="be0a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be0a2-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="be0a2-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="be0a2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be0a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be0a2-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="be0a2-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="be0a2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="be0a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="be0a2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="be0a2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="be0a2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="be0a2-112">Area:</span></span>  <br/> |<span data-ttu-id="be0a2-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="be0a2-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be0a2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be0a2-114">Remarks</span></span>

<span data-ttu-id="be0a2-115">Esta propriedade é um valor temporário que é válido apenas para a vida útil do objeto que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="be0a2-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="be0a2-116">Ele é exibido como uma coluna da tabela, mas não está armazenado.</span><span class="sxs-lookup"><span data-stu-id="be0a2-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="be0a2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="be0a2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be0a2-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="be0a2-118">Protocol specifications</span></span>

<span data-ttu-id="be0a2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be0a2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be0a2-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="be0a2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be0a2-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be0a2-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be0a2-122">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="be0a2-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be0a2-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="be0a2-123">Header files</span></span>

<span data-ttu-id="be0a2-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be0a2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="be0a2-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="be0a2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="be0a2-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be0a2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="be0a2-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="be0a2-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be0a2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="be0a2-128">See also</span></span>



[<span data-ttu-id="be0a2-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="be0a2-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="be0a2-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="be0a2-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="be0a2-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="be0a2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be0a2-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="be0a2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be0a2-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="be0a2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be0a2-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="be0a2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

