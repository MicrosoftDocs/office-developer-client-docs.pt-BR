---
title: Propriedade canônica PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342032"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="b1a05-103">Propriedade canônica PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="b1a05-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="b1a05-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1a05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1a05-105">Contém detalhes de personalização do usuário para exibir um contato como um cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="b1a05-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1a05-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b1a05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1a05-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="b1a05-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="b1a05-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="b1a05-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1a05-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b1a05-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b1a05-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b1a05-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1a05-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="b1a05-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="b1a05-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b1a05-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1a05-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1a05-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b1a05-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b1a05-114">Area:</span></span>  <br/> |<span data-ttu-id="b1a05-115">Contato</span><span class="sxs-lookup"><span data-stu-id="b1a05-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1a05-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1a05-116">Remarks</span></span>

<span data-ttu-id="b1a05-117">O layout de um cartão de visita pode ser representado como uma imagem e vários campos de texto.</span><span class="sxs-lookup"><span data-stu-id="b1a05-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="b1a05-118">A imagem pode ser uma foto de contato ou uma imagem de cartão.</span><span class="sxs-lookup"><span data-stu-id="b1a05-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="b1a05-119">Os campos de texto consistem em um valor de outra propriedade definida no contato e uma cadeia de caracteres de rótulo personalizada opcional fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b1a05-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="b1a05-120">Observe que os valores de vários byte são armazenados no formato little-endian no buffer.</span><span class="sxs-lookup"><span data-stu-id="b1a05-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b1a05-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1a05-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1a05-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b1a05-122">Protocol specifications</span></span>

<span data-ttu-id="b1a05-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1a05-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1a05-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b1a05-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1a05-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1a05-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1a05-126">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="b1a05-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1a05-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b1a05-127">Header files</span></span>

<span data-ttu-id="b1a05-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1a05-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1a05-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b1a05-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1a05-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1a05-130">See also</span></span>



[<span data-ttu-id="b1a05-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a05-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1a05-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a05-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1a05-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a05-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1a05-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b1a05-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

