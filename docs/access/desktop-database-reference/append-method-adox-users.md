---
title: Método Append (Usuários do ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297064"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="d9119-102">Método Append (Usuários do ADOX)</span><span class="sxs-lookup"><span data-stu-id="d9119-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="d9119-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9119-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9119-104">Adiciona um novo objeto [User](user-object-adox.md) à coleção [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d9119-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9119-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9119-105">Syntax</span></span>

<span data-ttu-id="d9119-106">*Usuários*. Anexar*usuário*\[,*senha*\]</span><span class="sxs-lookup"><span data-stu-id="d9119-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="d9119-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9119-107">Parameters</span></span>

|<span data-ttu-id="d9119-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9119-108">Parameter</span></span>|<span data-ttu-id="d9119-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9119-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d9119-110">*User*</span><span class="sxs-lookup"><span data-stu-id="d9119-110">*User*</span></span> |<span data-ttu-id="d9119-111">Um valor **Variant** que contém o objeto **User** a ser anexado ou o nome do usuário a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="d9119-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="d9119-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="d9119-112">*Password*</span></span> |<span data-ttu-id="d9119-p101">Opcional. Um valor **String** que contém a senha do usuário. O parâmetro *Password* corresponde ao valor especificado pelo método [ChangePassword](changepassword-method-adox.md) de um objeto **User**.</span><span class="sxs-lookup"><span data-stu-id="d9119-p101">Optional. A **String** value that contains the password for the user. The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d9119-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9119-116">Remarks</span></span>

<span data-ttu-id="d9119-p102">A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.</span><span class="sxs-lookup"><span data-stu-id="d9119-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="d9119-119">Ocorrerá um erro se o provedor não oferecer suporte para a criação de usuários.</span><span class="sxs-lookup"><span data-stu-id="d9119-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="d9119-120">[!OBSERVAçãO] Antes de um objeto **User** ser anexado à coleção **Users** de um objeto **Group**, na coleção **Users** do [Catálogo](name-property-adox.md) já deve existir um objeto **User** com o mesmo **Nome** daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="d9119-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


