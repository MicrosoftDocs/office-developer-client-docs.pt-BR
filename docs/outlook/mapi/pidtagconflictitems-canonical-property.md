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
ms.openlocfilehash: 61176ec6f9ff00fa5a38a2b385cb5281fa40961e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769035"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="e2a97-103">Propriedade canônica PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="e2a97-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="e2a97-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2a97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2a97-105">Contém uma ou mais IDs de itens que participaram de resolução de conflitos automática de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2a97-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="e2a97-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e2a97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2a97-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="e2a97-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="e2a97-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e2a97-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2a97-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="e2a97-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="e2a97-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="e2a97-110">Property type:</span></span>  <br/> |<span data-ttu-id="e2a97-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e2a97-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e2a97-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e2a97-112">Area:</span></span>  <br/> |<span data-ttu-id="e2a97-113">ICS</span><span class="sxs-lookup"><span data-stu-id="e2a97-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2a97-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2a97-114">Remarks</span></span>

<span data-ttu-id="e2a97-115">Os tipos de itens padrão do Microsoft Outlook que oferecem suporte a resolução de conflito automática incluem os seguintes tipos de item padrão: itens de compromisso, itens de contato, itens de diário, itens de email, itens de reunião, itens de nota e itens de tarefa.</span><span class="sxs-lookup"><span data-stu-id="e2a97-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="e2a97-116">Um item que pertence a uma classe de mensagem que derive de um desses tipos de item padrão também dá suporte a resolução de conflitos automática.</span><span class="sxs-lookup"><span data-stu-id="e2a97-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="e2a97-117">No Microsoft Outlook 2003 e o Microsoft Office Outlook 2007, quando o Outlook sincroniza os itens e considera que existe uma possibilidade de que a cópia resultante não pode conter todos os dados essenciais, o Outlook armazena as cópias conflitantes nos **conflitos** pasta, sob a pasta **Problemas de sincronização** .</span><span class="sxs-lookup"><span data-stu-id="e2a97-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e2a97-118">**Problemas de sincronização** e suas subpastas estão ocultas até você clicar em **Lista de pastas** no menu **Ir** .</span><span class="sxs-lookup"><span data-stu-id="e2a97-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="e2a97-119">Um item expõe a propriedade **PR_CONFLICT_ITEMS** se ele é um dos tipos de item que oferecem suporte a resolução de conflito automática, ganhou em uma resolução de conflito ou foi colocado na pasta **conflitos** devido a uma resolução de conflito.</span><span class="sxs-lookup"><span data-stu-id="e2a97-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="e2a97-120">A pasta na qual o item é colocado determina o conteúdo de **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="e2a97-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="e2a97-121">Se o item está localizado em alguma pasta que não seja a pasta **conflitos** e o item expõe a propriedade **PR_CONFLICT_ITEMS** , o item deve ter won a resolução de conflito e **PR_CONFLICT_ITEMS** conteria identificações de entrada de uma ou mais das os itens que perdidas na resolução de conflito.</span><span class="sxs-lookup"><span data-stu-id="e2a97-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="e2a97-122">Se o item está localizado na pasta **conflitos** e o item expõe a propriedade **PR_CONFLICT_ITEMS** , esse item deve ter perdido a resolução de conflito e **PR_CONFLICT_ITEMS** conteria a identificação de entrada do item que won no conflito resolução.</span><span class="sxs-lookup"><span data-stu-id="e2a97-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e2a97-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2a97-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2a97-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e2a97-124">Protocol specifications</span></span>

<span data-ttu-id="e2a97-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2a97-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2a97-126">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2a97-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2a97-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2a97-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2a97-128">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="e2a97-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2a97-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e2a97-129">Header files</span></span>

<span data-ttu-id="e2a97-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2a97-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2a97-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e2a97-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2a97-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2a97-132">Mapitags.h</span></span>
  
> <span data-ttu-id="e2a97-133">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e2a97-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2a97-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2a97-134">See also</span></span>



[<span data-ttu-id="e2a97-135">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="e2a97-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="e2a97-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e2a97-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2a97-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e2a97-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2a97-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e2a97-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2a97-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e2a97-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

