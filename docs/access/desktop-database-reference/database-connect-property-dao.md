---
title: Propriedade Database.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb3566a4f402c1b8ae75a47880f2101bf35d77db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294985"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="3ebce-102">Propriedade Database.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ebce-102">Database.Connect property (DAO)</span></span>


<span data-ttu-id="3ebce-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ebce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ebce-104">Define ou retorna um valor que fornece informações sobre a origem de um banco de dados aberto.</span><span class="sxs-lookup"><span data-stu-id="3ebce-104">Sets or returns a value that provides information about the source an open database.</span></span> <span data-ttu-id="3ebce-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3ebce-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebce-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ebce-106">Syntax</span></span>

<span data-ttu-id="3ebce-107">*expressão* . Connect</span><span class="sxs-lookup"><span data-stu-id="3ebce-107">*expression* .Connect</span></span>

<span data-ttu-id="3ebce-108">*expressão* Uma variável que representa um objeto do **Banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="3ebce-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ebce-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ebce-109">Remarks</span></span>

<span data-ttu-id="3ebce-p102">A definição da propriedade **Connect** é uma **String** composta de um especificador do tipo de banco de dados e zero ou mais parâmetros separados por ponto-e-vírgulas. A propriedade **Connect** passa informações adicionais para ODBC e determinados drivers ISAM conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="3ebce-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="3ebce-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo do banco de dados do Microsoft Access, defina primeiro a propriedade **Connect** do banco de dados da tabela vinculada como a sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="3ebce-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="3ebce-113">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="3ebce-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="3ebce-114">Em alguns casos (como nos bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deverá incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ebce-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="3ebce-115">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**.</span><span class="sxs-lookup"><span data-stu-id="3ebce-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ebce-116">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="3ebce-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="3ebce-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="3ebce-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="3ebce-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3ebce-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-119">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="3ebce-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="3ebce-120">[banco de dados],</span><span class="sxs-lookup"><span data-stu-id="3ebce-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="3ebce-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="3ebce-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="3ebce-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="3ebce-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="3ebce-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-124">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="3ebce-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="3ebce-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="3ebce-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-127">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="3ebce-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="3ebce-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="3ebce-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-130">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="3ebce-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="3ebce-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="3ebce-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-133">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="3ebce-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="3ebce-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="3ebce-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-136">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="3ebce-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="3ebce-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="3ebce-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-139">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="3ebce-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="3ebce-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="3ebce-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="3ebce-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="3ebce-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="3ebce-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="3ebce-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="3ebce-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="3ebce-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="3ebce-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="3ebce-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="3ebce-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="3ebce-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="3ebce-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="3ebce-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="3ebce-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-152">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="3ebce-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="3ebce-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="3ebce-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="3ebce-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="3ebce-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="3ebce-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="3ebce-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="3ebce-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="3ebce-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="3ebce-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="3ebce-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-160">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="3ebce-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="3ebce-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="3ebce-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="3ebce-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="3ebce-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="3ebce-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="3ebce-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="3ebce-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-166">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-167">Texto</span><span class="sxs-lookup"><span data-stu-id="3ebce-167">Text</span></span></p></td>
<td><p><span data-ttu-id="3ebce-168">Texto;</span><span class="sxs-lookup"><span data-stu-id="3ebce-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="3ebce-169">drive:\path</span><span class="sxs-lookup"><span data-stu-id="3ebce-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ebce-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="3ebce-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="3ebce-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="3ebce-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="3ebce-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ebce-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ebce-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="3ebce-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="3ebce-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="3ebce-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="3ebce-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="3ebce-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ebce-176">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ebce-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="3ebce-177">Se for necessária uma senha que não foi fornecida na definição da propriedade **Connect**, será exibida uma caixa de diálogo de logon na primeira vez que uma tabela for acessada pelo driver ODBC e mais uma vez se a conexão for fechada e aberta novamente.</span><span class="sxs-lookup"><span data-stu-id="3ebce-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="3ebce-178">Para os dados no Microsoft Exchange, a chave MAPILEVEL necessária deve ser definida como o caminho da pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="3ebce-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="3ebce-179">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso o nome dessa pasta deverá ser especificado como o argumento name para o método **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="3ebce-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="3ebce-180">A chave TABLETYPE deverá ser definida como "0" para abrir uma pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="3ebce-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="3ebce-181">A chave PROFILE é o padrão para o perfil usado no momento.</span><span class="sxs-lookup"><span data-stu-id="3ebce-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="3ebce-182">Você pode definir a **propriedade Connect** para um **objeto Database** fornecendo um argumento de origem para o **método OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="3ebce-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="3ebce-183">Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ebce-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="3ebce-184">Defina a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="3ebce-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="3ebce-185">É necessário ter permissões de acesso para o computador que contém o servidor do banco de dados que você está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="3ebce-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


