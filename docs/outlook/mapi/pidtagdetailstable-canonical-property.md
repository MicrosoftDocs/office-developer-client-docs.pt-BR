---
title: Propriedade canônica PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769170"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="20bb4-103">Propriedade canônica PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="20bb4-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="20bb4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20bb4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20bb4-105">Contém um objeto table de vídeo incorporado.</span><span class="sxs-lookup"><span data-stu-id="20bb4-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20bb4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="20bb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20bb4-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="20bb4-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="20bb4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="20bb4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20bb4-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="20bb4-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="20bb4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="20bb4-110">Data type:</span></span>  <br/> |<span data-ttu-id="20bb4-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="20bb4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="20bb4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="20bb4-112">Area:</span></span>  <br/> |<span data-ttu-id="20bb4-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="20bb4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20bb4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="20bb4-114">Remarks</span></span>

<span data-ttu-id="20bb4-115">Passar essa propriedade para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para o objeto retorna uma interface de [IMAPITable](imapitableiunknown.md) que permite a criação da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="20bb4-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="20bb4-116">MAPI usa esta tabela para exibir as folhas de propriedades para um objeto do catálogo de endereços em resposta a uma chamada [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="20bb4-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="20bb4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="20bb4-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="20bb4-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20bb4-118">Header files</span></span>

<span data-ttu-id="20bb4-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20bb4-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="20bb4-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="20bb4-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="20bb4-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20bb4-121">Mapitags.h</span></span>
  
> <span data-ttu-id="20bb4-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="20bb4-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20bb4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="20bb4-123">See also</span></span>



[<span data-ttu-id="20bb4-124">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="20bb4-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="20bb4-125">Propriedade canônica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="20bb4-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="20bb4-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20bb4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20bb4-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="20bb4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20bb4-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="20bb4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20bb4-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="20bb4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

