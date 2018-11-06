---
title: Método DBEngine.CreateDatabase (DAO)
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
ms.openlocfilehash: e9c77eabfc0689c6696c4ea6c8b4998b6b345458
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998347"
---
# <a name="dbenginecreatedatabase-method-dao"></a>Método DBEngine.CreateDatabase (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Cria um novo objeto **[Database](database-object-dao.md)**, salva o banco de dados no disco e retorna um objeto **Database** aberto (apenas espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . CreateDatabase (***nome***, a ***localidade***, ***opção***)

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Nome</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>Uma cadeia de caracteres até 255 caracteres que é o nome do arquivo de banco de dados que você está criando. Pode ser o nome de arquivo e caminho completo. Se sua rede oferecer suporte a ele, você pode também especificar um caminho de rede, tais como &quot; \\server1\share1\dir1\db1&quot;. Você só pode criar arquivos de banco de dados do Microsoft Access com este método.</p></td>
</tr>
<tr class="even">
<td><p><em>Localidade</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><ul>
<li><p>Uma expressão de cadeia de caracteres que especifica uma ordem de agrupamento para criar o banco de dados, conforme especificado em Configurações. Você deve fornecer esse argumento ou um erro ocorrerá.</p></li>
<li><p>Você também pode criar uma senha para o novo objeto <strong>Database</strong> concatenando a cadeia de caracteres de senha (começando com &quot;; pwd =&quot; ) com uma constante no argumento <em>locale</em> , semelhante a esta:</p></li>
<li><p>dbLangSpanish &amp; &quot;; pwd = novasenha&quot;</p></li>
<li><p>Se desejar usar o <em>local</em> padrão, mas especificar uma senha, simplesmente digite uma cadeia de caracteres como senha para o argumento <em>local</em>:</p></li>
<li><p>&quot;; pwd = novasenha&quot;</p></li>
<li><p>[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Opção</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante ou combinação de constantes que indica uma ou mais opções, conforme especificado em Configurações. Você pode combinar opções associando as constantes correspondentes.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar uma das seguintes constantes para o argumento locale a fim de especificar a propriedade **[CollatingOrder](database-collatingorder-property-dao.md)** do texto para comparações de cadeias de caracteres.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Ordem de agrupamento</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Inglês, alemão, francês, português, italiano e espanhol moderno</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>Árabe</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>Chinês simplificado</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Chinês tradicional</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>Russo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>Tcheco</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>Holandês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>Grego</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>Hebraico</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>Húngaro</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Islandês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>Japonês</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>Coreano</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Idiomas nórdicos (apenas mecanismo de banco de dados do Microsoft Jet versão 1.0)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Norueguês e dinamarquês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>Polonês</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>Esloveno</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Espanhol tradicional</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Sueco e finlandês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>Tailandês</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>Turco</p></td>
</tr>
</tbody>
</table>


Você pode usar uma ou mais das seguintes constantes no argumento options para especificar que versão o formato dos dados deve ter e se o banco de dados deve ser criptografado ou não.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Cria um banco de dados criptografado.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.1.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 2.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 3.0 (compatível com a versão 3.5).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 4.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Access versão 12.0.</p></td>
</tr>
</tbody>
</table>


Se você omitir a constante de criptografia, **CreateDatabase** criará um banco de dados não criptografado.

Use o método **CreateDatabase** para criar e abrir um banco de dados novo e vazio e retornar o objeto **Database**. Você deve completar sua estrutura e seu conteúdo usando objetos DAO adicionais. Se desejar fazer uma cópia completa ou parcial de um banco de dados existente, você pode usar o método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para fazer uma cópia que possa personalizar.

