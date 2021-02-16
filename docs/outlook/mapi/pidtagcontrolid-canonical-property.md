---
title: Propriedade canônica PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416017"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="6a18b-103">Propriedade canônica PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="6a18b-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="6a18b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a18b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a18b-105">Contém um identificador exclusivo para um controle usado em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6a18b-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a18b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6a18b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a18b-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="6a18b-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="6a18b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6a18b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a18b-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="6a18b-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="6a18b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6a18b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a18b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6a18b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6a18b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6a18b-112">Area:</span></span>  <br/> |<span data-ttu-id="6a18b-113">Tabela de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="6a18b-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a18b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a18b-114">Remarks</span></span>

<span data-ttu-id="6a18b-115">Essa propriedade contém um identificador exclusivo para o controle.</span><span class="sxs-lookup"><span data-stu-id="6a18b-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="6a18b-116">Esse identificador deve conter uma [estrutura GUID](guid.md) e um valor binário do tipo **LONG**.</span><span class="sxs-lookup"><span data-stu-id="6a18b-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="6a18b-117">Todos os controles na caixa de diálogo devem usar o mesmo **GUID** para identificar o provedor de serviços, e cada controle deve usar um valor **LONG** exclusivo para garantir que os controles não colidam.</span><span class="sxs-lookup"><span data-stu-id="6a18b-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="6a18b-118">Essa propriedade é usada em notificações.</span><span class="sxs-lookup"><span data-stu-id="6a18b-118">This property is used in notifications.</span></span> <span data-ttu-id="6a18b-119">Por exemplo, as notificações enviadas na tabela de exibição devem definir essa propriedade para identificar exclusivamente o controle a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6a18b-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6a18b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a18b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6a18b-121">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="6a18b-121">Header files</span></span>

<span data-ttu-id="6a18b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a18b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a18b-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6a18b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a18b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6a18b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6a18b-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6a18b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a18b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a18b-126">See also</span></span>



[<span data-ttu-id="6a18b-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6a18b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a18b-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6a18b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a18b-129">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6a18b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a18b-130">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6a18b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

