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
ms.openlocfilehash: 27e3a9687d66bd1cd3586a25a3ca5792523096c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769206"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="df48f-103">Propriedade canônica PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="df48f-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="df48f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df48f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df48f-105">Especifica o caminho de um contêiner de catálogo de endereços em um cenário offline ou o nome de domínio totalmente qualificado do servidor de catálogo global em que o contêiner de catálogo de endereços reside em um cenário online.</span><span class="sxs-lookup"><span data-stu-id="df48f-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="df48f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="df48f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df48f-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="df48f-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="df48f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="df48f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df48f-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="df48f-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="df48f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="df48f-110">Data type:</span></span>  <br/> |<span data-ttu-id="df48f-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="df48f-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="df48f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="df48f-112">Area:</span></span>  <br/> |<span data-ttu-id="df48f-113">Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="df48f-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df48f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df48f-114">Remarks</span></span>

<span data-ttu-id="df48f-115">Esta propriedade tem o tipo de propriedade redefinido com **PT_UNICODE** quando ele é compilado com a `UNICODE` símbolo em uma plataforma de Unicode e **PT_STRING8** quando ele não é compilado com a `UNICODE` símbolo.</span><span class="sxs-lookup"><span data-stu-id="df48f-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df48f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="df48f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df48f-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="df48f-117">Protocol specifications</span></span>

<span data-ttu-id="df48f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df48f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df48f-119">Fornece as definições do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="df48f-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df48f-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df48f-120">Header files</span></span>

<span data-ttu-id="df48f-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df48f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="df48f-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="df48f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="df48f-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df48f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="df48f-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="df48f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df48f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="df48f-125">See also</span></span>



[<span data-ttu-id="df48f-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="df48f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df48f-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="df48f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df48f-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="df48f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df48f-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="df48f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

