---
title: Usar ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: O Microsoft Access fornece três modelos de objeto a serem usados na criação, manutenção e gerenciamento de seus bancos de dados do Access e seus dados relacionados usando o Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312737"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="2c42b-103">Usar ADO (ActiveX Data Objects)</span><span class="sxs-lookup"><span data-stu-id="2c42b-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="2c42b-104">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c42b-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c42b-105">O Microsoft Access fornece três modelos de objeto a serem usados na criação, manutenção e gerenciamento de seus bancos de dados do Access e seus dados relacionados usando o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2c42b-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="2c42b-106">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="2c42b-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="2c42b-107">O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="2c42b-108">Microsoft ADO ext. para DDL e segurança (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2c42b-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="2c42b-109">O ADOX fornece os objetos de linguagem de definição de dados (DDL) necessários para criar um novo banco de dados e seus objetos contidos, além dos objetos necessários para gerenciar a segurança.</span><span class="sxs-lookup"><span data-stu-id="2c42b-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="2c42b-110">Microsoft Jet and Replication Objects 2,5 library (JRO)</span><span class="sxs-lookup"><span data-stu-id="2c42b-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="2c42b-111">Como os objetos ADO foram projetados para trabalhar com vários bancos de dados além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi dividida na biblioteca do JRO.</span><span class="sxs-lookup"><span data-stu-id="2c42b-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="2c42b-112">A tabela a seguir lista a funcionalidade fornecida por cada um deles em relação ao DAO.</span><span class="sxs-lookup"><span data-stu-id="2c42b-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="2c42b-113">Função</span><span class="sxs-lookup"><span data-stu-id="2c42b-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="2c42b-114">DAO</span><span class="sxs-lookup"><span data-stu-id="2c42b-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="2c42b-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="2c42b-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="2c42b-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="2c42b-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="2c42b-117">JRO</span><span class="sxs-lookup"><span data-stu-id="2c42b-117">JRO</span></span><br />
<span data-ttu-id="2c42b-118">(Somente MDBs)</span><span class="sxs-lookup"><span data-stu-id="2c42b-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-119">Criar conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="2c42b-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-120">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-120">X</span></span></p></td>
<td><p><span data-ttu-id="2c42b-121">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-122">Editar as propriedades de inicialização.</span><span class="sxs-lookup"><span data-stu-id="2c42b-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-123">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-123">X</span></span></p></td>
<td><p><span data-ttu-id="2c42b-124">X \* \*</span><span class="sxs-lookup"><span data-stu-id="2c42b-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-125">Suporte a SQL SQL ANSI92 compatível. \* \*</span><span class="sxs-lookup"><span data-stu-id="2c42b-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-126">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-126">X</span></span></p></td>
<td><p><span data-ttu-id="2c42b-127">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-128">Criar tabelas.</span><span class="sxs-lookup"><span data-stu-id="2c42b-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-129">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-130">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-131">Criar novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-132">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-133">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-134">Editar propriedades da tabela existente.</span><span class="sxs-lookup"><span data-stu-id="2c42b-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-135">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-136">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-137">Criar relações de tabelas.</span><span class="sxs-lookup"><span data-stu-id="2c42b-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-138">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-139">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-140">Editar configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="2c42b-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-141">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-142">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-143">Suporte para o atributo Compression para dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="2c42b-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-144">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-145">Editar modos de exibição ou consultas SQL básicas armazenadas.</span><span class="sxs-lookup"><span data-stu-id="2c42b-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-146">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-147">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-148">Criar consultas permanentes que são acessíveis somente através de código.</span><span class="sxs-lookup"><span data-stu-id="2c42b-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-149">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-150">Criar consultas acessíveis através de contêiner/IU do banco de dados e código.</span><span class="sxs-lookup"><span data-stu-id="2c42b-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-151">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-152">Compactar/codificar banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-153">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-154">X4</span><span class="sxs-lookup"><span data-stu-id="2c42b-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-155">Atualize o cache.</span><span class="sxs-lookup"><span data-stu-id="2c42b-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-156">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-157">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-158">Tornar o banco de dados replicável.</span><span class="sxs-lookup"><span data-stu-id="2c42b-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-159">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-160">X3</span><span class="sxs-lookup"><span data-stu-id="2c42b-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-161">Criar réplicas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-162">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-163">X3</span><span class="sxs-lookup"><span data-stu-id="2c42b-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-164">Sincronizar réplicas.</span><span class="sxs-lookup"><span data-stu-id="2c42b-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-165">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2c42b-166">X3</span><span class="sxs-lookup"><span data-stu-id="2c42b-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-167">Editar propriedades do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-168">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c42b-169">Criar propriedades de banco de dados personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2c42b-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-170">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c42b-171">Editar propriedades da coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="2c42b-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="2c42b-172">X</span><span class="sxs-lookup"><span data-stu-id="2c42b-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c42b-p101">\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="2c42b-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="2c42b-175">\*\* Disponível somente quando estiver trabalhando com projetos do Access.</span><span class="sxs-lookup"><span data-stu-id="2c42b-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="2c42b-176">\*\*\*Embora o mecanismo de banco de dados do Access ofereça suporte a alguns ANSI 92 SQL, ele ainda não é totalmente compatível com SQL ANSI92 compatível.</span><span class="sxs-lookup"><span data-stu-id="2c42b-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="2c42b-177">1 usa o objeto **Connection** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="2c42b-178">2 usa o objeto **Catalog** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="2c42b-179">3 usa \*\*\*\* o objeto Replication para o banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="2c42b-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="2c42b-180">4 usa o objeto **JetEngine** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2c42b-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="2c42b-181">Ao contrário do DAO, os objetos do ADO e do ADOX podem executar as ações marcadas em bancos de dados que não sejam Jet, contanto que o provedor desses bancos de dados ofereça suporte a essa ação.</span><span class="sxs-lookup"><span data-stu-id="2c42b-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


