---
title: Instrução ALTER USER ou DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ad03607b6452da016bad09fd33561bd811a2a16d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862608"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="fb46e-102">Instrução ALTER USER ou DATABASE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fb46e-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="fb46e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb46e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fb46e-104">Altera a senha de um usuário existente ou de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fb46e-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb46e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb46e-105">Syntax</span></span>

<span data-ttu-id="fb46e-106">ALTER DATABASE PASSWORD *novasenha senhaantiga*</span><span class="sxs-lookup"><span data-stu-id="fb46e-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="fb46e-107">ALTER USER *usuário* PASSWORD *novasenha senhaantiga*</span><span class="sxs-lookup"><span data-stu-id="fb46e-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="fb46e-108">A instrução ALTER USER ou DATABASE possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="fb46e-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb46e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fb46e-109">Part</span></span></p></th>
<th><p><span data-ttu-id="fb46e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb46e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb46e-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="fb46e-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="fb46e-112">O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fb46e-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb46e-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="fb46e-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="fb46e-114">A nova senha que será associada ao nome do <em>usuário</em> ou do <em>banco de dados</em> especificado.</span><span class="sxs-lookup"><span data-stu-id="fb46e-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb46e-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="fb46e-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="fb46e-116">A senha existente que será associada ao nome do <em>usuário</em> ou do <em>grupo</em> especificado.</span><span class="sxs-lookup"><span data-stu-id="fb46e-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

