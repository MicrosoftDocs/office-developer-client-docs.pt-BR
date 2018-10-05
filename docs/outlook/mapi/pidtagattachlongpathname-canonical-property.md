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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383104"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="a695d-103">Propriedade canônica PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="a695d-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="a695d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a695d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a695d-105">Contém o caminho longo totalmente qualificado e o nome de um anexo.</span><span class="sxs-lookup"><span data-stu-id="a695d-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a695d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a695d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a695d-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="a695d-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="a695d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a695d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a695d-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="a695d-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="a695d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a695d-110">Data type:</span></span>  <br/> |<span data-ttu-id="a695d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a695d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a695d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a695d-112">Area:</span></span>  <br/> |<span data-ttu-id="a695d-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="a695d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a695d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a695d-114">Remarks</span></span>

<span data-ttu-id="a695d-115">Essas propriedades são aplicáveis ao usar qualquer um dos valores da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indicam o anexo pela referência: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="a695d-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="a695d-116">Plataformas de nomes extensos de arquivos de suporte devem definir **PR_ATTACH_LONG_PATHNAME** ou propriedades associadas e propriedades de **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ao enviar e deve verificar \*\*PR_ATTACH_LONG_PATHNAME \*\*ou propriedades associadas inicialmente ao receber.</span><span class="sxs-lookup"><span data-stu-id="a695d-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="a695d-117">O aplicativo cliente deve definir essas propriedades para uma sugestão de caminho longo e o nome de arquivo a ser usado se a máquina host recebendo uma mensagem suporta nomes extensos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a695d-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="a695d-118">A definição dessas propriedades indica que os dados do anexo não estão incluídos com a mensagem, mas estão disponíveis em um servidor de arquivos comuns.</span><span class="sxs-lookup"><span data-stu-id="a695d-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="a695d-119">Ao contrário de diretórios e nomes de arquivo fornecido pelo **PR_ATTACH_PATHNAME**, esses nomes de arquivos e diretórios não são restritos a um diretório de oito caracteres ou filename além de extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="a695d-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="a695d-120">Em vez disso, cada diretório ou o nome de arquivo pode ser até 256 caracteres longos, incluindo o nome, a extensão e o período de separador.</span><span class="sxs-lookup"><span data-stu-id="a695d-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="a695d-121">No entanto, o caminho geral é limitado a 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a695d-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="a695d-122">Os clientes devem usar um caminho de convenção universal de nomenclatura (UNC) na maioria dos casos, quando o arquivo é compartilhado e deve usar um caminho absoluto quando o arquivo for local.</span><span class="sxs-lookup"><span data-stu-id="a695d-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="a695d-123">MAPI funciona somente com caminhos e nomes de arquivo ANSI do conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a695d-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="a695d-124">Aplicativos cliente que usam caminhos e nomes de arquivo em um conjunto de caracteres OEM deverá convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="a695d-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a695d-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a695d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a695d-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a695d-126">Protocol specifications</span></span>

<span data-ttu-id="a695d-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a695d-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a695d-128">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="a695d-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a695d-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a695d-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a695d-130">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a695d-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a695d-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a695d-131">Header files</span></span>

<span data-ttu-id="a695d-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a695d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="a695d-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a695d-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="a695d-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a695d-134">Mapitags.h</span></span>
  
> <span data-ttu-id="a695d-135">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a695d-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a695d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a695d-136">See also</span></span>



[<span data-ttu-id="a695d-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a695d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a695d-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a695d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a695d-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a695d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a695d-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a695d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

