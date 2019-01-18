---
title: Método GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710725"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="5d6b1-102">Método GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5d6b1-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="5d6b1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d6b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d6b1-104">Retorna o proprietário de um objeto em um [Catálogo](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5d6b1-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d6b1-105">Syntax</span></span>

<span data-ttu-id="5d6b1-106">*Proprietário* = *catálogo*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="5d6b1-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="5d6b1-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5d6b1-107">Return value</span></span>

<span data-ttu-id="5d6b1-108">Retorna um valor **String** que especifica o [Nome](name-property-adox.md) do [Usuário](user-object-adox.md) ou [Grupo](group-object-adox.md) proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d6b1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d6b1-109">Parameters</span></span>

|<span data-ttu-id="5d6b1-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d6b1-110">Parameter</span></span>|<span data-ttu-id="5d6b1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d6b1-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5d6b1-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="5d6b1-112">*ObjectName*</span></span> |<span data-ttu-id="5d6b1-113">Um valor **String** que especifica o nome do objeto para o qual o usuário deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="5d6b1-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="5d6b1-114">*ObjectType*</span></span> |<span data-ttu-id="5d6b1-115">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto cujo proprietário deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="5d6b1-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="5d6b1-116">*ObjectTypeId*</span></span> |<span data-ttu-id="5d6b1-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-117">Optional.</span></span> <span data-ttu-id="5d6b1-118">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="5d6b1-119">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5d6b1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d6b1-120">Remarks</span></span>

<span data-ttu-id="5d6b1-121">Ocorrerá um erro se o provedor não oferecer suporte para o retorno de proprietários de objetos.</span><span class="sxs-lookup"><span data-stu-id="5d6b1-121">An error will occur if the provider does not support returning object owners.</span></span>

