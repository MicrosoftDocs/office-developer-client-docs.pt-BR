---
title: Propriedade canônica PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357887"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="153e6-103">Propriedade canônica PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="153e6-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="153e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="153e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="153e6-105">Contém a versão do formato Rich Text (RTF) do texto da mensagem, geralmente em formato compactado.</span><span class="sxs-lookup"><span data-stu-id="153e6-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="153e6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="153e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="153e6-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="153e6-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="153e6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="153e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="153e6-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="153e6-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="153e6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="153e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="153e6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="153e6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="153e6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="153e6-112">Area:</span></span>  <br/> |<span data-ttu-id="153e6-113">Email</span><span class="sxs-lookup"><span data-stu-id="153e6-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="153e6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="153e6-114">Remarks</span></span>

<span data-ttu-id="153e6-115">Essa propriedade contém o mesmo texto de mensagem que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mas em RTF.</span><span class="sxs-lookup"><span data-stu-id="153e6-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="153e6-116">Normalmente, o texto da mensagem em RTF é armazenado em formato compactado.</span><span class="sxs-lookup"><span data-stu-id="153e6-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="153e6-117">No enTanto, alguns sistemas não compactam o texto formatado.</span><span class="sxs-lookup"><span data-stu-id="153e6-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="153e6-118">Para acomodá-los, o MAPI fornece o valor dwMagicUncompressedRTF para um cabeçalho de fluxo para identificar o RTF descompactado e o sinalizador **STORE_UNCOMPRESSED_RTF** no **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para a mensagem Store para indicar que pode armazenar RTF não compactado.</span><span class="sxs-lookup"><span data-stu-id="153e6-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="153e6-119">Para obter o conteúdo dessa propriedade, chame **OpenProperty**e, em seguida, chame [WrapCompressedRTFStream](wrapcompressedrtfstream.md) com o sinalizador **MAPI_READ** .</span><span class="sxs-lookup"><span data-stu-id="153e6-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="153e6-120">Para gravar nessa propriedade, abra-a com os sinalizadores **MAPI_MODIFY** e **MAPI_CREATE** .</span><span class="sxs-lookup"><span data-stu-id="153e6-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="153e6-121">Isso garante que os novos dados substituam completamente quaisquer dados antigos e que as gravações sejam realizadas usando o número mínimo de atualizações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="153e6-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="153e6-122">Os repositórios de mensagens que oferecem suporte a RTF ignoram qualquer alteração no espaço em branco no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="153e6-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="153e6-123">Quando o **PR_BODY** é armazenado pela primeira vez, o repositório de mensagens também gera e armazena essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="153e6-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="153e6-124">Se o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) for subsequentemente chamado e **PR_BODY** tiver sido modificado, o repositório de mensagens chamará a função [RTFSync](rtfsync.md) para garantir a sincronização com a versão RTF.</span><span class="sxs-lookup"><span data-stu-id="153e6-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="153e6-125">Se apenas o espaço em branco tiver sido alterado, as propriedades permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="153e6-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="153e6-126">Isso preserva qualquer formatação RTF não trivial quando a mensagem viaja por clientes e sistemas de mensagens que não reconhecem RTF.</span><span class="sxs-lookup"><span data-stu-id="153e6-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="153e6-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="153e6-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="153e6-128">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="153e6-128">Protocol specifications</span></span>

<span data-ttu-id="153e6-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="153e6-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="153e6-130">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="153e6-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="153e6-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="153e6-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="153e6-132">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="153e6-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="153e6-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="153e6-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="153e6-134">Codifica e decodifica um fluxo compactado em corpos de mensagens RTF.</span><span class="sxs-lookup"><span data-stu-id="153e6-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="153e6-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="153e6-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="153e6-136">Encapsula formatos de conteúdo adicionais (como HTML) dentro da propriedade de corpo RTF de mensagens e anexos.</span><span class="sxs-lookup"><span data-stu-id="153e6-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="153e6-137">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="153e6-137">Header files</span></span>

<span data-ttu-id="153e6-138">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="153e6-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="153e6-139">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="153e6-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="153e6-140">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="153e6-140">Mapitags.h</span></span>
  
> <span data-ttu-id="153e6-141">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="153e6-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="153e6-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="153e6-142">See also</span></span>



[<span data-ttu-id="153e6-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="153e6-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="153e6-144">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="153e6-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="153e6-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="153e6-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="153e6-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="153e6-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

