---
title: Propriedade canônica PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339365"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="30ab6-103">Propriedade canônica PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="30ab6-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="30ab6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ab6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ab6-105">Contém o caminho e o nome de arquivo longos totalmente qualificados de um anexo.</span><span class="sxs-lookup"><span data-stu-id="30ab6-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30ab6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="30ab6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30ab6-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="30ab6-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="30ab6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="30ab6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30ab6-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="30ab6-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="30ab6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="30ab6-110">Data type:</span></span>  <br/> |<span data-ttu-id="30ab6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="30ab6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="30ab6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="30ab6-112">Area:</span></span>  <br/> |<span data-ttu-id="30ab6-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="30ab6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30ab6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="30ab6-114">Remarks</span></span>

<span data-ttu-id="30ab6-115">Essas propriedades são aplicáveis quando você usa qualquer um dos valores da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indicam o anexo por referência: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="30ab6-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="30ab6-116">Plataformas que suportam nomes de filelong devem definir as propriedades **PR_ATTACH_LONG_PATHNAME** ou Associated Propriedades e **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ao enviar e verificar \*\*PR_ATTACH_LONG_PATHNAME \*\*ou propriedades associadas primeiro ao receber.</span><span class="sxs-lookup"><span data-stu-id="30ab6-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="30ab6-117">O aplicativo cliente deve definir essas propriedades como um caminho longo e um nome de arquivo sugeridos para serem usados se a máquina host que recebe uma mensagem suportar nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="30ab6-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="30ab6-118">A configuração dessas propriedades indica que os dados de anexo não estão incluídos na mensagem, mas estão disponíveis em um servidor de arquivos comum.</span><span class="sxs-lookup"><span data-stu-id="30ab6-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="30ab6-119">Diferentemente dos diretórios e nomes de arquivo fornecidos pelo **PR_ATTACH_PATHNAME**, esses diretórios e nomes de arquivo não estão restritos a um diretório de oito caracteres ou nome de arquivo, além de uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="30ab6-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="30ab6-120">Em vez disso, cada diretório ou nome de arquivo pode ter até 256 caracteres de comprimento, incluindo o nome, a extensão e o período separador.</span><span class="sxs-lookup"><span data-stu-id="30ab6-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="30ab6-121">No enTanto, o caminho geral está limitado a 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="30ab6-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="30ab6-122">Os clientes devem usar uma Convenção de nomenclatura universal (UNC) na maioria dos casos em que o arquivo é compartilhado e deve usar um caminho absoluto quando o arquivo for local.</span><span class="sxs-lookup"><span data-stu-id="30ab6-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="30ab6-123">O MAPI funciona somente com caminhos e nomes de fileset no conjunto de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="30ab6-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="30ab6-124">Os aplicativos clientes que usam caminhos e nomes de um conjunto de caracteres OEM devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="30ab6-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="30ab6-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="30ab6-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30ab6-126">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="30ab6-126">Protocol specifications</span></span>

<span data-ttu-id="30ab6-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30ab6-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30ab6-128">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="30ab6-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="30ab6-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30ab6-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30ab6-130">Especifica as propriedades de mensagens codificadas por direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="30ab6-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30ab6-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="30ab6-131">Header files</span></span>

<span data-ttu-id="30ab6-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="30ab6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="30ab6-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="30ab6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="30ab6-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="30ab6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="30ab6-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="30ab6-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30ab6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ab6-136">See also</span></span>



[<span data-ttu-id="30ab6-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="30ab6-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30ab6-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="30ab6-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30ab6-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="30ab6-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30ab6-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="30ab6-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

