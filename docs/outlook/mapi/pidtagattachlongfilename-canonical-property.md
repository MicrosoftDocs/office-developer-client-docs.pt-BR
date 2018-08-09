---
title: Propriedade canônica PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0debee5d480c4ea0c0a8fb4b54d9fa5d92a45987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768967"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="521eb-103">Propriedade canônica PidTagAttachLongFilename</span><span class="sxs-lookup"><span data-stu-id="521eb-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="521eb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="521eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="521eb-105">Contém o nome de arquivo longo e extensão, excluindo o caminho de um anexo.</span><span class="sxs-lookup"><span data-stu-id="521eb-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="521eb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="521eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="521eb-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="521eb-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="521eb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="521eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="521eb-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="521eb-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="521eb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="521eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="521eb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="521eb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="521eb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="521eb-112">Area:</span></span>  <br/> |<span data-ttu-id="521eb-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="521eb-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="521eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="521eb-114">Remarks</span></span>

<span data-ttu-id="521eb-115">Essas propriedades relativas aos valores da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE e ATTACH_BY_REF_ONLY.</span><span class="sxs-lookup"><span data-stu-id="521eb-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="521eb-116">Plataformas de nomes extensos de arquivos de suporte devem definir propriedades de **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) e o **PR_ATTACH_LONG_FILENAME** ao enviar e deve verificar **PR_ATTACH_LONG_FILENAME** que primeiro quando recebendo.</span><span class="sxs-lookup"><span data-stu-id="521eb-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="521eb-117">O aplicativo cliente deve definir essa propriedade como um nome de arquivo longo sugerido a ser usado se o computador host que você receber uma mensagem suporta nomes extensos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="521eb-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="521eb-118">**PR_ATTACH_LONG_FILENAME** pode ser usado como um nome de arquivo para salvar o anexo e fornecer a extensão de nome de arquivo, se a propriedade **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) não for fornecida.</span><span class="sxs-lookup"><span data-stu-id="521eb-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="521eb-119">Diferentemente o nome de arquivo fornecido pelo **PR_ATTACH_FILENAME**, esse nome não é restrito a um nome de arquivo de oito caracteres mais uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="521eb-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="521eb-120">Em vez disso, pode ser até 256 caracteres longos, incluindo o período de nome de arquivo, extensão e separador.</span><span class="sxs-lookup"><span data-stu-id="521eb-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="521eb-121">MAPI funciona somente com nomes de arquivo no conjunto de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="521eb-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="521eb-122">Aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres OEM deverá convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="521eb-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="521eb-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="521eb-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="521eb-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="521eb-124">Protocol specifications</span></span>

<span data-ttu-id="521eb-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521eb-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521eb-126">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="521eb-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="521eb-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521eb-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521eb-128">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="521eb-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="521eb-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521eb-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521eb-130">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="521eb-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="521eb-131">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521eb-131">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521eb-132">Especifica as propriedades e operações que são permitidas para representar mensagens de caixa postal e fax.</span><span class="sxs-lookup"><span data-stu-id="521eb-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="521eb-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="521eb-133">Header files</span></span>

<span data-ttu-id="521eb-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="521eb-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="521eb-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="521eb-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="521eb-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="521eb-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="521eb-137">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="521eb-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="521eb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="521eb-138">See also</span></span>



[<span data-ttu-id="521eb-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="521eb-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="521eb-140">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="521eb-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="521eb-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="521eb-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="521eb-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="521eb-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
