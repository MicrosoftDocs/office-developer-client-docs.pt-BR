---
title: Propriedade canônico de PidLidDistributionListMembers
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c27513474048e9805bc29116aa094bc47f8f0cae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768363"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="4e871-103">Propriedade canônico de PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="4e871-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="4e871-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e871-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e871-105">Especifica a lista de EntryIds dos objetos que correspondem aos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="4e871-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e871-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4e871-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e871-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="4e871-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="4e871-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4e871-108">Property set:</span></span>  <br/> |<span data-ttu-id="4e871-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="4e871-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="4e871-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4e871-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4e871-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="4e871-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="4e871-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4e871-112">Data type:</span></span>  <br/> |<span data-ttu-id="4e871-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4e871-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="4e871-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4e871-114">Area:</span></span>  <br/> |<span data-ttu-id="4e871-115">Contato</span><span class="sxs-lookup"><span data-stu-id="4e871-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e871-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4e871-116">Remarks</span></span>

<span data-ttu-id="4e871-117">Membros da lista de distribuição pessoal podem ser outras listas de distribuição pessoal, endereços eletrônicos contidos em um contato, os usuários da lista de endereços Global ou listas de distribuição ou endereços de email únicos.</span><span class="sxs-lookup"><span data-stu-id="4e871-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="4e871-118">O formato de cada EntryId deve ser uma EntryId único, conforme especificado na [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou uma EntryId com quebra.</span><span class="sxs-lookup"><span data-stu-id="4e871-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="4e871-119">Ao definir essa propriedade, o cliente ou o servidor deve assegurar que seu tamanho total for menor que 15.000 bytes.</span><span class="sxs-lookup"><span data-stu-id="4e871-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="4e871-120">Essa propriedade especifica a lista de EntryIds únicos que correspondem aos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="4e871-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="4e871-121">Esses EntryIds únicos encapsulam os nomes para exibição e endereços de email dos membros da lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="4e871-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="4e871-122">Se o cliente ou o servidor definir essa propriedade, ele deve ser sincronizado com esta propriedade **dispidDLMembers** para cada entrada na propriedade **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), deve haver uma entrada no mesma posição no **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="4e871-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e871-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e871-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e871-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4e871-124">Protocol specifications</span></span>

<span data-ttu-id="4e871-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e871-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e871-126">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4e871-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e871-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e871-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e871-128">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="4e871-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e871-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e871-129">Header files</span></span>

<span data-ttu-id="4e871-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e871-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e871-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4e871-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e871-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e871-132">See also</span></span>



[<span data-ttu-id="4e871-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e871-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e871-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4e871-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e871-135">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e871-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e871-136">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="4e871-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

