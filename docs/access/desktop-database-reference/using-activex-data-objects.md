---
title: Usando objetos de dados ActiveX
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463091"
---
# <a name="using-activex-data-objects"></a><span data-ttu-id="4b5c0-102">Usando objetos de dados ActiveX</span><span class="sxs-lookup"><span data-stu-id="4b5c0-102">Using ActiveX Data Objects</span></span>


<span data-ttu-id="4b5c0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b5c0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4b5c0-104">O Microsoft Access oferece três modelos de objetos para uso em criação, manutenção e gerenciamento de bancos de dados do Access e seus dados relacionados através do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-104">Microsoft Access provides three object models to use in the creation, maintaining and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="4b5c0-105">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="4b5c0-105">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="4b5c0-106">O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-106">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="4b5c0-107">O Microsoft ADO Ext. for DDL and Security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4b5c0-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span></span>

<span data-ttu-id="4b5c0-108">O ADOX fornece os objetos da Data Definition Language (DDL) necessários para a criação de novos bancos de dados e seus objetos contidos além dos objetos necessários para o gerenciamento da segurança.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-108">ADOX provides the Data Definition Language(DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

<span data-ttu-id="4b5c0-109">**O Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span><span class="sxs-lookup"><span data-stu-id="4b5c0-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span></span>

