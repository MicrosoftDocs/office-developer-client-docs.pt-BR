---
title: Propriedade Connection.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295923"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="87dfd-102">Propriedade Connection.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="87dfd-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="87dfd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87dfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87dfd-104">Define ou retorna um valor que fornece informações sobre a origem de uma conexão aberta.</span><span class="sxs-lookup"><span data-stu-id="87dfd-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="87dfd-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="87dfd-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87dfd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87dfd-106">Syntax</span></span>

<span data-ttu-id="87dfd-107">*expressão* . Connect</span><span class="sxs-lookup"><span data-stu-id="87dfd-107">*expression* .Connect</span></span>

<span data-ttu-id="87dfd-108">*expressão* Uma variável que representa um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="87dfd-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87dfd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="87dfd-109">Remarks</span></span>

<span data-ttu-id="87dfd-p102">A definição da propriedade **Connect** é uma **String** composta de um especificador do tipo de banco de dados e zero ou mais parâmetros separados por ponto-e-vírgulas. A propriedade **Connect** passa informações adicionais para ODBC e determinados drivers ISAM conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="87dfd-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="87dfd-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="87dfd-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="87dfd-113">Para um objeto **TableDef** que representa uma tabela vinculada, a definição da propriedade **Connect** é composta de uma ou duas partes (um especificador do tipo do banco de dados e um caminho para o banco de dados), cada uma delas termina com um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="87dfd-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="87dfd-114">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="87dfd-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="87dfd-115">Em alguns casos (como nos bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deverá incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87dfd-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="87dfd-116">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**.</span><span class="sxs-lookup"><span data-stu-id="87dfd-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87dfd-117">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="87dfd-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="87dfd-118">Especificador</span><span class="sxs-lookup"><span data-stu-id="87dfd-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="87dfd-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="87dfd-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-120">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="87dfd-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="87dfd-121">[banco de dados],</span><span class="sxs-lookup"><span data-stu-id="87dfd-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="87dfd-122">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="87dfd-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="87dfd-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="87dfd-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="87dfd-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-125">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="87dfd-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="87dfd-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="87dfd-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-128">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="87dfd-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="87dfd-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="87dfd-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-131">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="87dfd-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="87dfd-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="87dfd-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-134">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="87dfd-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="87dfd-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="87dfd-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-137">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="87dfd-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="87dfd-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="87dfd-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-140">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="87dfd-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="87dfd-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="87dfd-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-143">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="87dfd-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="87dfd-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="87dfd-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="87dfd-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-146">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="87dfd-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-147">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="87dfd-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="87dfd-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="87dfd-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-149">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="87dfd-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="87dfd-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="87dfd-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="87dfd-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-152">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="87dfd-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-153">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="87dfd-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="87dfd-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="87dfd-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-155">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="87dfd-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="87dfd-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="87dfd-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="87dfd-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-158">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="87dfd-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="87dfd-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="87dfd-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="87dfd-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-161">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="87dfd-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-162">HTML Import</span><span class="sxs-lookup"><span data-stu-id="87dfd-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="87dfd-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="87dfd-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-164">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="87dfd-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-165">HTML Export</span><span class="sxs-lookup"><span data-stu-id="87dfd-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="87dfd-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="87dfd-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-167">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-168">Texto</span><span class="sxs-lookup"><span data-stu-id="87dfd-168">Text</span></span></p></td>
<td><p><span data-ttu-id="87dfd-169">Texto;</span><span class="sxs-lookup"><span data-stu-id="87dfd-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="87dfd-170">drive:\path</span><span class="sxs-lookup"><span data-stu-id="87dfd-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dfd-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="87dfd-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="87dfd-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="87dfd-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="87dfd-173">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87dfd-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dfd-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="87dfd-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="87dfd-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="87dfd-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="87dfd-176">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="87dfd-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87dfd-177">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87dfd-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="87dfd-178">Se for necessária uma senha que não foi fornecida na definição da propriedade **Connect**, será exibida uma caixa de diálogo de logon na primeira vez que uma tabela for acessada pelo driver ODBC e mais uma vez se a conexão for fechada e aberta novamente.</span><span class="sxs-lookup"><span data-stu-id="87dfd-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="87dfd-179">Para os dados no Microsoft Exchange, a chave MAPILEVEL necessária deve ser definida como o caminho da pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="87dfd-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="87dfd-180">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso o nome dessa pasta deverá ser especificado como o argumento name para o método **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="87dfd-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="87dfd-181">A chave TABLETYPE deverá ser definida como "0" para abrir uma pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="87dfd-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="87dfd-182">A chave PROFILE é o padrão para o perfil usado no momento.</span><span class="sxs-lookup"><span data-stu-id="87dfd-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="87dfd-183">Para as tabelas base em um banco de dados do Microsoft Access, a definição da propriedade **Connect** será uma sequência de caracteres com comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="87dfd-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="87dfd-184">Você pode definir a **propriedade Connect** para um **objeto Database** fornecendo um argumento de origem para o **método OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="87dfd-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="87dfd-185">Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87dfd-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="87dfd-186">Em um objeto **QueryDef** no espaço de trabalho do Microsoft Access, você pode usar a propriedade **Connect** com a propriedade ReturnsRecords para criar uma consulta passagem ODBC SQL.</span><span class="sxs-lookup"><span data-stu-id="87dfd-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="87dfd-187">O databasetype da cadeia de conexão é "ODBC;", e o lembrete da sequência contém informações específicas para o driver ODBC utilizado para acessar os dados remotos.</span><span class="sxs-lookup"><span data-stu-id="87dfd-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="87dfd-188">Para obter mais informações, consulte a documentação do driver específico.</span><span class="sxs-lookup"><span data-stu-id="87dfd-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="87dfd-189">Defina a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="87dfd-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="87dfd-190">É necessário ter permissões de acesso para o computador que contém o servidor do banco de dados que você está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="87dfd-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


