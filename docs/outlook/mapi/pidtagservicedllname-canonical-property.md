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
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770027"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="cc27f-103">Propriedade canônica PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="cc27f-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="cc27f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc27f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc27f-105">Contém o nome de arquivo da DLL que contém a função do ponto de entrada do provedor de serviço de mensagem para chamar para configuração.</span><span class="sxs-lookup"><span data-stu-id="cc27f-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc27f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cc27f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc27f-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="cc27f-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="cc27f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc27f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc27f-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="cc27f-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="cc27f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cc27f-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc27f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cc27f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cc27f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc27f-112">Area:</span></span>  <br/> |<span data-ttu-id="cc27f-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="cc27f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc27f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc27f-114">Remarks</span></span>

<span data-ttu-id="cc27f-115">Quando o nome de função de ponto de entrada for exibida no método **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), isso indica que o ponto de entrada existe.</span><span class="sxs-lookup"><span data-stu-id="cc27f-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="cc27f-116">O MAPI usa uma convenção de nomenclatura de arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="cc27f-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="cc27f-117">O nome do arquivo base contém até seis caracteres que identificam exclusivamente a DLL.</span><span class="sxs-lookup"><span data-stu-id="cc27f-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="cc27f-118">MAPI acrescenta a sequência de caracteres 32 como o nome da DLL base para identificar a versão que é executado em plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cc27f-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="cc27f-119">Por exemplo, quando o nome MAPI. DLL for especificado, o nome MAPI32 construções de MAPI. DLL para representar a versão de 32 bits correspondente da DLL.</span><span class="sxs-lookup"><span data-stu-id="cc27f-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="cc27f-120">Essas propriedades devem especificar o nome de base.</span><span class="sxs-lookup"><span data-stu-id="cc27f-120">These properties should specify the base name.</span></span> <span data-ttu-id="cc27f-121">MAPI acrescenta a sequência de caracteres 32 conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="cc27f-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="cc27f-122">Como parte do resultado propriedades em um erro, incluindo a cadeia de caracteres 32.</span><span class="sxs-lookup"><span data-stu-id="cc27f-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc27f-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc27f-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc27f-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cc27f-124">Header files</span></span>

<span data-ttu-id="cc27f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc27f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc27f-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cc27f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc27f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc27f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cc27f-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc27f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc27f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc27f-129">See also</span></span>



[<span data-ttu-id="cc27f-130">Propriedade canônica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="cc27f-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="cc27f-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc27f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc27f-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cc27f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc27f-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cc27f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc27f-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cc27f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
