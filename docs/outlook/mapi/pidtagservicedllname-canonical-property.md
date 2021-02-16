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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330062"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="1fefe-103">Propriedade canônica PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="1fefe-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="1fefe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fefe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fefe-105">Contém o nome de arquivo da DLL que contém a função de ponto de entrada do provedor de serviços de mensagens a ser chamada para configuração.</span><span class="sxs-lookup"><span data-stu-id="1fefe-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1fefe-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1fefe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fefe-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1fefe-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="1fefe-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1fefe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fefe-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="1fefe-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="1fefe-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1fefe-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fefe-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1fefe-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1fefe-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1fefe-112">Area:</span></span>  <br/> |<span data-ttu-id="1fefe-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1fefe-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fefe-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fefe-114">Remarks</span></span>

<span data-ttu-id="1fefe-115">Quando o nome da função de ponto de entrada aparece **no método PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), ele indica que o ponto de entrada existe.</span><span class="sxs-lookup"><span data-stu-id="1fefe-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="1fefe-116">MAPI uses a DLL file naming convention.</span><span class="sxs-lookup"><span data-stu-id="1fefe-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="1fefe-117">Ele anexa a cadeia de caracteres 32 ao nome base da DLL para identificar a versão que é executado em plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1fefe-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="1fefe-118">Por exemplo, quando o nome MAPI.DLL especificado, MAPI constrói o nome MAPI32.DLL para representar a versão de 32 bits correspondente da DLL.</span><span class="sxs-lookup"><span data-stu-id="1fefe-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="1fefe-119">Essas propriedades devem especificar o nome base.</span><span class="sxs-lookup"><span data-stu-id="1fefe-119">These properties should specify the base name.</span></span> <span data-ttu-id="1fefe-120">MAPI anexa a cadeia de caracteres 32 conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="1fefe-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="1fefe-121">Incluir a cadeia de caracteres 32 como parte dessas propriedades resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="1fefe-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1fefe-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fefe-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1fefe-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1fefe-123">Header files</span></span>

<span data-ttu-id="1fefe-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fefe-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fefe-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1fefe-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fefe-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1fefe-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1fefe-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1fefe-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fefe-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fefe-128">See also</span></span>



[<span data-ttu-id="1fefe-129">Propriedade canônica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="1fefe-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="1fefe-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1fefe-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fefe-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1fefe-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fefe-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1fefe-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fefe-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1fefe-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

