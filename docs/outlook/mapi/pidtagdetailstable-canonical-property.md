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
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585784"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="80ca5-103">Propriedade canônica PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="80ca5-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="80ca5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80ca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80ca5-105">Contém um objeto table de vídeo incorporado.</span><span class="sxs-lookup"><span data-stu-id="80ca5-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80ca5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="80ca5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80ca5-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="80ca5-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="80ca5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="80ca5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80ca5-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="80ca5-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="80ca5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="80ca5-110">Data type:</span></span>  <br/> |<span data-ttu-id="80ca5-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="80ca5-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="80ca5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="80ca5-112">Area:</span></span>  <br/> |<span data-ttu-id="80ca5-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="80ca5-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80ca5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="80ca5-114">Remarks</span></span>

<span data-ttu-id="80ca5-115">Passar essa propriedade para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para o objeto retorna uma interface de [IMAPITable](imapitableiunknown.md) que permite a criação da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="80ca5-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="80ca5-116">MAPI usa esta tabela para exibir as folhas de propriedades para um objeto do catálogo de endereços em resposta a uma chamada [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="80ca5-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="80ca5-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="80ca5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="80ca5-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="80ca5-118">Header files</span></span>

<span data-ttu-id="80ca5-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80ca5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="80ca5-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="80ca5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="80ca5-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80ca5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="80ca5-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="80ca5-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80ca5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="80ca5-123">See also</span></span>



[<span data-ttu-id="80ca5-124">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="80ca5-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="80ca5-125">Propriedade canônica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="80ca5-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="80ca5-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="80ca5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80ca5-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="80ca5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80ca5-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="80ca5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80ca5-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="80ca5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

