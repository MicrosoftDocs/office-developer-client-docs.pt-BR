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
ms.openlocfilehash: 44752e147569619589b23a380b2fefa511724ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571728"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="400fd-103">Propriedade canônica PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="400fd-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="400fd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="400fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="400fd-105">Especifica a redundância cíclica de 32 bits (CRC-32) de seleção polinomial soma de verificação para obter uma lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="400fd-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="400fd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="400fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="400fd-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="400fd-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="400fd-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="400fd-108">Property set:</span></span>  <br/> |<span data-ttu-id="400fd-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="400fd-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="400fd-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="400fd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="400fd-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="400fd-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="400fd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="400fd-112">Data type:</span></span>  <br/> |<span data-ttu-id="400fd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="400fd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="400fd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="400fd-114">Area:</span></span>  <br/> |<span data-ttu-id="400fd-115">Contato</span><span class="sxs-lookup"><span data-stu-id="400fd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="400fd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="400fd-116">Remarks</span></span>

<span data-ttu-id="400fd-117">O valor dessa propriedade pode ser usado para detectar quando a propriedade **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) foi atualizada sem atualizar as outras propriedades membro da lista particular de distribuição por computação CRC-32, em existentes valor do **dispidDLMembers** e comparando com o valor da propriedade **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="400fd-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="400fd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="400fd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="400fd-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="400fd-119">Protocol specifications</span></span>

<span data-ttu-id="400fd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="400fd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="400fd-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="400fd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="400fd-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="400fd-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="400fd-123">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="400fd-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="400fd-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="400fd-124">Header files</span></span>

<span data-ttu-id="400fd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="400fd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="400fd-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="400fd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="400fd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="400fd-127">See also</span></span>



[<span data-ttu-id="400fd-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="400fd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="400fd-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="400fd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="400fd-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="400fd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="400fd-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="400fd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

