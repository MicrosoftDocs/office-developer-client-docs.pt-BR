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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326632"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="40a23-103">Propriedade canônica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="40a23-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="40a23-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40a23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40a23-105">Contém o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="40a23-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40a23-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="40a23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40a23-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="40a23-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="40a23-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="40a23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40a23-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="40a23-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="40a23-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="40a23-110">Data type:</span></span>  <br/> |<span data-ttu-id="40a23-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="40a23-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="40a23-112">Área:</span><span class="sxs-lookup"><span data-stu-id="40a23-112">Area:</span></span>  <br/> |<span data-ttu-id="40a23-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="40a23-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40a23-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="40a23-114">Remarks</span></span>

<span data-ttu-id="40a23-115">Essas propriedades normalmente são usadas somente em uma mensagem interpessoal (IPM).</span><span class="sxs-lookup"><span data-stu-id="40a23-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="40a23-116">Os repositórios de mensagens que dão suporte ao formato Rich Text (RTF) ignoram as alterações feitas no espaço em branco no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="40a23-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="40a23-117">Quando o **PR_BODY** é armazenado pela primeira vez, o repositório de mensagens também gera e armazena a propriedade **PR_RTF_COMPRESSED** ([PIDTAGRTFCOMPRESSED](pidtagrtfcompressed-canonical-property.md)), a versão rtf do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="40a23-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="40a23-118">Se o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) for subsequentemente chamado e **PR_BODY** tiver sido modificado, o repositório de mensagens chamará a função [RTFSync](rtfsync.md) para garantir a sincronização com a versão RTF.</span><span class="sxs-lookup"><span data-stu-id="40a23-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="40a23-119">Se apenas o espaço em branco tiver sido alterado, as propriedades permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="40a23-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="40a23-120">Isso preserva qualquer formatação RTF não trivial quando a mensagem viaja por clientes e sistemas de mensagens que não reconhecem RTF.</span><span class="sxs-lookup"><span data-stu-id="40a23-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="40a23-121">O valor dessa propriedade deve ser expresso na página de código do sistema operacional em que o MAPI está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="40a23-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="40a23-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="40a23-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40a23-123">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="40a23-123">Protocol specifications</span></span>

<span data-ttu-id="40a23-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40a23-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40a23-125">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="40a23-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40a23-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40a23-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40a23-127">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="40a23-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40a23-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="40a23-128">Header files</span></span>

<span data-ttu-id="40a23-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="40a23-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="40a23-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="40a23-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="40a23-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="40a23-131">Mapitags.h</span></span>
  
> <span data-ttu-id="40a23-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="40a23-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40a23-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a23-133">See also</span></span>



[<span data-ttu-id="40a23-134">Propriedade canônica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="40a23-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="40a23-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="40a23-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40a23-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="40a23-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40a23-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="40a23-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40a23-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="40a23-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

