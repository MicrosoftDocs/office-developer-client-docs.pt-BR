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
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708666"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="5bb3d-102">Método Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="5bb3d-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="5bb3d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bb3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bb3d-104">Altera a senha de um banco de dados existente do mecanismo de banco de dados do Microsoft Access (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5bb3d-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb3d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bb3d-105">Syntax</span></span>

<span data-ttu-id="5bb3d-106">*expressão* . NewPassword (***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="5bb3d-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="5bb3d-107">*expressão* Uma expressão que retorna um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="5bb3d-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bb3d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bb3d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bb3d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="5bb3d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5bb3d-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="5bb3d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5bb3d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5bb3d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5bb3d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bb3d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bb3d-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="5bb3d-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="5bb3d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bb3d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5bb3d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="5bb3d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5bb3d-116">A configuração atual da propriedade <strong>Password</strong> do objeto <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5bb3d-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="5bb3d-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="5bb3d-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bb3d-118">Required</span></span></p></td>
<td><p><span data-ttu-id="5bb3d-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="5bb3d-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5bb3d-120">A nova configuração da propriedade <strong>Password</strong> do objeto <strong>Database</strong> .</span><span class="sxs-lookup"><span data-stu-id="5bb3d-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="5bb3d-121"><strong>Observação</strong>: Use senhas fortes que combinam maiusculas e minúsculas, números e símbolos.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="5bb3d-122">As enhas fracas não combinam esses elementos.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="5bb3d-123">Senha forte: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="5bb3d-124">Senha fraca: House27.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-124">Weak password: House27.</span></span> <span data-ttu-id="5bb3d-125">Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5bb3d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bb3d-126">Remarks</span></span>

<span data-ttu-id="5bb3d-127">As cadeias de caracteres bstrOld e bstrNew podem ter até 20 caracteres e podem incluir qualquer caractere exceto o caractere ASCII 0 (nulo).</span><span class="sxs-lookup"><span data-stu-id="5bb3d-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="5bb3d-128">Para limpar a senha, use uma cadeia de caracteres de comprimento zero ("") para bstrNew.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="5bb3d-129">Senhas diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="5bb3d-130">Se um banco de dados não tiver senha, o mecanismo de banco de dados do Microsoft Access criará uma automaticamente passando uma cadeia de caracteres de comprimento zero ("") para a senha antiga.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="5bb3d-131">[!IMPORTANTE] Se perder a sua senha, você nunca mais poderá abrir o seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5bb3d-131">If you lose your password, you can never open the database again.</span></span>


