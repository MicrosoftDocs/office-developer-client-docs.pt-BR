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
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327838"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="6c1b4-103">Propriedade canônica PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="6c1b4-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6c1b4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c1b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c1b4-105">Contém a **EntryID** da pasta tarefas do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c1b4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6c1b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c1b4-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6c1b4-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6c1b4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6c1b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c1b4-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="6c1b4-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="6c1b4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6c1b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c1b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6c1b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6c1b4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6c1b4-112">Area:</span></span>  <br/> |<span data-ttu-id="6c1b4-113">Pasta</span><span class="sxs-lookup"><span data-stu-id="6c1b4-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c1b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c1b4-114">Remarks</span></span>

<span data-ttu-id="6c1b4-115">Essa propriedade é lida ou gravada usando o protocolo de objeto Property e Stream.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="6c1b4-116">Ele é lido e gravado na caixa de entrada ou na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="6c1b4-117">A implementação deve usar a pasta caixa de entrada quando o repositório é o do principal usuário de mensagens e deve usar a pasta raiz quando o repositório é o de um usuário delegado.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c1b4-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c1b4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c1b4-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="6c1b4-119">Protocol specifications</span></span>

<span data-ttu-id="6c1b4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c1b4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c1b4-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c1b4-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c1b4-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c1b4-123">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="6c1b4-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c1b4-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c1b4-125">Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c1b4-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c1b4-126">Header files</span></span>

<span data-ttu-id="6c1b4-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6c1b4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c1b4-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c1b4-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6c1b4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6c1b4-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6c1b4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c1b4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c1b4-131">See also</span></span>



[<span data-ttu-id="6c1b4-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c1b4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c1b4-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6c1b4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c1b4-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6c1b4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c1b4-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6c1b4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

