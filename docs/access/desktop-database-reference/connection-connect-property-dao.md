---
title: Propriedade Connection. Connect (DAO)
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
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="07690-102">Propriedade Connection. Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="07690-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="07690-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07690-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07690-104">Define ou retorna um valor que fornece informações sobre a origem de uma conexão aberta.</span><span class="sxs-lookup"><span data-stu-id="07690-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="07690-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="07690-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07690-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07690-106">Syntax</span></span>

<span data-ttu-id="07690-107">*expressão* . Ao</span><span class="sxs-lookup"><span data-stu-id="07690-107">*expression* .Connect</span></span>

<span data-ttu-id="07690-108">*expressão* Uma variável que representa um objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="07690-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="07690-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="07690-109">Remarks</span></span>

<span data-ttu-id="07690-p102">A definição da propriedade **Connect** é uma **String** composta de um especificador do tipo de banco de dados e zero ou mais parâmetros separados por ponto-e-vírgulas. A propriedade **Connect** passa informações adicionais para ODBC e determinados drivers ISAM conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="07690-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="07690-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="07690-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="07690-113">Para um objeto **TableDef** que representa uma tabela vinculada, a configuração da propriedade **Connect** consiste em uma ou duas partes (um especificador de tipo de banco de dados e um caminho para o banco de dados), que terminam com um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="07690-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="07690-114">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="07690-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="07690-115">Em alguns casos (como nos bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deverá incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="07690-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="07690-116">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**.</span><span class="sxs-lookup"><span data-stu-id="07690-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07690-117">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="07690-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="07690-118">Especificado</span><span class="sxs-lookup"><span data-stu-id="07690-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="07690-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="07690-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07690-120">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="07690-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="07690-121">[banco de dados];</span><span class="sxs-lookup"><span data-stu-id="07690-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="07690-122">unidade: \ path\filename</span><span class="sxs-lookup"><span data-stu-id="07690-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="07690-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="07690-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="07690-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="07690-125">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="07690-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="07690-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="07690-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="07690-128">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="07690-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="07690-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="07690-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="07690-131">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="07690-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="07690-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="07690-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="07690-134">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="07690-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="07690-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="07690-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="07690-137">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="07690-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="07690-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="07690-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="07690-140">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="07690-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="07690-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="07690-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="07690-143">unidade: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="07690-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="07690-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="07690-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="07690-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="07690-146">unidade: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="07690-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-147">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="07690-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="07690-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="07690-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="07690-149">unidade: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="07690-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="07690-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="07690-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="07690-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="07690-152">unidade: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="07690-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-153">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="07690-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="07690-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="07690-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="07690-155">unidade: \ path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="07690-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="07690-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="07690-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="07690-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="07690-158">unidade: \ path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="07690-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="07690-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="07690-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="07690-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="07690-161">unidade: \ path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="07690-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-162">HTML Import</span><span class="sxs-lookup"><span data-stu-id="07690-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="07690-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="07690-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="07690-164">unidade: \ path\filename</span><span class="sxs-lookup"><span data-stu-id="07690-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-165">HTML Export</span><span class="sxs-lookup"><span data-stu-id="07690-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="07690-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="07690-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="07690-167">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-168">Texto</span><span class="sxs-lookup"><span data-stu-id="07690-168">Text</span></span></p></td>
<td><p><span data-ttu-id="07690-169">Textos</span><span class="sxs-lookup"><span data-stu-id="07690-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="07690-170">unidade: \ caminho</span><span class="sxs-lookup"><span data-stu-id="07690-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07690-171">Connectivity</span><span class="sxs-lookup"><span data-stu-id="07690-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="07690-172">Connectivity DATABASE = database; UID = User; PWD = senha; DSN = DataSourceName; [LOGINTIMEOUT = segundos;]</span><span class="sxs-lookup"><span data-stu-id="07690-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="07690-173">Nenhum</span><span class="sxs-lookup"><span data-stu-id="07690-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07690-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="07690-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="07690-175">Exchange 4,0; MAPILEVEL = FolderPath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = senha;] [DATABASE = database;]</span><span class="sxs-lookup"><span data-stu-id="07690-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="07690-176">unidade: \ path\filename</span><span class="sxs-lookup"><span data-stu-id="07690-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="07690-177">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="07690-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="07690-178">Se for necessária uma senha que não foi fornecida na definição da propriedade **Connect**, será exibida uma caixa de diálogo de logon na primeira vez que uma tabela for acessada pelo driver ODBC e mais uma vez se a conexão for fechada e aberta novamente.</span><span class="sxs-lookup"><span data-stu-id="07690-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="07690-179">Para os dados no Microsoft Exchange, a chave MAPILEVEL necessária deve ser definida como o caminho da pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="07690-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="07690-180">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome da pasta deve ser especificado como o argumento \*\*\*\* Name para o método CreateTable.</span><span class="sxs-lookup"><span data-stu-id="07690-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="07690-181">A chave TABLETYPE deverá ser definida como "0" para abrir uma pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="07690-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="07690-182">A chave PROFILE é o padrão para o perfil usado no momento.</span><span class="sxs-lookup"><span data-stu-id="07690-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="07690-183">Para as tabelas base em um banco de dados do Microsoft Access, a definição da propriedade **Connect** será uma sequência de caracteres com comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="07690-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="07690-184">Você pode definir a propriedade **Connect** para um objeto **Database** fornecendo um argumento Source para o método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="07690-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="07690-185">Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="07690-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="07690-186">Em um objeto **QueryDef** no espaço de trabalho do Microsoft Access, você pode usar a propriedade **Connect** com a propriedade ReturnsRecords para criar uma consulta passagem ODBC SQL.</span><span class="sxs-lookup"><span data-stu-id="07690-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="07690-187">O databasetype da cadeia de conexão é "ODBC;", e o lembrete da sequência contém informações específicas para o driver ODBC utilizado para acessar os dados remotos.</span><span class="sxs-lookup"><span data-stu-id="07690-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="07690-188">Para obter mais informações, consulte a documentação do driver específico.</span><span class="sxs-lookup"><span data-stu-id="07690-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="07690-189">Defina a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="07690-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="07690-190">É necessário ter permissões de acesso para o computador que contém o servidor do banco de dados que você está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="07690-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


