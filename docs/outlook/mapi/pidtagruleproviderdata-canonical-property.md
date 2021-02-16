---
title: Propriedade canônica PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335417"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="9de8f-103">Propriedade canônica PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="9de8f-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="9de8f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9de8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9de8f-105">Uma propriedade opaca que o cliente define para uso exclusivo do cliente.</span><span class="sxs-lookup"><span data-stu-id="9de8f-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9de8f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9de8f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9de8f-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="9de8f-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="9de8f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9de8f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9de8f-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="9de8f-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="9de8f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9de8f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9de8f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9de8f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9de8f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9de8f-112">Area:</span></span>  <br/> |<span data-ttu-id="9de8f-113">Regras do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="9de8f-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9de8f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9de8f-114">Remarks</span></span>

<span data-ttu-id="9de8f-115">O servidor deve preservar o valor dessa propriedade se ele tiver sido definido pelo cliente, mas deve ignorar seu conteúdo durante a avaliação e o processamento da regra.</span><span class="sxs-lookup"><span data-stu-id="9de8f-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9de8f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9de8f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9de8f-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9de8f-117">Protocol specifications</span></span>

<span data-ttu-id="9de8f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9de8f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9de8f-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9de8f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9de8f-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9de8f-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9de8f-121">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="9de8f-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9de8f-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9de8f-122">Header files</span></span>

<span data-ttu-id="9de8f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9de8f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9de8f-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9de8f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9de8f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9de8f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9de8f-126">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="9de8f-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9de8f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9de8f-127">See also</span></span>



[<span data-ttu-id="9de8f-128">Propriedade canônica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="9de8f-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="9de8f-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9de8f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9de8f-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9de8f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9de8f-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9de8f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9de8f-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9de8f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

