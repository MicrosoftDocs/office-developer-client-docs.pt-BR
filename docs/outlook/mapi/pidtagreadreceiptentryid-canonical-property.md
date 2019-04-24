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
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356489"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="62598-103">Propriedade canônica PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="62598-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="62598-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62598-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62598-105">Contém um identificador de entrada para o usuário de mensagens onde o sistema de mensagens deve direcionar um relatório de leitura para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="62598-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62598-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="62598-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62598-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="62598-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="62598-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="62598-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62598-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="62598-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="62598-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="62598-110">Data type:</span></span>  <br/> |<span data-ttu-id="62598-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="62598-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="62598-112">Área:</span><span class="sxs-lookup"><span data-stu-id="62598-112">Area:</span></span>  <br/> |<span data-ttu-id="62598-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="62598-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62598-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="62598-114">Remarks</span></span>

<span data-ttu-id="62598-115">Essa propriedade é ignorada, a menos que a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) esteja definida como true.</span><span class="sxs-lookup"><span data-stu-id="62598-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="62598-116">Se um aplicativo cliente deseja receber relatórios de leitura em si, pode deixar essa propriedade indefinida ou defini-la como o identificador de entrada contido na propriedade **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) no horário de envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="62598-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62598-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="62598-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62598-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="62598-118">Protocol specifications</span></span>

<span data-ttu-id="62598-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62598-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62598-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="62598-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62598-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62598-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62598-122">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="62598-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62598-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62598-123">Header files</span></span>

<span data-ttu-id="62598-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="62598-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="62598-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="62598-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="62598-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="62598-126">Mapitags.h</span></span>
  
> <span data-ttu-id="62598-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="62598-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62598-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="62598-128">See also</span></span>



[<span data-ttu-id="62598-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="62598-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62598-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="62598-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62598-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="62598-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62598-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="62598-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

