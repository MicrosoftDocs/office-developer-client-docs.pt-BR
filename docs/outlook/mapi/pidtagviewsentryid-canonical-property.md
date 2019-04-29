---
title: Propriedade canônica PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427308"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="9ae68-103">Propriedade canônica PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="9ae68-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9ae68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ae68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ae68-105">Contém o identificador de entrada da pasta modos de exibição definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9ae68-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ae68-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9ae68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ae68-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9ae68-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9ae68-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9ae68-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ae68-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="9ae68-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="9ae68-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9ae68-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ae68-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ae68-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ae68-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9ae68-112">Area:</span></span>  <br/> |<span data-ttu-id="9ae68-113">Repositório de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae68-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ae68-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ae68-114">Remarks</span></span>

<span data-ttu-id="9ae68-115">A pasta de modo de exibição comum contém um conjunto predefinido de especificadores de exibição padrão, enquanto a pasta de exibição contém especificadores definidos por um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9ae68-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="9ae68-116">Essas pastas, que não estão visíveis na hierarquia de mensagens interpessoais (IPM), podem conter vários especificadores de exibição, cada um armazenado como uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ae68-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="9ae68-117">O aplicativo cliente pode optar por mesclar os dois conjuntos de especificadores e torná-los disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9ae68-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ae68-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ae68-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ae68-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ae68-119">Header files</span></span>

<span data-ttu-id="9ae68-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ae68-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ae68-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9ae68-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ae68-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9ae68-122">Mapitags.h</span></span>
  
> <span data-ttu-id="9ae68-123">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9ae68-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ae68-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ae68-124">See also</span></span>



[<span data-ttu-id="9ae68-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae68-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ae68-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae68-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ae68-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9ae68-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ae68-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9ae68-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

