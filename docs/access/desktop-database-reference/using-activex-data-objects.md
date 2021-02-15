---
title: Usar ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: O Microsoft Access fornece três modelos de objeto a ser usado na criação, manutenção e gerenciamento dos bancos de dados do Access e seus dados relacionados usando o Visual Basic.
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
# <a name="use-activex-data-objects"></a><span data-ttu-id="6b7cd-103">Usar ADO (ActiveX Data Objects)</span><span class="sxs-lookup"><span data-stu-id="6b7cd-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="6b7cd-104">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b7cd-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b7cd-105">O Microsoft Access fornece três modelos de objeto a ser usado na criação, manutenção e gerenciamento dos bancos de dados do Access e seus dados relacionados usando o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="6b7cd-106">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="6b7cd-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="6b7cd-107">O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="6b7cd-108">Ext. do Microsoft ADO para DDL e segurança (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6b7cd-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="6b7cd-109">O ADOX fornece os objetos DDL (Data Definition Language) necessários para criar um novo banco de dados e seus objetos contidos, além dos objetos necessários para gerenciar a segurança.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="6b7cd-110">Biblioteca do Microsoft Jet and Replication Objects 2.5 (JRO)</span><span class="sxs-lookup"><span data-stu-id="6b7cd-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="6b7cd-111">Como os objetos do ADO foram projetados para funcionar com muitos bancos de dados além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi dividida na biblioteca JRO.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="6b7cd-112">A tabela a seguir lista a funcionalidade fornecida por cada um deles em relação ao DAO.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="6b7cd-113">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="6b7cd-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="6b7cd-114">DAO</span><span class="sxs-lookup"><span data-stu-id="6b7cd-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="6b7cd-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="6b7cd-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="6b7cd-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="6b7cd-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="6b7cd-117">JRO</span><span class="sxs-lookup"><span data-stu-id="6b7cd-117">JRO</span></span><br />
<span data-ttu-id="6b7cd-118">(somente MDBs)</span><span class="sxs-lookup"><span data-stu-id="6b7cd-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-119">Criar Recordsets.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-120">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-120">X</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-121">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-122">Editar propriedades de Inicialização.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-123">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-123">X</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-125">Suporte a ANSI92 SQL.\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-126">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-126">X</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-127">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-128">Criar tabelas.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-129">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-130">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-131">Criar novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-132">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-133">X\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-134">Editar propriedades de tabela existentes.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-135">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-136">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-137">Criar relações de tabela.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-138">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-139">X\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-140">Editar configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-141">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-142">X\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-143">Suporte para o atributo Compression para dados de coluna.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-144">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-145">Editar consultas SQL ou exibições básicas armazenadas.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-146">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-147">X\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-148">Criar consultas permanentes que são acessíveis somente através de código.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-149">X\*</span><span class="sxs-lookup"><span data-stu-id="6b7cd-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-150">Criar consultas acessíveis através de contêiner/IU do banco de dados e código.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-151">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-152">Banco de dados compacta/codificado.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-153">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-154">X4</span><span class="sxs-lookup"><span data-stu-id="6b7cd-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-155">Atualize o cache.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-156">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-157">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-158">Tornar o banco de dados relicável.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-159">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-160">X3</span><span class="sxs-lookup"><span data-stu-id="6b7cd-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-161">Faça réplicas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-162">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-163">X3</span><span class="sxs-lookup"><span data-stu-id="6b7cd-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-164">Sincronizar réplicas.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-165">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6b7cd-166">X3</span><span class="sxs-lookup"><span data-stu-id="6b7cd-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-167">Editar propriedades do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-168">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7cd-169">Criar propriedades de banco de dados personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-170">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7cd-171">Editar propriedades de coluna de tabela.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="6b7cd-172">X</span><span class="sxs-lookup"><span data-stu-id="6b7cd-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6b7cd-p101">\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="6b7cd-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="6b7cd-175">\*\* Disponível somente quando estiver trabalhando com projetos do Access.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="6b7cd-176">\*\*\* Embora o mecanismo de banco de dados do Access suporte algum SQL ANSI 92, ele ainda não é totalmente compatível com ANSI92.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="6b7cd-177">1 Usa o **objeto Connection** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="6b7cd-178">2 Usa o **objeto Catalog** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="6b7cd-179">3 Usa o **objeto Replica** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="6b7cd-180">4 Usa **o objeto JetEngine** para fazer referência ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="6b7cd-181">Ao contrário do DAO, os objetos do ADO e do ADOX podem executar as ações marcadas em bancos de dados diferentes do Jet, desde que o provedor desses bancos de dados suporte essa ação.</span><span class="sxs-lookup"><span data-stu-id="6b7cd-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


