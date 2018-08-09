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
ms.openlocfilehash: 054299e6bdf685163bc23678a2070f5d702a4529
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769915"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="be5b1-103">Propriedade canônica PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="be5b1-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="be5b1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be5b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be5b1-105">Uma propriedade opaca que o cliente define para o uso exclusivo do cliente.</span><span class="sxs-lookup"><span data-stu-id="be5b1-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be5b1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="be5b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be5b1-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="be5b1-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="be5b1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be5b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be5b1-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="be5b1-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="be5b1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="be5b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="be5b1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="be5b1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="be5b1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="be5b1-112">Area:</span></span>  <br/> |<span data-ttu-id="be5b1-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="be5b1-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be5b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be5b1-114">Remarks</span></span>

<span data-ttu-id="be5b1-115">O servidor deve preservar o valor dessa propriedade se ele tiver sido definido pelo cliente, mas deve ignorar o seu conteúdo durante o processamento e avaliação de regra.</span><span class="sxs-lookup"><span data-stu-id="be5b1-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="be5b1-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="be5b1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be5b1-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="be5b1-117">Protocol specifications</span></span>

<span data-ttu-id="be5b1-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be5b1-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be5b1-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="be5b1-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be5b1-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be5b1-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be5b1-121">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="be5b1-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be5b1-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="be5b1-122">Header files</span></span>

<span data-ttu-id="be5b1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be5b1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="be5b1-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="be5b1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="be5b1-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be5b1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="be5b1-126">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="be5b1-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="be5b1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="be5b1-127">See also</span></span>



[<span data-ttu-id="be5b1-128">Propriedade canônica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="be5b1-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="be5b1-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="be5b1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be5b1-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="be5b1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be5b1-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="be5b1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be5b1-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="be5b1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

