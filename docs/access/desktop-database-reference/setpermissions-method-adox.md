---
title: Método SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710283"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="83819-102">Método SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="83819-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="83819-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="83819-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83819-104">Especifica as permissões referentes a um grupo ou usuário em um objeto.</span><span class="sxs-lookup"><span data-stu-id="83819-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="83819-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83819-105">Syntax</span></span>

<span data-ttu-id="83819-106">*GrupoOuUsuário*. SetPermissions*nome*, *ObjectType*, *ação*, *direitos* \[,*herdam* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="83819-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="83819-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83819-107">Parameters</span></span>

|<span data-ttu-id="83819-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="83819-108">Parameter</span></span>|<span data-ttu-id="83819-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="83819-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="83819-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="83819-110">*Name*</span></span> |<span data-ttu-id="83819-111">Um valor **String** que especifica o nome do objeto para o qual permissões serão definidas.</span><span class="sxs-lookup"><span data-stu-id="83819-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="83819-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="83819-112">*ObjectType*</span></span> |<span data-ttu-id="83819-113">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual permissões serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="83819-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="83819-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="83819-114">*Action*</span></span> |<span data-ttu-id="83819-115">Um valor **Long** que pode ser uma das constantes [ActionEnum](actionenum.md) que especifica o tipo de ação a ser executada durante a definição de permissões.</span><span class="sxs-lookup"><span data-stu-id="83819-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="83819-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="83819-116">*Rights*</span></span> |<span data-ttu-id="83819-117">Um valor **Long** que pode ser uma máscara de bits de uma ou mais constantes [RightsEnum](rightsenum.md), que indica os direitos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="83819-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="83819-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="83819-118">*Inherit*</span></span> |<span data-ttu-id="83819-p101">Opcional. Um valor **Long** que pode ser uma das constantes [InheritTypeEnum](inherittypeenum.md), que especifica como os objetos herdarão essas permissões. O valor padrão é **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="83819-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="83819-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="83819-122">*ObjectTypeId*</span></span> |<span data-ttu-id="83819-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="83819-123">Optional.</span></span> <span data-ttu-id="83819-124">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="83819-124">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="83819-125">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="83819-125">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="83819-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="83819-126">Remarks</span></span>

<span data-ttu-id="83819-127">Ocorrerá um erro se o provedor não oferecer suporte à definição de direitos de acesso para grupos ou usuários.</span><span class="sxs-lookup"><span data-stu-id="83819-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="83819-128">Ao chamar **SetPermissions**, a configuração de ações como **adAccessRevoke** substitui as configurações do parâmetro *direitos* .</span><span class="sxs-lookup"><span data-stu-id="83819-128">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter.</span></span> <span data-ttu-id="83819-129">Não defina *ações* para **adAccessRevoke** se quiser que os direitos especificados no parâmetro *direitos* entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="83819-129">Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


