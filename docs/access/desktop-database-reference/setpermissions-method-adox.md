---
title: Método SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d99608a938598135d713375875da9073c8f9f3c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927512"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="5381a-102">Método SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5381a-102">SetPermissions method (ADOX)</span></span>


<span data-ttu-id="5381a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5381a-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="5381a-104">Especifica as permissões referentes a um grupo ou usuário em um objeto.</span><span class="sxs-lookup"><span data-stu-id="5381a-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5381a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5381a-105">Syntax</span></span>

<span data-ttu-id="5381a-106">*GrupoOuUsuário*. SetPermissions*nome*, *ObjectType*, *ação*, *direitos* \[,*herdam* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="5381a-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="5381a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5381a-107">Parameters</span></span>

  - <span data-ttu-id="5381a-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="5381a-108">*Name*</span></span>

  - <span data-ttu-id="5381a-109">Um valor **String** que especifica o nome do objeto para o qual permissões serão definidas.</span><span class="sxs-lookup"><span data-stu-id="5381a-109">A **String** value that specifies the name of the object for which to set permissions.</span></span>

  - <span data-ttu-id="5381a-110">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="5381a-110">*ObjectType*</span></span>

  - <span data-ttu-id="5381a-111">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual permissões serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="5381a-111">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="5381a-112">*Action*</span><span class="sxs-lookup"><span data-stu-id="5381a-112">*Action*</span></span>

  - <span data-ttu-id="5381a-113">Um valor **Long** que pode ser uma das constantes [ActionEnum](actionenum.md) que especifica o tipo de ação a ser executada durante a definição de permissões.</span><span class="sxs-lookup"><span data-stu-id="5381a-113">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>

  - <span data-ttu-id="5381a-114">*Rights*</span><span class="sxs-lookup"><span data-stu-id="5381a-114">*Rights*</span></span>

  - <span data-ttu-id="5381a-115">Um valor **Long** que pode ser uma máscara de bits de uma ou mais constantes [RightsEnum](rightsenum.md), que indica os direitos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="5381a-115">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>

  - <span data-ttu-id="5381a-116">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="5381a-116">*Inherit*</span></span>

  - <span data-ttu-id="5381a-p101">Opcional. Um valor **Long** que pode ser uma das constantes [InheritTypeEnum](inherittypeenum.md), que especifica como os objetos herdarão essas permissões. O valor padrão é **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="5381a-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>

  - <span data-ttu-id="5381a-120">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="5381a-120">*ObjectTypeId*</span></span>

  - <span data-ttu-id="5381a-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5381a-121">Optional.</span></span> <span data-ttu-id="5381a-122">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5381a-122">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="5381a-123">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="5381a-123">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5381a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5381a-124">Remarks</span></span>

<span data-ttu-id="5381a-125">Ocorrerá um erro se o provedor não oferecer suporte à definição de direitos de acesso para grupos ou usuários.</span><span class="sxs-lookup"><span data-stu-id="5381a-125">An error will occur if the provider does not support setting access rights for groups or users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5381a-126">Ao chamar <STRONG>SetPermissions</STRONG>, a configuração de ações como <STRONG>adAccessRevoke</STRONG> substitui as configurações do parâmetro <EM>direitos</EM> .</span><span class="sxs-lookup"><span data-stu-id="5381a-126">When calling <STRONG>SetPermissions</STRONG>, setting Actions to <STRONG>adAccessRevoke</STRONG> overrides any settings of the <EM>Rights</EM> parameter.</span></span> <span data-ttu-id="5381a-127">Não defina <EM>ações</EM> para <STRONG>adAccessRevoke</STRONG> se quiser que os direitos especificados no parâmetro <EM>direitos</EM> entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="5381a-127">Do not set <EM>Actions</EM> to <STRONG>adAccessRevoke</STRONG> if you want the rights specified in the <EM>Rights</EM> parameter to take effect.</span></span></P>


