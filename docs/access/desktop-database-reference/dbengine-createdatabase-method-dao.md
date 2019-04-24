---
title: Método DBEngine. createDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 13e41dcd182f720b3611108311db6cd56fb4847e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294362"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="80370-102">Método DBEngine. createDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="80370-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="80370-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80370-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80370-104">Cria um novo objeto **[Database](database-object-dao.md)**, salva o banco de dados no disco e retorna um objeto **Database** aberto (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="80370-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="80370-105">.</span><span class="sxs-lookup"><span data-stu-id="80370-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="80370-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80370-106">Syntax</span></span>

<span data-ttu-id="80370-107">*expressão* . CreateDatabase (***nome***, ***localidade***, ***opção***)</span><span class="sxs-lookup"><span data-stu-id="80370-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="80370-108">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="80370-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="80370-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80370-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80370-110">Nome</span><span class="sxs-lookup"><span data-stu-id="80370-110">Name</span></span></p></th>
<th><p><span data-ttu-id="80370-111">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="80370-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="80370-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="80370-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="80370-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="80370-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80370-114"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="80370-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="80370-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="80370-115">Required</span></span></p></td>
<td><p><span data-ttu-id="80370-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="80370-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-117">Uma String com até 255 caracteres de comprimento que é o nome do arquivo de banco de dados que você está criando.</span><span class="sxs-lookup"><span data-stu-id="80370-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="80370-118">Ela pode ser o caminho completo e o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="80370-118">It can be the full path and file name.</span></span> <span data-ttu-id="80370-119">Se sua rede oferecer suporte a ele, você também poderá especificar um caminho de rede &quot; \\,&quot;como server1\share1\dir1\db1.</span><span class="sxs-lookup"><span data-stu-id="80370-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="80370-120">Você só pode criar arquivos de bancos de dados do Microsoft Access com esse método.</span><span class="sxs-lookup"><span data-stu-id="80370-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-121"><em>LCID</em></span><span class="sxs-lookup"><span data-stu-id="80370-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="80370-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="80370-122">Required</span></span></p></td>
<td><p><span data-ttu-id="80370-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="80370-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="80370-p103">Uma expressão de cadeia de caracteres que especifica uma ordem de agrupamento para criar o banco de dados, conforme especificado em Configurações. Você deve fornecer esse argumento ou um erro ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="80370-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="80370-126">Você também pode criar uma senha para o novo objeto <strong>Database</strong> concatenando a cadeia de caracteres da senha ( &quot;começando com;p&quot; WD =) com uma constante no argumento <em>locale</em> , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="80370-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="80370-127">dbLangSpanish &amp; &quot;;p wd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="80370-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="80370-128">Se desejar usar o <em>local</em> padrão, mas especificar uma senha, simplesmente digite uma cadeia de caracteres como senha para o argumento <em>local</em>:</span><span class="sxs-lookup"><span data-stu-id="80370-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="80370-129">&quot;;p WD = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="80370-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="80370-p104">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="80370-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-135"><em>Opção</em></span><span class="sxs-lookup"><span data-stu-id="80370-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="80370-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="80370-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="80370-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="80370-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-p105">Uma constante ou combinação de constantes que indica uma ou mais opções, conforme especificado em Configurações. Você pode combinar opções associando as constantes correspondentes.</span><span class="sxs-lookup"><span data-stu-id="80370-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="80370-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="80370-140">Remarks</span></span>

<span data-ttu-id="80370-141">Você pode usar uma das seguintes constantes para o argumento locale a fim de especificar a propriedade **[CollatingOrder](database-collatingorder-property-dao.md)** do texto para comparações de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="80370-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80370-142">Constant</span><span class="sxs-lookup"><span data-stu-id="80370-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="80370-143">Ordem de agrupamento</span><span class="sxs-lookup"><span data-stu-id="80370-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80370-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="80370-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-145">Inglês, francês, alemão, português, italiano e espanhol moderno</span><span class="sxs-lookup"><span data-stu-id="80370-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="80370-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-147">Árabe</span><span class="sxs-lookup"><span data-stu-id="80370-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="80370-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-149">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="80370-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="80370-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-151">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="80370-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="80370-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-153">Russo</span><span class="sxs-lookup"><span data-stu-id="80370-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="80370-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-155">Tcheco</span><span class="sxs-lookup"><span data-stu-id="80370-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="80370-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-157">Holandês</span><span class="sxs-lookup"><span data-stu-id="80370-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="80370-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-159">Grego</span><span class="sxs-lookup"><span data-stu-id="80370-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="80370-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-161">Hebraico</span><span class="sxs-lookup"><span data-stu-id="80370-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="80370-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-163">Húngaro</span><span class="sxs-lookup"><span data-stu-id="80370-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="80370-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-165">Islandês</span><span class="sxs-lookup"><span data-stu-id="80370-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="80370-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-167">Japonês</span><span class="sxs-lookup"><span data-stu-id="80370-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="80370-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-169">Coreano</span><span class="sxs-lookup"><span data-stu-id="80370-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="80370-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-171">Idiomas nórdicos (apenas mecanismo de banco de dados do Microsoft Jet versão 1.0)</span><span class="sxs-lookup"><span data-stu-id="80370-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="80370-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-173">Norueguês e dinamarquês</span><span class="sxs-lookup"><span data-stu-id="80370-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="80370-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-175">Polonês</span><span class="sxs-lookup"><span data-stu-id="80370-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="80370-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-177">Esloveno</span><span class="sxs-lookup"><span data-stu-id="80370-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="80370-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-179">Espanhol tradicional</span><span class="sxs-lookup"><span data-stu-id="80370-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="80370-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-181">Sueco e finlandês</span><span class="sxs-lookup"><span data-stu-id="80370-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="80370-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-183">Tailandês</span><span class="sxs-lookup"><span data-stu-id="80370-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="80370-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-185">Turco</span><span class="sxs-lookup"><span data-stu-id="80370-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80370-186">Você pode usar uma ou mais das seguintes constantes no argumento options para especificar que versão o formato dos dados deve ter e se o banco de dados deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="80370-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80370-187">Constante</span><span class="sxs-lookup"><span data-stu-id="80370-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="80370-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="80370-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80370-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="80370-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-190">Cria um banco de dados criptografado.</span><span class="sxs-lookup"><span data-stu-id="80370-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="80370-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-192">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.0.</span><span class="sxs-lookup"><span data-stu-id="80370-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="80370-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-194">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.1.</span><span class="sxs-lookup"><span data-stu-id="80370-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="80370-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-196">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 2.0.</span><span class="sxs-lookup"><span data-stu-id="80370-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="80370-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-198">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 3.0 (compatível com a versão 3.5).</span><span class="sxs-lookup"><span data-stu-id="80370-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80370-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="80370-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-200">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="80370-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80370-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="80370-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="80370-202">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Access versão 12.0.</span><span class="sxs-lookup"><span data-stu-id="80370-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80370-203">Se você omitir a constante de criptografia, **CreateDatabase** criará um banco de dados não criptografado.</span><span class="sxs-lookup"><span data-stu-id="80370-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="80370-p106">Use o método **CreateDatabase** para criar e abrir um banco de dados novo e vazio e retornar o objeto **Database**. Você deve completar sua estrutura e seu conteúdo usando objetos DAO adicionais. Se desejar fazer uma cópia completa ou parcial de um banco de dados existente, você pode usar o método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para fazer uma cópia que possa personalizar.</span><span class="sxs-lookup"><span data-stu-id="80370-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

