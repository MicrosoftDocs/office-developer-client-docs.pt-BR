---
title: Método Append (Usuários do ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc8f7a2d217a25a8404765aa05bae19fdccad2c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863861"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="1dda2-102">Método Append (Usuários do ADOX)</span><span class="sxs-lookup"><span data-stu-id="1dda2-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="1dda2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1dda2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="1dda2-104">Adiciona um novo objeto [User](user-object-adox.md) à coleção [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="1dda2-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dda2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dda2-105">Syntax</span></span>

<span data-ttu-id="1dda2-106">*Os usuários*. Acrescentar*usuário*\[,*senha*\]</span><span class="sxs-lookup"><span data-stu-id="1dda2-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="1dda2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dda2-107">Parameters</span></span>

  - <span data-ttu-id="1dda2-108">*User*</span><span class="sxs-lookup"><span data-stu-id="1dda2-108">*User*</span></span>

  - <span data-ttu-id="1dda2-109">Um valor **Variant** que contém o objeto **User** a ser anexado ou o nome do usuário a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="1dda2-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="1dda2-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="1dda2-110">*Password*</span></span>

  - <span data-ttu-id="1dda2-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1dda2-111">Optional.</span></span> <span data-ttu-id="1dda2-112">Um valor **String** que contém a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dda2-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="1dda2-113">O parâmetro *Password* corresponde ao valor especificado pelo método [ChangePassword](changepassword-method-adox.md) de um objeto de **usuário** .</span><span class="sxs-lookup"><span data-stu-id="1dda2-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dda2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dda2-114">Remarks</span></span>

<span data-ttu-id="1dda2-p102">A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.</span><span class="sxs-lookup"><span data-stu-id="1dda2-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="1dda2-117">Ocorrerá um erro se o provedor não oferecer suporte para a criação de usuários.</span><span class="sxs-lookup"><span data-stu-id="1dda2-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <span data-ttu-id="1dda2-118">[!OBSERVAçãO] Antes de um objeto **User** ser anexado à coleção **Users** de um objeto **Group**, na coleção **Users** do [Catálogo](name-property-adox.md) já deve existir um objeto **User** com o mesmo **Nome** daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="1dda2-118">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


