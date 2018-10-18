---
title: Método GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6c2432370f2480484cf1165249bc8573b27372
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603109"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="98b03-102">Método GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="98b03-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="98b03-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98b03-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="98b03-104">Retorna o proprietário de um objeto em um [Catálogo](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="98b03-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98b03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98b03-105">Syntax</span></span>

<span data-ttu-id="98b03-106">*Proprietário* = *catálogo*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="98b03-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="98b03-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="98b03-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="98b03-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="98b03-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="98b03-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="98b03-109">Return value</span></span>
>>>>>>> <span data-ttu-id="98b03-110">mestre</span><span class="sxs-lookup"><span data-stu-id="98b03-110">master</span></span>

<span data-ttu-id="98b03-111">Retorna um valor **String** que especifica o [Nome](name-property-adox.md) do [Usuário](user-object-adox.md) ou [Grupo](group-object-adox.md) proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="98b03-111">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="98b03-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b03-112">Parameters</span></span>

  - <span data-ttu-id="98b03-113">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="98b03-113">*ObjectName*</span></span>

  - <span data-ttu-id="98b03-114">Um valor **String** que especifica o nome do objeto para o qual o usuário deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="98b03-114">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="98b03-115">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="98b03-115">*ObjectType*</span></span>

  - <span data-ttu-id="98b03-116">Um valor **Long** que pode ser uma das constantes [ObjectTypeEnum](objecttypeenum.md), que especifica o tipo do objeto cujo proprietário deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="98b03-116">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="98b03-117">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="98b03-117">*ObjectTypeId*</span></span>

  - <span data-ttu-id="98b03-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="98b03-118">Optional.</span></span> <span data-ttu-id="98b03-119">Um valor **Variant** que especifica o GUID referente a um tipo de objeto de provedor não definido pela especificação OLE DB.</span><span class="sxs-lookup"><span data-stu-id="98b03-119">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="98b03-120">Este parâmetro é obrigatório se *ObjectType* estiver definida como **adPermObjProviderSpecific**; Caso contrário, ele não é usado.</span><span class="sxs-lookup"><span data-stu-id="98b03-120">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="98b03-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="98b03-121">Remarks</span></span>

<span data-ttu-id="98b03-122">Ocorrerá um erro se o provedor não oferecer suporte para o retorno de proprietários de objetos.</span><span class="sxs-lookup"><span data-stu-id="98b03-122">An error will occur if the provider does not support returning object owners.</span></span>

