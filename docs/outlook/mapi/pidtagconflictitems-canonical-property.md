---
title: Propriedade canônica PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338014"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="7f91c-103">Propriedade canônica PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="7f91c-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="7f91c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f91c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f91c-105">Contém uma ou mais IDs de entrada de itens envolvidos em uma resolução automática de conflitos.</span><span class="sxs-lookup"><span data-stu-id="7f91c-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7f91c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7f91c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f91c-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="7f91c-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="7f91c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7f91c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f91c-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="7f91c-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="7f91c-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="7f91c-110">Property type:</span></span>  <br/> |<span data-ttu-id="7f91c-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f91c-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f91c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7f91c-112">Area:</span></span>  <br/> |<span data-ttu-id="7f91c-113">ICS</span><span class="sxs-lookup"><span data-stu-id="7f91c-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f91c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f91c-114">Remarks</span></span>

<span data-ttu-id="7f91c-115">Os tipos de itens padrão do Microsoft Outlook que suportam a resolução automática de conflitos incluem os seguintes tipos de item padrão: itens de compromisso, itens de contato, itens de diário, itens de email, itens de reunião, itens de anotação sticky e itens de tarefa.</span><span class="sxs-lookup"><span data-stu-id="7f91c-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="7f91c-116">Um item pertencente a uma classe de mensagem que deriva de um desses tipos de item padrão também oferece suporte à resolução automática de conflitos.</span><span class="sxs-lookup"><span data-stu-id="7f91c-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="7f91c-117">No Microsoft Outlook 2003 e no Microsoft Office Outlook 2007, quando o Outlook sincroniza itens e considera que existe a possibilidade de  a cópia resultante  não conter todos os dados essenciais, o Outlook armazena as cópias conflitantes na pasta Conflitos, na pasta Problemas de Sincronização.</span><span class="sxs-lookup"><span data-stu-id="7f91c-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f91c-118">**Problemas de** sincronização e suas subpastas ficam ocultos até que você clique em **Lista** de Pastas **no** menu Ir.</span><span class="sxs-lookup"><span data-stu-id="7f91c-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="7f91c-119">Um item expõe a propriedade **PR_CONFLICT_ITEMS** se for um dos tipos de item que suportam resolução automática de  conflitos, tiver ganho em uma resolução de conflitos ou foi colocado na pasta Conflitos devido a uma resolução de conflitos.</span><span class="sxs-lookup"><span data-stu-id="7f91c-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="7f91c-120">A pasta na qual o item é colocado determina o conteúdo PR_CONFLICT_ITEMS **.**</span><span class="sxs-lookup"><span data-stu-id="7f91c-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="7f91c-121">Se o item estiver localizado em  alguma pasta diferente da pasta Conflitos e o item expor a propriedade **PR_CONFLICT_ITEMS,** o item deverá ter ganho a resolução de conflitos e **PR_CONFLICT_ITEMS** conterá uma ou mais IDs de entrada desses itens perdidos na resolução de conflitos.</span><span class="sxs-lookup"><span data-stu-id="7f91c-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="7f91c-122">Se o item estiver  localizado na pasta Conflitos e o item expor a propriedade **PR_CONFLICT_ITEMS,** esse item deverá ter perdido PR_CONFLICT_ITEMS resolução de conflitos e PR_CONFLICT_ITEMS conteria **a** ID de entrada do item que ganhou na resolução de conflitos.</span><span class="sxs-lookup"><span data-stu-id="7f91c-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7f91c-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f91c-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f91c-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7f91c-124">Protocol specifications</span></span>

<span data-ttu-id="7f91c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f91c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f91c-126">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7f91c-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f91c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f91c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f91c-128">Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="7f91c-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f91c-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7f91c-129">Header files</span></span>

<span data-ttu-id="7f91c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f91c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f91c-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7f91c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f91c-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f91c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="7f91c-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7f91c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f91c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f91c-134">See also</span></span>



[<span data-ttu-id="7f91c-135">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="7f91c-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="7f91c-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f91c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f91c-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7f91c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f91c-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7f91c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f91c-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7f91c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

