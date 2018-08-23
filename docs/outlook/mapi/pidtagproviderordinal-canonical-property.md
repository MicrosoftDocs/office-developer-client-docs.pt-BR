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
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573807"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="c8df3-103">Propriedade canônica PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="c8df3-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="c8df3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8df3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8df3-105">Contém o índice baseado em zero da posição de um provedor de serviços na tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="c8df3-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8df3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c8df3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8df3-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="c8df3-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="c8df3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c8df3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8df3-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="c8df3-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="c8df3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c8df3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8df3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c8df3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c8df3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c8df3-112">Area:</span></span>  <br/> |<span data-ttu-id="c8df3-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="c8df3-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8df3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8df3-114">Remarks</span></span>

<span data-ttu-id="c8df3-115">Essa propriedade é computada pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="c8df3-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="c8df3-116">Obter a tabela de provedor chamando o método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="c8df3-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="c8df3-117">Classificar a tabela de provedor nessa propriedade para exibir a ordem de transporte.</span><span class="sxs-lookup"><span data-stu-id="c8df3-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c8df3-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8df3-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c8df3-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c8df3-119">Header files</span></span>

<span data-ttu-id="c8df3-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8df3-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8df3-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c8df3-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8df3-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8df3-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c8df3-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c8df3-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8df3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8df3-124">See also</span></span>



[<span data-ttu-id="c8df3-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c8df3-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8df3-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c8df3-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8df3-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c8df3-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8df3-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c8df3-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

