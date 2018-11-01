---
title: Método SetPermissions (ADOX)
TOCTitle: SetPermissions Method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 433ddcc0394ff3543cd47b6399cb430890972920
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889522"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="7481f-102">Método SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7481f-102">SetPermissions Method (ADOX)</span></span>


<span data-ttu-id="7481f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7481f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="7481f-104">Especifica as permissões referentes a um grupo ou usuário em um objeto.</span><span class="sxs-lookup"><span data-stu-id="7481f-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7481f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7481f-105">Syntax</span></span>

<span data-ttu-id="7481f-106">*GrupoOuUsuário*. SetPermissions*nome*, *ObjectType*, *ação*, *direitos* \[,*herdam* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="7481f-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="7481f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7481f-107">Parameters</span></span>

  - <span data-ttu-id="7481f-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="7481f-108">*Name*</span></span>

  - <span data-ttu-id="7481f-109">Um valor **String** que especifica o nome do objeto para o qual permissões serão definidas.</span><span class="sxs-lookup"><span data-stu-id="7481f-109">A **String** value that specifies the name of the object for which to set permissions.</span></span>

  - <span data-ttu-id="7481f-110">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="7481f-110">*ObjectType*</span></span>

  - <span data-ttu-id="7481f-111">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual permissões serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="7481f-111">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="7481f-112">*Action*</span><span class="sxs-lookup"><span data-stu-id="7481f-112">*Action*</span></span>

  - <span data-ttu-id="7481f-113">Um valor **Long** que pode ser uma das constantes [ActionEnum](actionenum.md) que especifica o tipo de ação a ser executada durante a definição de permissões.</span><span class="sxs-lookup"><span data-stu-id="7481f-113">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>

  - <span data-ttu-id="7481f-114">*Rights*</span><span class="sxs-lookup"><span data-stu-id="7481f-114">*Rights*</span></span>

  - <span data-ttu-id="7481f-115">Um valor **Long** que pode ser uma máscara de bits de uma ou mais constantes [RightsEnum](rightsenum.md), que indica os direitos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="7481f-115">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>

  - <span data-ttu-id="7481f-116">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="7481f-116">*Inherit*</span></span>

  - <span data-ttu-id="7481f-p101">Opcional. Um valor **Long** que pode ser uma das constantes [InheritTypeEnum](inherittypeenum.md), que especifica como os objetos herdarão essas permissões. O valor padrão é **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="7481f-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>

  - <span data-ttu-id="7481f-120">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="7481f-120">*ObjectTypeId*</span></span>

  - <span data-ttu-id="7481f-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7481f-121">Optional.</span></span> <span data-ttu-id="7481f-122">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7481f-122">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="7481f-123">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="7481f-123">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7481f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7481f-124">Remarks</span></span>

<span data-ttu-id="7481f-125">Ocorrerá um erro se o provedor não oferecer suporte à definição de direitos de acesso para grupos ou usuários.</span><span class="sxs-lookup"><span data-stu-id="7481f-125">An error will occur if the provider does not support setting access rights for groups or users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7481f-126">Ao chamar <STRONG>SetPermissions</STRONG>, a configuração de ações como <STRONG>adAccessRevoke</STRONG> substitui as configurações do parâmetro <EM>direitos</EM> .</span><span class="sxs-lookup"><span data-stu-id="7481f-126">When calling <STRONG>SetPermissions</STRONG>, setting Actions to <STRONG>adAccessRevoke</STRONG> overrides any settings of the <EM>Rights</EM> parameter.</span></span> <span data-ttu-id="7481f-127">Não defina <EM>ações</EM> para <STRONG>adAccessRevoke</STRONG> se quiser que os direitos especificados no parâmetro <EM>direitos</EM> entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="7481f-127">Do not set <EM>Actions</EM> to <STRONG>adAccessRevoke</STRONG> if you want the rights specified in the <EM>Rights</EM> parameter to take effect.</span></span></P>


