---
title: O que há de novo no ActiveX Data Objects (ADO)
TOCTitle: What's New in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86d3c151ac77ab4138afcd84ee2a14d94dd07aef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462937"
---
# <a name="whats-new-in-ado"></a>O que há de novo no ADO


**Aplica-se a**: Access 2013 | Office 2013 
 

Os novos recursos a seguir e a documentação aperfeiçoada foram incluídos no ADO versão 2.5. A lista abrange o ADO, o ADO MD e o ADOX.

## <a name="new-features"></a>Novos recursos

**[Objetos Record e Stream](chapter-10-records-and-streams.md)**

Esta versão do ADO introduz o objeto [Record](record-object-ado.md), que pode representar e gerenciar itens, como diretórios e arquivos em um sistema de arquivos, bem como pastas e mensagens em um sistema de email. Um **Record** também pode representar uma linha em um [Recordset](recordset-object-ado.md), embora os objetos **Record** e **Recordset** tenham métodos e propriedades diferentes.

O novo objeto [Stream](stream-object-ado.md) permite ler, gravar e gerenciar o fluxo binário de bytes ou o texto que abrange um fluxo de arquivo ou de mensagem.

**[Uso de URL](absolute-and-relative-urls.md)**

Esta versão também introduz o uso de URLs, uma alternativa para sequências de conexão e texto de comando, para nomear objetos de repositório de dados. As URLs podem ser usadas com os objetos [Connection](connection-object-ado.md) e **Recordset** existentes, e também com os novos objetos **Record** e **Stream**.

Com esta versão, o ADO oferece suporte a provedores OLE DB que reconhecem seus próprios esquemas URL. Por exemplo, o [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* que acessa o sistema de arquivos do Windows 2000, reconhece o esquema HTTP existente.

**[Campos especiais para provedores de fonte de documentos](records-and-provider-supplied-fields.md)**

Uma classe especial de provedores, chamado provedores de *documento de origem* , gerenciar pastas e documentos. Quando um objeto **Record** representa um documento, ou um objeto **Recordset** representa uma pasta de documentos, o provedor de fonte de documentos preenche esses objetos com um conjunto exclusivo de campos que descrevem as características do documento. Esses campos constituem um *recurso* de **registro** ou **Recordset**.

## <a name="new-reference-topics"></a>Novos tópicos de referência

As novas propriedades a seguir foram incluídas nesta versão.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="charset-property-ado.md">Charset</a></p></td>
<td><p>Indica o conjunto de caracteres no qual o conteúdo de um objeto <strong>Stream</strong> de texto deve ser convertido.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Indica se a posição atual está no final do fluxo.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Indica o caractere binário a ser usado como o separador de linha nos objetos <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Indica as permissões disponíveis para modificar os dados em um objeto <strong>Connection</strong>, <strong>Record</strong> ou <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Indica uma sequência de URL absoluta que aponta para o <strong>Record</strong> pai do objeto <strong>Record</strong> atual.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Indica a posição atual em um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Indica o tipo de objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></p></td>
<td><p>Indica o tamanho do fluxo em número de bytes.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Origem</a></p></td>
<td><p>Indica a entidade representada pelo objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">Estado</a></p></td>
<td><p>Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado. Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Tipo</a></p></td>
<td><p>Indica o tipo de dados contido no objeto <strong>Stream</strong> (binário ou de texto).</p></td>
</tr>
</tbody>
</table>


Os novos métodos a seguir foram incluídos nesta versão.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copia um arquivo ou um diretório, e seu conteúdo, para outro local.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copia o número especificado de caracteres ou bytes (dependendo do <strong>tipo</strong>) no <strong>objeto</strong> <strong>Stream</strong> para outro objeto <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">ExcluirRegistro</a></p></td>
<td><p>Exclui um arquivo ou um diretório e todos os respectivos subdiretórios.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Liberar</a></p></td>
<td><p>Força o conteúdo do objeto <strong>Stream</strong> restante no buffer do ADO para o objeto subjacente ao qual o objeto <strong>Stream</strong> está associado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Retorna um <strong>Recordset</strong> cujas linhas representam os arquivos e os subdiretórios no diretório representado por este <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Carrega o conteúdo de um arquivo existente para um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Move um arquivo, ou um diretório e seu conteúdo, para outro local.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">Open</a></p></td>
<td><p>Abre um objeto <strong>Record</strong> existente ou cria um novo arquivo ou diretório.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
<td><p>Abre um objeto <strong>Stream</strong> para manipular fluxos de dados de texto ou binários.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lê um número de bytes especificado de um objeto <strong>Stream</strong> binário.</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lê o número de caracteres especificado de um objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Salva o conteúdo binário de um <strong>Stream</strong> para um arquivo.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Define a posição que é o final do fluxo.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Ignora uma linha inteira na leitura de um objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Gravação</a></p></td>
<td><p>Grava dados binários em um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Grava uma sequência de texto especificada em um objeto <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Nova documentação aprimorada

**[Tópicos de exemplo de código](ado-code-examples.md)**

Os exemplos aumentaram para incluir exemplos de código escritos em Microsoft Visual C++® e em Microsoft Visual J++®. Você pode copiar e colar esses exemplos de código em seu editor.

**[Tópicos sobre provedor](appendix-a-providers.md)**

Um novo tópico foi incluído e explica como usar o ADO com o [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).

**[Programando com o ADO](appendix-c-programming-with-ado.md)**

Esta nova seção contém dicas e truques para o uso do ADO com diversas linguagens de programação. Ela contém os índices de sintaxe existentes para as extensões do Visual C++ para ADO e o ADO/WFC, além de novas informações específicas aos desenvolvedores que utilizam Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++ ou Microsoft Visual J++.

