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
ms.openlocfilehash: a784c91a04cce572c8e30085b1760c28296a1d53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19768353"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="0b247-103">Propriedade canônica PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="0b247-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="0b247-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b247-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b247-105">Especifica o limpa global **ObjectID**.</span><span class="sxs-lookup"><span data-stu-id="0b247-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b247-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0b247-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b247-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="0b247-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="0b247-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="0b247-108">Property set:</span></span>  <br/> |<span data-ttu-id="0b247-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0b247-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0b247-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="0b247-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0b247-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="0b247-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="0b247-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0b247-112">Data type:</span></span>  <br/> |<span data-ttu-id="0b247-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0b247-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0b247-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0b247-114">Area:</span></span>  <br/> |<span data-ttu-id="0b247-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="0b247-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b247-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b247-116">Remarks</span></span>

<span data-ttu-id="0b247-117">O formato dessa propriedade é igual de **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0b247-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="0b247-118">O valor dessa propriedade deve ser igual ao valor de **LID_GLOBAL_OBJID**, exceto o YH, YL, M, e os campos de D devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="0b247-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="0b247-119">Todos os objetos que se referir a uma instância de uma série recorrente (incluindo uma instância órfão), bem como a série recorrente propriamente dito, terá o mesmo valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0b247-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b247-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b247-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b247-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b247-121">Protocol specifications</span></span>

<span data-ttu-id="0b247-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b247-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b247-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b247-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b247-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b247-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b247-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="0b247-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b247-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b247-126">Header files</span></span>

<span data-ttu-id="0b247-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b247-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b247-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0b247-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b247-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b247-129">See also</span></span>



[<span data-ttu-id="0b247-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b247-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b247-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0b247-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b247-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0b247-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b247-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0b247-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

