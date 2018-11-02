---
title: Ação da macro ExecutarSQL
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bb1bdb998373c8dba92910bd6331261514542a04
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923718"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="f1ce5-102">Ação da macro ExecutarSQL</span><span class="sxs-lookup"><span data-stu-id="f1ce5-102">RunSQL macro action</span></span>


<span data-ttu-id="f1ce5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1ce5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1ce5-104">Você pode usar a ação **ExecutarSQL** para executar uma consulta ação Access usando a instrução SQL correspondente.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-104">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement.</span></span> <span data-ttu-id="f1ce5-105">Pode também executar uma consulta de definição de dados.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-105">You can also run a data-definition query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f1ce5-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="f1ce5-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="f1ce5-108">Setting</span></span>

<span data-ttu-id="f1ce5-109">A ação **ExecutarSQL** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-109">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1ce5-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="f1ce5-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f1ce5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1ce5-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-112"><strong>Instrução SQL</strong></span><span class="sxs-lookup"><span data-stu-id="f1ce5-112"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ce5-p103">A instrução SQL da consulta ação ou da consulta de definição de dados a ser executada. O tamanho máximo dessa instrução é de 255 caracteres. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p103">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ce5-116"><strong>Usar transação</strong></span><span class="sxs-lookup"><span data-stu-id="f1ce5-116"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ce5-p104">Selecione <strong>Sim</strong> para incluir essa consulta em uma transação. Selecione <strong>Não</strong> se não quiser usar uma transação. O padrão é <strong>Sim</strong>. Se você selecionar <strong>Não</strong> para este argumento, a consulta poderá ser executada mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p104">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f1ce5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1ce5-121">Remarks</span></span>

<span data-ttu-id="f1ce5-p105">Você pode usar consultas ação para acrescentar, excluir e atualizar registros e para salvar o conjunto de resultados de uma consulta como uma nova tabela. As consultas de definições de dados podem ser usadas para criar, alterar e excluir tabelas, e para criar e excluir índices. Use a ação **ExecutarSQL** para executar essas operações diretamente em uma macro, sem precisar usar consultas armazenadas.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p105">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="f1ce5-p106">Se precisar digitar uma instrução SQL com mais de 255 caracteres, use o método **RunSQL** do objeto **DoCmd** em um módulo do VBA (Visual Basic for Applications). No VBA, é possível digitar instruções SQL com até 32.768 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p106">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="f1ce5-p107">As consultas do Access, na verdade, são instruções SQL criadas durante a criação de uma consulta com a grade de design na janela Consulta. A tabela a seguir mostra as consultas ação e as consultas de definições de dados, do Access, e as respectivas instruções SQL.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p107">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1ce5-129">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="f1ce5-129">Query type</span></span></p></th>
<th><p><span data-ttu-id="f1ce5-130">Instrução SQL</span><span class="sxs-lookup"><span data-stu-id="f1ce5-130">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-131"><strong>Ação</strong></span><span class="sxs-lookup"><span data-stu-id="f1ce5-131"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ce5-132">Acrescentar</span><span class="sxs-lookup"><span data-stu-id="f1ce5-132">Append</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-133">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="f1ce5-133">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-134">Excluir</span><span class="sxs-lookup"><span data-stu-id="f1ce5-134">Delete</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="f1ce5-135">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ce5-136">Criar tabela</span><span class="sxs-lookup"><span data-stu-id="f1ce5-136">Make-table</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-137">SELECIONE … EM</span><span class="sxs-lookup"><span data-stu-id="f1ce5-137">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-138">Atualizar</span><span class="sxs-lookup"><span data-stu-id="f1ce5-138">Update</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-139">UPDATE</span><span class="sxs-lookup"><span data-stu-id="f1ce5-139">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ce5-140"><strong>Definição de dados (específica de SQL)</strong></span><span class="sxs-lookup"><span data-stu-id="f1ce5-140"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-141">Criar uma tabela</span><span class="sxs-lookup"><span data-stu-id="f1ce5-141">Create a table</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-142">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="f1ce5-142">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ce5-143">Alterar uma tabela</span><span class="sxs-lookup"><span data-stu-id="f1ce5-143">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-144">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="f1ce5-144">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-145">Excluir uma tabela</span><span class="sxs-lookup"><span data-stu-id="f1ce5-145">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-146">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="f1ce5-146">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ce5-147">Criar um índice</span><span class="sxs-lookup"><span data-stu-id="f1ce5-147">Create an index</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-148">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="f1ce5-148">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ce5-149">Excluir um índice</span><span class="sxs-lookup"><span data-stu-id="f1ce5-149">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="f1ce5-150">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="f1ce5-150">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1ce5-151">Você também pode usar uma cláusula IN com essas instruções para modificar dados em outro banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-151">You can also use an IN clause with these statements to modify data in another database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f1ce5-p108">[!OBSERVAçãO] Para executar uma consulta seleção ou uma consulta de tabela de referência cruzada em uma macro, use o argumento Exibir da ação <STRONG>AbrirConsulta</STRONG> para abrir uma consulta seleção ou uma consulta de tabela de referência cruzada existente no modo Folha de Dados. Consultas ação e consultas específicas de SQL existentes também podem ser executadas dessa mesma forma.</span><span class="sxs-lookup"><span data-stu-id="f1ce5-p108">To run a select query or crosstab query from a macro, use the View argument of the <STRONG>OpenQuery</STRONG> action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span></P>


