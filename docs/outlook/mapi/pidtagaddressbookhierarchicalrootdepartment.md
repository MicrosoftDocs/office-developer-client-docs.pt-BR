---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 49c9b0a80f9bc3b45dfafa6f4e037fe55af289d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768975"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="25897-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="25897-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="25897-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25897-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="25897-105">Contém o nome diferenciado (DN) da autoridade raiz de catálogos de endereços hierárquicos (HAB).</span><span class="sxs-lookup"><span data-stu-id="25897-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25897-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="25897-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25897-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="25897-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="25897-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="25897-108">Property set:</span></span>  <br/> |<span data-ttu-id="25897-109">Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="25897-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="25897-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="25897-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25897-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="25897-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="25897-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="25897-112">Data type:</span></span>  <br/> |<span data-ttu-id="25897-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="25897-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="25897-114">Área:</span><span class="sxs-lookup"><span data-stu-id="25897-114">Area:</span></span>  <br/> |<span data-ttu-id="25897-115">Catálogo de endereços do Exchange</span><span class="sxs-lookup"><span data-stu-id="25897-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25897-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="25897-116">Remarks</span></span>

<span data-ttu-id="25897-117">Esta é uma propriedade no contêiner endereços global (GAL) da lista e representa o nome diferenciado da raiz de endereços hierárquicos.</span><span class="sxs-lookup"><span data-stu-id="25897-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="25897-118">Essa propriedade somente está presente no catálogo de endereços offline e nunca no serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="25897-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="25897-119">Os chamadores devem passar MAPI_CACHE_ONLY para a chamada GetProps para evitar uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="25897-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="25897-120">Se não estiver presente, os chamadores devem usar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que é do tipo PT_OBJECT, para localizar o departamento de raiz.</span><span class="sxs-lookup"><span data-stu-id="25897-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="25897-121">Depois que o departamento de raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="25897-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="25897-122">Se o tipo de objeto for MAPI_DISTLIST, o novo esquema é empregado.</span><span class="sxs-lookup"><span data-stu-id="25897-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="25897-123">Se o tipo de objeto for MAPI_MAILUSER, o esquema anterior é empregado.</span><span class="sxs-lookup"><span data-stu-id="25897-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="25897-124">Microsoft Office Outlook 2007 Service Pack 2 oferece suporte a ambos os esquemas.</span><span class="sxs-lookup"><span data-stu-id="25897-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="25897-125">Microsoft Outlook 2010 e o Microsoft Outlook 2013 compatíveis com o novo esquema.</span><span class="sxs-lookup"><span data-stu-id="25897-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="25897-126">No novo esquema, todos os grupos departamentais também são listas de distribuição em são do tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="25897-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="25897-127">Membros de grupos departamentais e departamentos dentro dos grupos departamentais são obtidos por meio de PR_EMS_AB_MEMBER, exatamente como membros da lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="25897-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="25897-128">Depois que o departamento de raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="25897-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="25897-129">Se o tipo de objeto for MAPI_DISTLIST, o novo esquema está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="25897-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="25897-130">Se o tipo de objeto for MAPI_MAILUSER, o esquema antigo está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="25897-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="25897-131">No novo esquema, todos os grupos departamentais são também DLs em do tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="25897-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25897-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="25897-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25897-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="25897-133">Protocol specifications</span></span>

<span data-ttu-id="25897-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25897-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25897-135">Fornece referências relacionados especificações de protocolo do Microsoft Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="25897-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25897-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="25897-136">Header files</span></span>

<span data-ttu-id="25897-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25897-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="25897-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="25897-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25897-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="25897-139">See also</span></span>



[<span data-ttu-id="25897-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="25897-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25897-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="25897-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25897-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="25897-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25897-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="25897-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

