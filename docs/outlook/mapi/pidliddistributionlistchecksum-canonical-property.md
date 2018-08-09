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
ms.openlocfilehash: bba1e78d79800b1c8e56ad50ce1abb144d4c9aae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768365"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="b5a2c-103">Propriedade canônica PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="b5a2c-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="b5a2c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5a2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5a2c-105">Especifica a redundância cíclica de 32 bits (CRC-32) de seleção polinomial soma de verificação para obter uma lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5a2c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b5a2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5a2c-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="b5a2c-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="b5a2c-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="b5a2c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b5a2c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b5a2c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b5a2c-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="b5a2c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b5a2c-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="b5a2c-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="b5a2c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b5a2c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b5a2c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b5a2c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b5a2c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b5a2c-114">Area:</span></span>  <br/> |<span data-ttu-id="b5a2c-115">Contato</span><span class="sxs-lookup"><span data-stu-id="b5a2c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5a2c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5a2c-116">Remarks</span></span>

<span data-ttu-id="b5a2c-117">O valor dessa propriedade pode ser usado para detectar quando a propriedade **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) foi atualizada sem atualizar as outras propriedades membro da lista particular de distribuição por computação CRC-32, em existentes valor do **dispidDLMembers** e comparando com o valor da propriedade **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="b5a2c-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b5a2c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5a2c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5a2c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b5a2c-119">Protocol specifications</span></span>

<span data-ttu-id="b5a2c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5a2c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5a2c-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5a2c-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5a2c-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5a2c-123">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5a2c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5a2c-124">Header files</span></span>

<span data-ttu-id="b5a2c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5a2c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5a2c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a2c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5a2c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5a2c-127">See also</span></span>



[<span data-ttu-id="b5a2c-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b5a2c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5a2c-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b5a2c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5a2c-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b5a2c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5a2c-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b5a2c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

