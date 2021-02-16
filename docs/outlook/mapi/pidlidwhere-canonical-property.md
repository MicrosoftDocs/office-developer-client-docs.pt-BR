---
title: Propriedade canônica PidLidWhere
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360428"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="65420-103">Propriedade canônica PidLidWhere</span><span class="sxs-lookup"><span data-stu-id="65420-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="65420-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65420-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65420-105">Especifica o local de um evento.</span><span class="sxs-lookup"><span data-stu-id="65420-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65420-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="65420-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65420-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="65420-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="65420-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="65420-108">Property set:</span></span>  <br/> |<span data-ttu-id="65420-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="65420-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="65420-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="65420-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="65420-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="65420-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="65420-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="65420-112">Data type:</span></span>  <br/> |<span data-ttu-id="65420-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="65420-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="65420-114">Área:</span><span class="sxs-lookup"><span data-stu-id="65420-114">Area:</span></span>  <br/> |<span data-ttu-id="65420-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="65420-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65420-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="65420-116">Remarks</span></span>

<span data-ttu-id="65420-117">O valor dessa propriedade deve ser igual ao valor da propriedade **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) da reunião associada.</span><span class="sxs-lookup"><span data-stu-id="65420-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="65420-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="65420-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65420-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="65420-119">Protocol specifications</span></span>

<span data-ttu-id="65420-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65420-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65420-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="65420-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65420-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65420-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65420-123">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="65420-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65420-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="65420-124">Header files</span></span>

<span data-ttu-id="65420-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65420-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="65420-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="65420-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65420-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="65420-127">See also</span></span>



[<span data-ttu-id="65420-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="65420-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65420-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="65420-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65420-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="65420-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65420-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="65420-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

