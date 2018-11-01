---
title: Método Workspace.CreateDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ad3d44d67efb240cb97a5b4716e9e00a6951045
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875620"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="02038-102">Método Workspace.CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="02038-102">Workspace.CreateDatabase Method (DAO)</span></span>


<span data-ttu-id="02038-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="02038-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02038-104">Cria um novo objeto **[Database](database-object-dao.md)**, salva o banco de dados no disco e retorna um objeto **Database** aberto (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="02038-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="02038-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02038-105">Syntax</span></span>

<span data-ttu-id="02038-106">*expressão* . CreateDatabase (***nome***, ***Conectar***, ***opção***)</span><span class="sxs-lookup"><span data-stu-id="02038-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="02038-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="02038-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="02038-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02038-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02038-109">Nome</span><span class="sxs-lookup"><span data-stu-id="02038-109">Name</span></span></p></th>
<th><p><span data-ttu-id="02038-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="02038-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="02038-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="02038-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="02038-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="02038-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02038-113">Name</span><span class="sxs-lookup"><span data-stu-id="02038-113">Name</span></span></p></td>
<td><p><span data-ttu-id="02038-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02038-114">Required</span></span></p></td>
<td><p><span data-ttu-id="02038-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="02038-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-116">Uma cadeia de caracteres até 255 caracteres que é o nome do arquivo de banco de dados que você está criando.</span><span class="sxs-lookup"><span data-stu-id="02038-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="02038-117">Pode ser o nome de arquivo e caminho completo.</span><span class="sxs-lookup"><span data-stu-id="02038-117">It can be the full path and file name.</span></span> <span data-ttu-id="02038-118">Se sua rede oferecer suporte a ele, você pode também especificar um caminho de rede, tais como &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="02038-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="02038-119">Você só pode criar arquivos de banco de dados do Microsoft Access com este método.</span><span class="sxs-lookup"><span data-stu-id="02038-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-120">Connect</span><span class="sxs-lookup"><span data-stu-id="02038-120">Connect</span></span></p></td>
<td><p><span data-ttu-id="02038-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02038-121">Required</span></span></p></td>
<td><p><span data-ttu-id="02038-122"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="02038-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="02038-p102">Uma expressão de cadeia de caracteres que especifica uma ordem de agrupamento para criar o banco de dados, conforme especificado em Configurações. Você deve fornecer esse argumento ou um erro ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="02038-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="02038-125">Você também pode criar uma senha para o novo objeto <strong>Database</strong> concatenando a cadeia de caracteres de senha (começando com &quot;; pwd =&quot;) com uma constante no argumento <em>locale</em> , semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="02038-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="02038-126">dbLangSpanish &amp; &quot;; pwd = novasenha&quot;</span><span class="sxs-lookup"><span data-stu-id="02038-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="02038-127">Se desejar usar o <em>local</em> padrão, mas especificar uma senha, simplesmente digite uma cadeia de caracteres como senha para o argumento <em>local</em>:</span><span class="sxs-lookup"><span data-stu-id="02038-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="02038-128">&quot;; pwd = novasenha&quot;</span><span class="sxs-lookup"><span data-stu-id="02038-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="02038-p103">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="02038-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-134">Opção</span><span class="sxs-lookup"><span data-stu-id="02038-134">Option</span></span></p></td>
<td><p><span data-ttu-id="02038-135">Opcional</span><span class="sxs-lookup"><span data-stu-id="02038-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="02038-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="02038-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-p104">Uma constante ou combinação de constantes que indica uma ou mais opções, conforme especificado em Configurações. Você pode combinar opções associando as constantes correspondentes.</span><span class="sxs-lookup"><span data-stu-id="02038-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="02038-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="02038-139">Remarks</span></span>

