---
title: Propriedade Database.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ccc238940ec75b04cf900fbc6604df7b41d2ca4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462721"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="c0cda-102">Propriedade Database.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0cda-102">Database.Connect Property (DAO)</span></span>


<span data-ttu-id="c0cda-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0cda-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c0cda-p101">Define ou retorna um valor que fornece informações sobre a origem de um banco de dados aberto. **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c0cda-p101">Sets or returns a value that provides information about the source an open database. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cda-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0cda-106">Syntax</span></span>

<span data-ttu-id="c0cda-107">*expressão* . Conecte-se</span><span class="sxs-lookup"><span data-stu-id="c0cda-107">*expression* .Connect</span></span>

<span data-ttu-id="c0cda-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="c0cda-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0cda-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0cda-109">Remarks</span></span>

<span data-ttu-id="c0cda-p102">A configuração da propriedade **Connect** é uma **String** composta por um especificador de tipo de banco de dados e nenhum ou mais parâmetros separados por ponto-e-vírgula. A propriedade **Connect** transmite informações adicionais para o ODBC e certos drivers do ISAM, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c0cda-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="c0cda-112">Para executar uma consulta passagem SQL em uma tabela vinculada ao arquivo de banco de dados do Microsoft Access, você deve primeiro definir a propriedade **Connect** do banco de dados da tabela vinculada para uma sequência de conexão ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="c0cda-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="c0cda-p103">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como os bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deve incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c0cda-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="c0cda-115">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**. Em um espaço de trabalho ODBCDirect, somente o especificador "ODBC" pode ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="c0cda-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0cda-116">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="c0cda-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="c0cda-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="c0cda-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="c0cda-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c0cda-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-119">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="c0cda-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="c0cda-120">[database;]</span><span class="sxs-lookup"><span data-stu-id="c0cda-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="c0cda-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="c0cda-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="c0cda-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="c0cda-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="c0cda-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-124">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="c0cda-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="c0cda-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="c0cda-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-127">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="c0cda-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="c0cda-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="c0cda-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-130">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="c0cda-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="c0cda-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="c0cda-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-133">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="c0cda-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="c0cda-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="c0cda-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-136">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="c0cda-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="c0cda-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="c0cda-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-139">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="c0cda-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="c0cda-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="c0cda-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="c0cda-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="c0cda-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="c0cda-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="c0cda-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="c0cda-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="c0cda-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="c0cda-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="c0cda-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="c0cda-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="c0cda-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="c0cda-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="c0cda-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="c0cda-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-152">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="c0cda-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="c0cda-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="c0cda-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="c0cda-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="c0cda-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="c0cda-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="c0cda-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="c0cda-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="c0cda-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="c0cda-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="c0cda-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-160">drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="c0cda-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="c0cda-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="c0cda-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="c0cda-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="c0cda-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="c0cda-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="c0cda-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="c0cda-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-166">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-167">Texto</span><span class="sxs-lookup"><span data-stu-id="c0cda-167">Text</span></span></p></td>
<td><p><span data-ttu-id="c0cda-168">Texto;</span><span class="sxs-lookup"><span data-stu-id="c0cda-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="c0cda-169">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="c0cda-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0cda-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="c0cda-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="c0cda-171">ODBC; Banco de dados = database; UID = user; PWD = password; DSN = datasourcename; [LOGINTIMEOUT = seconds;]</span><span class="sxs-lookup"><span data-stu-id="c0cda-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="c0cda-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c0cda-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0cda-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="c0cda-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="c0cda-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [Perfil = profile;] [PWD = password;] [Banco de dados = database;]</span><span class="sxs-lookup"><span data-stu-id="c0cda-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="c0cda-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="c0cda-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0cda-176">Se o especificador for apenas "ODBC;", o driver ODBC exibirá uma caixa de diálogo listando todos os nomes registrados de fonte de dados ODBC para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c0cda-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="c0cda-177">Se uma senha for solicitada, mas não for fornecida na configuração da propriedade **Connect**, uma caixa de diálogo de login será exibida na primeira vez em que a tabela for acessada pelo driver ODBC e novamente se a conexão for fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="c0cda-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="c0cda-178">Para dados no Microsoft Exchange, a chave MAPILEVEL exigida deve estar definida como um caminho de pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="c0cda-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="c0cda-179">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome dessa pasta deve ser especificado como o argumento nome para o método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="c0cda-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="c0cda-180">A chave TABLETYPE deve estar definida como "0" para abrir a pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="c0cda-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="c0cda-181">A chave PROFILE é padronizada para o perfil atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="c0cda-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="c0cda-182">Você pode definir a propriedade **Connect** para um objeto de **banco de dados** , fornecendo um argumento de origem para o método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="c0cda-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="c0cda-183">Você pode verificar a configuração para determinar o tipo, o caminho, a identificação do usuário, a senha ou a fonte de dados ODBC do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c0cda-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="c0cda-184">Você deve definir a propriedade <STRONG>Connect</STRONG> antes de definir a propriedade <STRONG>ReturnsRecords</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c0cda-184">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="c0cda-185">Você deve ter permissão de acesso ao computador que contém o servidor de banco de dados que está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="c0cda-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


