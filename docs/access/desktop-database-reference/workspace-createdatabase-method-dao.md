---
title: Método Workspace.CreateDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6d271676ef91d29dca78ba9ee4b6142e055b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305863"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="caed2-102">Método Workspace.CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="caed2-102">Workspace.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="caed2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="caed2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="caed2-104">Cria um novo objeto **[Database](database-object-dao.md)**, salva o banco de dados no disco e retorna um objeto **Database** aberto (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="caed2-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="caed2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caed2-105">Syntax</span></span>

<span data-ttu-id="caed2-106">*expressão* . CreateDatabase(***Name***, ***Connect***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="caed2-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="caed2-107">*expressão* Uma variável que representa um objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="caed2-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="caed2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caed2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caed2-109">Nome</span><span class="sxs-lookup"><span data-stu-id="caed2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="caed2-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="caed2-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="caed2-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="caed2-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="caed2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="caed2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caed2-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="caed2-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="caed2-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="caed2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="caed2-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-116">Uma String com até 255 caracteres de comprimento que é o nome do arquivo de banco de dados que você está criando.</span><span class="sxs-lookup"><span data-stu-id="caed2-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="caed2-117">Ela pode ser o caminho completo e o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="caed2-117">It can be the full path and file name.</span></span> <span data-ttu-id="caed2-118">Se sua rede oferece suporte a ele, você também pode especificar um caminho de rede, como &quot; \\ server1\share1\dir1\db1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="caed2-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="caed2-119">Você só pode criar arquivos de bancos de dados do Microsoft Access com esse método.</span><span class="sxs-lookup"><span data-stu-id="caed2-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-120"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="caed2-120"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="caed2-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="caed2-121">Required</span></span></p></td>
<td><p><span data-ttu-id="caed2-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="caed2-p102">Uma expressão de cadeia de caracteres que especifica uma ordem de agrupamento para criar o banco de dados, conforme especificado em Configurações. Você deve fornecer esse argumento ou um erro ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="caed2-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="caed2-125">Você também pode criar uma senha para o novo objeto <strong>Database</strong> concatenando a cadeia de caracteres de senha (começando com ;p wd= ) com uma constante no argumento &quot; &quot; <em>local,</em> como esta:</span><span class="sxs-lookup"><span data-stu-id="caed2-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="caed2-126">dbLangSpanish &amp; &quot; ;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="caed2-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="caed2-127">Se desejar usar o <em>local</em> padrão, mas especificar uma senha, simplesmente digite uma cadeia de caracteres como senha para o argumento <em>local</em>:</span><span class="sxs-lookup"><span data-stu-id="caed2-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="caed2-128">&quot;;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="caed2-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="caed2-p103">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="caed2-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-134"><em>Opção</em></span><span class="sxs-lookup"><span data-stu-id="caed2-134"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="caed2-135">Opcional</span><span class="sxs-lookup"><span data-stu-id="caed2-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="caed2-136"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-p104">Uma constante ou combinação de constantes que indica uma ou mais opções, conforme especificado em Configurações. Você pode combinar opções associando as constantes correspondentes.</span><span class="sxs-lookup"><span data-stu-id="caed2-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="caed2-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="caed2-139">Remarks</span></span>

<span data-ttu-id="caed2-140">Você pode usar uma das seguintes constantes para o argumento locale a fim de especificar a propriedade [CollatingOrder](database-collatingorder-property-dao.md) do texto para comparações de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="caed2-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caed2-141">Constante</span><span class="sxs-lookup"><span data-stu-id="caed2-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="caed2-142">Ordem de agrupamento</span><span class="sxs-lookup"><span data-stu-id="caed2-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caed2-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-144">Inglês, francês, alemão, português, italiano e espanhol moderno</span><span class="sxs-lookup"><span data-stu-id="caed2-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-146">Árabe</span><span class="sxs-lookup"><span data-stu-id="caed2-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-148">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="caed2-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-150">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="caed2-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-152">Russo</span><span class="sxs-lookup"><span data-stu-id="caed2-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-154">Tcheco</span><span class="sxs-lookup"><span data-stu-id="caed2-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-156">Holandês</span><span class="sxs-lookup"><span data-stu-id="caed2-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-158">Grego</span><span class="sxs-lookup"><span data-stu-id="caed2-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-160">Hebraico</span><span class="sxs-lookup"><span data-stu-id="caed2-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-162">Húngaro</span><span class="sxs-lookup"><span data-stu-id="caed2-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-164">Islandês</span><span class="sxs-lookup"><span data-stu-id="caed2-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-166">Japonês</span><span class="sxs-lookup"><span data-stu-id="caed2-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-168">Coreano</span><span class="sxs-lookup"><span data-stu-id="caed2-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-170">Idiomas nórdicos (apenas mecanismo de banco de dados do Microsoft Jet versão 1.0)</span><span class="sxs-lookup"><span data-stu-id="caed2-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-172">Norueguês e dinamarquês</span><span class="sxs-lookup"><span data-stu-id="caed2-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-174">Polonês</span><span class="sxs-lookup"><span data-stu-id="caed2-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-176">Esloveno</span><span class="sxs-lookup"><span data-stu-id="caed2-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-178">Espanhol tradicional</span><span class="sxs-lookup"><span data-stu-id="caed2-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-180">Sueco e finlandês</span><span class="sxs-lookup"><span data-stu-id="caed2-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-182">Tailandês</span><span class="sxs-lookup"><span data-stu-id="caed2-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-184">Turco</span><span class="sxs-lookup"><span data-stu-id="caed2-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="caed2-185">Você pode usar uma ou mais das seguintes constantes no argumento options para especificar que versão o formato dos dados deve ter e se o banco de dados deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="caed2-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caed2-186">Constante</span><span class="sxs-lookup"><span data-stu-id="caed2-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="caed2-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="caed2-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caed2-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-189">Cria um banco de dados criptografado.</span><span class="sxs-lookup"><span data-stu-id="caed2-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-191">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.0.</span><span class="sxs-lookup"><span data-stu-id="caed2-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-193">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.1.</span><span class="sxs-lookup"><span data-stu-id="caed2-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-195">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 2.0.</span><span class="sxs-lookup"><span data-stu-id="caed2-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-197">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 3.0 (compatível com a versão 3.5).</span><span class="sxs-lookup"><span data-stu-id="caed2-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caed2-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-199">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="caed2-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caed2-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="caed2-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="caed2-201">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Access versão 12.0.</span><span class="sxs-lookup"><span data-stu-id="caed2-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="caed2-202">Se você omitir a constante de criptografia, **CreateDatabase** criará um banco de dados não criptografado.</span><span class="sxs-lookup"><span data-stu-id="caed2-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="caed2-p105">Use o método **CreateDatabase** para criar e abrir um banco de dados novo e vazio e retornar o objeto **Database**. Você deve completar sua estrutura e seu conteúdo utilizando objetos DAO adicionais. Se você quiser fazer uma cópia parcial ou completa de um banco de dados existente, poderá usar o método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para fazer uma cópia que pode ser personalizada.</span><span class="sxs-lookup"><span data-stu-id="caed2-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="caed2-206">Exemplo</span><span class="sxs-lookup"><span data-stu-id="caed2-206">Example</span></span>

<span data-ttu-id="caed2-207">Este exemplo usa o **CreateDatabase** para criar um objeto **Database** novo e criptografado.</span><span class="sxs-lookup"><span data-stu-id="caed2-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
