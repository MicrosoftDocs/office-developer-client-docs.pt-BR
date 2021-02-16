---
title: Propriedade canônica PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349214"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="92a2a-103">Propriedade canônica PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="92a2a-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="92a2a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92a2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92a2a-105">Especifica o ObjectID global **limpo.**</span><span class="sxs-lookup"><span data-stu-id="92a2a-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92a2a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="92a2a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92a2a-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="92a2a-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="92a2a-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="92a2a-108">Property set:</span></span>  <br/> |<span data-ttu-id="92a2a-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="92a2a-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="92a2a-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="92a2a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="92a2a-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="92a2a-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="92a2a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="92a2a-112">Data type:</span></span>  <br/> |<span data-ttu-id="92a2a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="92a2a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="92a2a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="92a2a-114">Area:</span></span>  <br/> |<span data-ttu-id="92a2a-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="92a2a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92a2a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a2a-116">Remarks</span></span>

<span data-ttu-id="92a2a-117">O formato dessa propriedade é o mesmo de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="92a2a-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="92a2a-118">O valor dessa propriedade deve ser igual ao valor de **LID_GLOBAL_OBJID**, exceto os campos YH, YL, M e D devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="92a2a-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="92a2a-119">Todos os objetos que se referem a uma Instância de uma série recorrente (incluindo uma instância órfã), bem como a própria série recorrente, terão o mesmo valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="92a2a-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92a2a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="92a2a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92a2a-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="92a2a-121">Protocol specifications</span></span>

<span data-ttu-id="92a2a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92a2a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92a2a-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="92a2a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92a2a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92a2a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92a2a-125">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="92a2a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92a2a-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="92a2a-126">Header files</span></span>

<span data-ttu-id="92a2a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92a2a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="92a2a-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="92a2a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92a2a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a2a-129">See also</span></span>



[<span data-ttu-id="92a2a-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="92a2a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92a2a-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="92a2a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92a2a-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="92a2a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92a2a-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="92a2a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

