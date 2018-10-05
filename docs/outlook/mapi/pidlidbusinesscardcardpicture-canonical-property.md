---
title: Propriedade canônica PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400394"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="0fd0b-103">Propriedade canônica PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="0fd0b-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="0fd0b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fd0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fd0b-105">Contém a imagem a ser usada em um cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="0fd0b-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fd0b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0fd0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fd0b-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="0fd0b-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="0fd0b-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="0fd0b-108">Property set:</span></span>  <br/> |<span data-ttu-id="0fd0b-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="0fd0b-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0fd0b-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="0fd0b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0fd0b-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="0fd0b-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="0fd0b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0fd0b-112">Data type:</span></span>  <br/> |<span data-ttu-id="0fd0b-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0fd0b-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0fd0b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0fd0b-114">Area:</span></span>  <br/> |<span data-ttu-id="0fd0b-115">Contato</span><span class="sxs-lookup"><span data-stu-id="0fd0b-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fd0b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fd0b-116">Remarks</span></span>

<span data-ttu-id="0fd0b-117">O valor dessa propriedade deve ser um fluxo JPEG ou arquivo PNG (PNG).</span><span class="sxs-lookup"><span data-stu-id="0fd0b-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="0fd0b-118">Esta propriedade deve ser usada em conjunto com a propriedade **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) da seguinte maneira: **dispidBCCardPicture** não deve estar presente em um contato se \*\* dispidBCDisplayDefinition\*\* não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="0fd0b-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="0fd0b-119">Essa propriedade também não deve estar presente se os dados em **dispidBCCardPicture** não exigem uma imagem do cartão.</span><span class="sxs-lookup"><span data-stu-id="0fd0b-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0fd0b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fd0b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fd0b-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0fd0b-121">Protocol specifications</span></span>

<span data-ttu-id="0fd0b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fd0b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fd0b-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0fd0b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fd0b-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fd0b-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fd0b-125">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="0fd0b-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fd0b-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0fd0b-126">Header files</span></span>

<span data-ttu-id="0fd0b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fd0b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fd0b-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0fd0b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fd0b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fd0b-129">See also</span></span>



[<span data-ttu-id="0fd0b-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0fd0b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fd0b-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0fd0b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fd0b-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0fd0b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fd0b-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0fd0b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

