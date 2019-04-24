---
title: Propriedade canônica PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329264"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="3d286-103">Propriedade canônica PidTagNull</span><span class="sxs-lookup"><span data-stu-id="3d286-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="3d286-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d286-105">Representa um valor nulo ou configuração de uma propriedade ou reserva espaço de matriz.</span><span class="sxs-lookup"><span data-stu-id="3d286-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d286-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3d286-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d286-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="3d286-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="3d286-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3d286-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d286-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="3d286-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="3d286-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3d286-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d286-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="3d286-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="3d286-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3d286-112">Area:</span></span>  <br/> |<span data-ttu-id="3d286-113">Comum</span><span class="sxs-lookup"><span data-stu-id="3d286-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d286-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d286-114">Remarks</span></span>

<span data-ttu-id="3d286-115">Essa propriedade é usada para reservar espaço em matrizes de estruturas [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="3d286-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="3d286-116">Ele é usado em uma matriz de estruturas [SPropTagArray](sproptagarray.md) para dizer ao método para reservar espaço na matriz retornada de estruturas **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="3d286-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="3d286-117">Isso permite que as propriedades calculadas sejam preenchidas de forma barata.</span><span class="sxs-lookup"><span data-stu-id="3d286-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="3d286-118">Para obter mais informações, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3d286-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d286-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d286-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d286-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3d286-120">Protocol specifications</span></span>

<span data-ttu-id="3d286-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d286-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d286-122">Especifica as propriedades e as operações que são permitidas em contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="3d286-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d286-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d286-123">Header files</span></span>

<span data-ttu-id="3d286-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3d286-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d286-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3d286-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d286-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3d286-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3d286-127">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="3d286-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d286-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d286-128">See also</span></span>



[<span data-ttu-id="3d286-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3d286-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d286-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3d286-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d286-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3d286-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d286-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3d286-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

