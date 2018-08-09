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
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769885"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="20c75-103">Propriedade canônica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="20c75-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="20c75-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20c75-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20c75-105">Conterá TRUE se a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) tem o mesmo conteúdo de texto que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="20c75-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20c75-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="20c75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20c75-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="20c75-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="20c75-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="20c75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20c75-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="20c75-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="20c75-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="20c75-110">Data type:</span></span>  <br/> |<span data-ttu-id="20c75-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="20c75-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="20c75-112">Área:</span><span class="sxs-lookup"><span data-stu-id="20c75-112">Area:</span></span>  <br/> |<span data-ttu-id="20c75-113">Email</span><span class="sxs-lookup"><span data-stu-id="20c75-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20c75-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="20c75-114">Remarks</span></span>

<span data-ttu-id="20c75-115">Um valor de verdadeiro significa que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a versão de texto sem formatação dessa mensagem e a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a versão do formato Rich Text (RTF), são idênticas, exceto para espaço em branco no **PR_BODY** e a formatação **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="20c75-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="20c75-116">O texto nas duas versões consiste nos mesmos caracteres na mesma sequência.</span><span class="sxs-lookup"><span data-stu-id="20c75-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="20c75-117">Um valor FALSE significa que as duas versões não estão sincronizadas para conteúdo de texto, mas são capazes de sendo sincronizados pela função [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="20c75-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="20c75-118">Uma versão tenha sido alterada, e a outra versão não tem.</span><span class="sxs-lookup"><span data-stu-id="20c75-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="20c75-119">Nenhum valor significa que as duas versões, se ambos existirem ou existiam alguma, não podem ser sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="20c75-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="20c75-120">Uma versão foi excluída ou alterada radicalmente que sincronização não é mais possível.</span><span class="sxs-lookup"><span data-stu-id="20c75-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="20c75-121">Um aplicativo cliente que tenha modificado **PR_RTF_COMPRESSED** deve definir um valor False nessa propriedade para forçar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="20c75-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="20c75-122">Repositórios de mensagem RTF reconhecimento devem realizar a sincronização usando **RTFSync** durante uma chamada de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="20c75-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="20c75-123">Clientes de reconhecimento de RTF devem verificar a configuração de **PR_RTF_IN_SYNC** antes de ler **PR_RTF_COMPRESSED**e chamar **RTFSync** primeiro, se necessário.</span><span class="sxs-lookup"><span data-stu-id="20c75-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="20c75-124">Se **PR_BODY** teve modificações como algo diferente de seus espaços em branco, o armazenamento de mensagens deve excluir **PR_RTF_IN_SYNC** para encerrar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="20c75-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="20c75-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="20c75-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20c75-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="20c75-126">Protocol specifications</span></span>

<span data-ttu-id="20c75-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20c75-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20c75-128">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="20c75-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20c75-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20c75-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20c75-130">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="20c75-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20c75-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20c75-131">Header files</span></span>

<span data-ttu-id="20c75-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20c75-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="20c75-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="20c75-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="20c75-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20c75-134">Mapitags.h</span></span>
  
> <span data-ttu-id="20c75-135">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="20c75-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20c75-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="20c75-136">See also</span></span>



[<span data-ttu-id="20c75-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20c75-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20c75-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="20c75-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20c75-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="20c75-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20c75-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="20c75-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

