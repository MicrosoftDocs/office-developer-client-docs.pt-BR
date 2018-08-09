---
title: Propriedade canônica PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1d4d4404d175458d5b708948b11c93b734a8bd1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769734"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="6ca44-103">Propriedade canônica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6ca44-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="6ca44-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ca44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ca44-105">Contém TRUE se quiser que o sistema de mensagens para gerar um relatório de leitura quando o destinatário tenha lido uma mensagem de um remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6ca44-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ca44-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6ca44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ca44-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="6ca44-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="6ca44-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6ca44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ca44-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="6ca44-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="6ca44-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6ca44-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ca44-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6ca44-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6ca44-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6ca44-112">Area:</span></span>  <br/> |<span data-ttu-id="6ca44-113">Email</span><span class="sxs-lookup"><span data-stu-id="6ca44-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ca44-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca44-114">Remarks</span></span>

<span data-ttu-id="6ca44-115">Essa propriedade deve ser definida como TRUE para validar os valores nas propriedades de **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) e **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6ca44-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="6ca44-116">Se uma mensagem com **PR_READ_RECEIPT_REQUESTED** conjunto for excluída ou expira antes que o sistema de mensagens pode gerar um relatório de leitura, é gerado um relatório de nonread.</span><span class="sxs-lookup"><span data-stu-id="6ca44-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6ca44-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ca44-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ca44-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6ca44-118">Protocol specifications</span></span>

<span data-ttu-id="6ca44-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ca44-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ca44-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6ca44-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ca44-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ca44-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ca44-122">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6ca44-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ca44-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ca44-123">Header files</span></span>

<span data-ttu-id="6ca44-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ca44-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ca44-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6ca44-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ca44-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ca44-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6ca44-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6ca44-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ca44-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ca44-128">See also</span></span>



[<span data-ttu-id="6ca44-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6ca44-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ca44-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6ca44-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ca44-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6ca44-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ca44-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6ca44-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

