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
ms.openlocfilehash: 7016b1a7039d5df8d4e9fdedea580526eebe04bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585938"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="f8df9-103">Propriedade canônica PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="f8df9-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="f8df9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8df9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8df9-105">Contém uma chave de pesquisa para o usuário de mensagens para o qual o sistema de mensagens deve direcionar um relatório de leitura para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f8df9-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8df9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f8df9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8df9-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="f8df9-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="f8df9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f8df9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8df9-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="f8df9-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="f8df9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f8df9-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8df9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f8df9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f8df9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f8df9-112">Area:</span></span>  <br/> |<span data-ttu-id="f8df9-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="f8df9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8df9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8df9-114">Remarks</span></span>

<span data-ttu-id="f8df9-115">Essa propriedade será ignorada se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) não estiver definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="f8df9-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="f8df9-116">Se um aplicativo cliente quiser receber ler relatórios em si, ele pode deixar esta propriedade não definidas ou defini-la como a chave de pesquisa contida na propriedade **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) em tempo de envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f8df9-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8df9-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8df9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8df9-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f8df9-118">Protocol specifications</span></span>

<span data-ttu-id="f8df9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8df9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8df9-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f8df9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8df9-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8df9-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8df9-122">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="f8df9-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8df9-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8df9-123">Header files</span></span>

<span data-ttu-id="f8df9-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="f8df9-124">Mapidef.h</span></span>
  
> <span data-ttu-id="f8df9-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f8df9-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8df9-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8df9-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f8df9-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f8df9-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8df9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8df9-128">See also</span></span>



[<span data-ttu-id="f8df9-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f8df9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8df9-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f8df9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8df9-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f8df9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8df9-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f8df9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

