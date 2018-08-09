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
ms.openlocfilehash: b9ea8af971f9a731aecab0ee6f4b8ea67b651643
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769644"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="48e71-103">Propriedade canônica PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="48e71-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="48e71-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48e71-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48e71-105">Contém o identificador de entrada ligação estreita armazenamento de um transporte de mensagens.</span><span class="sxs-lookup"><span data-stu-id="48e71-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48e71-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="48e71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48e71-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="48e71-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="48e71-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="48e71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48e71-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="48e71-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="48e71-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="48e71-110">Data type:</span></span>  <br/> |<span data-ttu-id="48e71-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48e71-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48e71-112">Área:</span><span class="sxs-lookup"><span data-stu-id="48e71-112">Area:</span></span>  <br/> |<span data-ttu-id="48e71-113">Propriedades do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="48e71-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48e71-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="48e71-114">Remarks</span></span>

<span data-ttu-id="48e71-115">Essa propriedade especifica o identificador de entrada para o repositório de ligação estreita, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="48e71-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="48e71-116">Por exemplo, um provedor de transporte pode especificar a pasta particular armazenar o identificador de entrada para que o MAPI spooler pode conectar o provedor de transporte para o repositório.</span><span class="sxs-lookup"><span data-stu-id="48e71-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48e71-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48e71-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="48e71-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="48e71-118">Header files</span></span>

<span data-ttu-id="48e71-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48e71-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="48e71-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="48e71-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="48e71-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48e71-121">Mapitags.h</span></span>
  
> <span data-ttu-id="48e71-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="48e71-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48e71-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="48e71-123">See also</span></span>



[<span data-ttu-id="48e71-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48e71-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48e71-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="48e71-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48e71-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="48e71-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48e71-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="48e71-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

