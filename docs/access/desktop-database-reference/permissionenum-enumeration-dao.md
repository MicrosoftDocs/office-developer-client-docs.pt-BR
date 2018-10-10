---
title: Enumeração PermissionEnum (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e87482940918f3e12713f2e207e2e590895838a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463562"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="cbb27-102">Enumeração PermissionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="cbb27-102">PermissionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="cbb27-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbb27-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cbb27-104">Usada com a propriedade **Permissions** para especificar o tipo das permissões.</span><span class="sxs-lookup"><span data-stu-id="cbb27-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbb27-105">Nome</span><span class="sxs-lookup"><span data-stu-id="cbb27-105">Name</span></span></p></th>
<th><p><span data-ttu-id="cbb27-106">Valor</span><span class="sxs-lookup"><span data-stu-id="cbb27-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cbb27-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbb27-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="cbb27-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="cbb27-109">1</span><span class="sxs-lookup"><span data-stu-id="cbb27-109">1</span></span></p></td>
<td><p><span data-ttu-id="cbb27-110">O usuário pode criar novos documentos (não é válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="cbb27-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="cbb27-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="cbb27-112">8</span><span class="sxs-lookup"><span data-stu-id="cbb27-112">8</span></span></p></td>
<td><p><span data-ttu-id="cbb27-113">O usuário pode replicar um banco de dados e alterar a senha do banco de dados (não é válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="cbb27-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="cbb27-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="cbb27-115">1</span><span class="sxs-lookup"><span data-stu-id="cbb27-115">1</span></span></p></td>
<td><p><span data-ttu-id="cbb27-p101">O usuário pode criar novos bancos de dados. Esta opção é válida somente no contêiner Bancos de Dados do arquivo de informações do grupo de trabalho (Systen.mdw). Esta constante não é válida para objetos Document.</span><span class="sxs-lookup"><span data-stu-id="cbb27-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="cbb27-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="cbb27-120">4</span><span class="sxs-lookup"><span data-stu-id="cbb27-120">4</span></span></p></td>
<td><p><span data-ttu-id="cbb27-121">O usuário tem acesso exclusivo ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cbb27-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="cbb27-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="cbb27-123">2</span><span class="sxs-lookup"><span data-stu-id="cbb27-123">2</span></span></p></td>
<td><p><span data-ttu-id="cbb27-124">O usuário pode abrir o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cbb27-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="cbb27-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="cbb27-126">65536</span><span class="sxs-lookup"><span data-stu-id="cbb27-126">65536</span></span></p></td>
<td><p><span data-ttu-id="cbb27-127">O usuário pode excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="cbb27-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="cbb27-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="cbb27-129">128</span><span class="sxs-lookup"><span data-stu-id="cbb27-129">128</span></span></p></td>
<td><p><span data-ttu-id="cbb27-130">O usuário pode excluir registros.</span><span class="sxs-lookup"><span data-stu-id="cbb27-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="cbb27-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="cbb27-132">1048575</span><span class="sxs-lookup"><span data-stu-id="cbb27-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="cbb27-133">O usuário tem acesso completo ao objeto.</span><span class="sxs-lookup"><span data-stu-id="cbb27-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="cbb27-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="cbb27-135">32</span><span class="sxs-lookup"><span data-stu-id="cbb27-135">32</span></span></p></td>
<td><p><span data-ttu-id="cbb27-136">O usuário pode adicionar registros.</span><span class="sxs-lookup"><span data-stu-id="cbb27-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="cbb27-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="cbb27-138">0</span><span class="sxs-lookup"><span data-stu-id="cbb27-138">0</span></span></p></td>
<td><p><span data-ttu-id="cbb27-139">O usuário não tem acesso ao objeto (não é válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="cbb27-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="cbb27-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="cbb27-141">4</span><span class="sxs-lookup"><span data-stu-id="cbb27-141">4</span></span></p></td>
<td><p><span data-ttu-id="cbb27-142">O usuário pode ler a definição da tabela, inclusive informações de coluna e índice.</span><span class="sxs-lookup"><span data-stu-id="cbb27-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="cbb27-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="cbb27-144">131072</span><span class="sxs-lookup"><span data-stu-id="cbb27-144">131072</span></span></p></td>
<td><p><span data-ttu-id="cbb27-145">O usuário pode ler as informações relativas à segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="cbb27-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="cbb27-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="cbb27-147">64</span><span class="sxs-lookup"><span data-stu-id="cbb27-147">64</span></span></p></td>
<td><p><span data-ttu-id="cbb27-148">O usuário pode modificar registros.</span><span class="sxs-lookup"><span data-stu-id="cbb27-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="cbb27-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="cbb27-150">20</span><span class="sxs-lookup"><span data-stu-id="cbb27-150">20</span></span></p></td>
<td><p><span data-ttu-id="cbb27-151">O usuário pode recuperar dados do objeto Document.</span><span class="sxs-lookup"><span data-stu-id="cbb27-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="cbb27-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="cbb27-153">65548</span><span class="sxs-lookup"><span data-stu-id="cbb27-153">65548</span></span></p></td>
<td><p><span data-ttu-id="cbb27-154">O usuário pode modificar ou excluir a definição da tabela, inclusive as informações de coluna e índice.</span><span class="sxs-lookup"><span data-stu-id="cbb27-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbb27-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="cbb27-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="cbb27-156">524288</span><span class="sxs-lookup"><span data-stu-id="cbb27-156">524288</span></span></p></td>
<td><p><span data-ttu-id="cbb27-157">O usuário pode alterar a configuração da propriedade Proprietário.</span><span class="sxs-lookup"><span data-stu-id="cbb27-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbb27-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="cbb27-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="cbb27-159">262144</span><span class="sxs-lookup"><span data-stu-id="cbb27-159">262144</span></span></p></td>
<td><p><span data-ttu-id="cbb27-160">O usuário pode alterar permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="cbb27-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

