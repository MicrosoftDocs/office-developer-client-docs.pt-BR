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
ms.openlocfilehash: 48c068599506e5c050c69594caca46f28be83b0b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565799"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="0f24e-103">Propriedade canônica PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="0f24e-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="0f24e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f24e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f24e-105">Contém o identificador de entrada do modelo para obter uma lista de distribuição padrão.</span><span class="sxs-lookup"><span data-stu-id="0f24e-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f24e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0f24e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f24e-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="0f24e-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="0f24e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0f24e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f24e-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="0f24e-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="0f24e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0f24e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f24e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f24e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f24e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0f24e-112">Area:</span></span>  <br/> |<span data-ttu-id="0f24e-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="0f24e-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f24e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f24e-114">Remarks</span></span>

<span data-ttu-id="0f24e-115">Aplicativos cliente usam essa propriedade para criar uma lista de distribuição dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="0f24e-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="0f24e-116">Suporte para criação de entrada é opcional para contêineres do catálogo de endereços; aqueles que não têm suporte não são necessárias para expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0f24e-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="0f24e-117">Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="0f24e-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="0f24e-118">Depois de obter o identificador, o cliente usa-lo em uma chamada ao método [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="0f24e-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="0f24e-119">A entrada representa o modelo para a lista de distribuição padrão.</span><span class="sxs-lookup"><span data-stu-id="0f24e-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f24e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f24e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0f24e-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f24e-121">Header files</span></span>

<span data-ttu-id="0f24e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f24e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f24e-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0f24e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f24e-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f24e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0f24e-125">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="0f24e-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f24e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f24e-126">See also</span></span>



[<span data-ttu-id="0f24e-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0f24e-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="0f24e-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0f24e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f24e-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0f24e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f24e-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0f24e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f24e-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0f24e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

