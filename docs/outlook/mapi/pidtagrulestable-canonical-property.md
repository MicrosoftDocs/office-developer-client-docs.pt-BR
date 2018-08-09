---
title: Propriedade canônica PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769919"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="900fb-103">Propriedade canônica PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="900fb-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="900fb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="900fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="900fb-105">Contém uma tabela com todas as regras aplicadas a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="900fb-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="900fb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="900fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="900fb-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="900fb-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="900fb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="900fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="900fb-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="900fb-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="900fb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="900fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="900fb-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="900fb-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="900fb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="900fb-112">Area:</span></span>  <br/> |<span data-ttu-id="900fb-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="900fb-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="900fb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="900fb-114">Remarks</span></span>

<span data-ttu-id="900fb-115">Essa propriedade está presente em todos os objetos de pasta em um servidor do Exchange que têm regras.</span><span class="sxs-lookup"><span data-stu-id="900fb-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="900fb-116">Valores incluídos nesta propriedade são usados para ler e modificar as regras.</span><span class="sxs-lookup"><span data-stu-id="900fb-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="900fb-117">Você pode usar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o identificador de interface **IID_IExchangeModifyTable** para obter uma [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interface à tabela de regras em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="900fb-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="900fb-118">Você pode usar essa interface para ler e modificar as regras.</span><span class="sxs-lookup"><span data-stu-id="900fb-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="900fb-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="900fb-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="900fb-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="900fb-120">Header files</span></span>

<span data-ttu-id="900fb-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="900fb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="900fb-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="900fb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="900fb-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="900fb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="900fb-124">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="900fb-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="900fb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="900fb-125">See also</span></span>



[<span data-ttu-id="900fb-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="900fb-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="900fb-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="900fb-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="900fb-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="900fb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="900fb-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="900fb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="900fb-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="900fb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="900fb-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="900fb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