<span data-ttu-id="02038-140">Você pode usar uma das seguintes constantes para o argumento locale a fim de especificar a propriedade [CollatingOrder](database-collatingorder-property-dao.md) do texto para comparações de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="02038-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02038-141">Constante</span><span class="sxs-lookup"><span data-stu-id="02038-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="02038-142">Ordem de agrupamento</span><span class="sxs-lookup"><span data-stu-id="02038-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02038-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="02038-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-144">Inglês, alemão, francês, português, italiano e espanhol moderno</span><span class="sxs-lookup"><span data-stu-id="02038-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="02038-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-146">Árabe</span><span class="sxs-lookup"><span data-stu-id="02038-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="02038-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-148">Chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="02038-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="02038-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-150">Chinês tradicional</span><span class="sxs-lookup"><span data-stu-id="02038-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="02038-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-152">Russo</span><span class="sxs-lookup"><span data-stu-id="02038-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="02038-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-154">Tcheco</span><span class="sxs-lookup"><span data-stu-id="02038-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="02038-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-156">Holandês</span><span class="sxs-lookup"><span data-stu-id="02038-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="02038-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-158">Grego</span><span class="sxs-lookup"><span data-stu-id="02038-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="02038-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-160">Hebraico</span><span class="sxs-lookup"><span data-stu-id="02038-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="02038-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-162">Húngaro</span><span class="sxs-lookup"><span data-stu-id="02038-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="02038-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-164">Islandês</span><span class="sxs-lookup"><span data-stu-id="02038-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="02038-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-166">Japonês</span><span class="sxs-lookup"><span data-stu-id="02038-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="02038-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-168">Coreano</span><span class="sxs-lookup"><span data-stu-id="02038-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="02038-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-170">Idiomas nórdicos (apenas mecanismo de banco de dados do Microsoft Jet versão 1.0)</span><span class="sxs-lookup"><span data-stu-id="02038-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="02038-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-172">Norueguês e dinamarquês</span><span class="sxs-lookup"><span data-stu-id="02038-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="02038-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-174">Polonês</span><span class="sxs-lookup"><span data-stu-id="02038-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="02038-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-176">Esloveno</span><span class="sxs-lookup"><span data-stu-id="02038-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="02038-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-178">Espanhol tradicional</span><span class="sxs-lookup"><span data-stu-id="02038-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="02038-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-180">Sueco e finlandês</span><span class="sxs-lookup"><span data-stu-id="02038-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="02038-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-182">Tailandês</span><span class="sxs-lookup"><span data-stu-id="02038-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="02038-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-184">Turco</span><span class="sxs-lookup"><span data-stu-id="02038-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02038-185">Você pode usar uma ou mais das seguintes constantes no argumento options para especificar que versão o formato dos dados deve ter e se o banco de dados deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="02038-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02038-186">Constant</span><span class="sxs-lookup"><span data-stu-id="02038-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="02038-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="02038-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02038-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="02038-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-189">Cria um banco de dados criptografado.</span><span class="sxs-lookup"><span data-stu-id="02038-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="02038-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-191">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.0.</span><span class="sxs-lookup"><span data-stu-id="02038-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="02038-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-193">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.1.</span><span class="sxs-lookup"><span data-stu-id="02038-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="02038-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-195">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 2.0.</span><span class="sxs-lookup"><span data-stu-id="02038-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="02038-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-197">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 3.0 (compatível com a versão 3.5).</span><span class="sxs-lookup"><span data-stu-id="02038-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02038-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="02038-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-199">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="02038-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02038-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="02038-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="02038-201">Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Access versão 12.0.</span><span class="sxs-lookup"><span data-stu-id="02038-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02038-202">Se você omitir a constante de criptografia, **CreateDatabase** criará um banco de dados não criptografado.</span><span class="sxs-lookup"><span data-stu-id="02038-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="02038-p105">Use o método **CreateDatabase** para criar e abrir um banco de dados novo e vazio e retornar o objeto **Database**. Você deve completar sua estrutura e seu conteúdo utilizando objetos DAO adicionais. Se você quiser fazer uma cópia parcial ou completa de um banco de dados existente, poderá usar o método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para fazer uma cópia que pode ser personalizada.</span><span class="sxs-lookup"><span data-stu-id="02038-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="02038-206">Exemplo</span><span class="sxs-lookup"><span data-stu-id="02038-206">Example</span></span>

<span data-ttu-id="02038-207">Este exemplo usa o **CreateDatabase** para criar um objeto **Database** novo e criptografado.</span><span class="sxs-lookup"><span data-stu-id="02038-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
