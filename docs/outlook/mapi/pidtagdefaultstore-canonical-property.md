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
ms.openlocfilehash: 573ac849bba026ec6a5988220a7e49688393440d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769154"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="5b7c4-103">Propriedade canônica PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="5b7c4-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="5b7c4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b7c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b7c4-105">Conterá TRUE se um armazenamento de mensagens é o armazenamento de mensagens padrão na tabela de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5b7c4-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b7c4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5b7c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b7c4-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="5b7c4-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="5b7c4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5b7c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b7c4-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="5b7c4-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="5b7c4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5b7c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b7c4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5b7c4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5b7c4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5b7c4-112">Area:</span></span>  <br/> |<span data-ttu-id="5b7c4-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="5b7c4-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b7c4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b7c4-114">Remarks</span></span>

<span data-ttu-id="5b7c4-115">Essa propriedade é exibida como uma coluna na tabela de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5b7c4-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="5b7c4-116">O valor é baseado no **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5b7c4-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5b7c4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b7c4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b7c4-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5b7c4-118">Protocol specifications</span></span>

<span data-ttu-id="5b7c4-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7c4-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7c4-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5b7c4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b7c4-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b7c4-121">Header files</span></span>

<span data-ttu-id="5b7c4-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b7c4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b7c4-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5b7c4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b7c4-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b7c4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5b7c4-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5b7c4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b7c4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b7c4-126">See also</span></span>



[<span data-ttu-id="5b7c4-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b7c4-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b7c4-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5b7c4-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b7c4-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b7c4-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b7c4-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5b7c4-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

