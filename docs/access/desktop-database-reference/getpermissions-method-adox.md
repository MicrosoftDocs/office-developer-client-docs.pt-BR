---
title: Método GetPermissions (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 388cbc5a69f57778d8a9a46db8d1dbec5ddf09d6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604957"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="f6615-102">Método GetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f6615-102">GetPermissions Method (ADOX)</span></span>


<span data-ttu-id="f6615-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6615-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="f6615-104">Retorna as permissões de um grupo ou usuário em um objeto ou contêiner de objetos.</span><span class="sxs-lookup"><span data-stu-id="f6615-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6615-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6615-105">Syntax</span></span>

<span data-ttu-id="f6615-106">*ReturnValue* = *GrupoOuUsuário*. GetPermissions (*nome*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="f6615-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="f6615-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="f6615-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f6615-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f6615-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f6615-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f6615-109">Return value</span></span>
>>>>>>> <span data-ttu-id="f6615-110">mestre</span><span class="sxs-lookup"><span data-stu-id="f6615-110">master</span></span>

<span data-ttu-id="f6615-p101">Retorna um valor **Long** que especifica um bitmask que contém as permissões do grupo ou usuário no objeto. Este valor pode ser uma ou mais das constantes [RightsEnum](rightsenum.md).</span><span class="sxs-lookup"><span data-stu-id="f6615-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6615-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6615-113">Parameters</span></span>

  - <span data-ttu-id="f6615-114">*Name*</span><span class="sxs-lookup"><span data-stu-id="f6615-114">*Name*</span></span>

  - <span data-ttu-id="f6615-115">Um valor **Variant** que especifica o nome do objeto cujas permissões devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="f6615-115">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="f6615-116">Definir o *nome* como um valor nulo se você deseja obter as permissões para o contêiner do objeto.</span><span class="sxs-lookup"><span data-stu-id="f6615-116">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>

  - <span data-ttu-id="f6615-117">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="f6615-117">*ObjectType*</span></span>

  - <span data-ttu-id="f6615-118">Um valor **Long**, que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto para o qual devem ser obtidas permissões.</span><span class="sxs-lookup"><span data-stu-id="f6615-118">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="f6615-119">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="f6615-119">*ObjectTypeId*</span></span>

  - <span data-ttu-id="f6615-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f6615-120">Optional.</span></span> <span data-ttu-id="f6615-121">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f6615-121">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="f6615-122">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="f6615-122">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

