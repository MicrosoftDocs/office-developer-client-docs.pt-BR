---
title: Propriedade canônica PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 21fdff2aa713905a27a3d0cc5545ceb59f030378
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586855"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="b3f3b-103">Propriedade canônica PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="b3f3b-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="b3f3b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3f3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3f3b-105">Contém o identificador de modelo de entrada para um padrão de objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f3b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b3f3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3f3b-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b3f3b-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="b3f3b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b3f3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b3f3b-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="b3f3b-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="b3f3b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b3f3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="b3f3b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b3f3b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b3f3b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b3f3b-112">Area:</span></span>  <br/> |<span data-ttu-id="b3f3b-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="b3f3b-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3f3b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3f3b-114">Remarks</span></span>

<span data-ttu-id="b3f3b-115">Aplicativos cliente usam essa propriedade para criar um objeto de usuário mensagens dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="b3f3b-116">Suporte para criação de entrada é opcional para contêineres do catálogo de endereços; aqueles que não têm suporte não são necessárias para expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="b3f3b-117">Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="b3f3b-118">Depois de obter o identificador, o cliente usa-lo em uma chamada ao método [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="b3f3b-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="b3f3b-119">A entrada representa o modelo para o usuário de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b3f3b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3f3b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b3f3b-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3f3b-121">Header files</span></span>

<span data-ttu-id="b3f3b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3f3b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3f3b-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b3f3b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b3f3b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b3f3b-125">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="b3f3b-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3f3b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3f3b-126">See also</span></span>



[<span data-ttu-id="b3f3b-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f3b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3f3b-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b3f3b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3f3b-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f3b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3f3b-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b3f3b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

