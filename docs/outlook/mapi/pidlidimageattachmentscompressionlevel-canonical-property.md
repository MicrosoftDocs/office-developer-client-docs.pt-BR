---
title: Propriedade canônica PidLidImageAttachmentsCompressionLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357579"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="75eeb-103">Propriedade canônica PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="75eeb-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="75eeb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75eeb-105">Define um nível de compactação a ser aplicado em anexos de imagem.</span><span class="sxs-lookup"><span data-stu-id="75eeb-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75eeb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="75eeb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75eeb-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="75eeb-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="75eeb-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="75eeb-108">Property set:</span></span>  <br/> |<span data-ttu-id="75eeb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="75eeb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="75eeb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="75eeb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75eeb-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="75eeb-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="75eeb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="75eeb-112">Data type:</span></span>  <br/> |<span data-ttu-id="75eeb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75eeb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75eeb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="75eeb-114">Area:</span></span>  <br/> |<span data-ttu-id="75eeb-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="75eeb-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75eeb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="75eeb-116">Remarks</span></span>

<span data-ttu-id="75eeb-117">Os seguintes níveis de compactação são válidos:</span><span class="sxs-lookup"><span data-stu-id="75eeb-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="75eeb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75eeb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75eeb-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="75eeb-119">Protocol specifications</span></span>

<span data-ttu-id="75eeb-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="75eeb-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="75eeb-121">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="75eeb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75eeb-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75eeb-122">Header files</span></span>

<span data-ttu-id="75eeb-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="75eeb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="75eeb-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="75eeb-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75eeb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="75eeb-125">See also</span></span>



[<span data-ttu-id="75eeb-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75eeb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75eeb-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="75eeb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75eeb-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="75eeb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75eeb-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="75eeb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

