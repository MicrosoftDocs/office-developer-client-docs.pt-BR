---
title: Método Append (Usuários do ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462764"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="35045-102">Método Append (Usuários do ADOX)</span><span class="sxs-lookup"><span data-stu-id="35045-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="35045-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="35045-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="35045-104">Adiciona um novo objeto [User](user-object-adox.md) à coleção [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="35045-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="35045-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35045-105">Syntax</span></span>

<span data-ttu-id="35045-106">*Os usuários*. Acrescentar*usuário*\[,*senha*\]</span><span class="sxs-lookup"><span data-stu-id="35045-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="35045-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35045-107">Parameters</span></span>

  - <span data-ttu-id="35045-108">*User*</span><span class="sxs-lookup"><span data-stu-id="35045-108">*User*</span></span>

  - <span data-ttu-id="35045-109">Um valor **Variant** que contém o objeto **User** a ser anexado ou o nome do usuário a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="35045-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="35045-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="35045-110">*Password*</span></span>

  - <span data-ttu-id="35045-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="35045-111">Optional.</span></span> <span data-ttu-id="35045-112">Um valor **String** que contém a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="35045-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="35045-113">O parâmetro *Password* corresponde ao valor especificado pelo método [ChangePassword](changepassword-method-adox.md) de um objeto de **usuário** .</span><span class="sxs-lookup"><span data-stu-id="35045-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="35045-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="35045-114">Remarks</span></span>

<span data-ttu-id="35045-p102">A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.</span><span class="sxs-lookup"><span data-stu-id="35045-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="35045-117">Ocorrerá um erro se o provedor não oferecer suporte para a criação de usuários.</span><span class="sxs-lookup"><span data-stu-id="35045-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="35045-118">[!OBSERVAçãO] Antes de um objeto <STRONG>User</STRONG> ser anexado à coleção <STRONG>Users</STRONG> de um objeto <STRONG>Group</STRONG>, na coleção <STRONG>Users</STRONG> do <A href="name-property-adox.md">Catálogo</A> já deve existir um objeto <STRONG>User</STRONG> com o mesmo <STRONG>Nome</STRONG> daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="35045-118">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


