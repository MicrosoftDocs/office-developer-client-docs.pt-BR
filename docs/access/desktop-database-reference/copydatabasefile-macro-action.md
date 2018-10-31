---
title: Ação de macro CopiarArquivoDeBancodeDados
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 934a44ee754c403a9ef185537c8af114f1200d82
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862531"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="23394-102">Ação de macro CopiarArquivoDeBancodeDados</span><span class="sxs-lookup"><span data-stu-id="23394-102">CopyDatabaseFile Macro Action</span></span>


<span data-ttu-id="23394-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="23394-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23394-104">Você pode usar a ação **CopiarArquivoDeBancodeDados** para fazer uma cópia do banco de dados atual do Microsoft SQL Server 7.0 ou versões posteriores conectado ao projeto do Access.</span><span class="sxs-lookup"><span data-stu-id="23394-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="23394-105">Access desanexa o banco de dados atual e, em seguida, anexa-o ao servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="23394-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="23394-106">Para obter mais informações sobre como desanexar e anexar um banco de dados, consulte a documentação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="23394-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <span data-ttu-id="23394-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="23394-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="23394-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="23394-109">Setting</span></span>

<span data-ttu-id="23394-110">A ação **CopiarArquivoDeBancodeDados** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="23394-110">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23394-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="23394-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="23394-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="23394-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23394-113"><strong>Nome de Arquivo do Banco de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="23394-113"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="23394-p103">O nome do novo Arquivo de Dados Mestre. O caminho padrão do arquivo é o local atual do arquivo de projeto do Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="23394-p103">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23394-116"><strong>Substituir Arquivo Existente</strong></span><span class="sxs-lookup"><span data-stu-id="23394-116"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="23394-p104">Especifica se será ou não substituído um arquivo existente pelo mesmo nome. Se estiver definido como <strong>Sim</strong> e o nome de arquivo já existir , o arquivo será substituído. Se estiver definido como <strong>Não</strong> e o nome de arquivo já existir, o arquivo não será substituído e a ação falhará. Se o arquivo ainda não existir, essa configuração será ignorada. O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="23394-p104">Specifies whether or not to replace an existing file with the same name. If set to <strong>Yes</strong> and the filename already exists, the file is overwritten. If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails. If the file does not already exist, this setting is ignored. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23394-122"><strong>Desconectar Todos os Usuários</strong></span><span class="sxs-lookup"><span data-stu-id="23394-122"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="23394-p105">Especifica se o Access deve ou não remover os usuários do banco de dados. Se estiver definido como <strong>Sim</strong>, quaisquer usuários conectados ao banco de dados atual serão desconectados para que a operação de banco de dados de cópia possa prosseguir. Se estiver definido como <strong>Não</strong> e um ou mais usuários estiverem conectados ao banco de dados, a operação de banco de dados de cópia falhará. O padrão é <strong>Não</strong>. 

</span><span class="sxs-lookup"><span data-stu-id="23394-p105">Specifies whether or not Access should force users off the database. If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed. If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails. The default is <strong>No</strong>.</span></span></p>

> [!WARNING]
> <span data-ttu-id="23394-127">Desconectar usuários de um banco de dados sem aviso adequado pode causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="23394-127">Disconnecting users from a database without adequate warning can lead to data loss.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="23394-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="23394-128">Remarks</span></span>

<span data-ttu-id="23394-129">A operação de cópia é síncrona, por isso não será possível executar outras operações enquanto a cópia do banco de dados não for concluída.</span><span class="sxs-lookup"><span data-stu-id="23394-129">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="23394-130">A ação **CopiarArquivoDeBancodeDados** não só copia os dados, as definições de dados e os objetos de banco de dados, como também copia propriedades estendidas, como valores padrão, restrições de texto e valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="23394-130">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="23394-131">Requisitos para copiar um banco de dados:</span><span class="sxs-lookup"><span data-stu-id="23394-131">Requirements for copying a database:</span></span>

  - <span data-ttu-id="23394-132">Todos os aplicativos e usuários precisam ser desconectados antes de copiar o arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23394-132">You must disconnect all applications and users before you copy the database file.</span></span>

  - <span data-ttu-id="23394-133">Todos os objetos e modos de exibição, com exceção do Painel de Navegação, precisam ser fechados.</span><span class="sxs-lookup"><span data-stu-id="23394-133">All objects and views except the Navigation Pane must be closed.</span></span>

  - <span data-ttu-id="23394-134">O banco de dados atual não pode ser replicado.</span><span class="sxs-lookup"><span data-stu-id="23394-134">The current database must not be replicated.</span></span>

  - <span data-ttu-id="23394-135">O banco de dados de servidor de origem precisa ser o Microsoft SQL Server 7.0 ou versão posterior, ou o SQL Server 2000 Desktop Engine executado em um computador local.</span><span class="sxs-lookup"><span data-stu-id="23394-135">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="23394-136">O banco de dados do SQL Server no servidor de origem precisa consistir em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="23394-136">The SQL Server database on the source server must be a single file database.</span></span>

  - <span data-ttu-id="23394-137">Você precisa ser membro da função sysadmin nos computadores SQL Server de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="23394-137">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="23394-138">Para executar a ação **CopiarArquivoDeBancodeDados** em um módulo do Visual Basic for Applications, use o método **CopyDatabaseFile** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="23394-138">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

