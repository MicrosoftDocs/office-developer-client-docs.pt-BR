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
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769712"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="27946-103">Propriedade canônica PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="27946-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="27946-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27946-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27946-105">Contém o índice baseado em zero da posição de um provedor de serviços na tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="27946-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27946-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="27946-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27946-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="27946-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="27946-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="27946-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27946-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="27946-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="27946-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="27946-110">Data type:</span></span>  <br/> |<span data-ttu-id="27946-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27946-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27946-112">Área:</span><span class="sxs-lookup"><span data-stu-id="27946-112">Area:</span></span>  <br/> |<span data-ttu-id="27946-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="27946-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27946-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="27946-114">Remarks</span></span>

<span data-ttu-id="27946-115">Essa propriedade é computada pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="27946-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="27946-116">Obter a tabela de provedor chamando o método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="27946-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="27946-117">Classificar a tabela de provedor nessa propriedade para exibir a ordem de transporte.</span><span class="sxs-lookup"><span data-stu-id="27946-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="27946-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="27946-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="27946-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="27946-119">Header files</span></span>

<span data-ttu-id="27946-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27946-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="27946-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="27946-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="27946-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27946-122">Mapitags.h</span></span>
  
> <span data-ttu-id="27946-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="27946-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27946-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="27946-124">See also</span></span>



[<span data-ttu-id="27946-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="27946-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27946-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="27946-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27946-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="27946-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27946-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="27946-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

