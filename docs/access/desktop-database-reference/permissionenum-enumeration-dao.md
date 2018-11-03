---
title: Enumeração PermissionEnum (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3abb0e3ff76ae19c6c19a3e2040b338e2b5ff3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945863"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="9f94a-102">Enumeração PermissionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f94a-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="9f94a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f94a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f94a-104">Usada com a propriedade **Permissions** para especificar o tipo das permissões.</span><span class="sxs-lookup"><span data-stu-id="9f94a-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f94a-105">Nome</span><span class="sxs-lookup"><span data-stu-id="9f94a-105">Name</span></span></p></th>
<th><p><span data-ttu-id="9f94a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9f94a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9f94a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f94a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="9f94a-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="9f94a-109">1</span><span class="sxs-lookup"><span data-stu-id="9f94a-109">1</span></span></p></td>
<td><p><span data-ttu-id="9f94a-110">O usuário pode criar novos documentos (não é válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="9f94a-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="9f94a-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="9f94a-112">8</span><span class="sxs-lookup"><span data-stu-id="9f94a-112">8</span></span></p></td>
<td><p><span data-ttu-id="9f94a-113">O usuário pode replicar um banco de dados e alterar a senha do banco de dados (não é válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="9f94a-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="9f94a-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="9f94a-115">1</span><span class="sxs-lookup"><span data-stu-id="9f94a-115">1</span></span></p></td>
<td><p><span data-ttu-id="9f94a-p101">O usuário pode criar novos bancos de dados. Esta opção é válida somente no contêiner Bancos de Dados do arquivo de informações do grupo de trabalho (Systen.mdw). Esta constante não é válida para objetos Document.</span><span class="sxs-lookup"><span data-stu-id="9f94a-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="9f94a-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="9f94a-120">4</span><span class="sxs-lookup"><span data-stu-id="9f94a-120">4</span></span></p></td>
<td><p><span data-ttu-id="9f94a-121">O usuário tem acesso exclusivo ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f94a-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="9f94a-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="9f94a-123">2</span><span class="sxs-lookup"><span data-stu-id="9f94a-123">2</span></span></p></td>
<td><p><span data-ttu-id="9f94a-124">O usuário pode abrir o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f94a-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="9f94a-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="9f94a-126">65536</span><span class="sxs-lookup"><span data-stu-id="9f94a-126">65536</span></span></p></td>
<td><p><span data-ttu-id="9f94a-127">O usuário pode excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="9f94a-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="9f94a-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="9f94a-129">128</span><span class="sxs-lookup"><span data-stu-id="9f94a-129">128</span></span></p></td>
<td><p><span data-ttu-id="9f94a-130">O usuário pode excluir registros.</span><span class="sxs-lookup"><span data-stu-id="9f94a-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="9f94a-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="9f94a-132">1048575</span><span class="sxs-lookup"><span data-stu-id="9f94a-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="9f94a-133">O usuário tem acesso completo ao objeto.</span><span class="sxs-lookup"><span data-stu-id="9f94a-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="9f94a-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="9f94a-135">32</span><span class="sxs-lookup"><span data-stu-id="9f94a-135">32</span></span></p></td>
<td><p><span data-ttu-id="9f94a-136">O usuário pode adicionar registros.</span><span class="sxs-lookup"><span data-stu-id="9f94a-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="9f94a-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="9f94a-138">0</span><span class="sxs-lookup"><span data-stu-id="9f94a-138">0</span></span></p></td>
<td><p><span data-ttu-id="9f94a-139">O usuário não tem acesso ao objeto (não é válido para objetos Document).</span><span class="sxs-lookup"><span data-stu-id="9f94a-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="9f94a-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="9f94a-141">4</span><span class="sxs-lookup"><span data-stu-id="9f94a-141">4</span></span></p></td>
<td><p><span data-ttu-id="9f94a-142">O usuário pode ler a definição da tabela, inclusive informações de coluna e índice.</span><span class="sxs-lookup"><span data-stu-id="9f94a-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="9f94a-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="9f94a-144">131072</span><span class="sxs-lookup"><span data-stu-id="9f94a-144">131072</span></span></p></td>
<td><p><span data-ttu-id="9f94a-145">O usuário pode ler as informações relativas à segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="9f94a-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="9f94a-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="9f94a-147">64</span><span class="sxs-lookup"><span data-stu-id="9f94a-147">64</span></span></p></td>
<td><p><span data-ttu-id="9f94a-148">O usuário pode modificar registros.</span><span class="sxs-lookup"><span data-stu-id="9f94a-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="9f94a-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="9f94a-150">20</span><span class="sxs-lookup"><span data-stu-id="9f94a-150">20</span></span></p></td>
<td><p><span data-ttu-id="9f94a-151">O usuário pode recuperar dados do objeto Document.</span><span class="sxs-lookup"><span data-stu-id="9f94a-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="9f94a-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="9f94a-153">65548</span><span class="sxs-lookup"><span data-stu-id="9f94a-153">65548</span></span></p></td>
<td><p><span data-ttu-id="9f94a-154">O usuário pode modificar ou excluir a definição da tabela, inclusive as informações de coluna e índice.</span><span class="sxs-lookup"><span data-stu-id="9f94a-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f94a-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="9f94a-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="9f94a-156">524288</span><span class="sxs-lookup"><span data-stu-id="9f94a-156">524288</span></span></p></td>
<td><p><span data-ttu-id="9f94a-157">O usuário pode alterar a configuração da propriedade Proprietário.</span><span class="sxs-lookup"><span data-stu-id="9f94a-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f94a-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="9f94a-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="9f94a-159">262144</span><span class="sxs-lookup"><span data-stu-id="9f94a-159">262144</span></span></p></td>
<td><p><span data-ttu-id="9f94a-160">O usuário pode alterar permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="9f94a-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

