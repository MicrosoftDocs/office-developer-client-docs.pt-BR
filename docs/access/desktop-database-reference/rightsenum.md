---
title: RightsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffc964be66649536b89e7f95ace1325eddee6169
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463434"
---
# <a name="rightsenum"></a><span data-ttu-id="bfdee-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="bfdee-102">RightsEnum</span></span>


<span data-ttu-id="bfdee-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfdee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bfdee-104">Especifica os direitos ou permissões de um grupo ou usuário em um objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfdee-105">Constante</span><span class="sxs-lookup"><span data-stu-id="bfdee-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="bfdee-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bfdee-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bfdee-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfdee-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-109">16384</span><span class="sxs-lookup"><span data-stu-id="bfdee-109">16384</span></span><br />
<span data-ttu-id="bfdee-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-111">O usuário ou grupo tem permissão para criar novos objetos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="bfdee-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-113">65536</span><span class="sxs-lookup"><span data-stu-id="bfdee-113">65536</span></span><br />
<span data-ttu-id="bfdee-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-p101">O usuário ou grupo tem permissão para excluir dados de um objeto. Para objetos como <strong>Tables</strong>, o usuário tem permissão para excluir valores de dados dos registros.</span><span class="sxs-lookup"><span data-stu-id="bfdee-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-118">256</span><span class="sxs-lookup"><span data-stu-id="bfdee-118">256</span></span><br />
<span data-ttu-id="bfdee-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="bfdee-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-p102">O usuário ou grupo tem permissão para remover objetos do catálogo. Por exemplo, <strong>Tables</strong> pode ser excluído por um comando SQL DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="bfdee-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-123">512</span><span class="sxs-lookup"><span data-stu-id="bfdee-123">512</span></span><br />
<span data-ttu-id="bfdee-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="bfdee-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-125">O usuário ou grupo tem permissão para acessar o objeto exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="bfdee-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-127">536870912</span><span class="sxs-lookup"><span data-stu-id="bfdee-127">536870912</span></span><br />
<span data-ttu-id="bfdee-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-129">O usuário ou grupo tem permissão para executar o objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-131">268435456</span><span class="sxs-lookup"><span data-stu-id="bfdee-131">268435456</span></span><br />
<span data-ttu-id="bfdee-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-133">O usuário ou grupo tem todas as permissões no objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-135">32768</span><span class="sxs-lookup"><span data-stu-id="bfdee-135">32768</span></span><br />
<span data-ttu-id="bfdee-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-p103">O usuário ou grupo tem permissão para inserir o objeto. Para objetos como <strong>Tables</strong>, o usuário tem permissão para inserir dados na tabela.</span><span class="sxs-lookup"><span data-stu-id="bfdee-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-p104">O usuário ou grupo tem o número máximo de permissões concedidas pelo provedor. As permissões específicas dependem do provedor.</span><span class="sxs-lookup"><span data-stu-id="bfdee-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-144">0</span><span class="sxs-lookup"><span data-stu-id="bfdee-144">0</span></span></p></td>
<td><p><span data-ttu-id="bfdee-145">O usuário ou grupo não tem nenhuma permissão para o objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="bfdee-147">-2147483648</span></span><br />
<span data-ttu-id="bfdee-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-p105">O usuário ou grupo tem permissão para ler o objeto. Para objetos como <a href="table-object-adox.md">Tables</a>, o usuário tem permissão para ler os dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="bfdee-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-152">1024</span><span class="sxs-lookup"><span data-stu-id="bfdee-152">1024</span></span><br />
<span data-ttu-id="bfdee-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="bfdee-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-154">O usuário ou grupo tem permissão para ler o design do objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-156">131072</span><span class="sxs-lookup"><span data-stu-id="bfdee-156">131072</span></span><br />
<span data-ttu-id="bfdee-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-158">O usuário ou grupo pode exibir (mas não alterar) as permissões específicas de um objeto no catálogo.</span><span class="sxs-lookup"><span data-stu-id="bfdee-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-160">8192</span><span class="sxs-lookup"><span data-stu-id="bfdee-160">8192</span></span><br />
<span data-ttu-id="bfdee-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-162">O usuário ou grupo tem permissão para referenciar o objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="bfdee-164">1073741824</span></span><br />
<span data-ttu-id="bfdee-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-p106">O usuário ou grupo tem permissão para atualizar o objeto. Para objetos como <strong>Tables</strong>, o usuário tem permissão para atualizar os dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="bfdee-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-169">4096</span><span class="sxs-lookup"><span data-stu-id="bfdee-169">4096</span></span><br />
<span data-ttu-id="bfdee-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-171">O usuário ou grupo tem permissão para conceder permissões para o objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-173">2048</span><span class="sxs-lookup"><span data-stu-id="bfdee-173">2048</span></span><br />
<span data-ttu-id="bfdee-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="bfdee-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-175">O usuário ou grupo tem permissão para modificar o design do objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfdee-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-177">524288</span><span class="sxs-lookup"><span data-stu-id="bfdee-177">524288</span></span><br />
<span data-ttu-id="bfdee-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-179">O usuário ou grupo tem permissão para modificar o proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="bfdee-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfdee-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="bfdee-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="bfdee-181">262144</span><span class="sxs-lookup"><span data-stu-id="bfdee-181">262144</span></span><br />
<span data-ttu-id="bfdee-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="bfdee-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="bfdee-183">O usuário ou grupo pode modificar as permissões específicas de um objeto no catálogo.</span><span class="sxs-lookup"><span data-stu-id="bfdee-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

