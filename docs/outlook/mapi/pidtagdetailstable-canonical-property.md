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
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419251"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="31832-103">Propriedade canônica PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="31832-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="31832-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31832-105">Contém um objeto de tabela de exibição incorporado.</span><span class="sxs-lookup"><span data-stu-id="31832-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31832-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="31832-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31832-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="31832-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="31832-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="31832-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31832-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="31832-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="31832-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="31832-110">Data type:</span></span>  <br/> |<span data-ttu-id="31832-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="31832-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="31832-112">Área:</span><span class="sxs-lookup"><span data-stu-id="31832-112">Area:</span></span>  <br/> |<span data-ttu-id="31832-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="31832-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31832-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="31832-114">Remarks</span></span>

<span data-ttu-id="31832-115">Passar essa propriedade para o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para o objeto retorna uma interface [IMAPITable](imapitableiunknown.md) que permite a criação da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="31832-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="31832-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::D etails](iaddrbook-details.md) call.</span><span class="sxs-lookup"><span data-stu-id="31832-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31832-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="31832-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="31832-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="31832-118">Header files</span></span>

<span data-ttu-id="31832-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31832-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="31832-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="31832-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="31832-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31832-121">Mapitags.h</span></span>
  
> <span data-ttu-id="31832-122">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="31832-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31832-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="31832-123">See also</span></span>



[<span data-ttu-id="31832-124">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="31832-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="31832-125">Propriedade canônica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="31832-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="31832-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="31832-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31832-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="31832-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31832-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="31832-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31832-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="31832-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

