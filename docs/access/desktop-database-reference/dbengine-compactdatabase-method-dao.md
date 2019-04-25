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
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294334"
---
# <a name="dbenginecompactdatabase-method-dao"></a>Método DBEngine.CompactDatabase (DAO)

**Aplica-se ao**: Access 2013 | Access 2016

Copia e compacta um banco de dados fechado e dá a você a opção de alterar sua versão, ordem de agrupamento e criptografia. (Espaços de trabalho do Microsoft Access apenas).

> [!NOTE]
> Ao usar tabelas vinculadas criptografadas para ação e atualizar consultas SQL [como uma instrução SQL UPDATE (CurrentDb.Execute "UPDATE...")], você deverá fornecer a chave de criptografia. Além disso, as tabelas vinculadas têm um limite de 19 de caracteres para a chave de criptografia. Confira a seção **tabelas vinculadas criptografadas** no final deste tópico.

## <a name="syntax"></a>Sintaxe

*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)

*expressão* Uma expressão que retorna um objeto **DBEngine**.

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
<th><p>Necessário/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Identifica um banco de dados existente e fechado. Pode ser um caminho completo e o nome do arquivo, como &quot;C:\db1.mdb&quot;. Se o nome do arquivo possui uma extensão, você deve especificá-la. Se sua rede oferecer suporte, você também pode especificar um caminho de rede como &quot;\\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>o nome de arquivo (e o caminho) do banco de dados compactado que você está criando. Você também pode especificar um caminho de rede. Não é possível usar este argumento para especificar o mesmo arquivo de banco de dados como SrcName.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma expressão de cadeia de caracteres que especifica uma ordem de agrupamento para criar DstName, conforme especificado nos comentários.</p>
<ul>
<li><p>Se você omitir esse argumento, a localidade DstName é igual a SrcName.</p></li>
<li><p>Você também pode criar uma senha para DstName concatenando a cadeia de caracteres da senha (começando com &quot;;pwd=&quot;) com uma constante no argumento DstLocale, da seguinte forma: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</p></li>
<li><p>Se desejar usar o mesmo DstLocale como SrcName (o valor padrão), mas especificar uma nova senha, simplesmente digite uma cadeia de caracteres de senha para DstLocale: &quot;;pwd=NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Opções</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Opcional. Uma constante ou combinação de constantes que indica uma ou mais opções, conforme especificado em Comentários. Você pode combinar opções associando as constantes correspondentes.</p></td>
</tr>
<tr class="odd">
<td><p><em>senha</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma expressão de cadeia de caracteres com uma chave de criptografia, se o banco de dados é criptografado. A cadeia de caracteres &quot;;pwd =&quot; deve preceder a senha atual. Se você incluir uma configuração de senha DstLocale, essa configuração será ignorada.</p><p><strong>OBSERVAÇÃO</strong>:Esse é um parâmetro preterido e não tem suporte no formato .ACCDB. Para criptografar um arquivo .ACCDB, use a opção de cadeia de caracteres. "pwd =". Use senhas fortes que combinam letras maiúsculas e minúsculas, números e símbolos. As enhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: Casa27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar uma das seguintes constantes para o argumento DstLocale a fim de especificar a propriedade **CollatingOrder** do texto para comparações de cadeias de caracteres.

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
<td><p>Inglês, francês, alemão, português, italiano e espanhol moderno</p></td>
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

<br/>

Você pode usar uma das seguintes constantes no argumento options para especificar se o banco de dados será criptografado ou descriptografado durante sua compactação.

> [!NOTE]
> As constantes DbEncrypt e dbDecrypt são substituídas e não são suportadas pelos formatos de arquivo .ACCDB.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Criptografa o banco de dados durante a compactação.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>Descriptografe o banco de dados durante a compactação.</p></td>
</tr>
</tbody>
</table>

<br/>

Se você omitir uma constante de criptografia ou se incluir o **dbDecrypt** e o **dbEncrypt**, o DstName terá a mesma criptografia que o SrcName.

Você pode usar uma das seguintes constantes no argumento options para especificar a versão do formato dos dados para o banco de dados compactado. Essa constante afeta apenas a versão do formato dos dados de DstName e não afeta a versão de objetos definidos pelo Microsoft Access, como formulários e relatórios.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.0 durante a compactação.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 1.1 durante a compactação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 2.0 durante a compactação.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 3.0 (compatível com a versão 3.5) durante a compactação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo do mecanismo de banco de dados Microsoft Jet versão 4.0 durante a compactação.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Cria um banco de dados que usa o formato de arquivo da versão 12.0 do mecanismo do banco de dados do Microsoft Access durante a compactação.</p></td>
</tr>
</tbody>
</table>

<br/>

É possível especificar apenas uma constante de versão. Se você omitir uma constante de versão, o DstName terá a mesma versão do SrcName. Você pode compactar o DstName apenas para uma versão que seja igual ou posterior ao SrcName.

À medida que você altera dados em um banco de dados, o arquivo do banco de dados pode se fragmentar e usar mais espaço em disco do que o necessário. Periodicamente, você pode usar o método **CompactDatabase** para compactar seu banco de dados para desfragmentar o arquivo do banco de dados. O banco de dados compactado é geralmente menor e com frequência é executado mais rapidamente. Também é possível alterar a ordem de agrupamento, a criptografia ou a versão do formato de dados enquanto copia ou compacta o banco de dados.

Você deve fechar o SrcName antes de compactá-lo. Em um ambiente multiusuário, outros usuários não podem estar com o SrcName aberto enquanto você o estiver compactando. Se o SrcName não estiver fechado ou disponível para uso exclusivo, ocorrerá um erro.

Como **CompactDatabase** cria uma cópia do banco de dados, é preciso ter espaço em disco suficiente tanto para o banco de dados original como para o duplicado. A operação de compactação falhará se não houver espaço em disco suficiente disponível. O banco de dados DstName duplicado não precisa estar no mesmo disco que o SrcName. Depois de compactar com sucesso um banco de dados, você pode excluir o arquivo SrcName e renomear o arquivo DstName compactado com o nome do arquivo original.

O método **CompactDatabase** copia todos os dados e as configurações de permissão de segurança do banco de dados especificado por SrcName para o banco de dados especificado por DstName.

> [!NOTE]
> Como o método **CompactDatabase** não converte objetos do Microsoft Access, não use **CompactDatabase** para converter um banco de dados contendo esses objetos.

## <a name="encrypted-linked-tables"></a>Tabelas vinculadas criptografadas

Senhas criptografadas dependem do formato do arquivo do banco de dados que você está usando. Se você estiver usando um Access 2003 (.mdb) ou um banco de dados anterior, você terá uma senha para proteger o banco de dados e uma senha separada para criptografar o banco de dados. Para o Access 2007 (.accdb) e bancos de dados (.mdb) posteriores, a única opção é criptografar e proteger o banco de dados com uma senha, pois a opção para fazer duas senhas separadas foi removida.

> [!NOTE]
> Para bancos de dados do Access 2007 (.accdb), a senha é a chave de criptografia

Você pode usar o seguinte exemplo do código VBA para um botão de comando:

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

O exemplo de código a seguir mostra como usar o CompactDatabase com uma senha (chave de criptografia) e vincular a uma tabela no banco de dados compactado. Observe que uma senha deve ser fornecida.

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
