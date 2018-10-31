---
title: REVOGAR instrução (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860543"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="81323-102">REVOGAR instrução (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="81323-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="81323-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="81323-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="81323-104">Revoga privilégios específicos de um usuário ou grupo existente.</span><span class="sxs-lookup"><span data-stu-id="81323-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="81323-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81323-105">Syntax</span></span>

<span data-ttu-id="81323-106">REVOGAR {*privilégio*\[, *privilégios*,... \]} Diante {tabela *tabela* | OBJETO *objeto*|</span><span class="sxs-lookup"><span data-stu-id="81323-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="81323-107">*Contêiner*do CONTÊINER} FROM {*authorizationname*\[, *authorizationname*, … \]}</span><span class="sxs-lookup"><span data-stu-id="81323-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="81323-108">A instrução REVOKE contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="81323-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81323-109">Parte</span><span class="sxs-lookup"><span data-stu-id="81323-109">Part</span></span></p></th>
<th><p><span data-ttu-id="81323-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="81323-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81323-111"><em>privilege</em></span><span class="sxs-lookup"><span data-stu-id="81323-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="81323-112">O privilégio ou privilégios a serem revogados.</span><span class="sxs-lookup"><span data-stu-id="81323-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="81323-113">Privilégios são especificados com as seguintes palavras-chave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="81323-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81323-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="81323-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="81323-115">Nenhum nome de tabela válido.</span><span class="sxs-lookup"><span data-stu-id="81323-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81323-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="81323-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="81323-p102">Isso pode incluir qualquer objeto não-tabela. Uma consulta armazenada (visualização ou procedimento) é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="81323-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81323-119"><em>container</em></span><span class="sxs-lookup"><span data-stu-id="81323-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="81323-120">O nome de um contêiner válido.</span><span class="sxs-lookup"><span data-stu-id="81323-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81323-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="81323-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="81323-122">Um nome de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="81323-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

