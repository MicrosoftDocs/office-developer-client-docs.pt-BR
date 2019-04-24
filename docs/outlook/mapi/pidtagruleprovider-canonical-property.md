---
title: Propriedade canônica PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280602"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="ba5e2-103">Propriedade canônica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="ba5e2-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="ba5e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba5e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba5e2-105">Contém o nome do aplicativo que define uma regra.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba5e2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ba5e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba5e2-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="ba5e2-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="ba5e2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ba5e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba5e2-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="ba5e2-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="ba5e2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ba5e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba5e2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ba5e2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ba5e2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ba5e2-112">Area:</span></span>  <br/> |<span data-ttu-id="ba5e2-113">Regras no servidor</span><span class="sxs-lookup"><span data-stu-id="ba5e2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba5e2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba5e2-114">Remarks</span></span>

<span data-ttu-id="ba5e2-115">As ações adiadas precisam dessas propriedades para identificar o código que deve interpretar e executar a ação de regra.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="ba5e2-116">As regras armazenadas em caixas de correio e pastas são associadas ao aplicativo que as detém por uma cadeia de caracteres de provedor de regras.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="ba5e2-117">Um provedor de regras define e manipula regras em uma tabela de regras.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="ba5e2-118">Ele também fornece um meio de lidar com quaisquer ações adiadas se essas regras forem definidas.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="ba5e2-119">As ações adiadas são criadas implicitamente pelo armazenamento de informações.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="ba5e2-120">Para operações de movimentação ou cópia para um repositório diferente, se um provedor definir uma regra de ação adiada, deve fornecer um manipulador para executar a ação quando a regra é disparada e uma ação adiada é criada.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba5e2-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba5e2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ba5e2-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="ba5e2-122">Protocol specifications</span></span>

<span data-ttu-id="ba5e2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba5e2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba5e2-124">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ba5e2-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba5e2-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba5e2-126">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ba5e2-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba5e2-127">Header files</span></span>

<span data-ttu-id="ba5e2-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ba5e2-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba5e2-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba5e2-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ba5e2-130">Mapitags.h</span></span>
  
> <span data-ttu-id="ba5e2-131">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ba5e2-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba5e2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba5e2-132">See also</span></span>



[<span data-ttu-id="ba5e2-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ba5e2-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba5e2-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ba5e2-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba5e2-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ba5e2-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba5e2-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ba5e2-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

