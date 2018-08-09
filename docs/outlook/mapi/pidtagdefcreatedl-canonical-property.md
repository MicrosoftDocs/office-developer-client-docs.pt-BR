---
title: Propriedade canônica PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769166"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="d4498-103">Propriedade canônica PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="d4498-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="d4498-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4498-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4498-105">Contém o identificador de entrada do modelo para obter uma lista de distribuição padrão.</span><span class="sxs-lookup"><span data-stu-id="d4498-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4498-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d4498-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4498-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="d4498-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="d4498-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d4498-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4498-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="d4498-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="d4498-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d4498-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4498-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d4498-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d4498-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d4498-112">Area:</span></span>  <br/> |<span data-ttu-id="d4498-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="d4498-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4498-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4498-114">Remarks</span></span>

<span data-ttu-id="d4498-115">Aplicativos cliente usam essa propriedade para criar uma lista de distribuição dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="d4498-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="d4498-116">Suporte para criação de entrada é opcional para contêineres do catálogo de endereços; aqueles que não têm suporte não são necessárias para expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d4498-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="d4498-117">Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d4498-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="d4498-118">Depois de obter o identificador, o cliente usa-lo em uma chamada ao método [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="d4498-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="d4498-119">A entrada representa o modelo para a lista de distribuição padrão.</span><span class="sxs-lookup"><span data-stu-id="d4498-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d4498-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4498-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d4498-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4498-121">Header files</span></span>

<span data-ttu-id="d4498-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4498-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4498-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d4498-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4498-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4498-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d4498-125">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="d4498-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4498-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4498-126">See also</span></span>



[<span data-ttu-id="d4498-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="d4498-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="d4498-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d4498-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4498-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d4498-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4498-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d4498-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4498-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d4498-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

