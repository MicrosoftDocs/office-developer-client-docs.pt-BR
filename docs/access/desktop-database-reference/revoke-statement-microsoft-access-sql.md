---
title: Instrução REVOKE (Microsoft Access SQL)
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
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306528"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="c57e2-102">Instrução REVOKE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c57e2-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c57e2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c57e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c57e2-104">Revoga privilégios específicos de um usuário ou grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c57e2-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c57e2-105">Syntax</span></span>

<span data-ttu-id="c57e2-106">REVOKE {*privilégio*\[, *privilégio*,... \]} Em { *tabela* Table | *Objeto* Object|</span><span class="sxs-lookup"><span data-stu-id="c57e2-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="c57e2-107">*Contêiner*separador} de {*authorizationname*\[, *authorizationname*,... \]}</span><span class="sxs-lookup"><span data-stu-id="c57e2-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="c57e2-108">A instrução REVOKE contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="c57e2-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c57e2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c57e2-109">Part</span></span></p></th>
<th><p><span data-ttu-id="c57e2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c57e2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c57e2-111"><em>mínimo</em></span><span class="sxs-lookup"><span data-stu-id="c57e2-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="c57e2-112">O privilégio ou os privilégios a serem revogados.</span><span class="sxs-lookup"><span data-stu-id="c57e2-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="c57e2-113">Os privilégios são especificados usando as seguintes palavras-chave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="c57e2-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57e2-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="c57e2-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="c57e2-115">Nenhum nome de tabela válido.</span><span class="sxs-lookup"><span data-stu-id="c57e2-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57e2-116"><em>objeto</em></span><span class="sxs-lookup"><span data-stu-id="c57e2-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="c57e2-117">Isso pode incluir qualquer objeto não-tabela.</span><span class="sxs-lookup"><span data-stu-id="c57e2-117">This can encompass any non-table object.</span></span> <span data-ttu-id="c57e2-118">Uma consulta armazenada (visualização ou procedimento) é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="c57e2-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c57e2-119"><em>contêiner</em></span><span class="sxs-lookup"><span data-stu-id="c57e2-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="c57e2-120">O nome de um contêiner válido.</span><span class="sxs-lookup"><span data-stu-id="c57e2-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c57e2-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="c57e2-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="c57e2-122">Um nome de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="c57e2-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

