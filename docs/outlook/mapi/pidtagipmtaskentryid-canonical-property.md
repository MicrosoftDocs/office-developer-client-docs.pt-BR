---
title: Propriedade canônica PidTagIpmTaskEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769404"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="6dd99-103">Propriedade canônica PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="6dd99-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6dd99-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dd99-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dd99-105">Contém a **EntryID** da pasta de tarefas do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6dd99-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6dd99-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6dd99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6dd99-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6dd99-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6dd99-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6dd99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6dd99-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="6dd99-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="6dd99-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6dd99-110">Data type:</span></span>  <br/> |<span data-ttu-id="6dd99-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6dd99-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6dd99-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6dd99-112">Area:</span></span>  <br/> |<span data-ttu-id="6dd99-113">Folder</span><span class="sxs-lookup"><span data-stu-id="6dd99-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dd99-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dd99-114">Remarks</span></span>

<span data-ttu-id="6dd99-115">Essa propriedade é lido ou gravada por meio do protocolo de propriedade e o objeto Stream.</span><span class="sxs-lookup"><span data-stu-id="6dd99-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="6dd99-116">Ele é lido a partir e gravado na pasta caixa de entrada ou de raiz.</span><span class="sxs-lookup"><span data-stu-id="6dd99-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="6dd99-117">A implementação deve usar a pasta de caixa de entrada quando o armazenamento é do usuário mensagens principal e ela deve usar a pasta raiz, quando o armazenamento é de um usuário delegado.</span><span class="sxs-lookup"><span data-stu-id="6dd99-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6dd99-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6dd99-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6dd99-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6dd99-119">Protocol specifications</span></span>

<span data-ttu-id="6dd99-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd99-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd99-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6dd99-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6dd99-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd99-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd99-123">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="6dd99-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="6dd99-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd99-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd99-125">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="6dd99-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6dd99-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6dd99-126">Header files</span></span>

<span data-ttu-id="6dd99-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dd99-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6dd99-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6dd99-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6dd99-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6dd99-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6dd99-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6dd99-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6dd99-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dd99-131">See also</span></span>



[<span data-ttu-id="6dd99-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd99-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6dd99-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6dd99-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6dd99-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd99-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6dd99-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6dd99-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
