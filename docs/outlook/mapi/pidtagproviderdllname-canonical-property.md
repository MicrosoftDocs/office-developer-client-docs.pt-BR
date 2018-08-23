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
ms.openlocfilehash: 3bf6347102fc0865b081847a0b66763ba2654665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589480"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="301ae-103">Propriedade canônica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="301ae-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="301ae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="301ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="301ae-105">Contém o nome de base do arquivo da biblioteca de vínculo dinâmico provedor de serviço MAPI (DLL).</span><span class="sxs-lookup"><span data-stu-id="301ae-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="301ae-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="301ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="301ae-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="301ae-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="301ae-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="301ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="301ae-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="301ae-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="301ae-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="301ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="301ae-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="301ae-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="301ae-112">Área:</span><span class="sxs-lookup"><span data-stu-id="301ae-112">Area:</span></span>  <br/> |<span data-ttu-id="301ae-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="301ae-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="301ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="301ae-114">Remarks</span></span>

<span data-ttu-id="301ae-115">O MAPI usa uma convenção de nomenclatura de arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="301ae-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="301ae-116">O nome do arquivo base contém até seis caracteres que identificam exclusivamente a DLL.</span><span class="sxs-lookup"><span data-stu-id="301ae-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="301ae-117">MAPI acrescenta a sequência de caracteres 32 como o nome da DLL base para identificar a versão que é executado em plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="301ae-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="301ae-118">Por exemplo, quando o nome MAPI. DLL for especificado, o nome MAPI32 construções de MAPI. DLL para representar a versão de 32 bits correspondente da DLL.</span><span class="sxs-lookup"><span data-stu-id="301ae-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="301ae-119">Essas propriedades devem especificar o nome de base.</span><span class="sxs-lookup"><span data-stu-id="301ae-119">These properties should specify the base name.</span></span> <span data-ttu-id="301ae-120">MAPI acrescenta a sequência de caracteres 32 conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="301ae-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="301ae-121">Como parte dos resultados propriedade em um erro, incluindo a cadeia de caracteres 32.</span><span class="sxs-lookup"><span data-stu-id="301ae-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="301ae-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="301ae-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="301ae-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="301ae-123">Header files</span></span>

<span data-ttu-id="301ae-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="301ae-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="301ae-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="301ae-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="301ae-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="301ae-126">Mapitags.h</span></span>
  
> <span data-ttu-id="301ae-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="301ae-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="301ae-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="301ae-128">See also</span></span>



[<span data-ttu-id="301ae-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="301ae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="301ae-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="301ae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="301ae-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="301ae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="301ae-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="301ae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

