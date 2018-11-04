---
title: Método DBEngine.CompactDatabase (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: df7533376bf6f6d3c5387173a90c7d5e1a5013cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950041"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="b9b72-102">Método DBEngine.CompactDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9b72-102">DBEngine.CompactDatabase method (DAO)</span></span>

<span data-ttu-id="b9b72-103">**Aplica-se a**: Access 2013 | Acesso 2016</span><span class="sxs-lookup"><span data-stu-id="b9b72-103">**Applies to**: Access 2013 | Access 2016</span></span>

<span data-ttu-id="b9b72-104">Copia e compacta um banco de dados fechado e oferece a opção de alterar sua versão, ordem de agrupamento e criptografia.</span><span class="sxs-lookup"><span data-stu-id="b9b72-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="b9b72-105">(apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b9b72-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="b9b72-106">Ao usar as tabelas vinculadas criptografadas para ação, atualizar e consultas SQL [como uma instrução UPDATE do SQL (CurrentDb.Execute "Atualizar …")], você deve fornecer a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b9b72-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="b9b72-107">Além disso, as tabelas vinculadas tem um limite de caracteres 19 da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b9b72-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="b9b72-108">Consulte a seção **tabelas vinculadas do criptografadas** no final deste tópico.</span><span class="sxs-lookup"><span data-stu-id="b9b72-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b72-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9b72-109">Syntax</span></span>

<span data-ttu-id="b9b72-110">*expressão* . CompactDatabase (***SrcName***, ***DstName***, ***DstLocale***, ***Opções***, ***senha***)</span><span class="sxs-lookup"><span data-stu-id="b9b72-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="b9b72-111">*expressão* Uma expressão que retorna um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b9b72-111">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9b72-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9b72-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b72-113">Nome</span><span class="sxs-lookup"><span data-stu-id="b9b72-113">Name</span></span></p></th>
<th><p><span data-ttu-id="b9b72-114">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="b9b72-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b9b72-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b9b72-115">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b9b72-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9b72-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-117"><em>SrcName</em></span><span class="sxs-lookup"><span data-stu-id="b9b72-117"><em>SrcName</em></span></span></p></td>
<td><p><span data-ttu-id="b9b72-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b9b72-118">Required</span></span></p></td>
<td><p><span data-ttu-id="b9b72-119"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-120">Identifica um banco de dados existente, fechado.</span><span class="sxs-lookup"><span data-stu-id="b9b72-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="b9b72-121">Ele pode ser um caminho completo e nome de arquivo, como &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="b9b72-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="b9b72-122">Se o nome do arquivo tiver uma extensão, você deve especificá-lo.</span><span class="sxs-lookup"><span data-stu-id="b9b72-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="b9b72-123">Se sua rede oferecer suporte a ele, você pode também especificar um caminho de rede, tais como &quot; \\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="b9b72-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-124"><em>DstName</em></span><span class="sxs-lookup"><span data-stu-id="b9b72-124"><em>DstName</em></span></span></p></td>
<td><p><span data-ttu-id="b9b72-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b9b72-125">Required</span></span></p></td>
<td><p><span data-ttu-id="b9b72-126"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-127">o nome do arquivo (e caminho) do banco de dados compactado que você está criando.</span><span class="sxs-lookup"><span data-stu-id="b9b72-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="b9b72-128">Você também pode especificar um caminho de rede.</span><span class="sxs-lookup"><span data-stu-id="b9b72-128">You can also specify a network path.</span></span> <span data-ttu-id="b9b72-129">Você não pode usar esse argumento para especificar o mesmo arquivo de banco de dados srcname.</span><span class="sxs-lookup"><span data-stu-id="b9b72-129">You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-130"><em>DstLocale</em></span><span class="sxs-lookup"><span data-stu-id="b9b72-130"><em>DstLocale</em></span></span></p></td>
<td><p><span data-ttu-id="b9b72-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="b9b72-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9b72-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-133">Uma expressão de cadeia de caracteres que especifica uma ordem de agrupamento para criar DstName, conforme especificado em Comentários.</span><span class="sxs-lookup"><span data-stu-id="b9b72-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="b9b72-134">Se você omitir esse argumento, o local de DstName será o mesmo de SrcName.</span><span class="sxs-lookup"><span data-stu-id="b9b72-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="b9b72-135">Você também pode criar uma senha para DstName concatenando a cadeia de caracteres de senha (começando com &quot;; pwd =&quot;) com uma constante no argumento DstLocale, semelhante a esta: dbLangSpanish &amp; &quot;; pwd = novasenha&quot;.</span><span class="sxs-lookup"><span data-stu-id="b9b72-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="b9b72-136">Se você quiser usar o mesmo DstLocale como SrcName (o valor padrão), mas especificar uma nova senha, simplesmente digite uma cadeia de caracteres de senha para DstLocale: &quot;; pwd = novasenha&quot;</span><span class="sxs-lookup"><span data-stu-id="b9b72-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-137"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="b9b72-137"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="b9b72-138">Opcional</span><span class="sxs-lookup"><span data-stu-id="b9b72-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9b72-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-p105">Opcional. Uma constante ou combinação de constantes que indica uma ou mais opções, conforme especificado em Comentários. Você pode combinar opções associando as constantes correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b9b72-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-143"><em>senha</em></span><span class="sxs-lookup"><span data-stu-id="b9b72-143"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="b9b72-144">Opcional</span><span class="sxs-lookup"><span data-stu-id="b9b72-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9b72-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-146">Uma expressão de cadeia de caracteres que contém uma chave de criptografia, se o banco de dados é criptografado.</span><span class="sxs-lookup"><span data-stu-id="b9b72-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="b9b72-147">A cadeia de caracteres &quot;; pwd =&quot; devem preceder a senha real.</span><span class="sxs-lookup"><span data-stu-id="b9b72-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="b9b72-148">Se você incluir uma configuração de senha em DstLocale, essa configuração será ignorada.</span><span class="sxs-lookup"><span data-stu-id="b9b72-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p><p><span data-ttu-id="b9b72-149"><strong>Observação</strong>: Este é o parâmetro preterido e não é suportado no. Formato ACCDB.</span><span class="sxs-lookup"><span data-stu-id="b9b72-149"><strong>NOTE</strong>: This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="b9b72-150">Para criptografar uma. Arquivo ACCDB, use o "pwd =" cadeia de caracteres de opção.</span><span class="sxs-lookup"><span data-stu-id="b9b72-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="b9b72-151">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos.</span><span class="sxs-lookup"><span data-stu-id="b9b72-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="b9b72-152">As senhas fracas não combinam esses elementos.</span><span class="sxs-lookup"><span data-stu-id="b9b72-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="b9b72-153">Senha forte: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="b9b72-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="b9b72-154">Senha fraca: House27.</span><span class="sxs-lookup"><span data-stu-id="b9b72-154">Weak password: House27.</span></span> <span data-ttu-id="b9b72-155">Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="b9b72-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b9b72-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9b72-156">Remarks</span></span>

<span data-ttu-id="b9b72-157">Você pode usar uma das seguintes constantes para o argumento DstLocale a fim de especificar a propriedade **CollatingOrder** para comparações de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b9b72-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b72-158">Constante</span><span class="sxs-lookup"><span data-stu-id="b9b72-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="b9b72-159">Ordem de agrupamento</span><span class="sxs-lookup"><span data-stu-id="b9b72-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-161">Inglês, alemão, francês, português, italiano e espanhol moderno</span><span class="sxs-lookup"><span data-stu-id="b9b72-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-163">Árabe</span><span class="sxs-lookup"><span data-stu-id="b9b72-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-165">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="b9b72-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-167">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="b9b72-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-169">Russo</span><span class="sxs-lookup"><span data-stu-id="b9b72-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-171">Tcheco</span><span class="sxs-lookup"><span data-stu-id="b9b72-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-173">Holandês</span><span class="sxs-lookup"><span data-stu-id="b9b72-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-175">Grego</span><span class="sxs-lookup"><span data-stu-id="b9b72-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-177">Hebraico</span><span class="sxs-lookup"><span data-stu-id="b9b72-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-179">Húngaro</span><span class="sxs-lookup"><span data-stu-id="b9b72-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-181">Islandês</span><span class="sxs-lookup"><span data-stu-id="b9b72-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-183">Japonês</span><span class="sxs-lookup"><span data-stu-id="b9b72-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-185">Coreano</span><span class="sxs-lookup"><span data-stu-id="b9b72-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-187">Idiomas nórdicos (apenas mecanismo de banco de dados do Microsoft Jet versão 1.0)</span><span class="sxs-lookup"><span data-stu-id="b9b72-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-189">Norueguês e dinamarquês</span><span class="sxs-lookup"><span data-stu-id="b9b72-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-191">Polonês</span><span class="sxs-lookup"><span data-stu-id="b9b72-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-193">Esloveno</span><span class="sxs-lookup"><span data-stu-id="b9b72-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-195">Espanhol tradicional</span><span class="sxs-lookup"><span data-stu-id="b9b72-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-197">Sueco e finlandês</span><span class="sxs-lookup"><span data-stu-id="b9b72-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-199">Tailandês</span><span class="sxs-lookup"><span data-stu-id="b9b72-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-201">Turco</span><span class="sxs-lookup"><span data-stu-id="b9b72-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b9b72-202">Você pode usar uma das seguintes constantes no argumento options para especificar se o banco de dados será criptografado ou descriptografado durante sua compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="b9b72-203">As constantes dbEncrypt e dbDecrypt são preteridos e não são suportados no. Formatos de arquivo ACCDB.</span><span class="sxs-lookup"><span data-stu-id="b9b72-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b72-204">Constant</span><span class="sxs-lookup"><span data-stu-id="b9b72-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="b9b72-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9b72-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-207">Criptografa o banco de dados durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-209">Descriptografa o banco de dados durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b9b72-210">Se você omitir uma constante de criptografia ou se incluir tanto **dbDecrypt** como **dbEncrypt**, o DstName terá a mesma criptografia de srcname.</span><span class="sxs-lookup"><span data-stu-id="b9b72-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="b9b72-p108">Você pode usar uma das seguintes constantes no argumento options para especificar a versão do formato dos dados para o banco de dados compactado. Essa constante afeta apenas a versão do formato dos dados de DstName e não afeta a versão de objetos definidos pelo Microsoft Access, como formulários e relatórios.</span><span class="sxs-lookup"><span data-stu-id="b9b72-p108">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database. This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b72-213">Constant</span><span class="sxs-lookup"><span data-stu-id="b9b72-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="b9b72-214">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9b72-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-216">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.0 durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-218">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.1 durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-220">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 2.0 durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-222">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 3.0 (compatível com a versão 3.5) durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b72-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-224">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 4.0 durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b72-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="b9b72-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b72-226">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Access versão 12.0 durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="b9b72-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b9b72-227">Você pode especificar apenas uma constante de versão.</span><span class="sxs-lookup"><span data-stu-id="b9b72-227">You can specify only one version constant.</span></span> <span data-ttu-id="b9b72-228">Se você omitir uma constante de versão, o DstName terá a mesma versão srcname.</span><span class="sxs-lookup"><span data-stu-id="b9b72-228">If you omit a version constant, DstName will have the same version as SrcName.</span></span> <span data-ttu-id="b9b72-229">Você pode compactar DstName apenas para uma versão que é o mesmo ou posterior de SrcName.</span><span class="sxs-lookup"><span data-stu-id="b9b72-229">You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="b9b72-p110">À medida que você altera dados em um banco de dados, o arquivo do banco de dados pode se fragmentar e usar mais espaço em disco do que o necessário. Periodicamente, você pode usar o método **CompactDatabase** para compactar seu banco de dados para desfragmentar o arquivo do banco de dados. O banco de dados compactado é geralmente menor e com frequência é executado mais rapidamente. Também é possível alterar a ordem de agrupamento, a criptografia ou a versão do formato de dados enquanto copia ou compacta o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b9b72-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="b9b72-234">Você deve fechar SrcName antes de fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="b9b72-234">You must close SrcName before you compact it.</span></span> <span data-ttu-id="b9b72-235">Em um ambiente multiusuário, outros usuários não podem ter SrcName abrir enquanto você estiver compactando-lo.</span><span class="sxs-lookup"><span data-stu-id="b9b72-235">In a multiuser environment, other users can't have SrcName open while you're compacting it.</span></span> <span data-ttu-id="b9b72-236">Se SrcName não estiver fechado ou não está disponível para uso exclusivo, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="b9b72-236">If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="b9b72-237">Como **CompactDatabase** cria uma cópia do banco de dados, é preciso ter espaço em disco suficiente tanto para o banco de dados original como para o duplicado.</span><span class="sxs-lookup"><span data-stu-id="b9b72-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="b9b72-238">A operação de compactação falhará se não houver espaço em disco suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="b9b72-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="b9b72-239">O banco de dados duplicado DstName não tem que estar no mesmo disco srcname.</span><span class="sxs-lookup"><span data-stu-id="b9b72-239">The DstName duplicate database doesn't have to be on the same disk as SrcName.</span></span> <span data-ttu-id="b9b72-240">Após a compactação de um banco de dados com êxito, você pode exclua o arquivo de SrcName e renomeie o arquivo compactado de DstName ao nome do arquivo original.</span><span class="sxs-lookup"><span data-stu-id="b9b72-240">After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="b9b72-241">O método **CompactDatabase** copia todos os dados e as configurações de permissão de segurança do banco de dados especificado por SrcName para o banco de dados especificado por DstName.</span><span class="sxs-lookup"><span data-stu-id="b9b72-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="b9b72-242">[!OBSERVAçãO] Como o método **CompactDatabase** não converte objetos do Microsoft Access, você não deve usar **CompactDatabase** para converter um banco de dados que contém esses objetos.</span><span class="sxs-lookup"><span data-stu-id="b9b72-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="b9b72-243">Tabelas vinculadas criptografadas</span><span class="sxs-lookup"><span data-stu-id="b9b72-243">Encrypted linked tables</span></span>

<span data-ttu-id="b9b72-244">Senhas criptografadas dependem do formato de arquivo do banco de dados que você está usando.</span><span class="sxs-lookup"><span data-stu-id="b9b72-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="b9b72-245">Se você estiver usando um banco de dados anterior ou o Access 2003 (. mdb), você terá uma senha para proteger o banco de dados e uma senha separada para criptografar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b9b72-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="b9b72-246">Para Access 2007 (. accdb) e posteriores bancos de dados (. mdb), a única opção é criptografar e proteger o banco de dados com uma senha, como optar por ter duas senhas separadas foi removido.</span><span class="sxs-lookup"><span data-stu-id="b9b72-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="b9b72-247">Bancos de dados do Access 2007 (. accdb), a senha é a chave de criptografia</span><span class="sxs-lookup"><span data-stu-id="b9b72-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="b9b72-248">Você pode usar o seguinte exemplo de código VBA para um botão de comando:</span><span class="sxs-lookup"><span data-stu-id="b9b72-248">You can use the following example VBA code for a command button:</span></span>

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

<span data-ttu-id="b9b72-249">O exemplo de código a seguir mostra como usar CompactDatabase com uma senha (chave de criptografia) e vincular a uma tabela no banco de dados compactado.</span><span class="sxs-lookup"><span data-stu-id="b9b72-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="b9b72-250">Observe que uma senha deve ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="b9b72-250">Note that a password must be supplied.</span></span>

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
