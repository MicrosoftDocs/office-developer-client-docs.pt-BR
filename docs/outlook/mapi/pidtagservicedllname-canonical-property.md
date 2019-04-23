---
title: Propriedade canônica PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980450"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="e8f7a-103">Propriedade canônica PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="e8f7a-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="e8f7a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8f7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8f7a-105">Contém o nome de arquivo da DLL que contém a função de ponto de entrada do provedor de serviço de mensagens para chamar a configuração.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8f7a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e8f7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8f7a-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e8f7a-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e8f7a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e8f7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8f7a-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="e8f7a-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="e8f7a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e8f7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8f7a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8f7a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e8f7a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e8f7a-112">Area:</span></span>  <br/> |<span data-ttu-id="e8f7a-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f7a-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8f7a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8f7a-114">Remarks</span></span>

<span data-ttu-id="e8f7a-115">Quando o nome da função de ponto de entrada aparece no método **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), ele indica que o ponto de entrada existe.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="e8f7a-116">MAPI usa uma Convenção de nomenclatura de arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="e8f7a-117">Ele acrescenta a cadeia de caracteres 32 ao nome da DLL base para identificar a versão que é executada em plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="e8f7a-118">Por exemplo, quando o nome MAPI. DLL for especificado, MAPI cria o nome MAPI32. DLL para representar a versão correspondente de 32 bits da DLL.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="e8f7a-119">Essas propriedades devem especificar o nome base.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-119">These properties should specify the base name.</span></span> <span data-ttu-id="e8f7a-120">O MAPI anexa a cadeia de caracteres 32 conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="e8f7a-121">Incluir a cadeia de caracteres 32 como parte dessas propriedades resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8f7a-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8f7a-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8f7a-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8f7a-123">Header files</span></span>

<span data-ttu-id="e8f7a-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8f7a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8f7a-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8f7a-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e8f7a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e8f7a-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8f7a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8f7a-128">See also</span></span>



[<span data-ttu-id="e8f7a-129">Propriedade canônica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="e8f7a-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="e8f7a-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f7a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8f7a-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f7a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8f7a-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f7a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8f7a-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e8f7a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

