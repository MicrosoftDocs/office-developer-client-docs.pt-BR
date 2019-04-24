---
title: Propriedade canônica PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335793"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="6f80f-103">Propriedade canônica PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="6f80f-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="6f80f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f80f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f80f-105">Especifica o caminho de um contêiner de catálogo de endereços em um cenário offline ou o nome de domínio totalmente qualificado do servidor de catálogo global onde o contêiner do catálogo de endereços reside em um cenário online.</span><span class="sxs-lookup"><span data-stu-id="6f80f-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6f80f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6f80f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f80f-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="6f80f-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="6f80f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6f80f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f80f-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="6f80f-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="6f80f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6f80f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f80f-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="6f80f-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="6f80f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6f80f-112">Area:</span></span>  <br/> |<span data-ttu-id="6f80f-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="6f80f-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f80f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f80f-114">Remarks</span></span>

<span data-ttu-id="6f80f-115">Essa propriedade tem o tipo de propriedade reset como **PT_UNICODE** quando ele é compilado com `UNICODE` o símbolo em uma plataforma Unicode e para **PT_STRING8** quando não é compilado com o `UNICODE` símbolo.</span><span class="sxs-lookup"><span data-stu-id="6f80f-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f80f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f80f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f80f-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="6f80f-117">Protocol specifications</span></span>

<span data-ttu-id="6f80f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f80f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f80f-119">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f80f-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f80f-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f80f-120">Header files</span></span>

<span data-ttu-id="6f80f-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6f80f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f80f-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6f80f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f80f-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6f80f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6f80f-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6f80f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f80f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f80f-125">See also</span></span>



[<span data-ttu-id="6f80f-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6f80f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f80f-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6f80f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f80f-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6f80f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f80f-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6f80f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

