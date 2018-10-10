---
title: Método GetPermissions (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b7e6603d8da5bafc7a479cb8bfe94577a0679bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464421"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="e4950-102">Método GetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e4950-102">GetPermissions Method (ADOX)</span></span>


<span data-ttu-id="e4950-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4950-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e4950-104">Retorna as permissões de um grupo ou usuário em um objeto ou contêiner de objetos.</span><span class="sxs-lookup"><span data-stu-id="e4950-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4950-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4950-105">Syntax</span></span>

<span data-ttu-id="e4950-106">*ReturnValue* = *GrupoOuUsuário*. GetPermissions (*nome*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="e4950-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="e4950-107">Return Value</span><span class="sxs-lookup"><span data-stu-id="e4950-107">Return Value</span></span>

<span data-ttu-id="e4950-p101">Retorna um valor **Long** que especifica um bitmask que contém as permissões do grupo ou usuário no objeto. Este valor pode ser uma ou mais das constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="e4950-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4950-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4950-110">Parameters</span></span>

  - <span data-ttu-id="e4950-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="e4950-111">*Name*</span></span>

  - <span data-ttu-id="e4950-112">Um valor **Variant** que especifica o nome do objeto cujas permissões devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="e4950-112">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="e4950-113">Definir o *nome* como um valor nulo se você deseja obter as permissões para o contêiner do objeto.</span><span class="sxs-lookup"><span data-stu-id="e4950-113">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>

  - <span data-ttu-id="e4950-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="e4950-114">*ObjectType*</span></span>

  - <span data-ttu-id="e4950-115">Um valor **Long**, que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual devem ser obtidas permissões.</span><span class="sxs-lookup"><span data-stu-id="e4950-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="e4950-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="e4950-116">*ObjectTypeId*</span></span>

  - <span data-ttu-id="e4950-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e4950-117">Optional.</span></span> <span data-ttu-id="e4950-118">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e4950-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="e4950-119">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="e4950-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

