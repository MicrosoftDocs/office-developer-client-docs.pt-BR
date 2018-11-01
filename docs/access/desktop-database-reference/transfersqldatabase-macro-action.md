---
title: Ação da macro TransferirBancoDeDadosSQL
TOCTitle: TransferSQLDatabase Macro Action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fff0c9ac46e4a616fb5ea134e3dabc6b4e90576f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873100"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="c0664-102">Ação da macro TransferirBancoDeDadosSQL</span><span class="sxs-lookup"><span data-stu-id="c0664-102">TransferSQLDatabase Macro Action</span></span>


<span data-ttu-id="c0664-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0664-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0664-104">Em um projeto do Access, você pode usar a ação **TransferirBancoDeDadosSQL** para transferir um banco de dados do Microsoft SQL Server 7.0 ou posterior para outro banco de dados SQL Server 7.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c0664-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="c0664-105">Para obter mais informações sobre como transferir um banco de dados, consulte a documentação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0664-105">For more information about transferring a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <span data-ttu-id="c0664-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="c0664-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="c0664-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="c0664-108">Setting</span></span>

<span data-ttu-id="c0664-109">A ação **TransferirBancoDeDadosSQL** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c0664-109">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0664-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c0664-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c0664-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0664-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0664-112"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c0664-112"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c0664-113">O nome do servidor de banco de dados do SQL Server 7.0 ou posterior no qual você está copiando.</span><span class="sxs-lookup"><span data-stu-id="c0664-113">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0664-114"><strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="c0664-114"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="c0664-115">O nome do novo banco de dados a ser criado no servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="c0664-115">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0664-116"><strong>Usar conexão confiável</strong></span><span class="sxs-lookup"><span data-stu-id="c0664-116"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="c0664-117">Especifica se há ou não é uma conexão confiável ao SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0664-117">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="c0664-118">Se definido como <strong>Sim</strong>, não há uma conexão confiável e os argumentos de <strong>logon</strong> e <strong>senha</strong> não são necessários.</span><span class="sxs-lookup"><span data-stu-id="c0664-118">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="c0664-119">Se definido como <strong>não</strong>, o <strong>logon</strong> e a <strong>senha</strong> de argumentos é necessário.</span><span class="sxs-lookup"><span data-stu-id="c0664-119">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="c0664-120">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="c0664-120">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="c0664-121">Quando você usa uma conexão confiável, a segurança do SQL Server se integra com a segurança do sistema operacional Windows para fornecer um logon único com a rede e o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c0664-121">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0664-122"><strong>Logon</strong></span><span class="sxs-lookup"><span data-stu-id="c0664-122"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="c0664-123">O nome do logon no servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="c0664-123">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0664-124"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="c0664-124"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="c0664-p104">A senha do argumento <strong>Logon</strong>. Essa senha é armazenada como texto no projeto do Access, mas fica oculta durante a operação de transferência de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c0664-p104">The password for the <strong>Login</strong> argument. This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0664-127"><strong>Transferir dados de cópia</strong></span><span class="sxs-lookup"><span data-stu-id="c0664-127"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="c0664-p105">Especifica se os dados devem ser incluídos na operação de transferência de banco de dados. Se definido como <strong>Sim</strong>, todos os dados serão incluídos em todas as tabelas, juntamente com todas as estruturas de dados, propriedades estendidas e objetos de banco de dados. Se definido como <strong>Não</strong>, nenhum dado será incluído nas tabelas. Somente a estrutura da tabela e as propriedades estendidas serão criadas no servidor de destino, juntamente com todos os outros objetos de banco de dados (com exceção dos diagramas de banco de dados). O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="c0664-p105">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c0664-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0664-133">Remarks</span></span>

<span data-ttu-id="c0664-134">Não é possível executar outras operações enquanto o banco de dados está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="c0664-134">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="c0664-135">A ação **TransferirBancoDeDadosSQL**, por padrão, copia dados, definições de dados, objetos de banco de dados e propriedades estendidas; por exemplo, valores padrão, restrições de texto e valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c0664-135">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="c0664-136">Há requisitos para a transferência de um banco de dados:</span><span class="sxs-lookup"><span data-stu-id="c0664-136">There are requirements for transferring a database:</span></span>

  - <span data-ttu-id="c0664-137">Você deve ser membro da função sysadmin no servidor de destino (nenhuma função especial é exigida no servidor de origem).</span><span class="sxs-lookup"><span data-stu-id="c0664-137">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

<!-- end list -->

  - <span data-ttu-id="c0664-138">O servidor SQL atualmente conectado ao projeto do Access e ao servidor de destino para o qual você está transferindo o banco de dados deve ser SQL Server versão 7.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c0664-138">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c0664-139">[!OBSERVAçãO] Servidores vinculados não são transferidos durante a operação de transferência de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c0664-139">Linked servers are not transferred during a database transfer operation.</span></span></P>



<span data-ttu-id="c0664-140">Para executar a ação **TransferirBancoDeDadosSQL** em um módulo do VBA (Visual Basic for Applications), use o método **TransferSQLDatabase** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="c0664-140">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

