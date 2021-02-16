---
title: Propriedade canônica PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319219"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="a1b95-103">Propriedade canônica PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="a1b95-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="a1b95-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1b95-105">Contém o nome e a extensão do arquivo base de um anexo, excluindo o caminho.</span><span class="sxs-lookup"><span data-stu-id="a1b95-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b95-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a1b95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1b95-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="a1b95-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="a1b95-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a1b95-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1b95-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="a1b95-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="a1b95-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a1b95-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1b95-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1b95-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a1b95-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a1b95-112">Area:</span></span>  <br/> |<span data-ttu-id="a1b95-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="a1b95-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1b95-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1b95-114">Remarks</span></span>

<span data-ttu-id="a1b95-115">É recomendável que os objetos anexos exponham essas propriedades que pertencem aos valores **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** e **ATTACH_BY_REF_ONLY** da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a1b95-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="a1b95-116">**PR_ATTACH_FILENAME** e as propriedades associadas são necessárias quando qualquer um desses valores é usado.</span><span class="sxs-lookup"><span data-stu-id="a1b95-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="a1b95-117">Essas propriedades podem ser usadas como um nome de arquivo sugerido para salvar o anexo e fornecer a extensão de nome de arquivo se a propriedade **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) não for fornecida.</span><span class="sxs-lookup"><span data-stu-id="a1b95-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="a1b95-118">O nome do arquivo é restrito a oito caracteres, além de uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1b95-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="a1b95-119">Para uma plataforma que oferece suporte a nomes de arquivo longos, de definir essa propriedade e a propriedade **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="a1b95-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="a1b95-120">O MAPI funciona apenas com nomes de arquivo e outras cadeias de caracteres passadas para ele, no conjunto de caracteres do American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a1b95-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="a1b95-121">Os aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres OEM (fabricante de equipamento original) devem convertê-los em ANSI antes de chamar o MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1b95-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1b95-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1b95-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1b95-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a1b95-123">Protocol specifications</span></span>

<span data-ttu-id="a1b95-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1b95-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1b95-125">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="a1b95-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a1b95-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1b95-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1b95-127">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a1b95-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a1b95-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1b95-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1b95-129">Especifica as propriedades de mensagens codificadas gerenciadas por direitos.</span><span class="sxs-lookup"><span data-stu-id="a1b95-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="a1b95-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1b95-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1b95-131">Especifica as propriedades de mensagem assinada e criptografada S/MIME.</span><span class="sxs-lookup"><span data-stu-id="a1b95-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="a1b95-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1b95-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1b95-133">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a1b95-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1b95-134">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a1b95-134">Header files</span></span>

<span data-ttu-id="a1b95-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1b95-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1b95-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a1b95-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1b95-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1b95-137">Mapitags.h</span></span>
  
> <span data-ttu-id="a1b95-138">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a1b95-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1b95-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1b95-139">See also</span></span>



[<span data-ttu-id="a1b95-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b95-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1b95-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b95-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1b95-142">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b95-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1b95-143">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a1b95-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

