---
title: Usar ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: O Microsoft Access oferece três modelos de objetos para uso em criação, manutenção e gerenciamento de seus bancos de dados do Access e seus dados relacionados usando o Visual Basic.
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719222"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="e882d-103">Usar ADO (ActiveX Data Objects)</span><span class="sxs-lookup"><span data-stu-id="e882d-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="e882d-104">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e882d-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e882d-105">O Microsoft Access oferece três modelos de objetos para uso em criação, manutenção e gerenciamento de seus bancos de dados do Access e seus dados relacionados usando o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e882d-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="e882d-106">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="e882d-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="e882d-107">O ADO contém os objetos necessários para criar, atualizar e excluir registros em uma determinada fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="e882d-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="e882d-108">Microsoft ADO Ext. DDL e segurança (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e882d-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="e882d-109">O ADOX fornece os objetos da Data Definition Language (DDL) necessários para criar um novo banco de dados e seus objetos contidos além dos objetos necessários para gerenciar a segurança.</span><span class="sxs-lookup"><span data-stu-id="e882d-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="e882d-110">O Microsoft Jet and Replication objetos 2.5 library (JRO)</span><span class="sxs-lookup"><span data-stu-id="e882d-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="e882d-111">Porque os objetos ADO foram estruturados para funcionar com muitos bancos de dados, além dos bancos de dados do Microsoft Jet, a funcionalidade específica do Jet foi segmentada na biblioteca JRO.</span><span class="sxs-lookup"><span data-stu-id="e882d-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="e882d-112">A tabela a seguir lista a funcionalidade fornecida por cada um deles em relação ao DAO.</span><span class="sxs-lookup"><span data-stu-id="e882d-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="e882d-113">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="e882d-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="e882d-114">DAO</span><span class="sxs-lookup"><span data-stu-id="e882d-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="e882d-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="e882d-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="e882d-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="e882d-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="e882d-117">JRO</span><span class="sxs-lookup"><span data-stu-id="e882d-117">JRO</span></span><br />
<span data-ttu-id="e882d-118">(MDBs)</span><span class="sxs-lookup"><span data-stu-id="e882d-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e882d-119">Crie conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="e882d-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="e882d-120">X</span><span class="sxs-lookup"><span data-stu-id="e882d-120">X</span></span></p></td>
<td><p><span data-ttu-id="e882d-121">X</span><span class="sxs-lookup"><span data-stu-id="e882d-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-122">Edite propriedades de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e882d-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="e882d-123">X</span><span class="sxs-lookup"><span data-stu-id="e882d-123">X</span></span></p></td>
<td><p><span data-ttu-id="e882d-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="e882d-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-125">Suporte ANSI92 SQL.\* \* \*</span><span class="sxs-lookup"><span data-stu-id="e882d-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-126">X</span><span class="sxs-lookup"><span data-stu-id="e882d-126">X</span></span></p></td>
<td><p><span data-ttu-id="e882d-127">X</span><span class="sxs-lookup"><span data-stu-id="e882d-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-128">Crie tabelas.</span><span class="sxs-lookup"><span data-stu-id="e882d-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="e882d-129">X</span><span class="sxs-lookup"><span data-stu-id="e882d-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-130">X</span><span class="sxs-lookup"><span data-stu-id="e882d-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-131">Crie um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e882d-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="e882d-132">X</span><span class="sxs-lookup"><span data-stu-id="e882d-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-133">X\*</span><span class="sxs-lookup"><span data-stu-id="e882d-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-134">Edite propriedades da tabela existente.</span><span class="sxs-lookup"><span data-stu-id="e882d-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="e882d-135">X</span><span class="sxs-lookup"><span data-stu-id="e882d-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-136">X</span><span class="sxs-lookup"><span data-stu-id="e882d-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-137">Crie relações entre tabelas.</span><span class="sxs-lookup"><span data-stu-id="e882d-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="e882d-138">X</span><span class="sxs-lookup"><span data-stu-id="e882d-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-139">X\*</span><span class="sxs-lookup"><span data-stu-id="e882d-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-140">Edite configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="e882d-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="e882d-141">X</span><span class="sxs-lookup"><span data-stu-id="e882d-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-142">X\*</span><span class="sxs-lookup"><span data-stu-id="e882d-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-143">Suporte para o atributo compactação dos dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="e882d-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-144">X</span><span class="sxs-lookup"><span data-stu-id="e882d-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-145">Edite armazenado, básica modos de exibição ou consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="e882d-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="e882d-146">X</span><span class="sxs-lookup"><span data-stu-id="e882d-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-147">X\*</span><span class="sxs-lookup"><span data-stu-id="e882d-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-148">Criar consultas permanentes que são acessíveis somente através de código.</span><span class="sxs-lookup"><span data-stu-id="e882d-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-149">X\*</span><span class="sxs-lookup"><span data-stu-id="e882d-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-150">Criar consultas acessíveis através de contêiner/IU do banco de dados e código.</span><span class="sxs-lookup"><span data-stu-id="e882d-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="e882d-151">X</span><span class="sxs-lookup"><span data-stu-id="e882d-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-152">Compactar/codifica banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e882d-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="e882d-153">X</span><span class="sxs-lookup"><span data-stu-id="e882d-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-154">X4</span><span class="sxs-lookup"><span data-stu-id="e882d-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-155">Atualize o cache.</span><span class="sxs-lookup"><span data-stu-id="e882d-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="e882d-156">X</span><span class="sxs-lookup"><span data-stu-id="e882d-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-157">X</span><span class="sxs-lookup"><span data-stu-id="e882d-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-158">Torne o banco de dados replicável.</span><span class="sxs-lookup"><span data-stu-id="e882d-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="e882d-159">X</span><span class="sxs-lookup"><span data-stu-id="e882d-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-160">X3</span><span class="sxs-lookup"><span data-stu-id="e882d-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-161">Criar réplicas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e882d-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="e882d-162">X</span><span class="sxs-lookup"><span data-stu-id="e882d-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-163">X3</span><span class="sxs-lookup"><span data-stu-id="e882d-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-164">Sincronize as réplicas.</span><span class="sxs-lookup"><span data-stu-id="e882d-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="e882d-165">X</span><span class="sxs-lookup"><span data-stu-id="e882d-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e882d-166">X3</span><span class="sxs-lookup"><span data-stu-id="e882d-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-167">Edite propriedades de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e882d-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="e882d-168">X</span><span class="sxs-lookup"><span data-stu-id="e882d-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e882d-169">Crie propriedades de banco de dados personalizado.</span><span class="sxs-lookup"><span data-stu-id="e882d-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="e882d-170">X</span><span class="sxs-lookup"><span data-stu-id="e882d-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e882d-171">Edite propriedades de coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="e882d-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="e882d-172">X</span><span class="sxs-lookup"><span data-stu-id="e882d-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e882d-p101">\* Disponível somente quando estiver trabalhando com bancos de dados do Microsoft Access (.mdb). As versões futuras do provedor do SQL poderão proporcionar essa funcionalidade nos projetos do Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="e882d-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="e882d-175">\*\* Disponível somente quando estiver trabalhando com projetos do Access.</span><span class="sxs-lookup"><span data-stu-id="e882d-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="e882d-176">\*\*\*Embora o mecanismo de banco de dados do Access oferece suporte algum ANSI 92 SQL, ele ainda não está totalmente compatível com ANSI92.</span><span class="sxs-lookup"><span data-stu-id="e882d-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="e882d-177">1 objeto usa **Conexão** ao banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="e882d-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="e882d-178">Objeto de usos **catálogo** 2 ao banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="e882d-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="e882d-179">Objeto de usos **réplica** 3 ao banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="e882d-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="e882d-180">Objeto de usos **JetEngine** 4 ao banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="e882d-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="e882d-181">Ao contrário do DAO, objetos ADO e ADOX podem executar as ações marcadas em bancos de dados que não sejam Jet desde que o provedor desses bancos de dados oferece suporte a essa ação.</span><span class="sxs-lookup"><span data-stu-id="e882d-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


