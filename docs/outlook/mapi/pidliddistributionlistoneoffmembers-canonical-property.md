---
title: Propriedade canônica PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335046"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="8962a-103">Propriedade canônica PidLidDistributionListOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="8962a-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="8962a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8962a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8962a-105">Especifica a lista de EntryIds únicos que correspondem aos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="8962a-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8962a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8962a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8962a-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="8962a-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="8962a-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="8962a-108">Property set:</span></span>  <br/> |<span data-ttu-id="8962a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8962a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8962a-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8962a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8962a-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="8962a-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="8962a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8962a-112">Data type:</span></span>  <br/> |<span data-ttu-id="8962a-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8962a-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8962a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8962a-114">Area:</span></span>  <br/> |<span data-ttu-id="8962a-115">Contato</span><span class="sxs-lookup"><span data-stu-id="8962a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8962a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8962a-116">Remarks</span></span>

<span data-ttu-id="8962a-117">Esses EntryIds únicos encapsulam nomes de exibição e endereços de email dos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="8962a-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="8962a-118">Se o cliente ou o servidor definir essa propriedade, ele deverá ser sincronizado com a propriedade **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)): para cada entrada na propriedade **dispidDLOneOffMembers** , deverá haver uma entrada no mesmo posição na propriedade **dispidDLMembers** .</span><span class="sxs-lookup"><span data-stu-id="8962a-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="8962a-119">Ao definir **dispidDLOneOffMembers**, o cliente ou o servidor deve garantir que o tamanho total seja menor que 15.000 bytes de tamanho.</span><span class="sxs-lookup"><span data-stu-id="8962a-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8962a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8962a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8962a-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="8962a-121">Protocol specifications</span></span>

<span data-ttu-id="8962a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8962a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8962a-123">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8962a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8962a-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8962a-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8962a-125">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="8962a-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8962a-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8962a-126">Header files</span></span>

<span data-ttu-id="8962a-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8962a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8962a-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8962a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8962a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8962a-129">See also</span></span>



[<span data-ttu-id="8962a-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8962a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8962a-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8962a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8962a-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8962a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8962a-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8962a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

