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
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407477"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="984fa-103">Propriedade canônica PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="984fa-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="984fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="984fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="984fa-105">Contém o identificador de entrada de modelo para um objeto de usuário de mensagem padrão.</span><span class="sxs-lookup"><span data-stu-id="984fa-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="984fa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="984fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="984fa-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="984fa-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="984fa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="984fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="984fa-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="984fa-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="984fa-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="984fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="984fa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="984fa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="984fa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="984fa-112">Area:</span></span>  <br/> |<span data-ttu-id="984fa-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="984fa-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="984fa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="984fa-114">Remarks</span></span>

<span data-ttu-id="984fa-115">Os aplicativos cliente usam essa propriedade para criar um objeto de usuário de mensagens dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="984fa-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="984fa-116">O suporte à criação de entrada é opcional para contêineres do catálogo de endereços; os que não oferecem suporte a ele não são necessários para expor essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="984fa-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="984fa-117">Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="984fa-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="984fa-118">Após obter o identificador, o cliente o usará em uma chamada para o método [IABContainer:: createentry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="984fa-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="984fa-119">A entrada representa o modelo do usuário de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="984fa-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="984fa-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="984fa-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="984fa-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="984fa-121">Header files</span></span>

<span data-ttu-id="984fa-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="984fa-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="984fa-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="984fa-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="984fa-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="984fa-124">Mapitags.h</span></span>
  
> <span data-ttu-id="984fa-125">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="984fa-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="984fa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="984fa-126">See also</span></span>



[<span data-ttu-id="984fa-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="984fa-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="984fa-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="984fa-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="984fa-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="984fa-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="984fa-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="984fa-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

