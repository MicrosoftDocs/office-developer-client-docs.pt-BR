---
title: Instrução ALTER USER ou DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297176"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="19fd3-102">Instrução ALTER USER ou DATABASE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="19fd3-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="19fd3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19fd3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19fd3-104">Altera a senha de um usuário existente ou de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="19fd3-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fd3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19fd3-105">Syntax</span></span>

<span data-ttu-id="19fd3-106">ALTER DATABASE PASSWORD *novasenha senhaantiga*</span><span class="sxs-lookup"><span data-stu-id="19fd3-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="19fd3-107">ALTER USER *usuário* PASSWORD *novasenha senhaantiga*</span><span class="sxs-lookup"><span data-stu-id="19fd3-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="19fd3-108">A instrução ALTER USER ou DATABASE possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="19fd3-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19fd3-109">Sair</span><span class="sxs-lookup"><span data-stu-id="19fd3-109">Part</span></span></p></th>
<th><p><span data-ttu-id="19fd3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="19fd3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19fd3-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="19fd3-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="19fd3-112">O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="19fd3-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19fd3-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="19fd3-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="19fd3-114">A nova senha que será associada ao nome do <em>usuário</em> ou do <em>banco de dados</em> especificado.</span><span class="sxs-lookup"><span data-stu-id="19fd3-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19fd3-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="19fd3-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="19fd3-116">A senha existente que será associada ao nome do <em>usuário</em> ou do <em>grupo</em> especificado.</span><span class="sxs-lookup"><span data-stu-id="19fd3-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

