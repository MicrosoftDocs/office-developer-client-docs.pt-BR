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
ms.openlocfilehash: e72d879482c3ed69b262f2f4d0f07a4e11f8fa4c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998935"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="61336-102">Método Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="61336-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="61336-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="61336-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61336-104">Altera a senha de um banco de dados existente do mecanismo de banco de dados do Microsoft Access (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="61336-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="61336-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61336-105">Syntax</span></span>

<span data-ttu-id="61336-106">*expressão* . NewPassword (***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="61336-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="61336-107">*expressão* Uma expressão que retorna um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="61336-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="61336-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61336-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61336-109">Nome</span><span class="sxs-lookup"><span data-stu-id="61336-109">Name</span></span></p></th>
<th><p><span data-ttu-id="61336-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="61336-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="61336-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="61336-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="61336-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="61336-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61336-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="61336-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="61336-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61336-114">Required</span></span></p></td>
<td><p><span data-ttu-id="61336-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="61336-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="61336-116">A configuração atual da propriedade <strong>Password</strong> do objeto <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="61336-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61336-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="61336-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="61336-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61336-118">Required</span></span></p></td>
<td><p><span data-ttu-id="61336-119"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="61336-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="61336-120">A nova configuração da propriedade <strong>Password</strong> do objeto <strong>Database</strong> .</span><span class="sxs-lookup"><span data-stu-id="61336-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="61336-121"><strong>Observação</strong>: Use senhas fortes que combinam maiusculas e minúsculas, números e símbolos.</span><span class="sxs-lookup"><span data-stu-id="61336-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="61336-122">As senhas fracas não combinam esses elementos.</span><span class="sxs-lookup"><span data-stu-id="61336-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="61336-123">Senha forte: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="61336-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="61336-124">Senha fraca: House27.</span><span class="sxs-lookup"><span data-stu-id="61336-124">Weak password: House27.</span></span> <span data-ttu-id="61336-125">Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="61336-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="61336-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="61336-126">Remarks</span></span>

<span data-ttu-id="61336-127">As cadeias de caracteres bstrOld e bstrNew podem ter até 20 caracteres e podem incluir qualquer caractere exceto o caractere ASCII 0 (nulo).</span><span class="sxs-lookup"><span data-stu-id="61336-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="61336-128">Para limpar a senha, use uma cadeia de caracteres de comprimento zero ("") para bstrNew.</span><span class="sxs-lookup"><span data-stu-id="61336-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="61336-129">Senhas diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="61336-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="61336-130">Se um banco de dados não tiver senha, o mecanismo de banco de dados do Microsoft Access criará uma automaticamente passando uma cadeia de caracteres de comprimento zero ("") para a senha antiga.</span><span class="sxs-lookup"><span data-stu-id="61336-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="61336-131">[!IMPORTANTE] Se perder a sua senha, você nunca mais poderá abrir o seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="61336-131">If you lose your password, you can never open the database again.</span></span>


