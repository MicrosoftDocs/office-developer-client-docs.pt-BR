---
title: Instrução GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716394"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="88090-102">Instrução GRANT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="88090-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="88090-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="88090-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88090-104">Concede privilégios específicos a um usuário ou grupo existente.</span><span class="sxs-lookup"><span data-stu-id="88090-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="88090-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88090-105">Syntax</span></span>

<span data-ttu-id="88090-106">GRANT {*privilégio*\[, *privilégios*,... \]} Diante {tabela *tabela* | OBJETO *objeto*|</span><span class="sxs-lookup"><span data-stu-id="88090-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="88090-107">CONTAINER *contêiner* } TO {*authorizationname*\[, *authorizationname*, … \]}</span><span class="sxs-lookup"><span data-stu-id="88090-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="88090-108">A instrução GRANT tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="88090-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88090-109">Parte</span><span class="sxs-lookup"><span data-stu-id="88090-109">Part</span></span></p></th>
<th><p><span data-ttu-id="88090-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="88090-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88090-111"><em>privilege</em></span><span class="sxs-lookup"><span data-stu-id="88090-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="88090-112">O privilégio ou privilégios a serem concedidos.</span><span class="sxs-lookup"><span data-stu-id="88090-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="88090-113">Privilégios são especificados com as seguintes palavras-chave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="88090-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88090-114"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="88090-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="88090-115">Nenhum nome de tabela válido.</span><span class="sxs-lookup"><span data-stu-id="88090-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88090-116"><em>objeto</em></span><span class="sxs-lookup"><span data-stu-id="88090-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="88090-p102">Isso pode incluir qualquer objeto não-tabela. Uma consulta armazenada (visualização ou procedimento) é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="88090-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88090-119"><em>container</em></span><span class="sxs-lookup"><span data-stu-id="88090-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="88090-120">O nome de um contêiner válido.</span><span class="sxs-lookup"><span data-stu-id="88090-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88090-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="88090-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="88090-122">Um nome de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="88090-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

