---
title: Propriedade QueryDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698271"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="8c77b-102">Propriedade QueryDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="8c77b-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="8c77b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c77b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c77b-p101">Define ou retorna um valor que fornece as informações sobre a fonte do banco de dados usada em uma consulta passagem. **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8c77b-p101">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c77b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c77b-106">Syntax</span></span>

<span data-ttu-id="8c77b-107">*expressão* . Conecte-se</span><span class="sxs-lookup"><span data-stu-id="8c77b-107">*expression* .Connect</span></span>

<span data-ttu-id="8c77b-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="8c77b-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c77b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c77b-109">Remarks</span></span>

<span data-ttu-id="8c77b-p102">A configuração da propriedade **Connect** é uma **String** composta por um especificador de tipo de banco de dados e nenhum ou mais parâmetros separados por ponto-e-vírgula. A propriedade **Connect** transmite informações adicionais para o ODBC e certos drivers do ISAM, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="8c77b-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="8c77b-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="8c77b-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="8c77b-p103">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como os bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deve incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8c77b-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="8c77b-115">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**. Em um espaço de trabalho ODBCDirect, somente o especificador "ODBC" pode ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="8c77b-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c77b-116">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="8c77b-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="8c77b-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="8c77b-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="8c77b-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8c77b-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-119">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="8c77b-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="8c77b-120">[database;]</span><span class="sxs-lookup"><span data-stu-id="8c77b-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="8c77b-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8c77b-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="8c77b-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="8c77b-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="8c77b-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-124">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="8c77b-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="8c77b-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="8c77b-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-127">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="8c77b-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="8c77b-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="8c77b-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-130">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="8c77b-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="8c77b-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="8c77b-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-133">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="8c77b-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="8c77b-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="8c77b-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-136">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="8c77b-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="8c77b-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="8c77b-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-139">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="8c77b-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="8c77b-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="8c77b-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8c77b-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="8c77b-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="8c77b-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="8c77b-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8c77b-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="8c77b-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="8c77b-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="8c77b-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8c77b-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="8c77b-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="8c77b-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="8c77b-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8c77b-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-152">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="8c77b-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="8c77b-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="8c77b-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="8c77b-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="8c77b-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="8c77b-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="8c77b-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="8c77b-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="8c77b-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="8c77b-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="8c77b-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-160">drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="8c77b-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="8c77b-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="8c77b-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="8c77b-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8c77b-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="8c77b-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="8c77b-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="8c77b-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-166">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-167">Texto</span><span class="sxs-lookup"><span data-stu-id="8c77b-167">Text</span></span></p></td>
<td><p><span data-ttu-id="8c77b-168">Texto;</span><span class="sxs-lookup"><span data-stu-id="8c77b-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="8c77b-169">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="8c77b-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c77b-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="8c77b-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="8c77b-171">ODBC; Banco de dados = database; UID = user; PWD = password; DSN = datasourcename; [LOGINTIMEOUT = seconds;]</span><span class="sxs-lookup"><span data-stu-id="8c77b-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="8c77b-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8c77b-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c77b-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8c77b-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="8c77b-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [Perfil = profile;] [PWD = password;] [Banco de dados = database;]</span><span class="sxs-lookup"><span data-stu-id="8c77b-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="8c77b-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8c77b-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c77b-176">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8c77b-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="8c77b-177">Se uma senha for solicitada, mas não for fornecida na configuração da propriedade **Connect**, uma caixa de diálogo de login será exibida na primeira vez em que a tabela for acessada pelo driver ODBC e novamente se a conexão for fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="8c77b-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="8c77b-178">Para dados no Microsoft Exchange, a chave MAPILEVEL exigida deve estar definida como um caminho de pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="8c77b-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="8c77b-179">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome dessa pasta deve ser especificado como o argumento nome para o método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="8c77b-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="8c77b-180">A chave TABLETYPE deve estar definida como "0" para abrir a pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="8c77b-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="8c77b-181">A chave PROFILE é o padrão para o perfil usado no momento.</span><span class="sxs-lookup"><span data-stu-id="8c77b-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="8c77b-182">Em um objeto **QueryDef** em um espaço de trabalho do Microsoft Access, use a propriedade **Connect** com a propriedade ReturnsRecords para criar uma consulta SQL Passagem para ODBC.</span><span class="sxs-lookup"><span data-stu-id="8c77b-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="8c77b-183">Databasetype da cadeia de caracteres de conexão for "ODBC;", e o restante da cadeia de caracteres contém informações específicas para o driver ODBC usado para acessar os dados remotos.</span><span class="sxs-lookup"><span data-stu-id="8c77b-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="8c77b-184">Para obter mais informações, consulte a documentação do driver específico.</span><span class="sxs-lookup"><span data-stu-id="8c77b-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="8c77b-185">Você deve definir a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="8c77b-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="8c77b-186">Você deve ter permissão de acesso ao computador que contém o servidor de banco de dados que está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="8c77b-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


