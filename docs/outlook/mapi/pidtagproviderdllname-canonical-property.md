---
title: Propriedade canônica PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286485"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="2b6d9-103">Propriedade canônica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="2b6d9-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="2b6d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b6d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b6d9-105">Contém o nome de arquivo base da biblioteca de vínculo dinâmico (DLL) do provedor de serviços MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b6d9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2b6d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b6d9-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2b6d9-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2b6d9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2b6d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b6d9-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="2b6d9-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="2b6d9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2b6d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b6d9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b6d9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2b6d9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2b6d9-112">Area:</span></span>  <br/> |<span data-ttu-id="2b6d9-113">MAPI comum</span><span class="sxs-lookup"><span data-stu-id="2b6d9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b6d9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b6d9-114">Remarks</span></span>

<span data-ttu-id="2b6d9-115">MAPI usa uma Convenção de nomenclatura de arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="2b6d9-116">Ele acrescenta a cadeia de caracteres 32 ao nome da DLL base para identificar a versão que é executada em plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="2b6d9-117">Por exemplo, quando o nome MAPI. DLL for especificado, MAPI cria o nome MAPI32. DLL para representar a versão correspondente de 32 bits da DLL.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="2b6d9-118">Essas propriedades devem especificar o nome base.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-118">These properties should specify the base name.</span></span> <span data-ttu-id="2b6d9-119">O MAPI anexa a cadeia de caracteres 32 conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="2b6d9-120">Incluir a cadeia de caracteres 32 como parte dessa propriedade resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b6d9-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b6d9-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2b6d9-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2b6d9-122">Header files</span></span>

<span data-ttu-id="2b6d9-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2b6d9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b6d9-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b6d9-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2b6d9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2b6d9-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2b6d9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b6d9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b6d9-127">See also</span></span>



[<span data-ttu-id="2b6d9-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2b6d9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b6d9-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2b6d9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b6d9-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2b6d9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b6d9-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2b6d9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

