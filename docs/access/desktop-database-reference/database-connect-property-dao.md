---
title: Propriedade Database.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 82b75af86d45b8711660d769607c46b626477bac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872792"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="95ba8-102">Propriedade Database.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="95ba8-102">Database.Connect Property (DAO)</span></span>


<span data-ttu-id="95ba8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="95ba8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95ba8-p101">Define ou retorna um valor que fornece informações sobre a origem de um banco de dados aberto. **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="95ba8-p101">Sets or returns a value that provides information about the source an open database. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ba8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95ba8-106">Syntax</span></span>

<span data-ttu-id="95ba8-107">*expressão* . Conecte-se</span><span class="sxs-lookup"><span data-stu-id="95ba8-107">*expression* .Connect</span></span>

<span data-ttu-id="95ba8-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="95ba8-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ba8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="95ba8-109">Remarks</span></span>

<span data-ttu-id="95ba8-p102">A configuração da propriedade **Connect** é uma **String** composta por um especificador de tipo de banco de dados e nenhum ou mais parâmetros separados por ponto-e-vírgula. A propriedade **Connect** transmite informações adicionais para o ODBC e certos drivers do ISAM, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="95ba8-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="95ba8-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="95ba8-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="95ba8-p103">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como os bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deve incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="95ba8-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="95ba8-115">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**. Em um espaço de trabalho ODBCDirect, somente o especificador "ODBC" pode ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="95ba8-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95ba8-116">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="95ba8-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="95ba8-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="95ba8-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="95ba8-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="95ba8-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-119">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="95ba8-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="95ba8-120">[database;]</span><span class="sxs-lookup"><span data-stu-id="95ba8-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="95ba8-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="95ba8-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="95ba8-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="95ba8-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="95ba8-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-124">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="95ba8-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="95ba8-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="95ba8-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-127">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="95ba8-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="95ba8-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="95ba8-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-130">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="95ba8-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="95ba8-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="95ba8-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-133">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="95ba8-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="95ba8-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="95ba8-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-136">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="95ba8-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="95ba8-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="95ba8-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-139">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="95ba8-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="95ba8-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="95ba8-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="95ba8-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="95ba8-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="95ba8-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="95ba8-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="95ba8-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="95ba8-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="95ba8-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="95ba8-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="95ba8-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="95ba8-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="95ba8-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="95ba8-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="95ba8-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-152">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="95ba8-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="95ba8-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="95ba8-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="95ba8-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="95ba8-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="95ba8-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="95ba8-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="95ba8-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="95ba8-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="95ba8-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="95ba8-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-160">drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="95ba8-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="95ba8-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="95ba8-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="95ba8-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="95ba8-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="95ba8-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="95ba8-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="95ba8-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-166">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-167">Texto</span><span class="sxs-lookup"><span data-stu-id="95ba8-167">Text</span></span></p></td>
<td><p><span data-ttu-id="95ba8-168">Texto;</span><span class="sxs-lookup"><span data-stu-id="95ba8-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="95ba8-169">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="95ba8-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95ba8-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="95ba8-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="95ba8-171">ODBC; Banco de dados = database; UID = user; PWD = password; DSN = datasourcename; [LOGINTIMEOUT = seconds;]</span><span class="sxs-lookup"><span data-stu-id="95ba8-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="95ba8-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="95ba8-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95ba8-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="95ba8-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="95ba8-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [Perfil = profile;] [PWD = password;] [Banco de dados = database;]</span><span class="sxs-lookup"><span data-stu-id="95ba8-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="95ba8-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="95ba8-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95ba8-176">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="95ba8-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="95ba8-177">Se uma senha for solicitada, mas não for fornecida na configuração da propriedade **Connect**, uma caixa de diálogo de login será exibida na primeira vez em que a tabela for acessada pelo driver ODBC e novamente se a conexão for fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="95ba8-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="95ba8-178">Para dados no Microsoft Exchange, a chave MAPILEVEL exigida deve estar definida como um caminho de pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="95ba8-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="95ba8-179">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome dessa pasta deve ser especificado como o argumento nome para o método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="95ba8-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="95ba8-180">A chave TABLETYPE deve estar definida como "0" para abrir a pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="95ba8-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="95ba8-181">A chave PROFILE é padronizada para o perfil atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="95ba8-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="95ba8-182">Você pode definir a propriedade **Connect** para um objeto de **banco de dados** , fornecendo um argumento de origem para o método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="95ba8-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="95ba8-183">Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="95ba8-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="95ba8-184">Você deve definir a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="95ba8-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="95ba8-185">Você deve ter permissão de acesso ao computador que contém o servidor de banco de dados que está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="95ba8-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


