---
title: Propriedade canônica PidTagStoreState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399008"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="3e8e1-103">Propriedade canônica PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="3e8e1-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="3e8e1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e8e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e8e1-105">Contém um sinalizador que descreve o estado do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3e8e1-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e8e1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3e8e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e8e1-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="3e8e1-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="3e8e1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3e8e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e8e1-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="3e8e1-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="3e8e1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3e8e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e8e1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3e8e1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3e8e1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3e8e1-112">Area:</span></span>  <br/> |<span data-ttu-id="3e8e1-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8e1-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e8e1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e8e1-114">Remarks</span></span>

<span data-ttu-id="3e8e1-115">Essa propriedade é dinâmica e pode ser alterado com base nas ações do usuário, ao contrário da propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8e1-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="3e8e1-116">O seguinte valor pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3e8e1-116">The following value can be set:</span></span>
  
<span data-ttu-id="3e8e1-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="3e8e1-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="3e8e1-118">O usuário criou um ou mais pesquisas ativas no repositório.</span><span class="sxs-lookup"><span data-stu-id="3e8e1-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3e8e1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8e1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e8e1-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3e8e1-120">Protocol specifications</span></span>

<span data-ttu-id="3e8e1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e8e1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e8e1-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3e8e1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3e8e1-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e8e1-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e8e1-124">Especifica as operações permitidas para os objetos do repositório de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="3e8e1-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e8e1-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3e8e1-125">Header files</span></span>

<span data-ttu-id="3e8e1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e8e1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e8e1-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e8e1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e8e1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3e8e1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="3e8e1-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3e8e1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e8e1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e8e1-130">See also</span></span>



[<span data-ttu-id="3e8e1-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8e1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e8e1-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3e8e1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e8e1-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8e1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e8e1-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3e8e1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

