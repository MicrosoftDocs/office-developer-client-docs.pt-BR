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
ms.openlocfilehash: 55b965374bb1d7e5859f0cac5cc2f61956ea5b55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578917"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="7b954-103">Propriedade canônica PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="7b954-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="7b954-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b954-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b954-105">Define um nível de compactação a ser aplicado em anexos de imagem.</span><span class="sxs-lookup"><span data-stu-id="7b954-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b954-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7b954-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b954-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="7b954-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="7b954-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="7b954-108">Property set:</span></span>  <br/> |<span data-ttu-id="7b954-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7b954-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7b954-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="7b954-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7b954-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="7b954-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="7b954-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7b954-112">Data type:</span></span>  <br/> |<span data-ttu-id="7b954-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7b954-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7b954-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7b954-114">Area:</span></span>  <br/> |<span data-ttu-id="7b954-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7b954-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b954-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b954-116">Remarks</span></span>

<span data-ttu-id="7b954-117">Estes são os níveis de compactação válidos:</span><span class="sxs-lookup"><span data-stu-id="7b954-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="7b954-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b954-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b954-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7b954-119">Protocol specifications</span></span>

<span data-ttu-id="7b954-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="7b954-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="7b954-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7b954-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b954-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7b954-122">Header files</span></span>

<span data-ttu-id="7b954-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b954-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b954-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7b954-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b954-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b954-125">See also</span></span>



[<span data-ttu-id="7b954-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7b954-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b954-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7b954-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b954-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7b954-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b954-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7b954-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

