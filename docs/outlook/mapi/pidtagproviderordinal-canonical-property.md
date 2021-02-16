---
title: Propriedade canônica PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438348"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="bf646-103">Propriedade canônica PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="bf646-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="bf646-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf646-105">Contém o índice baseado em zero da posição de um provedor de serviços na tabela do provedor.</span><span class="sxs-lookup"><span data-stu-id="bf646-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf646-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bf646-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf646-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="bf646-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="bf646-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bf646-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf646-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="bf646-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="bf646-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bf646-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf646-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf646-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf646-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bf646-112">Area:</span></span>  <br/> |<span data-ttu-id="bf646-113">MAPI comum</span><span class="sxs-lookup"><span data-stu-id="bf646-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf646-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf646-114">Remarks</span></span>

<span data-ttu-id="bf646-115">Essa propriedade é calculada por MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf646-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="bf646-116">Obtenha a tabela do provedor chamando o [método IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md)</span><span class="sxs-lookup"><span data-stu-id="bf646-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="bf646-117">Classificar a tabela do provedor nessa propriedade para exibir o pedido de transporte.</span><span class="sxs-lookup"><span data-stu-id="bf646-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bf646-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf646-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf646-119">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="bf646-119">Header files</span></span>

<span data-ttu-id="bf646-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf646-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf646-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bf646-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf646-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf646-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bf646-123">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bf646-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf646-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf646-124">See also</span></span>



[<span data-ttu-id="bf646-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bf646-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf646-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bf646-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf646-127">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bf646-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf646-128">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bf646-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

