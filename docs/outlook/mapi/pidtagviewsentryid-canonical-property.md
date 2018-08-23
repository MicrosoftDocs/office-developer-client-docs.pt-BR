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
ms.openlocfilehash: 73ed7213ea2bd5079458ccc237b65590f06e8d53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586260"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="36d8a-103">Propriedade canônica PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="36d8a-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="36d8a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36d8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36d8a-105">Contém o identificador de entrada da pasta exibições definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="36d8a-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36d8a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="36d8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36d8a-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="36d8a-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="36d8a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="36d8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36d8a-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="36d8a-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="36d8a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="36d8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="36d8a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="36d8a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="36d8a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="36d8a-112">Area:</span></span>  <br/> |<span data-ttu-id="36d8a-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="36d8a-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36d8a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="36d8a-114">Remarks</span></span>

<span data-ttu-id="36d8a-115">A pasta de exibição comuns contém um conjunto predefinido de especificadores de exibição padrão, enquanto a pasta de exibição contém especificadores definidas por um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="36d8a-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="36d8a-116">Essas pastas, que não são visíveis na hierarquia de mensagem interpessoais (IPM), podem conter várias especificadores de exibição, cada uma delas armazenada como uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="36d8a-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="36d8a-117">O aplicativo cliente pode optar por mesclar os dois conjuntos de especificadores e disponibilizá-los ambos.</span><span class="sxs-lookup"><span data-stu-id="36d8a-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="36d8a-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="36d8a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="36d8a-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="36d8a-119">Header files</span></span>

<span data-ttu-id="36d8a-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36d8a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="36d8a-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="36d8a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="36d8a-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="36d8a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="36d8a-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="36d8a-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36d8a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="36d8a-124">See also</span></span>



[<span data-ttu-id="36d8a-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="36d8a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36d8a-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="36d8a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36d8a-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="36d8a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36d8a-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="36d8a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

