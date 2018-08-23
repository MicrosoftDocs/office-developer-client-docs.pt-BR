---
title: Propriedade canônica PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563356"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="8f9c2-103">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="8f9c2-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="8f9c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f9c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f9c2-105">Contém um objeto incorporado de tabela que contém os identificadores de entrada de modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8f9c2-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f9c2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8f9c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f9c2-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="8f9c2-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="8f9c2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8f9c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f9c2-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="8f9c2-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="8f9c2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8f9c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f9c2-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8f9c2-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8f9c2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8f9c2-112">Area:</span></span>  <br/> |<span data-ttu-id="8f9c2-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="8f9c2-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f9c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f9c2-114">Remarks</span></span>

<span data-ttu-id="8f9c2-115">Para saber qual modelo de objetos que podem ser criados dentro de um contêiner, chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8f9c2-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="8f9c2-116">O objeto resultante é a tabela único que oferece os identificadores de entrada para todos os modelos que você pode criar dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8f9c2-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="8f9c2-117">Para criar os objetos do modelo, chame o método de **CreateEntry** do objeto container nos valores de coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da tabela único.</span><span class="sxs-lookup"><span data-stu-id="8f9c2-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f9c2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f9c2-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8f9c2-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8f9c2-119">Header files</span></span>

<span data-ttu-id="8f9c2-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f9c2-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f9c2-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8f9c2-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f9c2-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8f9c2-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8f9c2-123">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8f9c2-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f9c2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f9c2-124">See also</span></span>



[<span data-ttu-id="8f9c2-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="8f9c2-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="8f9c2-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8f9c2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f9c2-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8f9c2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f9c2-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8f9c2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f9c2-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8f9c2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