<span data-ttu-id="4b5c0-110">Como os objetos do ADO foram estruturados para funcionar com muitos bancos de dados além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi segmentada na biblioteca JRO.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-110">Since ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="4b5c0-111">A tabela a seguir lista a funcionalidade fornecida por cada um deles em relação ao DAO.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-111">The following table lists the functionality provided by each compared to DAO.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b5c0-112">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="4b5c0-112">Functionality</span></span></p></th>
<th><p><span data-ttu-id="4b5c0-113">DAO</span><span class="sxs-lookup"><span data-stu-id="4b5c0-113">DAO</span></span></p></th>
<th><p><span data-ttu-id="4b5c0-114">ADO1</span><span class="sxs-lookup"><span data-stu-id="4b5c0-114">ADO1</span></span></p></th>
<th><p><span data-ttu-id="4b5c0-115">ADOX2</span><span class="sxs-lookup"><span data-stu-id="4b5c0-115">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="4b5c0-116">JRO</span><span class="sxs-lookup"><span data-stu-id="4b5c0-116">JRO</span></span><br />
<span data-ttu-id="4b5c0-117">(MDB do somente)</span><span class="sxs-lookup"><span data-stu-id="4b5c0-117">(MDB's Only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-118">Criar conjuntos de registros</span><span class="sxs-lookup"><span data-stu-id="4b5c0-118">Create Recordsets</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-119">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-119">X</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-120">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-120">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-121">Propriedades Edit Startup</span><span class="sxs-lookup"><span data-stu-id="4b5c0-121">Edit Startup properties</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-122">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-122">X</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-123">X\*\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-123">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-124">Suporte a SQL ANSI92 \*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-124">Support ANSI92 SQL\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-125">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-125">X</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-126">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-126">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-127">Criar tabelas</span><span class="sxs-lookup"><span data-stu-id="4b5c0-127">Create Tables</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-128">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-128">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-129">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-129">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-130">Criar novo banco de dados</span><span class="sxs-lookup"><span data-stu-id="4b5c0-130">Create New Database</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-131">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-131">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-132">X\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-132">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-133">Propriedades Edit Existing Table</span><span class="sxs-lookup"><span data-stu-id="4b5c0-133">Edit Existing Table properties</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-134">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-134">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-135">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-135">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-136">Criar relações entre tabelas</span><span class="sxs-lookup"><span data-stu-id="4b5c0-136">Create table relationships</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-137">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-138">X\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-138">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-139">Editar configurações de segurança</span><span class="sxs-lookup"><span data-stu-id="4b5c0-139">Edit security settings</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-140">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-140">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-141">X\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-141">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-142">Suporte para o atributo Compactação dos dados da coluna</span><span class="sxs-lookup"><span data-stu-id="4b5c0-142">Support for Compression attribute for column data</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-143">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-143">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-144">Editar modos de exibição ou consultas SQL básicas armazenadas</span><span class="sxs-lookup"><span data-stu-id="4b5c0-144">Edit stored, basic SQL queries or views</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-145">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-145">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-146">X\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-146">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-147">Criar consultas permanentes que são acessíveis somente através de código.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-147">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-148">X\*</span><span class="sxs-lookup"><span data-stu-id="4b5c0-148">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-149">Criar consultas acessíveis através de contêiner/IU do banco de dados e código.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-149">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-150">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-150">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-151">Compactar/Codificar banco de dados</span><span class="sxs-lookup"><span data-stu-id="4b5c0-151">Compact/Encode database</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-152">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-152">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-153">X4</span><span class="sxs-lookup"><span data-stu-id="4b5c0-153">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-154">Atualizar cache</span><span class="sxs-lookup"><span data-stu-id="4b5c0-154">Refresh Cache</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-155">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-155">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-156">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-156">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-157">Criar banco de dados replicável</span><span class="sxs-lookup"><span data-stu-id="4b5c0-157">Make Database Replicable</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-158">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-158">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-159">X3</span><span class="sxs-lookup"><span data-stu-id="4b5c0-159">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-160">Criar réplicas de banco de dados</span><span class="sxs-lookup"><span data-stu-id="4b5c0-160">Make Database Replicas</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-161">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-161">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-162">X3</span><span class="sxs-lookup"><span data-stu-id="4b5c0-162">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-163">Sincronizar réplicas</span><span class="sxs-lookup"><span data-stu-id="4b5c0-163">Synchronize Replicas</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-164">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-164">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="4b5c0-165">X3</span><span class="sxs-lookup"><span data-stu-id="4b5c0-165">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-166">Propriedades Edit Database</span><span class="sxs-lookup"><span data-stu-id="4b5c0-166">Edit Database properties</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-167">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-167">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5c0-168">Criar propriedades de banco de dados personalizadas</span><span class="sxs-lookup"><span data-stu-id="4b5c0-168">Create custom database properties</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-169">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-169">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5c0-170">Editar propriedades da coluna da tabela</span><span class="sxs-lookup"><span data-stu-id="4b5c0-170">Edit table column properties</span></span></p></td>
<td><p><span data-ttu-id="4b5c0-171">X</span><span class="sxs-lookup"><span data-stu-id="4b5c0-171">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b5c0-p101">\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="4b5c0-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="4b5c0-174">\*\* Disponível somente quando estiver trabalhando com projetos do Access.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-174">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="4b5c0-175">\*\*\* Embora o mecanismo do banco de dados do Access ofereça suporte parcial a SQL ANSI92, ele ainda não é totalmente compatível.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-175">\*\*\* Though the Access database engine does support some ANSI 92 SQL it is not yet fully ANSI92 compliant.</span></span>

<span data-ttu-id="4b5c0-176">1Usa o objeto **Connection** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-176">1 Uses **Connection** object to reference to database</span></span>

<span data-ttu-id="4b5c0-177">2Usa o objeto **Catalog** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-177">2 Uses **Catalog** object to reference database</span></span>

<span data-ttu-id="4b5c0-178">3Usa o objeto **Replica** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-178">3 Uses **Replica** object to reference database</span></span>

<span data-ttu-id="4b5c0-179">4Usa o objeto **JetEngine** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-179">4 Uses **JetEngine** object to reference database</span></span>


> [!NOTE]
> <P><span data-ttu-id="4b5c0-180">[!OBSERVAçãO] Ao contrário do DAO, os objetos do ADO e ADOX podem executar as ações marcadas em bancos de dados que não sejam Jet desde que o provedor desses bancos de dados ofereça suporte a essa ação.</span><span class="sxs-lookup"><span data-stu-id="4b5c0-180">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other then Jet as long as the provider for those databases supports that action.</span></span></P>


