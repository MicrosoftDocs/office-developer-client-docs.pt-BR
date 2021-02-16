---
title: Propriedade canônica PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335067"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="717d1-103">Propriedade canônica PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="717d1-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="717d1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="717d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="717d1-105">Especifica a lista de EntryIds dos objetos que correspondem aos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="717d1-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="717d1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="717d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="717d1-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="717d1-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="717d1-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="717d1-108">Property set:</span></span>  <br/> |<span data-ttu-id="717d1-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="717d1-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="717d1-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="717d1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="717d1-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="717d1-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="717d1-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="717d1-112">Data type:</span></span>  <br/> |<span data-ttu-id="717d1-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="717d1-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="717d1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="717d1-114">Area:</span></span>  <br/> |<span data-ttu-id="717d1-115">Contato</span><span class="sxs-lookup"><span data-stu-id="717d1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="717d1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="717d1-116">Remarks</span></span>

<span data-ttu-id="717d1-117">Os membros da lista de distribuição pessoal podem ser outras listas de distribuição pessoais, endereços eletrônicos contidos em um contato, usuários ou listas de distribuição da Lista de Endereços Global ou endereços de email único.</span><span class="sxs-lookup"><span data-stu-id="717d1-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="717d1-118">O formato de cada EntryId deve ser uma EntryId única, conforme especificado em [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou uma EntryId empacotada.</span><span class="sxs-lookup"><span data-stu-id="717d1-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="717d1-119">Ao definir essa propriedade, o cliente ou o servidor deve garantir que seu tamanho total seja inferior a 15.000 bytes.</span><span class="sxs-lookup"><span data-stu-id="717d1-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="717d1-120">Esta propriedade especifica a lista de EntryIds que correspondem aos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="717d1-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="717d1-121">Esses EntryIds one-off encapsulam nomes de exibição e endereços de email dos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="717d1-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="717d1-122">Se o cliente ou o servidor definir essa propriedade, ela deverá ser sincronizada com essa propriedade **dispidDLMembers** para cada entrada na **propriedade dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), deve haver uma entrada na mesma posição na **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="717d1-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="717d1-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="717d1-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="717d1-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="717d1-124">Protocol specifications</span></span>

<span data-ttu-id="717d1-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="717d1-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="717d1-126">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="717d1-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="717d1-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="717d1-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="717d1-128">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="717d1-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="717d1-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="717d1-129">Header files</span></span>

<span data-ttu-id="717d1-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="717d1-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="717d1-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="717d1-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="717d1-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="717d1-132">See also</span></span>



[<span data-ttu-id="717d1-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="717d1-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="717d1-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="717d1-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="717d1-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="717d1-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="717d1-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="717d1-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

