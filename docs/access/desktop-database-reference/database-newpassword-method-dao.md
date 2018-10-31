---
title: Método Database.NewPassword (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 892dc16d0422572e83f92316ce2c1c67f9ce5cc0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860641"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="2fe6b-102">Método Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="2fe6b-102">Database.NewPassword Method (DAO)</span></span>


<span data-ttu-id="2fe6b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fe6b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2fe6b-104">Altera a senha de um banco de dados existente do mecanismo de banco de dados do Microsoft Access (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fe6b-105">Syntax</span></span>

<span data-ttu-id="2fe6b-106">*expressão* . NewPassword (***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="2fe6b-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="2fe6b-107">*expressão* Uma expressão que retorna um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="2fe6b-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2fe6b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fe6b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fe6b-109">Nome</span><span class="sxs-lookup"><span data-stu-id="2fe6b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2fe6b-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="2fe6b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2fe6b-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2fe6b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2fe6b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2fe6b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fe6b-113">bstrOld</span><span class="sxs-lookup"><span data-stu-id="2fe6b-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="2fe6b-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2fe6b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2fe6b-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="2fe6b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2fe6b-116">A configuração atual da propriedade <strong>Password</strong> do objeto <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fe6b-117">bstrNew</span><span class="sxs-lookup"><span data-stu-id="2fe6b-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="2fe6b-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2fe6b-118">Required</span></span></p></td>
<td><p><span data-ttu-id="2fe6b-119"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="2fe6b-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2fe6b-120">A nova configuração da propriedade <strong>Password</strong> do objeto <strong>Database</strong> .</span><span class="sxs-lookup"><span data-stu-id="2fe6b-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>

> [!NOTE]
> <span data-ttu-id="2fe6b-p101">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-p101">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2fe6b-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fe6b-126">Remarks</span></span>

<span data-ttu-id="2fe6b-127">As cadeias de caracteres bstrOld e bstrNew podem ter até 20 caracteres e podem incluir qualquer caractere exceto o caractere ASCII 0 (nulo).</span><span class="sxs-lookup"><span data-stu-id="2fe6b-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="2fe6b-128">Para limpar a senha, use uma cadeia de caracteres de comprimento zero ("") para bstrNew.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="2fe6b-129">Senhas diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="2fe6b-130">Se um banco de dados não tiver senha, o mecanismo de banco de dados do Microsoft Access criará uma automaticamente passando uma cadeia de caracteres de comprimento zero ("") para a senha antiga.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="2fe6b-131">[!IMPORTANTE] Se perder a sua senha, você nunca mais poderá abrir o seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2fe6b-131">If you lose your password, you can never open the database again.</span></span>


