---
title: Propriedade canônica PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357607"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="1e6df-103">Propriedade canônica PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="1e6df-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="1e6df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e6df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e6df-105">Especifica a verificação de redundância cíclica de 32 bits (CRC-32) para uma lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="1e6df-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e6df-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1e6df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e6df-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="1e6df-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="1e6df-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="1e6df-108">Property set:</span></span>  <br/> |<span data-ttu-id="1e6df-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1e6df-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1e6df-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1e6df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1e6df-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="1e6df-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="1e6df-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1e6df-112">Data type:</span></span>  <br/> |<span data-ttu-id="1e6df-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e6df-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e6df-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1e6df-114">Area:</span></span>  <br/> |<span data-ttu-id="1e6df-115">Contato</span><span class="sxs-lookup"><span data-stu-id="1e6df-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e6df-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e6df-116">Remarks</span></span>

<span data-ttu-id="1e6df-117">O valor dessa propriedade pode ser usado para detectar quando a propriedade **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) foi atualizada sem Atualizar as outras propriedades de membros da lista de distribuição pessoal comparando o CRC-32 no existente valor de **dispidDLMembers** e comparando-o com o valor da propriedade **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="1e6df-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e6df-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e6df-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e6df-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="1e6df-119">Protocol specifications</span></span>

<span data-ttu-id="1e6df-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e6df-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e6df-121">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1e6df-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e6df-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e6df-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e6df-123">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="1e6df-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e6df-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1e6df-124">Header files</span></span>

<span data-ttu-id="1e6df-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1e6df-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e6df-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1e6df-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e6df-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e6df-127">See also</span></span>



[<span data-ttu-id="1e6df-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1e6df-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e6df-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1e6df-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e6df-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1e6df-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e6df-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1e6df-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

