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
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438180"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="4a3ef-103">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="4a3ef-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="4a3ef-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a3ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a3ef-105">Contém um objeto Table incorporado que contém identificadores de entrada de modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a3ef-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4a3ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a3ef-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="4a3ef-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="4a3ef-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a3ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a3ef-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="4a3ef-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="4a3ef-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4a3ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a3ef-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="4a3ef-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="4a3ef-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a3ef-112">Area:</span></span>  <br/> |<span data-ttu-id="4a3ef-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="4a3ef-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a3ef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a3ef-114">Remarks</span></span>

<span data-ttu-id="4a3ef-115">Para saber quais objetos de modelo podem ser criados dentro de um contêiner, chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="4a3ef-116">O objeto resultante é a tabela única que fornece os identificadores de entrada para todos os modelos que você pode criar dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="4a3ef-117">Para criar os objetos de modelo, chame o método **createentry** do objeto Container nos valores de coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da tabela one-off.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a3ef-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a3ef-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4a3ef-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a3ef-119">Header files</span></span>

<span data-ttu-id="4a3ef-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4a3ef-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a3ef-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a3ef-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4a3ef-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4a3ef-123">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a3ef-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a3ef-124">See also</span></span>



[<span data-ttu-id="4a3ef-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="4a3ef-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="4a3ef-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a3ef-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a3ef-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4a3ef-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a3ef-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4a3ef-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a3ef-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4a3ef-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

