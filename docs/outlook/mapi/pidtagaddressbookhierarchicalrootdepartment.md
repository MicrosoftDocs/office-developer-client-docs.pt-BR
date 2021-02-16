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
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326121"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="4c183-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="4c183-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="4c183-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c183-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4c183-105">Contém o nome diferenciado (DN) da raiz de endereço hierárquica (HAB).</span><span class="sxs-lookup"><span data-stu-id="4c183-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c183-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4c183-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c183-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="4c183-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="4c183-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="4c183-108">Property set:</span></span>  <br/> |<span data-ttu-id="4c183-109">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="4c183-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="4c183-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4c183-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4c183-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="4c183-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="4c183-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4c183-112">Data type:</span></span>  <br/> |<span data-ttu-id="4c183-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4c183-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4c183-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4c183-114">Area:</span></span>  <br/> |<span data-ttu-id="4c183-115">Exchange Address Book</span><span class="sxs-lookup"><span data-stu-id="4c183-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c183-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c183-116">Remarks</span></span>

<span data-ttu-id="4c183-117">Esta é uma propriedade no contêiner de lista de endereços global (GAL) e representa o nome diferenciado da raiz de endereço hierárquica.</span><span class="sxs-lookup"><span data-stu-id="4c183-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="4c183-118">Essa propriedade só está presente no livro de endereços offline e nunca no Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="4c183-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="4c183-119">Os chamadores devem passar MAPI_CACHE_ONLY chamada GetProps para evitar uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4c183-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="4c183-120">Se isso não estiver presente, os chamadores deverão usar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que é do tipo PT_OBJECT, para encontrar o departamento raiz.</span><span class="sxs-lookup"><span data-stu-id="4c183-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="4c183-121">Depois que o departamento raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="4c183-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="4c183-122">Se o tipo de objeto MAPI_DISTLIST, o novo esquema está sendo empregado.</span><span class="sxs-lookup"><span data-stu-id="4c183-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="4c183-123">Se o tipo de objeto MAPI_MAILUSER, o esquema anterior está sendo empregado.</span><span class="sxs-lookup"><span data-stu-id="4c183-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="4c183-124">O Microsoft Office Outlook 2007 Service Pack 2 oferece suporte a ambos os esquemas.</span><span class="sxs-lookup"><span data-stu-id="4c183-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="4c183-125">O Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam o novo esquema.</span><span class="sxs-lookup"><span data-stu-id="4c183-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="4c183-126">No novo esquema, todos os grupos de departamentos também são listas de distribuição e são do tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="4c183-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="4c183-127">Membros de grupos de departamentos e departamentos dentro de grupos de departamentos são obtidos usando PR_EMS_AB_MEMBER, exatamente como membros da lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="4c183-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="4c183-128">Depois que o departamento raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="4c183-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="4c183-129">Se o tipo de objeto MAPI_DISTLIST, o novo esquema está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="4c183-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="4c183-130">Se o tipo de objeto MAPI_MAILUSER, o esquema antigo está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="4c183-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="4c183-131">No novo esquema, todos os grupos de departamentos também são DLs e são do tipo MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="4c183-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c183-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c183-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c183-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4c183-133">Protocol specifications</span></span>

<span data-ttu-id="4c183-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c183-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c183-135">Fornece definições de conjunto de propriedades e referências a especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4c183-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c183-136">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="4c183-136">Header files</span></span>

<span data-ttu-id="4c183-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c183-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c183-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4c183-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c183-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c183-139">See also</span></span>



[<span data-ttu-id="4c183-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4c183-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c183-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4c183-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c183-142">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4c183-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c183-143">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4c183-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

