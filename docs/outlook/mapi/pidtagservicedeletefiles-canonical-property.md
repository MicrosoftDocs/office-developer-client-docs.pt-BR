---
title: Propriedade canônica PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436822"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="e54e2-103">Propriedade canônica PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="e54e2-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="e54e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e54e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e54e2-105">Contém uma lista de nomes de FileNames que devem ser excluídos quando o serviço de mensagens é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="e54e2-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e54e2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e54e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e54e2-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="e54e2-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="e54e2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e54e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e54e2-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="e54e2-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="e54e2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e54e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="e54e2-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e54e2-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e54e2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e54e2-112">Area:</span></span>  <br/> |<span data-ttu-id="e54e2-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="e54e2-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e54e2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e54e2-114">Remarks</span></span>

<span data-ttu-id="e54e2-115">Os nomes de FileNames da lista contidos nessas propriedades são excluídos do computador ao usar o painel de controle para desinstalar o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e54e2-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="e54e2-116">Não inclua na lista qualquer DLL que ofereça suporte a vários serviços de mensagens ou que os serviços de mensagens adicionais possam ser removidos inadvertidamente.</span><span class="sxs-lookup"><span data-stu-id="e54e2-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="e54e2-117">O MAPI funciona somente com nomes de Filee outras cadeias de caracteres passadas para ele, no conjunto de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="e54e2-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="e54e2-118">Os aplicativos que usam nomes de fileformados em um conjunto de caracteres OEM devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="e54e2-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e54e2-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e54e2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e54e2-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e54e2-120">Header files</span></span>

<span data-ttu-id="e54e2-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e54e2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e54e2-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e54e2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e54e2-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e54e2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e54e2-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e54e2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e54e2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e54e2-125">See also</span></span>



[<span data-ttu-id="e54e2-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e54e2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e54e2-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e54e2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e54e2-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e54e2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e54e2-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e54e2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

