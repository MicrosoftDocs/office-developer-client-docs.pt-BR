---
title: Método GetPermissions (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719740"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="cbea9-102">Método GetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cbea9-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="cbea9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbea9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbea9-104">Retorna as permissões de um grupo ou usuário em um objeto ou contêiner de objetos.</span><span class="sxs-lookup"><span data-stu-id="cbea9-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbea9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbea9-105">Syntax</span></span>

<span data-ttu-id="cbea9-106">*ReturnValue* = *GrupoOuUsuário*. GetPermissions (*nome*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="cbea9-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="cbea9-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cbea9-107">Return value</span></span>

<span data-ttu-id="cbea9-p101">Retorna um valor **Long** que especifica um bitmask que contém as permissões do grupo ou usuário no objeto. Este valor pode ser uma ou mais das constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="cbea9-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbea9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbea9-110">Parameters</span></span>

|<span data-ttu-id="cbea9-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbea9-111">Parameter</span></span>|<span data-ttu-id="cbea9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbea9-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cbea9-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="cbea9-113">*Name*</span></span> |<span data-ttu-id="cbea9-114">Um valor **Variant** que especifica o nome do objeto cujas permissões devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="cbea9-114">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="cbea9-115">Definir o *nome* como um valor nulo se você deseja obter as permissões para o contêiner do objeto.</span><span class="sxs-lookup"><span data-stu-id="cbea9-115">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="cbea9-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="cbea9-116">*ObjectType*</span></span> |<span data-ttu-id="cbea9-117">Um valor **Long**, que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual devem ser obtidas permissões.</span><span class="sxs-lookup"><span data-stu-id="cbea9-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="cbea9-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="cbea9-118">*ObjectTypeId*</span></span> |<span data-ttu-id="cbea9-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cbea9-119">Optional.</span></span> <span data-ttu-id="cbea9-120">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cbea9-120">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="cbea9-121">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="cbea9-121">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

