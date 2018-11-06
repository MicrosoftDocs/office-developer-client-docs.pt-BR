---
title: Propriedade QueryDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4956d9d2652ab8268a5f49a9b7edc63ebe2878c7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997976"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="8100c-102">Propriedade QueryDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="8100c-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="8100c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8100c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8100c-p101">Define ou retorna um valor que fornece as informações sobre a fonte do banco de dados usada em uma consulta passagem. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8100c-p101">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8100c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8100c-106">Syntax</span></span>

<span data-ttu-id="8100c-107">*expressão* . Conecte-se</span><span class="sxs-lookup"><span data-stu-id="8100c-107">*expression* .Connect</span></span>

<span data-ttu-id="8100c-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="8100c-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8100c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8100c-109">Remarks</span></span>

<span data-ttu-id="8100c-p102">A configuração da propriedade **Connect** é uma **String** composta por um especificador de tipo de banco de dados e nenhum ou mais parâmetros separados por ponto-e-vírgula. A propriedade **Connect** transmite informações adicionais para o ODBC e certos drivers do ISAM, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="8100c-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="8100c-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="8100c-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="8100c-p103">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como os bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deve incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8100c-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="8100c-115">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**. Em um espaço de trabalho ODBCDirect, somente o especificador "ODBC" pode ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="8100c-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8100c-116">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="8100c-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="8100c-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="8100c-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="8100c-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8100c-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8100c-119">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="8100c-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="8100c-120">[database;]</span><span class="sxs-lookup"><span data-stu-id="8100c-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="8100c-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8100c-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="8100c-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="8100c-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="8100c-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="8100c-124">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="8100c-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="8100c-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="8100c-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="8100c-127">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="8100c-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="8100c-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="8100c-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8100c-130">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="8100c-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="8100c-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="8100c-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="8100c-133">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="8100c-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="8100c-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="8100c-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="8100c-136">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="8100c-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="8100c-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="8100c-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="8100c-139">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="8100c-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="8100c-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="8100c-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="8100c-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8100c-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="8100c-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="8100c-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="8100c-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="8100c-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8100c-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="8100c-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="8100c-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="8100c-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8100c-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8100c-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="8100c-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="8100c-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="8100c-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="8100c-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8100c-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-152">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="8100c-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="8100c-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="8100c-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="8100c-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="8100c-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="8100c-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="8100c-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="8100c-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="8100c-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="8100c-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="8100c-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="8100c-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="8100c-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="8100c-160">drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="8100c-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="8100c-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="8100c-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="8100c-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="8100c-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8100c-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="8100c-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="8100c-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="8100c-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="8100c-166">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-167">Texto</span><span class="sxs-lookup"><span data-stu-id="8100c-167">Text</span></span></p></td>
<td><p><span data-ttu-id="8100c-168">Texto;</span><span class="sxs-lookup"><span data-stu-id="8100c-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="8100c-169">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8100c-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8100c-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="8100c-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="8100c-171">ODBC; Banco de dados = database; UID = user; PWD = password; DSN = datasourcename; [LOGINTIMEOUT = seconds;]</span><span class="sxs-lookup"><span data-stu-id="8100c-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="8100c-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8100c-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8100c-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8100c-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="8100c-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [Perfil = profile;] [PWD = password;] [Banco de dados = database;]</span><span class="sxs-lookup"><span data-stu-id="8100c-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="8100c-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8100c-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8100c-176">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8100c-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="8100c-177">Se uma senha for solicitada, mas não for fornecida na configuração da propriedade **Connect**, uma caixa de diálogo de login será exibida na primeira vez em que a tabela for acessada pelo driver ODBC e novamente se a conexão for fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="8100c-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="8100c-178">Para dados no Microsoft Exchange, a chave MAPILEVEL exigida deve estar definida como um caminho de pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="8100c-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="8100c-179">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome dessa pasta deve ser especificado como o argumento nome para o método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="8100c-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="8100c-180">A chave TABLETYPE deve estar definida como "0" para abrir a pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="8100c-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="8100c-181">A chave PROFILE é o padrão para o perfil usado no momento.</span><span class="sxs-lookup"><span data-stu-id="8100c-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="8100c-182">Em um objeto **QueryDef** em um espaço de trabalho do Microsoft Access, use a propriedade **Connect** com a propriedade ReturnsRecords para criar uma consulta SQL Passagem para ODBC.</span><span class="sxs-lookup"><span data-stu-id="8100c-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="8100c-183">Databasetype da cadeia de caracteres de conexão for "ODBC;", e o restante da cadeia de caracteres contém informações específicas para o driver ODBC usado para acessar os dados remotos.</span><span class="sxs-lookup"><span data-stu-id="8100c-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="8100c-184">Para obter mais informações, consulte a documentação do driver específico.</span><span class="sxs-lookup"><span data-stu-id="8100c-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="8100c-185">Você deve definir a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="8100c-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="8100c-186">Você deve ter permissão de acesso ao computador que contém o servidor de banco de dados que está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="8100c-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


