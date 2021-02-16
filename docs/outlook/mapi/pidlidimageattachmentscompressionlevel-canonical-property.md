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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413826"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="3157c-103">Propriedade canônica PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="3157c-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="3157c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3157c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3157c-105">Define um nível de compactação a ser aplicado em anexos de imagem.</span><span class="sxs-lookup"><span data-stu-id="3157c-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3157c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3157c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3157c-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="3157c-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="3157c-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="3157c-108">Property set:</span></span>  <br/> |<span data-ttu-id="3157c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3157c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3157c-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3157c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3157c-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="3157c-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="3157c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3157c-112">Data type:</span></span>  <br/> |<span data-ttu-id="3157c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3157c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3157c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3157c-114">Area:</span></span>  <br/> |<span data-ttu-id="3157c-115">Configuração em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="3157c-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3157c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3157c-116">Remarks</span></span>

<span data-ttu-id="3157c-117">A seguir estão os níveis de compactação válidos:</span><span class="sxs-lookup"><span data-stu-id="3157c-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="3157c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3157c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3157c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3157c-119">Protocol specifications</span></span>

<span data-ttu-id="3157c-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3157c-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3157c-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3157c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3157c-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3157c-122">Header files</span></span>

<span data-ttu-id="3157c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3157c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3157c-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3157c-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3157c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3157c-125">See also</span></span>



[<span data-ttu-id="3157c-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3157c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3157c-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3157c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3157c-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3157c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3157c-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3157c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

