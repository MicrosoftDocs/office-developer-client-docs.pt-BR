---
title: Propriedade canônica PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357873"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="c6264-103">Propriedade canônica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="c6264-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="c6264-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6264-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6264-105">Contém TRUE se a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tem o mesmo conteúdo de texto que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="c6264-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6264-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c6264-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6264-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="c6264-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="c6264-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c6264-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6264-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="c6264-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="c6264-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c6264-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6264-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c6264-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c6264-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c6264-112">Area:</span></span>  <br/> |<span data-ttu-id="c6264-113">Email</span><span class="sxs-lookup"><span data-stu-id="c6264-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6264-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6264-114">Remarks</span></span>

<span data-ttu-id="c6264-115">Um valor TRUE significa que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a versão de texto sem formatação dessa mensagem e a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a versão do formato Rich Text (RTF), são idênticas, exceto para espaço em branco no **PR_BODY** e formatação no **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="c6264-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="c6264-116">O texto nas duas versões consiste dos mesmos caracteres na mesma sequência.</span><span class="sxs-lookup"><span data-stu-id="c6264-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="c6264-117">Um valor FALSE significa que as duas versões não estão sincronizadas para conteúdo de texto, mas podem ser sincronizadas pela função [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="c6264-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="c6264-118">Uma versão foi alterada e a outra versão não.</span><span class="sxs-lookup"><span data-stu-id="c6264-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="c6264-119">Nenhum valor significa que as duas versões, se existirem ou já existiam, não poderão ser sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="c6264-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="c6264-120">Uma versão foi excluída ou alterada tão radicalmente que a sincronização não é mais possível.</span><span class="sxs-lookup"><span data-stu-id="c6264-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="c6264-121">Um aplicativo cliente que modificou o **PR_RTF_COMPRESSED** deve definir um valor false nessa propriedade para forçar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="c6264-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="c6264-122">Repositórios de mensagens com reconhecimento de RTF devem executar a sincronização usando o **RTFSync** durante uma chamada [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="c6264-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="c6264-123">Os clientes com reconhecimento de RTF devem verificar a configuração do **PR_RTF_IN_SYNC** antes de ler **PR_RTF_COMPRESSED**e chamar o **RTFSync** primeiro, se necessário.</span><span class="sxs-lookup"><span data-stu-id="c6264-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="c6264-124">Se o **PR_BODY** tiver modificações em algo diferente de seu espaço em branco, o repositório de mensagens deverá excluir **PR_RTF_IN_SYNC** para encerrar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="c6264-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6264-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6264-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6264-126">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="c6264-126">Protocol specifications</span></span>

<span data-ttu-id="c6264-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6264-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6264-128">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c6264-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6264-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6264-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6264-130">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="c6264-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6264-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c6264-131">Header files</span></span>

<span data-ttu-id="c6264-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c6264-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6264-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c6264-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6264-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c6264-134">Mapitags.h</span></span>
  
> <span data-ttu-id="c6264-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c6264-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6264-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6264-136">See also</span></span>



[<span data-ttu-id="c6264-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c6264-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6264-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6264-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6264-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c6264-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6264-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c6264-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

