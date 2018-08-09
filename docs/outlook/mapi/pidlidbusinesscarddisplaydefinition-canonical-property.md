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
ms.openlocfilehash: 34d29b9a15cc6f5a3f88a6477738eb63904e1fdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768331"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="0a3ee-103">Propriedade canônica PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="0a3ee-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="0a3ee-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a3ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a3ee-105">Contém detalhes de personalização do usuário para a exibição de um contato como um cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a3ee-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0a3ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a3ee-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="0a3ee-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="0a3ee-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="0a3ee-108">Property set:</span></span>  <br/> |<span data-ttu-id="0a3ee-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="0a3ee-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0a3ee-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="0a3ee-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0a3ee-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="0a3ee-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="0a3ee-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0a3ee-112">Data type:</span></span>  <br/> |<span data-ttu-id="0a3ee-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0a3ee-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0a3ee-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0a3ee-114">Area:</span></span>  <br/> |<span data-ttu-id="0a3ee-115">Contato</span><span class="sxs-lookup"><span data-stu-id="0a3ee-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a3ee-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a3ee-116">Remarks</span></span>

<span data-ttu-id="0a3ee-117">O layout de um cartão de visita pode ser representado como uma imagem e um número de campos de texto.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="0a3ee-118">A imagem pode ser uma foto do contato ou uma imagem do cartão.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="0a3ee-119">Campos de texto consistem em um valor de propriedade de outra definido no contato e uma cadeia de caracteres do rótulo personalizado opcional fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="0a3ee-120">Observe que os valores de multibyte são armazenados no formato de pouca-endian no buffer.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a3ee-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a3ee-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a3ee-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0a3ee-122">Protocol specifications</span></span>

<span data-ttu-id="0a3ee-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a3ee-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a3ee-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a3ee-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a3ee-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a3ee-126">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a3ee-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0a3ee-127">Header files</span></span>

<span data-ttu-id="0a3ee-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a3ee-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a3ee-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0a3ee-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a3ee-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a3ee-130">See also</span></span>



[<span data-ttu-id="0a3ee-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0a3ee-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a3ee-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0a3ee-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a3ee-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0a3ee-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a3ee-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0a3ee-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
