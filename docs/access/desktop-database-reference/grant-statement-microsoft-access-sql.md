---
title: Instrução GRANT (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461985"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="bdfdc-102">Instrução GRANT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="bdfdc-102">GRANT Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="bdfdc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bdfdc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bdfdc-104">Concede privilégios específicos a um usuário ou grupo existente.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfdc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdfdc-105">Syntax</span></span>

<span data-ttu-id="bdfdc-106">GRANT {*privilégio*\[, *privilégios*,... \]} Diante {tabela *tabela* | OBJETO *objeto*|</span><span class="sxs-lookup"><span data-stu-id="bdfdc-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="bdfdc-107">CONTAINER *contêiner* } TO {*authorizationname*\[, *authorizationname*, … \]}</span><span class="sxs-lookup"><span data-stu-id="bdfdc-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="bdfdc-108">A instrução GRANT tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="bdfdc-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdfdc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bdfdc-109">Part</span></span></p></th>
<th><p><span data-ttu-id="bdfdc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdfdc-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdfdc-111"><em>privilege</em></span><span class="sxs-lookup"><span data-stu-id="bdfdc-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="bdfdc-112">O privilégio ou privilégios a serem concedidos.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="bdfdc-113">Privilégios são especificados com as seguintes palavras-chave: selecionar, excluir, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfdc-114"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="bdfdc-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="bdfdc-115">Nenhum nome de tabela válido.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfdc-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="bdfdc-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="bdfdc-p102">Isso pode incluir qualquer objeto não-tabela. Uma consulta armazenada (visualização ou procedimento) é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdfdc-119"><em>container</em></span><span class="sxs-lookup"><span data-stu-id="bdfdc-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="bdfdc-120">O nome de um contêiner válido.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdfdc-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="bdfdc-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="bdfdc-122">Um nome de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="bdfdc-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

