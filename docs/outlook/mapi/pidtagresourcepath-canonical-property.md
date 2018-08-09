---
title: Propriedade canônica PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769850"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="a5327-103">Propriedade canônica PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="a5327-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="a5327-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5327-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5327-105">Contém um caminho para o servidor do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="a5327-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5327-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a5327-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5327-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="a5327-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="a5327-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a5327-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5327-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="a5327-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="a5327-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a5327-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5327-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5327-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a5327-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a5327-112">Area:</span></span>  <br/> |<span data-ttu-id="a5327-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="a5327-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5327-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5327-114">Remarks</span></span>

<span data-ttu-id="a5327-115">O caminho contido nessas propriedades representa a sugestão de caminho onde o usuário pode localizar recursos.</span><span class="sxs-lookup"><span data-stu-id="a5327-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="a5327-116">A definição dessas propriedades é específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="a5327-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="a5327-117">Por exemplo, um aplicativo de agendamento usa essas propriedades para especificar o local sugerido para seus arquivos de aplicativo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="a5327-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="a5327-118">O perfil de usuário de mensagens fornece essas propriedades como conveniência para que um aplicativo cliente não precisa solicitar ao usuário de mensagens de um caminho de rede ou uma letra de unidade de rede.</span><span class="sxs-lookup"><span data-stu-id="a5327-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="a5327-119">MAPI funciona somente com nomes de arquivo no conjunto de caracteres American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a5327-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="a5327-120">Aplicativos que usam os nomes de arquivo em um conjunto de caracteres do fabricante do equipamento original (OEM) devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5327-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5327-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5327-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a5327-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a5327-122">Header files</span></span>

<span data-ttu-id="a5327-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5327-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5327-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a5327-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5327-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5327-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a5327-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a5327-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5327-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5327-127">See also</span></span>



[<span data-ttu-id="a5327-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a5327-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5327-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a5327-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5327-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a5327-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5327-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a5327-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

