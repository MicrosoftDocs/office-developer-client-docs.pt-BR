---
title: Propriedade canônica PidTagRuleUserFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a44c88cbc971d9d5358fc6b24093e56e9565eb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769928"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="f94bf-103">Propriedade canônica PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="f94bf-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f94bf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f94bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f94bf-105">Essa propriedade é definida pelo cliente para o uso exclusivo do cliente.</span><span class="sxs-lookup"><span data-stu-id="f94bf-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f94bf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f94bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f94bf-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f94bf-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f94bf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f94bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f94bf-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="f94bf-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="f94bf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f94bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="f94bf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f94bf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f94bf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f94bf-112">Area:</span></span>  <br/> |<span data-ttu-id="f94bf-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="f94bf-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f94bf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f94bf-114">Remarks</span></span>

<span data-ttu-id="f94bf-115">O servidor deve preservar o valor dessa propriedade se ele tiver sido definido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="f94bf-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="f94bf-116">O servidor deve ignorar durante o processamento e avaliação de regra.</span><span class="sxs-lookup"><span data-stu-id="f94bf-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f94bf-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f94bf-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f94bf-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f94bf-118">Protocol specifications</span></span>

<span data-ttu-id="f94bf-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f94bf-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f94bf-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f94bf-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f94bf-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f94bf-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f94bf-122">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="f94bf-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f94bf-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f94bf-123">Header files</span></span>

<span data-ttu-id="f94bf-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f94bf-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f94bf-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f94bf-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f94bf-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f94bf-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f94bf-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f94bf-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f94bf-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f94bf-128">See also</span></span>



[<span data-ttu-id="f94bf-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f94bf-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f94bf-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f94bf-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f94bf-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f94bf-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f94bf-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f94bf-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

