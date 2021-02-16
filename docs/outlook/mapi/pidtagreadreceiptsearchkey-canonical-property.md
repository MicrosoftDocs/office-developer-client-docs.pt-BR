---
title: Propriedade canônica PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320038"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="03138-103">Propriedade canônica PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="03138-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="03138-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03138-105">Contém uma chave de pesquisa para o usuário de mensagens para o qual o sistema de mensagens deve direcionar um relatório de leitura para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="03138-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03138-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="03138-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03138-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="03138-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="03138-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="03138-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03138-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="03138-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="03138-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="03138-110">Data type:</span></span>  <br/> |<span data-ttu-id="03138-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="03138-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="03138-112">Área:</span><span class="sxs-lookup"><span data-stu-id="03138-112">Area:</span></span>  <br/> |<span data-ttu-id="03138-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="03138-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03138-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="03138-114">Remarks</span></span>

<span data-ttu-id="03138-115">Essa propriedade será ignorada, a menos **que PR_READ_RECEIPT_REQUESTED** propriedade ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) esteja definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="03138-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="03138-116">Se um aplicativo cliente quiser receber relatórios de leitura em si, ele poderá deixar essa propriedade desajustada ou defini-la como a chave de pesquisa contida na propriedade **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) no momento do envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="03138-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03138-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="03138-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03138-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="03138-118">Protocol specifications</span></span>

<span data-ttu-id="03138-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03138-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03138-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="03138-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03138-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03138-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03138-122">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="03138-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03138-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="03138-123">Header files</span></span>

<span data-ttu-id="03138-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="03138-124">Mapidef.h</span></span>
  
> <span data-ttu-id="03138-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03138-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="03138-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03138-126">Mapitags.h</span></span>
  
> <span data-ttu-id="03138-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="03138-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03138-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="03138-128">See also</span></span>



[<span data-ttu-id="03138-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="03138-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03138-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="03138-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03138-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="03138-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03138-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="03138-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

