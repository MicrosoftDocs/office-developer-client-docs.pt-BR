---
title: Propriedade canônica PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769141"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="95268-103">Propriedade canônica PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95268-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="95268-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95268-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95268-105">Conterá TRUE se um perfil de usuário de mensagens é o perfil padrão MAPI.</span><span class="sxs-lookup"><span data-stu-id="95268-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95268-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="95268-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95268-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="95268-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="95268-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="95268-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95268-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="95268-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="95268-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="95268-110">Data type:</span></span>  <br/> |<span data-ttu-id="95268-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="95268-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="95268-112">Área:</span><span class="sxs-lookup"><span data-stu-id="95268-112">Area:</span></span>  <br/> |<span data-ttu-id="95268-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="95268-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95268-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="95268-114">Remarks</span></span>

<span data-ttu-id="95268-115">Essa propriedade não é exibido como uma propriedade de qualquer objeto, mas apenas como uma coluna em uma tabela de perfil.</span><span class="sxs-lookup"><span data-stu-id="95268-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="95268-116">Um aplicativo cliente pode usar o método [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) para designar o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="95268-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="95268-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="95268-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="95268-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95268-118">Header files</span></span>

<span data-ttu-id="95268-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95268-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="95268-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="95268-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="95268-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95268-121">Mapitags.h</span></span>
  
> <span data-ttu-id="95268-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="95268-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95268-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="95268-123">See also</span></span>



[<span data-ttu-id="95268-124">Propriedade canônica PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="95268-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="95268-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="95268-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95268-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="95268-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95268-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="95268-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95268-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="95268-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

