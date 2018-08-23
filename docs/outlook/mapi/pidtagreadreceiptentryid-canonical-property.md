---
title: Propriedade canônica PidTagReadReceiptEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 658f3694e7592fab54b2ddf303da2e15e4510354
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567101"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="a70f4-103">Propriedade canônica PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="a70f4-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a70f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a70f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a70f4-105">Contém um identificador de entrada para o usuário mensagens onde o sistema de mensagens deve direcionar um relatório de leitura para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="a70f4-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a70f4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a70f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a70f4-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a70f4-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a70f4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a70f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a70f4-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="a70f4-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="a70f4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a70f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="a70f4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a70f4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a70f4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a70f4-112">Area:</span></span>  <br/> |<span data-ttu-id="a70f4-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="a70f4-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a70f4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a70f4-114">Remarks</span></span>

<span data-ttu-id="a70f4-115">Essa propriedade será ignorada se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) não estiver definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="a70f4-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="a70f4-116">Se um aplicativo cliente quiser receber ler relatórios em si, ele pode deixar esta propriedade não definidas ou defini-la como o identificador de entrada contido na propriedade **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) em tempo de envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a70f4-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a70f4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a70f4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a70f4-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a70f4-118">Protocol specifications</span></span>

<span data-ttu-id="a70f4-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a70f4-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a70f4-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a70f4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a70f4-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a70f4-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a70f4-122">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a70f4-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a70f4-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a70f4-123">Header files</span></span>

<span data-ttu-id="a70f4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a70f4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a70f4-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a70f4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a70f4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a70f4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a70f4-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a70f4-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a70f4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a70f4-128">See also</span></span>



[<span data-ttu-id="a70f4-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a70f4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a70f4-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a70f4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a70f4-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a70f4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a70f4-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a70f4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

