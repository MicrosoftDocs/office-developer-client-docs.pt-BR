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
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="729bf-103">Propriedade canônica PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="729bf-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="729bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729bf-105">Contém o nome e a extensão do arquivo base de um anexo, excluindo o caminho.</span><span class="sxs-lookup"><span data-stu-id="729bf-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="729bf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="729bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="729bf-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="729bf-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="729bf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="729bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="729bf-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="729bf-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="729bf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="729bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="729bf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="729bf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="729bf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="729bf-112">Area:</span></span>  <br/> |<span data-ttu-id="729bf-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="729bf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="729bf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="729bf-114">Remarks</span></span>

<span data-ttu-id="729bf-115">É recomendável que os objetos Attachment exponham essas propriedades que pertencem aos valores de **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**e **ATTACH_BY_REF_ONLY** do **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) propriedade.</span><span class="sxs-lookup"><span data-stu-id="729bf-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="729bf-116">**PR_ATTACH_FILENAME** e as propriedades associadas são necessárias quando qualquer um desses valores é usado.</span><span class="sxs-lookup"><span data-stu-id="729bf-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="729bf-117">Essas propriedades podem ser usadas como um nome de arquivo sugerido para salvar o anexo e para fornecer a extensão de nome de arquivo se a propriedade **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) não for fornecida.</span><span class="sxs-lookup"><span data-stu-id="729bf-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="729bf-118">O nome do arquivo é restrito a oito caracteres mais uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="729bf-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="729bf-119">Para uma plataforma que suporte nomes de arquivo longos, defina essa propriedade e a propriedade **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="729bf-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="729bf-120">O MAPI funciona somente com nomes de arquivo e outras cadeias de caracteres passadas para ele, no conjunto de caracteres ANSI (American National Standards Institute).</span><span class="sxs-lookup"><span data-stu-id="729bf-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="729bf-121">Os aplicativos clientes que usam nomes de arquivo em um conjunto de caracteres OEM (fabricante original de equipamento) devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="729bf-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="729bf-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="729bf-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="729bf-123">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="729bf-123">Protocol specifications</span></span>

<span data-ttu-id="729bf-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729bf-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729bf-125">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="729bf-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="729bf-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729bf-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729bf-127">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="729bf-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="729bf-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729bf-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729bf-129">Especifica as propriedades de mensagens codificadas por direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="729bf-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="729bf-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729bf-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729bf-131">Especifica propriedades de mensagens assinadas e criptografadas S/MIME.</span><span class="sxs-lookup"><span data-stu-id="729bf-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="729bf-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729bf-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729bf-133">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="729bf-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="729bf-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="729bf-134">Header files</span></span>

<span data-ttu-id="729bf-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="729bf-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="729bf-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="729bf-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="729bf-137">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="729bf-137">Mapitags.h</span></span>
  
> <span data-ttu-id="729bf-138">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="729bf-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="729bf-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="729bf-139">See also</span></span>



[<span data-ttu-id="729bf-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="729bf-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="729bf-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="729bf-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="729bf-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="729bf-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="729bf-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="729bf-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

