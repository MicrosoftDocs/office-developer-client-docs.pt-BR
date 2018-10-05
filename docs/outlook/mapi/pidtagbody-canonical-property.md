---
title: Propriedade canônica PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392575"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="ad343-103">Propriedade canônica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="ad343-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="ad343-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad343-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad343-105">Contém o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ad343-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad343-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ad343-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad343-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="ad343-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="ad343-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ad343-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad343-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="ad343-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="ad343-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ad343-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad343-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ad343-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ad343-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ad343-112">Area:</span></span>  <br/> |<span data-ttu-id="ad343-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="ad343-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad343-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad343-114">Remarks</span></span>

<span data-ttu-id="ad343-115">Geralmente, essas propriedades são usadas somente em uma mensagem interpessoais (IPM).</span><span class="sxs-lookup"><span data-stu-id="ad343-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="ad343-116">Repositórios de mensagem que oferecem suporte ao formato Rich Text (RTF) ignoram quaisquer alterações para o espaço em branco no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ad343-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="ad343-117">Quando **PR_BODY** é armazenada pela primeira vez, o armazenamento de mensagens também gera e armazena a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a versão RTF do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ad343-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="ad343-118">Se o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado subsequentemente e **PR_BODY** foi modificado, o armazenamento de mensagens chama a função [RTFSync](rtfsync.md) para assegurar a sincronização com a versão RTF.</span><span class="sxs-lookup"><span data-stu-id="ad343-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="ad343-119">Se apenas o espaço em branco tiver sido alterado, as propriedades são deixadas inalteradas.</span><span class="sxs-lookup"><span data-stu-id="ad343-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="ad343-120">Isso preserva qualquer RTF não trivial formatação quando a mensagem passa por clientes sem reconhecimento de RTF e sistemas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ad343-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="ad343-121">O valor dessa propriedade deve ser expresso na página de código do sistema operacional que está executando o MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad343-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad343-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad343-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad343-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ad343-123">Protocol specifications</span></span>

<span data-ttu-id="ad343-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad343-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad343-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ad343-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad343-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad343-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad343-127">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="ad343-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad343-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ad343-128">Header files</span></span>

<span data-ttu-id="ad343-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad343-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad343-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ad343-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad343-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad343-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ad343-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ad343-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad343-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad343-133">See also</span></span>



[<span data-ttu-id="ad343-134">Propriedade canônica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="ad343-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="ad343-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ad343-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad343-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ad343-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad343-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ad343-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad343-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ad343-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

