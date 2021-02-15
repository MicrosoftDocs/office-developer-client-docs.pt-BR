---
title: Ação da macro TransferirBancoDeDadosSQL
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306843"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="39c13-102">Ação da macro TransferirBancoDeDadosSQL</span><span class="sxs-lookup"><span data-stu-id="39c13-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="39c13-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39c13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39c13-104">Em um projeto do Access, você pode usar a ação **TransferirBancoDeDadosSQL** para transferir um banco de dados do Microsoft SQL Server 7.0 ou posterior para outro banco de dados SQL Server 7.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="39c13-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="39c13-105">Para obter mais informações sobre como transferir um banco de dados, consulte a documentação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39c13-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="39c13-106">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="39c13-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="39c13-107">Setting</span><span class="sxs-lookup"><span data-stu-id="39c13-107">Setting</span></span>

<span data-ttu-id="39c13-108">A ação **TransferirBancoDeDadosSQL** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="39c13-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39c13-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="39c13-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="39c13-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c13-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c13-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="39c13-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39c13-112">O nome do servidor de banco de dados do SQL Server 7.0 ou posterior no qual você está copiando.</span><span class="sxs-lookup"><span data-stu-id="39c13-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c13-113"><strong>Banco de dados</strong></span><span class="sxs-lookup"><span data-stu-id="39c13-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="39c13-114">O nome do novo banco de dados a ser criado no servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="39c13-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c13-115"><strong>Usar conexão confiável</strong></span><span class="sxs-lookup"><span data-stu-id="39c13-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="39c13-116">Especifica se há ou não uma conexão confiável para o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39c13-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="39c13-117">Se definido como <strong>Sim</strong>, isso indicará que há uma conexão confiável e os argumentos <strong>Logon</strong> e <strong>Senha</strong> não serão exigidos.</span><span class="sxs-lookup"><span data-stu-id="39c13-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="39c13-118">Se definido como <strong>Não</strong>, os argumentos <strong>Logon</strong> e <strong>Senha</strong> serão exigidos.</span><span class="sxs-lookup"><span data-stu-id="39c13-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="39c13-119">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="39c13-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="39c13-120">Quando você usa uma conexão confiável, a segurança do SQL Server se integra à segurança do sistema operacional Windows para fornecer um único logoff na rede e no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39c13-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c13-121"><strong>Logon</strong></span><span class="sxs-lookup"><span data-stu-id="39c13-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="39c13-122">O nome do logon no servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="39c13-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c13-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="39c13-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="39c13-p103">A senha do argumento <strong>Logon</strong>. Essa senha é armazenada como texto no projeto do Access, mas fica oculta durante a operação de transferência de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39c13-p103">The password for the <strong>Login</strong> argument. This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c13-126"><strong>Transferir dados de cópia</strong></span><span class="sxs-lookup"><span data-stu-id="39c13-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="39c13-p104">Especifica se os dados devem ser incluídos na operação de transferência de banco de dados. Se definido como <strong>Sim</strong>, todos os dados serão incluídos em todas as tabelas, juntamente com todas as estruturas de dados, propriedades estendidas e objetos de banco de dados. Se definido como <strong>Não</strong>, nenhum dado será incluído nas tabelas. Somente a estrutura da tabela e as propriedades estendidas serão criadas no servidor de destino, juntamente com todos os outros objetos de banco de dados (com exceção dos diagramas de banco de dados). O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="39c13-p104">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="39c13-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="39c13-132">Remarks</span></span>

<span data-ttu-id="39c13-133">Não é possível executar outras operações enquanto o banco de dados está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="39c13-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="39c13-134">A ação **TransferirBancoDeDadosSQL**, por padrão, copia dados, definições de dados, objetos de banco de dados e propriedades estendidas; por exemplo, valores padrão, restrições de texto e valores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="39c13-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="39c13-135">Há requisitos para a transferência de um banco de dados:</span><span class="sxs-lookup"><span data-stu-id="39c13-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="39c13-136">Você deve ser membro da função sysadmin no servidor de destino (nenhuma função especial é exigida no servidor de origem).</span><span class="sxs-lookup"><span data-stu-id="39c13-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="39c13-137">O servidor SQL atualmente conectado ao projeto do Access e ao servidor de destino para o qual você está transferindo o banco de dados deve ser SQL Server versão 7.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="39c13-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="39c13-138">[!OBSERVAçãO] Servidores vinculados não são transferidos durante a operação de transferência de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39c13-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="39c13-139">Para executar a ação **TransferirBancoDeDadosSQL** em um módulo do VBA (Visual Basic for Applications), use o método **TransferSQLDatabase** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="39c13-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

