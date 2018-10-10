---
title: Instrução REVOKE (Microsoft Access SQL)
TOCTitle: REVOKE Statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf8bbe65b8fe359e9e410d652deb41a1192efa92
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462612"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="05808-102">Instrução REVOKE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="05808-102">REVOKE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="05808-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05808-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05808-104">Revoga privilégios específicos de um usuário ou grupo existente.</span><span class="sxs-lookup"><span data-stu-id="05808-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="05808-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05808-105">Syntax</span></span>

<span data-ttu-id="05808-106">REVOGAR {*privilégio*\[, *privilégios*,... \]} Diante {tabela *tabela* | OBJETO *objeto*|</span><span class="sxs-lookup"><span data-stu-id="05808-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="05808-107">*Contêiner*do CONTÊINER} FROM {*authorizationname*\[, *authorizationname*, … \]}</span><span class="sxs-lookup"><span data-stu-id="05808-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="05808-108">A instrução REVOKE contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="05808-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05808-109">Parte</span><span class="sxs-lookup"><span data-stu-id="05808-109">Part</span></span></p></th>
<th><p><span data-ttu-id="05808-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="05808-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05808-111"><em>privilege</em></span><span class="sxs-lookup"><span data-stu-id="05808-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="05808-112">O privilégio ou privilégios a serem revogados.</span><span class="sxs-lookup"><span data-stu-id="05808-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="05808-113">Privilégios são especificados com as seguintes palavras-chave: selecionar, excluir, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA e UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="05808-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05808-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="05808-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="05808-115">Nenhum nome de tabela válido.</span><span class="sxs-lookup"><span data-stu-id="05808-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05808-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="05808-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="05808-p102">Isso pode incluir qualquer objeto não-tabela. Uma consulta armazenada (visualização ou procedimento) é um exemplo.</span><span class="sxs-lookup"><span data-stu-id="05808-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05808-119"><em>container</em></span><span class="sxs-lookup"><span data-stu-id="05808-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="05808-120">O nome de um contêiner válido.</span><span class="sxs-lookup"><span data-stu-id="05808-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05808-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="05808-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="05808-122">Um nome de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="05808-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

