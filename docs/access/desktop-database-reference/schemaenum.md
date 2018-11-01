---
title: SchemaEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c7f9f9e52f2220a384ba73a64d96dd93fec2cd91
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871280"
---
# <a name="schemaenum"></a><span data-ttu-id="1f04b-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="1f04b-102">SchemaEnum</span></span>

<span data-ttu-id="1f04b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f04b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f04b-104">Especifica o tipo de esquema do **Recordset** que o método [OpenSchema](openschema-method-ado.md) recupera.</span><span class="sxs-lookup"><span data-stu-id="1f04b-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f04b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f04b-105">Remarks</span></span>

<span data-ttu-id="1f04b-106">Informações adicionais sobre a função e colunas retornadas para cada constante ADO pode ser encontrado nos tópicos do Apêndice B do *OLE DB programadores referência*.</span><span class="sxs-lookup"><span data-stu-id="1f04b-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="1f04b-107">O nome de cada tópico é listado entre parênteses na seção descrição da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f04b-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="1f04b-108">Informações adicionais sobre a função e colunas retornadas para cada constante do ADO MD podem ser encontradas nos tópicos de 23 de capítulo da documentação do *OLE DB para OLAP* .</span><span class="sxs-lookup"><span data-stu-id="1f04b-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="1f04b-109">O nome de cada tópico é listado entre parênteses e marcado com um asterisco (\*) na coluna Descrição da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f04b-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="1f04b-110">Converta os tipos de dados das colunas na documentação OLE DB para tipos de dados do ADO, consultando a coluna Descrição do tópico ADO [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="1f04b-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="1f04b-111">Por exemplo, um tipo de dados OLE DB do **DBTYPE\_WSTR** é equivalente a um tipo de dados de ADO do **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="1f04b-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="1f04b-112">O ADO gera resultados como esquema para as constantes **adSchemaDBInfoKeywords** e **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="1f04b-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="1f04b-113">ADO cria um **Recordset**e, em seguida, preenche cada linha com os valores retornados respectivamente pelos métodos **IDBInfo::GetKeywords** e **IDBInfo::GetLiteralInfo** .</span><span class="sxs-lookup"><span data-stu-id="1f04b-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="1f04b-114">Informações adicionais sobre esses métodos podem ser encontradas na seção da *referência do programador do OLE DB do*IDBInfo.</span><span class="sxs-lookup"><span data-stu-id="1f04b-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f04b-115">Constant</span><span class="sxs-lookup"><span data-stu-id="1f04b-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f04b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1f04b-116">Value</span></span></p></th>
<th><p><span data-ttu-id="1f04b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f04b-117">Description</span></span></p></th>
<th><p><span data-ttu-id="1f04b-118">Colunas de restrição</span><span class="sxs-lookup"><span data-stu-id="1f04b-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-120">0</span><span class="sxs-lookup"><span data-stu-id="1f04b-120">0</span></span></p></td>
<td><p><span data-ttu-id="1f04b-121">Retorna as asserções definidas no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-122">(Conjunto de linhas ASSERTIONS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="1f04b-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-127">1</span><span class="sxs-lookup"><span data-stu-id="1f04b-127">1</span></span></p></td>
<td><p><span data-ttu-id="1f04b-128">Retorna os atributos físicos associados aos catálogos acessíveis do DBMS.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="1f04b-129">(Conjunto de linhas CATALOGS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-132">2</span><span class="sxs-lookup"><span data-stu-id="1f04b-132">2</span></span></p></td>
<td><p><span data-ttu-id="1f04b-133">Retorna os conjuntos de caracteres definidos no catálogo que estão acessíveis para um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="1f04b-134">(Conjunto de linhas CHARACTER_SETS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="1f04b-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-139">5</span><span class="sxs-lookup"><span data-stu-id="1f04b-139">5</span></span></p></td>
<td><p><span data-ttu-id="1f04b-140">Retorna as restrições de verificação definidas no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-141">(Conjunto de linhas CHECK_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="1f04b-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-146">3</span><span class="sxs-lookup"><span data-stu-id="1f04b-146">3</span></span></p></td>
<td><p><span data-ttu-id="1f04b-147">Retorna as coleções de caracteres definidas no catálogo que estão acessíveis para um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="1f04b-148">(Conjunto de linhas COLLATIONS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="1f04b-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-153">13</span><span class="sxs-lookup"><span data-stu-id="1f04b-153">13</span></span></p></td>
<td><p><span data-ttu-id="1f04b-154">Retorna, nas colunas das tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="1f04b-155">(Conjunto de linhas COLUMN_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-158">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-159">NOME DA COLUNA</span><span class="sxs-lookup"><span data-stu-id="1f04b-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="1f04b-160">CONCEDEROU</span><span class="sxs-lookup"><span data-stu-id="1f04b-160">GRANTOR</span></span><br />
<span data-ttu-id="1f04b-161">RECEBEDOR DA PERMISSÃO</span><span class="sxs-lookup"><span data-stu-id="1f04b-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-163">4</span><span class="sxs-lookup"><span data-stu-id="1f04b-163">4</span></span></p></td>
<td><p><span data-ttu-id="1f04b-164">Retorna as colunas das tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="1f04b-165">(Conjunto de linhas COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-168">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-169">NOME DA COLUNA</span><span class="sxs-lookup"><span data-stu-id="1f04b-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-171">11</span><span class="sxs-lookup"><span data-stu-id="1f04b-171">11</span></span></p></td>
<td><p><span data-ttu-id="1f04b-172">Retorna as colunas definidas no catálogo que são dependentes de um domínio definido no catálogo e pertencem a um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="1f04b-173">(Conjunto de linhas COLUMN_DOMAIN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="1f04b-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="1f04b-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-176">NOME_DO_DOMÍNIO</span><span class="sxs-lookup"><span data-stu-id="1f04b-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="1f04b-177">NOME DA COLUNA</span><span class="sxs-lookup"><span data-stu-id="1f04b-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-179">6</span><span class="sxs-lookup"><span data-stu-id="1f04b-179">6</span></span></p></td>
<td><p><span data-ttu-id="1f04b-180">Retorna as colunas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="1f04b-181">(Conjunto de linhas CONSTRAINT_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="1f04b-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-184">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-185">NOME DA COLUNA</span><span class="sxs-lookup"><span data-stu-id="1f04b-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-187">7</span><span class="sxs-lookup"><span data-stu-id="1f04b-187">7</span></span></p></td>
<td><p><span data-ttu-id="1f04b-188">Retorna as tabelas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="1f04b-189">(Conjunto de linhas CONSTRAINT_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="1f04b-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-194">32</span><span class="sxs-lookup"><span data-stu-id="1f04b-194">32</span></span></p></td>
<td><p><span data-ttu-id="1f04b-195">Retorna informações sobre os cubos disponíveis em um esquema (ou o catálogo se o provedor não oferecer suporte a esquemas).
</span><span class="sxs-lookup"><span data-stu-id="1f04b-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="1f04b-196">(Conjunto de linhas CUBES\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-201">30</span><span class="sxs-lookup"><span data-stu-id="1f04b-201">30</span></span></p></td>
<td><p><span data-ttu-id="1f04b-202">Retorna uma lista de palavras-chave específicas do provedor.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="1f04b-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-204">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="1f04b-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-206">31</span><span class="sxs-lookup"><span data-stu-id="1f04b-206">31</span></span></p></td>
<td><p><span data-ttu-id="1f04b-207">Retorna uma lista de literais específicos do provedor utilizados em comandos de texto.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="1f04b-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-209">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="1f04b-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-211">33</span><span class="sxs-lookup"><span data-stu-id="1f04b-211">33</span></span></p></td>
<td><p><span data-ttu-id="1f04b-212">Retorna informações sobre as dimensões em um cubo específico.</span><span class="sxs-lookup"><span data-stu-id="1f04b-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="1f04b-213">Ele tem uma linha para cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="1f04b-213">It has one row for each dimension.</span></span> <span data-ttu-id="1f04b-214">(Conjunto de linhas DIMENSIONS\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-217">CUBE_NAME</span></span><br />
<span data-ttu-id="1f04b-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="1f04b-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-221">27</span><span class="sxs-lookup"><span data-stu-id="1f04b-221">27</span></span></p></td>
<td><p><span data-ttu-id="1f04b-222">Retorna as colunas de chave estrangeira definidas no catálogo por um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="1f04b-223">(Conjunto de linhas FOREIGN_KEYS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-231">34</span><span class="sxs-lookup"><span data-stu-id="1f04b-231">34</span></span></p></td>
<td><p><span data-ttu-id="1f04b-232">Retorna informações sobre as hierarquias disponíveis em uma dimensão.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="1f04b-233">(Conjunto de linhas HIERARCHIES\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-236">CUBE_NAME</span></span><br />
<span data-ttu-id="1f04b-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="1f04b-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-241">12</span><span class="sxs-lookup"><span data-stu-id="1f04b-241">12</span></span></p></td>
<td><p><span data-ttu-id="1f04b-242">Retorna os índices definidos no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-243">(Conjunto de linhas INDEXES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-246">INDEX_NAME</span></span><br />
<span data-ttu-id="1f04b-247">TIPO</span><span class="sxs-lookup"><span data-stu-id="1f04b-247">TYPE</span></span><br />
<span data-ttu-id="1f04b-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-250">8</span><span class="sxs-lookup"><span data-stu-id="1f04b-250">8</span></span></p></td>
<td><p><span data-ttu-id="1f04b-251">Retorna as colunas definidas no catálogo, restritas a chaves por um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="1f04b-252">(Conjunto de linhas KEY_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="1f04b-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="1f04b-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="1f04b-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-258">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-259">NOME DA COLUNA</span><span class="sxs-lookup"><span data-stu-id="1f04b-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-261">35</span><span class="sxs-lookup"><span data-stu-id="1f04b-261">35</span></span></p></td>
<td><p><span data-ttu-id="1f04b-262">Retorna informações sobre os níveis disponíveis em uma dimensão.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="1f04b-263">(Conjunto de linhas LEVELS\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-266">CUBE_NAME</span></span><br />
<span data-ttu-id="1f04b-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="1f04b-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-272">36</span><span class="sxs-lookup"><span data-stu-id="1f04b-272">36</span></span></p></td>
<td><p><span data-ttu-id="1f04b-273">Retorna informações sobre as medidas disponíveis.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-273">Returns information about the available measures.</span></span> <span data-ttu-id="1f04b-274">(Conjunto de linhas MEASURES\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-277">CUBE_NAME</span></span><br />
<span data-ttu-id="1f04b-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="1f04b-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-281">38</span><span class="sxs-lookup"><span data-stu-id="1f04b-281">38</span></span></p></td>
<td><p><span data-ttu-id="1f04b-282">Retorna informações sobre os membros disponíveis.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-282">Returns information about the available members.</span></span> <span data-ttu-id="1f04b-283">(Conjunto de linhas MEMBERS\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-286">CUBE_NAME</span></span><br />
<span data-ttu-id="1f04b-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="1f04b-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="1f04b-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="1f04b-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="1f04b-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="1f04b-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f04b-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="1f04b-295">O operador de árvore (para obter mais informações, consulte o OLE DB para a documentação do OLAP).</span><span class="sxs-lookup"><span data-stu-id="1f04b-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-297">28</span><span class="sxs-lookup"><span data-stu-id="1f04b-297">28</span></span></p></td>
<td><p><span data-ttu-id="1f04b-298">Retorna as colunas de chave principal definidas no catálogo por um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="1f04b-299">(Conjunto de linhas PRIMARY_KEYS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-304">29</span><span class="sxs-lookup"><span data-stu-id="1f04b-304">29</span></span></p></td>
<td><p><span data-ttu-id="1f04b-305">Retorna informações sobre as colunas de conjuntos de linhas por procedimentos.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="1f04b-306">(Conjunto de linhas PROCEDURE_COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="1f04b-310">NOME DA COLUNA</span><span class="sxs-lookup"><span data-stu-id="1f04b-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-312">26</span><span class="sxs-lookup"><span data-stu-id="1f04b-312">26</span></span></p></td>
<td><p><span data-ttu-id="1f04b-313">Retorna informações sobre parâmetros e códigos de retorno de procedimentos.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="1f04b-314">(Conjunto de linhas PROCEDURE_PARAMETERS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="1f04b-318">NOME_DO</span><span class="sxs-lookup"><span data-stu-id="1f04b-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-320">16</span><span class="sxs-lookup"><span data-stu-id="1f04b-320">16</span></span></p></td>
<td><p><span data-ttu-id="1f04b-321">Retorna os procedimentos definidos no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-322">(Conjunto de linhas PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="1f04b-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f04b-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-328">37</span><span class="sxs-lookup"><span data-stu-id="1f04b-328">37</span></span></p></td>
<td><p><span data-ttu-id="1f04b-329">Retorna informações sobre as propriedades disponíveis para cada nível de dimensão.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="1f04b-330">(Conjunto de linhas PROPERTIES\*)</span><span class="sxs-lookup"><span data-stu-id="1f04b-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-333">CUBE_NAME</span></span><br />
<span data-ttu-id="1f04b-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="1f04b-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f04b-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="1f04b-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-341">-1</span><span class="sxs-lookup"><span data-stu-id="1f04b-341">-1</span></span></p></td>
<td><p><span data-ttu-id="1f04b-342">Utilizada se o provedor define suas próprias consultas de esquema não padrão.</span><span class="sxs-lookup"><span data-stu-id="1f04b-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="1f04b-343">&lt;Provedor específico&gt;</span><span class="sxs-lookup"><span data-stu-id="1f04b-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-345">22</span><span class="sxs-lookup"><span data-stu-id="1f04b-345">22</span></span></p></td>
<td><p><span data-ttu-id="1f04b-346">Retorna os tipos de dados (base) aceitos pelo provedor de dados.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="1f04b-347">(Conjunto de linhas PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f04b-348">DATA_TYPE</span></span><br />
<span data-ttu-id="1f04b-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="1f04b-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-351">9</span><span class="sxs-lookup"><span data-stu-id="1f04b-351">9</span></span></p></td>
<td><p><span data-ttu-id="1f04b-352">Retorna as restrições de referência definidas no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-353">(Conjunto de linhas REFERENTIAL_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="1f04b-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-358">17</span><span class="sxs-lookup"><span data-stu-id="1f04b-358">17</span></span></p></td>
<td><p><span data-ttu-id="1f04b-359">Retorna os esquemas (objetos de banco de dados) pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="1f04b-360">(Conjunto de linhas SCHEMATA)</span><span class="sxs-lookup"><span data-stu-id="1f04b-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="1f04b-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="1f04b-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="1f04b-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-365">18</span><span class="sxs-lookup"><span data-stu-id="1f04b-365">18</span></span></p></td>
<td><p><span data-ttu-id="1f04b-366">Retorna os níveis, as opções e os dialetos de conformidade aceitos pelos dados de processamento de implementação do SQL definidos no catálogo.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="1f04b-367">(Conjunto de linhas SQL_LANGUAGES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-368">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="1f04b-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-370">19</span><span class="sxs-lookup"><span data-stu-id="1f04b-370">19</span></span></p></td>
<td><p><span data-ttu-id="1f04b-371">Retorna as estatísticas definidas no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-372">(Conjunto de linhas STATISTICS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-377">10</span><span class="sxs-lookup"><span data-stu-id="1f04b-377">10</span></span></p></td>
<td><p><span data-ttu-id="1f04b-378">Retorna as restrições de tabela definidas no catálogo, pertencentes a um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="1f04b-379">(Conjunto de linha TABLE_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="1f04b-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="1f04b-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-385">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-386">TIPO_RESTRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="1f04b-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-388">14</span><span class="sxs-lookup"><span data-stu-id="1f04b-388">14</span></span></p></td>
<td><p><span data-ttu-id="1f04b-389">Retorna, nas tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="1f04b-390">(Conjunto de linhas TABLE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-393">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-394">CONCEDEROU</span><span class="sxs-lookup"><span data-stu-id="1f04b-394">GRANTOR</span></span><br />
<span data-ttu-id="1f04b-395">RECEBEDOR DA PERMISSÃO</span><span class="sxs-lookup"><span data-stu-id="1f04b-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-397">20</span><span class="sxs-lookup"><span data-stu-id="1f04b-397">20</span></span></p></td>
<td><p><span data-ttu-id="1f04b-398">Retorna as tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="1f04b-399">(Conjunto de linhas TABLES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-402">TABLE_NAME</span></span><br />
<span data-ttu-id="1f04b-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f04b-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-405">21</span><span class="sxs-lookup"><span data-stu-id="1f04b-405">21</span></span></p></td>
<td><p><span data-ttu-id="1f04b-406">Retorna as conversões de caracteres definidas no catálogo que estão acessíveis para um usuário específico.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="1f04b-407">(Conjunto de linhas TRANSLATIONS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="1f04b-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-412">39</span><span class="sxs-lookup"><span data-stu-id="1f04b-412">39</span></span></p></td>
<td><p><span data-ttu-id="1f04b-413">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1f04b-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-415">15</span><span class="sxs-lookup"><span data-stu-id="1f04b-415">15</span></span></p></td>
<td><p><span data-ttu-id="1f04b-416">Retorna, nos objetos definidos no catálogo, os privilégios USAGE que estão disponíveis para um determinado usuário ou foram concedidos a ele.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="1f04b-417">(Conjunto de linhas USAGE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="1f04b-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="1f04b-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="1f04b-421">TIPO_DO_OBJETO</span><span class="sxs-lookup"><span data-stu-id="1f04b-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="1f04b-422">CONCEDEROU</span><span class="sxs-lookup"><span data-stu-id="1f04b-422">GRANTOR</span></span><br />
<span data-ttu-id="1f04b-423">RECEBEDOR DA PERMISSÃO</span><span class="sxs-lookup"><span data-stu-id="1f04b-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-425">24</span><span class="sxs-lookup"><span data-stu-id="1f04b-425">24</span></span></p></td>
<td><p><span data-ttu-id="1f04b-426">Retorna as colunas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="1f04b-427">(Conjunto de linhas VIEW_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="1f04b-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="1f04b-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-432">23</span><span class="sxs-lookup"><span data-stu-id="1f04b-432">23</span></span></p></td>
<td><p><span data-ttu-id="1f04b-433">Retorna as exibições definidas no catálogo que estão acessíveis para um determinado usuário.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="1f04b-434">(Conjunto de linhas VIEWS)</span><span class="sxs-lookup"><span data-stu-id="1f04b-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="1f04b-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="1f04b-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="1f04b-439">25</span><span class="sxs-lookup"><span data-stu-id="1f04b-439">25</span></span></p></td>
<td><p><span data-ttu-id="1f04b-440">Retorna as tabelas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.
</span><span class="sxs-lookup"><span data-stu-id="1f04b-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="1f04b-441">(Conjunto de linhas VIEW_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="1f04b-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="1f04b-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="1f04b-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="1f04b-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="1f04b-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="1f04b-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="1f04b-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1f04b-445">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1f04b-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="1f04b-446">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1f04b-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f04b-447">Constante</span><span class="sxs-lookup"><span data-stu-id="1f04b-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="1f04b-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="1f04b-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="1f04b-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="1f04b-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="1f04b-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="1f04b-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="1f04b-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f04b-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f04b-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f04b-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="1f04b-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="1f04b-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="1f04b-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="1f04b-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="1f04b-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="1f04b-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="1f04b-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f04b-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="1f04b-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="1f04b-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="1f04b-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="1f04b-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="1f04b-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f04b-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="1f04b-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="1f04b-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="1f04b-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="1f04b-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="1f04b-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="1f04b-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="1f04b-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="1f04b-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="1f04b-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="1f04b-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="1f04b-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="1f04b-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="1f04b-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="1f04b-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f04b-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f04b-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="1f04b-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f04b-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="1f04b-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

