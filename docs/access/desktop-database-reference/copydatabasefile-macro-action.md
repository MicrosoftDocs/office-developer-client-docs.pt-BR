---
title: Ação da macro CopiarArquivoDeBancodeDados
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3c98d8795bb7039c0ae158414401dc5d754066f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699440"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="5fb6d-102">Ação da macro CopiarArquivoDeBancodeDados</span><span class="sxs-lookup"><span data-stu-id="5fb6d-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="5fb6d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fb6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5fb6d-104">Você pode usar a ação **CopiarArquivoDeBancodeDados** para fazer uma cópia do banco de dados atual do Microsoft SQL Server 7.0 ou versões posteriores conectado ao projeto do Access.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="5fb6d-105">Access desanexa o banco de dados atual e, em seguida, anexa-o ao servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="5fb6d-106">Para obter mais informações sobre como desanexar e anexar um banco de dados, consulte a documentação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="5fb6d-107">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="5fb6d-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="5fb6d-108">Setting</span></span>

<span data-ttu-id="5fb6d-109">A ação **CopiarArquivoDeBancodeDados** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fb6d-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="5fb6d-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5fb6d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fb6d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fb6d-112"><strong>Nome de Arquivo do Banco de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="5fb6d-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5fb6d-p102">O nome do novo Arquivo de Dados Mestre. O caminho padrão do arquivo é o local atual do arquivo de projeto do Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="5fb6d-p102">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fb6d-115"><strong>Substituir Arquivo Existente</strong></span><span class="sxs-lookup"><span data-stu-id="5fb6d-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="5fb6d-p103">Especifica se será ou não substituído um arquivo existente pelo mesmo nome. Se estiver definido como <strong>Sim</strong> e o nome de arquivo já existir , o arquivo será substituído. Se estiver definido como <strong>Não</strong> e o nome de arquivo já existir, o arquivo não será substituído e a ação falhará. Se o arquivo ainda não existir, essa configuração será ignorada. O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-p103">Specifies whether or not to replace an existing file with the same name. If set to <strong>Yes</strong> and the filename already exists, the file is overwritten. If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails. If the file does not already exist, this setting is ignored. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fb6d-121"><strong>Desconectar Todos os Usuários</strong></span><span class="sxs-lookup"><span data-stu-id="5fb6d-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="5fb6d-p104">Especifica se o Access deve ou não remover os usuários do banco de dados. Se estiver definido como <strong>Sim</strong>, quaisquer usuários conectados ao banco de dados atual serão desconectados para que a operação de banco de dados de cópia possa prosseguir. Se estiver definido como <strong>Não</strong> e um ou mais usuários estiverem conectados ao banco de dados, a operação de banco de dados de cópia falhará. O padrão é <strong>Não</strong>. 

</span><span class="sxs-lookup"><span data-stu-id="5fb6d-p104">Specifies whether or not Access should force users off the database. If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed. If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails. The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="5fb6d-126"><strong>Aviso</strong>: desconectar usuários de um banco de dados, sem aviso adequado pode levar à perda de dados.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5fb6d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fb6d-127">Remarks</span></span>

<span data-ttu-id="5fb6d-128">A operação de cópia é síncrona, por isso não será possível executar outras operações enquanto a cópia do banco de dados não for concluída.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="5fb6d-129">A ação **CopiarArquivoDeBancodeDados** não só copia os dados, as definições de dados e os objetos de banco de dados, como também copia propriedades estendidas, como valores padrão, restrições de texto e valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="5fb6d-130">Requisitos para copiar um banco de dados:</span><span class="sxs-lookup"><span data-stu-id="5fb6d-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="5fb6d-131">Todos os aplicativos e usuários precisam ser desconectados antes de copiar o arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="5fb6d-132">Todos os objetos e modos de exibição, com exceção do Painel de Navegação, precisam ser fechados.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="5fb6d-133">O banco de dados atual não pode ser replicado.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="5fb6d-134">O banco de dados de servidor de origem precisa ser o Microsoft SQL Server 7.0 ou versão posterior, ou o SQL Server 2000 Desktop Engine executado em um computador local.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="5fb6d-135">O banco de dados do SQL Server no servidor de origem precisa consistir em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="5fb6d-136">Você precisa ser membro da função sysadmin nos computadores SQL Server de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="5fb6d-137">Para executar a ação **CopiarArquivoDeBancodeDados** em um módulo do Visual Basic for Applications, use o método **CopyDatabaseFile** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5fb6d-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

