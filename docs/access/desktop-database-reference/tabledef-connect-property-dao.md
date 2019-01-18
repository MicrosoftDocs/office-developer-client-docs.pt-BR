---
title: Propriedade TableDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722750"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="47a71-102">Propriedade TableDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="47a71-102">TableDef.Connect property (DAO)</span></span>

<span data-ttu-id="47a71-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="47a71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47a71-p101">Define ou retorna um valor que fornece informações sobre uma tabela vinculada. **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="47a71-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="47a71-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47a71-106">Syntax</span></span>

<span data-ttu-id="47a71-107">*expressão* . Conecte-se</span><span class="sxs-lookup"><span data-stu-id="47a71-107">*expression* .Connect</span></span>

<span data-ttu-id="47a71-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="47a71-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a71-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="47a71-109">Remarks</span></span>

<span data-ttu-id="47a71-p102">A definição da propriedade **Connect** é uma **String** composta de um especificador do tipo de banco de dados e zero ou mais parâmetros separados por ponto-e-vírgulas. A propriedade **Connect** passa informações adicionais para ODBC e determinados drivers ISAM conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="47a71-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="47a71-112">Para um objeto **TableDef** que representa uma tabela vinculada, a definição da propriedade **Connect** é composta de uma ou duas partes (um especificador do tipo do banco de dados e um caminho para o banco de dados), cada uma delas termina com um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="47a71-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="47a71-p103">O caminho, como mostrado na tabela a seguir, é um caminho completo para o diretório que contém os arquivos de banco de dados e deve ser precedido pelo identificador DATABASE=. Em alguns casos (como os bancos de dados do mecanismo de banco de dados do Microsoft Excel e do Microsoft Access), você deve incluir um nome de arquivo específico no argumento do caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47a71-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="47a71-115">A tabela a seguir mostra os tipos possíveis de bancos de dados e seus especificadores e caminhos correspondentes para a configuração da propriedade **Connect**. Em um espaço de trabalho ODBCDirect, somente o especificador "ODBC" pode ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="47a71-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47a71-116">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="47a71-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="47a71-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="47a71-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="47a71-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="47a71-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47a71-119">Banco de dados do Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="47a71-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="47a71-120">[database;]</span><span class="sxs-lookup"><span data-stu-id="47a71-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="47a71-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="47a71-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="47a71-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="47a71-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="47a71-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="47a71-124">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="47a71-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="47a71-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="47a71-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="47a71-127">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="47a71-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="47a71-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="47a71-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="47a71-130">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="47a71-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="47a71-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="47a71-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="47a71-133">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="47a71-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="47a71-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="47a71-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="47a71-136">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="47a71-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="47a71-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="47a71-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="47a71-139">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="47a71-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="47a71-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="47a71-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="47a71-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="47a71-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="47a71-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="47a71-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="47a71-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="47a71-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="47a71-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="47a71-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="47a71-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="47a71-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="47a71-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="47a71-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="47a71-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="47a71-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="47a71-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="47a71-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="47a71-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-152">Lotus 1-2-3 WKS e WK1</span><span class="sxs-lookup"><span data-stu-id="47a71-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="47a71-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="47a71-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="47a71-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="47a71-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="47a71-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="47a71-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="47a71-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="47a71-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="47a71-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="47a71-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="47a71-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="47a71-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="47a71-160">drive:\path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="47a71-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-161">HTML Import</span><span class="sxs-lookup"><span data-stu-id="47a71-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="47a71-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="47a71-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="47a71-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="47a71-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-164">HTML Export</span><span class="sxs-lookup"><span data-stu-id="47a71-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="47a71-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="47a71-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="47a71-166">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-167">Texto</span><span class="sxs-lookup"><span data-stu-id="47a71-167">Text</span></span></p></td>
<td><p><span data-ttu-id="47a71-168">Texto;</span><span class="sxs-lookup"><span data-stu-id="47a71-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="47a71-169">unidade: \path</span><span class="sxs-lookup"><span data-stu-id="47a71-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47a71-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="47a71-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="47a71-171">ODBC; Banco de dados = database; UID = user; PWD = password; DSN = datasourcename; [LOGINTIMEOUT = seconds;]</span><span class="sxs-lookup"><span data-stu-id="47a71-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="47a71-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="47a71-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47a71-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="47a71-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="47a71-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [Perfil = profile;] [PWD = password;] [Banco de dados = database;]</span><span class="sxs-lookup"><span data-stu-id="47a71-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="47a71-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="47a71-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47a71-176">Se uma senha for solicitada, mas não for fornecida na configuração da propriedade **Connect**, uma caixa de diálogo de login será exibida na primeira vez em que a tabela for acessada pelo driver ODBC e novamente se a conexão for fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="47a71-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="47a71-177">Para dados no Microsoft Exchange, a chave MAPILEVEL exigida deve estar definida como um caminho de pasta totalmente resolvido (por exemplo, "Mailbox - Pat SmithIAlpha/Today").</span><span class="sxs-lookup"><span data-stu-id="47a71-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="47a71-178">O caminho não inclui o nome da pasta que será aberta como uma tabela; em vez disso, o nome dessa pasta deve ser especificado como o argumento nome para o método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="47a71-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="47a71-179">A chave TABLETYPE deve estar definida como "0" para abrir a pasta (padrão) ou "1" para abrir um catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="47a71-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="47a71-180">A chave PROFILE é padronizada para o perfil atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="47a71-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="47a71-181">Para as tabelas base em um banco de dados do Microsoft Access, a definição da propriedade **Connect** será uma sequência de caracteres com comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="47a71-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="47a71-182">Defina a propriedade **Connect** antes de definir a propriedade **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="47a71-182">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="47a71-183">Você deve ter permissão de acesso ao computador que contém o servidor de banco de dados que está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="47a71-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>
