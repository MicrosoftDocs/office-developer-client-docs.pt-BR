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
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428498"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="f5e77-103">Propriedade canônica PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="f5e77-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="f5e77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5e77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5e77-105">Contém uma tabela com todas as regras aplicadas a uma pasta.</span><span class="sxs-lookup"><span data-stu-id="f5e77-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5e77-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f5e77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5e77-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="f5e77-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="f5e77-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f5e77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5e77-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="f5e77-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="f5e77-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f5e77-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5e77-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f5e77-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f5e77-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f5e77-112">Area:</span></span>  <br/> |<span data-ttu-id="f5e77-113">Regras do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="f5e77-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5e77-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5e77-114">Remarks</span></span>

<span data-ttu-id="f5e77-115">Essa propriedade está presente em todos os objetos de pasta em um Exchange Server que tem regras.</span><span class="sxs-lookup"><span data-stu-id="f5e77-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="f5e77-116">Os valores incluídos nesta propriedade são usados para ler e modificar regras.</span><span class="sxs-lookup"><span data-stu-id="f5e77-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="f5e77-117">Você pode usar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o identificador de interface IID_IExchangeModifyTable para obter uma interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) para **a** tabela de regras em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="f5e77-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="f5e77-118">Você pode usar essa interface para ler e modificar essas regras.</span><span class="sxs-lookup"><span data-stu-id="f5e77-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5e77-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5e77-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f5e77-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="f5e77-120">Header files</span></span>

<span data-ttu-id="f5e77-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5e77-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5e77-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5e77-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5e77-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5e77-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f5e77-124">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="f5e77-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f5e77-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5e77-125">See also</span></span>



[<span data-ttu-id="f5e77-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5e77-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="f5e77-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f5e77-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="f5e77-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5e77-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5e77-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f5e77-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5e77-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5e77-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5e77-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f5e77-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

