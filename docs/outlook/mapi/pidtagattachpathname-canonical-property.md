---
title: Propriedade canônica PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389166"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="76ec8-103">Propriedade canônica PidTagAttachPathname</span><span class="sxs-lookup"><span data-stu-id="76ec8-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="76ec8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76ec8-105">Contém o caminho totalmente qualificado e o nome de um anexo.</span><span class="sxs-lookup"><span data-stu-id="76ec8-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76ec8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="76ec8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76ec8-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="76ec8-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="76ec8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="76ec8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76ec8-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="76ec8-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="76ec8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="76ec8-110">Data type:</span></span>  <br/> |<span data-ttu-id="76ec8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76ec8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="76ec8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="76ec8-112">Area:</span></span>  <br/> |<span data-ttu-id="76ec8-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="76ec8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76ec8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="76ec8-114">Remarks</span></span>

<span data-ttu-id="76ec8-115">É recomendável que o anexo subobjetos exponham essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="76ec8-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="76ec8-116">Defini-las indica que os dados do anexo não estão incluídos com a mensagem, mas estão disponíveis em um servidor de arquivos comuns.</span><span class="sxs-lookup"><span data-stu-id="76ec8-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="76ec8-117">Estas propriedades são necessárias em conjunto com qualquer um dos sinalizadores **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indicam o anexo pela referência: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY_REF_ SOMENTE**.</span><span class="sxs-lookup"><span data-stu-id="76ec8-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="76ec8-118">Cada diretório ou o nome de arquivo é restrito a um nome de oito caracteres mais uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="76ec8-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="76ec8-119">O caminho geral é restrito aos 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="76ec8-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="76ec8-120">Para uma plataforma que ofereça suporte a nomes extensos de arquivos, defina essas propriedades e o **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="76ec8-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="76ec8-121">Aplicativos cliente devem usar uma convenção de nomenclatura universal (UNC) na maioria dos casos, quando o arquivo é compartilhado e deve usar um caminho absoluto quando o arquivo for local.</span><span class="sxs-lookup"><span data-stu-id="76ec8-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="76ec8-122">MAPI funciona somente com caminhos e nomes de arquivo ANSI do conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76ec8-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="76ec8-123">Clientes que usam os caminhos e nomes de arquivo em um conjunto de caracteres OEM deverá convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="76ec8-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="76ec8-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="76ec8-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76ec8-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="76ec8-125">Protocol specifications</span></span>

<span data-ttu-id="76ec8-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ec8-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ec8-127">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="76ec8-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="76ec8-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ec8-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ec8-129">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="76ec8-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76ec8-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="76ec8-130">Header files</span></span>

<span data-ttu-id="76ec8-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76ec8-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="76ec8-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="76ec8-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="76ec8-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76ec8-133">Mapitags.h</span></span>
  
> <span data-ttu-id="76ec8-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="76ec8-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76ec8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="76ec8-135">See also</span></span>



[<span data-ttu-id="76ec8-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="76ec8-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="76ec8-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="76ec8-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="76ec8-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="76ec8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76ec8-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="76ec8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76ec8-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="76ec8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76ec8-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="76ec8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

