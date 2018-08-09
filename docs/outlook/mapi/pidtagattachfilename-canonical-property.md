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
ms.openlocfilehash: 4468ecd5946c95fab62d0885d9c0b3343a1508dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768969"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="f4d9d-103">Propriedade canônica PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="f4d9d-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="f4d9d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4d9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4d9d-105">Contém o nome de base do arquivo e extensão, excluindo o caminho de um anexo.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4d9d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f4d9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4d9d-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="f4d9d-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="f4d9d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f4d9d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4d9d-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="f4d9d-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="f4d9d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f4d9d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4d9d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4d9d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4d9d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f4d9d-112">Area:</span></span>  <br/> |<span data-ttu-id="f4d9d-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="f4d9d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4d9d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4d9d-114">Remarks</span></span>

<span data-ttu-id="f4d9d-115">É recomendável que os objetos attachment exponham essas propriedades que pertencem aos valores da entrada de **PR_ATTACH_METHOD** **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**e **ATTACH_BY_REF_ONLY** Propriedade ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4d9d-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="f4d9d-116">**PR_ATTACH_FILENAME** e propriedades associadas são necessárias quando qualquer um desses valores é usado.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="f4d9d-117">Essas propriedades podem ser usadas como um nome de arquivo sugerido para salvar o anexo e fornecer a extensão de nome de arquivo, se a propriedade **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) não for fornecida.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="f4d9d-118">O nome de arquivo é restrito aos oito caracteres mais uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="f4d9d-119">Para uma plataforma que ofereça suporte a nomes longos de arquivos, defina essa propriedade e a propriedade **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4d9d-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="f4d9d-120">MAPI funciona somente com nomes de arquivo e outras cadeias de caracteres passada para ele, no conjunto de caracteres American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f4d9d-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="f4d9d-121">Aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres do fabricante do equipamento original (OEM) devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4d9d-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4d9d-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4d9d-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f4d9d-123">Protocol specifications</span></span>

<span data-ttu-id="f4d9d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d9d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d9d-125">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f4d9d-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d9d-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d9d-127">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f4d9d-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d9d-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d9d-129">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="f4d9d-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d9d-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d9d-131">Especifica o S/MIME assinadas e criptografadas propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="f4d9d-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d9d-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d9d-133">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4d9d-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4d9d-134">Header files</span></span>

<span data-ttu-id="f4d9d-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4d9d-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4d9d-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4d9d-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4d9d-137">Mapitags.h</span></span>
  
> <span data-ttu-id="f4d9d-138">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f4d9d-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4d9d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4d9d-139">See also</span></span>



[<span data-ttu-id="f4d9d-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d9d-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4d9d-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f4d9d-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4d9d-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d9d-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4d9d-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f4d9d-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

