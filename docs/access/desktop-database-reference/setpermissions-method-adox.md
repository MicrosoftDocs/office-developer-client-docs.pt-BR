---
title: Método setPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314578"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="39dd2-102">Método setPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="39dd2-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="39dd2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39dd2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39dd2-104">Especifica as permissões referentes a um grupo ou usuário em um objeto.</span><span class="sxs-lookup"><span data-stu-id="39dd2-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="39dd2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39dd2-105">Syntax</span></span>

<span data-ttu-id="39dd2-106">*GroupOrUser*. SetPermissions*Name*, *objecttype*, *Action*, *Rights* \[,*Inherit* \] \[, objecttypeid\*\*\]</span><span class="sxs-lookup"><span data-stu-id="39dd2-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="39dd2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39dd2-107">Parameters</span></span>

|<span data-ttu-id="39dd2-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="39dd2-108">Parameter</span></span>|<span data-ttu-id="39dd2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="39dd2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="39dd2-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="39dd2-110">*Name*</span></span> |<span data-ttu-id="39dd2-111">Um valor **String** que especifica o nome do objeto para o qual permissões serão definidas.</span><span class="sxs-lookup"><span data-stu-id="39dd2-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="39dd2-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="39dd2-112">*ObjectType*</span></span> |<span data-ttu-id="39dd2-113">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual permissões serão obtidas.</span><span class="sxs-lookup"><span data-stu-id="39dd2-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="39dd2-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="39dd2-114">*Action*</span></span> |<span data-ttu-id="39dd2-115">Um valor **Long** que pode ser uma das constantes [ActionEnum](actionenum.md) que especifica o tipo de ação a ser executada durante a definição de permissões.</span><span class="sxs-lookup"><span data-stu-id="39dd2-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="39dd2-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="39dd2-116">*Rights*</span></span> |<span data-ttu-id="39dd2-117">Um valor **Long** que pode ser uma máscara de bits de uma ou mais constantes [RightsEnum](rightsenum.md), que indica os direitos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="39dd2-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="39dd2-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="39dd2-118">*Inherit*</span></span> |<span data-ttu-id="39dd2-p101">Opcional. Um valor **Long** que pode ser uma das constantes [InheritTypeEnum](inherittypeenum.md), que especifica como os objetos herdarão essas permissões. O valor padrão é **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="39dd2-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="39dd2-122">*ObjectTypeid*</span><span class="sxs-lookup"><span data-stu-id="39dd2-122">*ObjectTypeId*</span></span> |<span data-ttu-id="39dd2-p102">Opcional. Um valor **Variant** que especifica o GUID de um tipo de objeto do provedor, não definido pela especificação do OLE DB. Este parâmetro será necessário se *ObjectType* for definido como **adPermObjProviderSpecific**; caso contrário, ele não será usado.</span><span class="sxs-lookup"><span data-stu-id="39dd2-p102">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="39dd2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="39dd2-126">Remarks</span></span>

<span data-ttu-id="39dd2-127">Ocorrerá um erro se o provedor não oferecer suporte à definição de direitos de acesso para grupos ou usuários.</span><span class="sxs-lookup"><span data-stu-id="39dd2-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="39dd2-p103">Durante a chamada de **SetPermissions**, a definição de Actions como **adAccessRevoke** substituirá as configurações do parâmetro *Rights*. Não defina *Actions* como **adAccessRevoke** se desejar que os direitos especificados no parâmetro *Rights* entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="39dd2-p103">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter. Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


