---
title: Propriedade canônica PidTagDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385162"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="0bee2-103">Propriedade canônica PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="0bee2-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="0bee2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bee2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bee2-105">Conterá TRUE se um armazenamento de mensagens é o armazenamento de mensagens padrão na tabela de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0bee2-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bee2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0bee2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bee2-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="0bee2-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="0bee2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0bee2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0bee2-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="0bee2-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="0bee2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0bee2-110">Data type:</span></span>  <br/> |<span data-ttu-id="0bee2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0bee2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0bee2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0bee2-112">Area:</span></span>  <br/> |<span data-ttu-id="0bee2-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="0bee2-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bee2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bee2-114">Remarks</span></span>

<span data-ttu-id="0bee2-115">Essa propriedade é exibida como uma coluna na tabela de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0bee2-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="0bee2-116">O valor é baseado no **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0bee2-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0bee2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bee2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bee2-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0bee2-118">Protocol specifications</span></span>

<span data-ttu-id="0bee2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bee2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bee2-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0bee2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bee2-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0bee2-121">Header files</span></span>

<span data-ttu-id="0bee2-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bee2-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bee2-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0bee2-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0bee2-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0bee2-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0bee2-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0bee2-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bee2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bee2-126">See also</span></span>



[<span data-ttu-id="0bee2-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0bee2-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bee2-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0bee2-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bee2-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0bee2-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bee2-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0bee2-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

