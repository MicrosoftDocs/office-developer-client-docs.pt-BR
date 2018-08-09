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
ms.openlocfilehash: 33c62b81982aaac3659ad4d41ea2cf5298b42287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769159"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="08537-103">Propriedade canônica PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="08537-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="08537-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08537-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08537-105">Contém o identificador de modelo de entrada para um padrão de objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="08537-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08537-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="08537-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08537-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="08537-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="08537-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="08537-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08537-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="08537-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="08537-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="08537-110">Data type:</span></span>  <br/> |<span data-ttu-id="08537-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08537-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08537-112">Área:</span><span class="sxs-lookup"><span data-stu-id="08537-112">Area:</span></span>  <br/> |<span data-ttu-id="08537-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="08537-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08537-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="08537-114">Remarks</span></span>

<span data-ttu-id="08537-115">Aplicativos cliente usam essa propriedade para criar um objeto de usuário mensagens dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="08537-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="08537-116">Suporte para criação de entrada é opcional para contêineres do catálogo de endereços; aqueles que não têm suporte não são necessárias para expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="08537-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="08537-117">Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="08537-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="08537-118">Depois de obter o identificador, o cliente usa-lo em uma chamada ao método [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="08537-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="08537-119">A entrada representa o modelo para o usuário de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="08537-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08537-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="08537-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="08537-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="08537-121">Header files</span></span>

<span data-ttu-id="08537-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08537-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="08537-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="08537-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="08537-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08537-124">Mapitags.h</span></span>
  
> <span data-ttu-id="08537-125">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="08537-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08537-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="08537-126">See also</span></span>



[<span data-ttu-id="08537-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="08537-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08537-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="08537-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08537-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="08537-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08537-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="08537-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

