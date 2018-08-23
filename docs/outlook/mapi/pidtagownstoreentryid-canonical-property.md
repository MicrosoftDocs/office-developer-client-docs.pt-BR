---
title: Propriedade canônica PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 54014ab25d268c161465349b4e33c6a1df19f140
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591684"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="92624-103">Propriedade canônica PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="92624-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="92624-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92624-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92624-105">Contém o identificador de entrada ligação estreita armazenamento de um transporte de mensagens.</span><span class="sxs-lookup"><span data-stu-id="92624-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92624-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="92624-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92624-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="92624-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="92624-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="92624-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92624-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="92624-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="92624-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="92624-110">Data type:</span></span>  <br/> |<span data-ttu-id="92624-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="92624-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="92624-112">Área:</span><span class="sxs-lookup"><span data-stu-id="92624-112">Area:</span></span>  <br/> |<span data-ttu-id="92624-113">Propriedades do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="92624-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92624-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="92624-114">Remarks</span></span>

<span data-ttu-id="92624-115">Essa propriedade especifica o identificador de entrada para o repositório de ligação estreita, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="92624-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="92624-116">Por exemplo, um provedor de transporte pode especificar a pasta particular armazenar o identificador de entrada para que o MAPI spooler pode conectar o provedor de transporte para o repositório.</span><span class="sxs-lookup"><span data-stu-id="92624-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92624-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="92624-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="92624-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="92624-118">Header files</span></span>

<span data-ttu-id="92624-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92624-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="92624-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="92624-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="92624-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92624-121">Mapitags.h</span></span>
  
> <span data-ttu-id="92624-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="92624-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92624-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="92624-123">See also</span></span>



[<span data-ttu-id="92624-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="92624-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92624-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="92624-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92624-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="92624-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92624-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="92624-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

