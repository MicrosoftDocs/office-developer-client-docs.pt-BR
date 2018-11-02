---
title: Método GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927806"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="59361-102">Método GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="59361-102">GetObjectOwner method (ADOX)</span></span>


<span data-ttu-id="59361-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="59361-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="59361-104">Retorna o proprietário de um objeto em um [Catálogo](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="59361-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59361-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59361-105">Syntax</span></span>

<span data-ttu-id="59361-106">*Proprietário* = *catálogo*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="59361-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="59361-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="59361-107">Return value</span></span>

<span data-ttu-id="59361-108">Retorna um valor **String** que especifica o [Nome](name-property-adox.md) do [Usuário](user-object-adox.md) ou [Grupo](group-object-adox.md) proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="59361-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="59361-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59361-109">Parameters</span></span>

  - <span data-ttu-id="59361-110">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="59361-110">*ObjectName*</span></span>

  - <span data-ttu-id="59361-111">Um valor **String** que especifica o nome do objeto para o qual o usuário deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="59361-111">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="59361-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="59361-112">*ObjectType*</span></span>

  - <span data-ttu-id="59361-113">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto cujo proprietário deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="59361-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="59361-114">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="59361-114">*ObjectTypeId*</span></span>

  - <span data-ttu-id="59361-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59361-115">Optional.</span></span> <span data-ttu-id="59361-116">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="59361-116">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="59361-117">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="59361-117">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="59361-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="59361-118">Remarks</span></span>

<span data-ttu-id="59361-119">Ocorrerá um erro se o provedor não oferecer suporte para o retorno de proprietários de objetos.</span><span class="sxs-lookup"><span data-stu-id="59361-119">An error will occur if the provider does not support returning object owners.</span></span>

