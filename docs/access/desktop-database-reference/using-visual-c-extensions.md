---
title: Usando as extensões do Visual C++
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0076eae8a930688219da413a31d73a376bc53a39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464835"
---
# <a name="using-visual-c-extensions"></a>Usando as extensões do Visual C++


**Aplica-se a**: Access 2013 | Office 2013

## <a name="the-iadorecordbinding-interface"></a>A interface IADORecordBinding

As extensões do Microsoft Visual C++ para ADO associam, ou acoplam, os campos de um objeto [Recordset](recordset-object-ado.md) às variáveis C/C++. Sempre que a linha atual do **Recordset** acoplado é alterada, todos os campos acoplados no **Recordset** são copiados para essas variáveis. Se necessário, os dados copiados são convertidos no tipo de dados declarado da variável C/C++.

O método **BindToRecordset** da interface **IADORecordBinding** acopla campos às variáveis C/C++. O método **AddNew** adiciona uma nova linha ao **Recordset** acoplado. O método **Update** preenche os campos nas novas linhas de **Recordset** ou atualiza os campos nas linhas existentes, com o valor das variáveis C/C++.

A interface **IADORecordBinding** é implementada pelo objeto **Recordset**. Não é possível codificar a implementação sozinho.

## <a name="binding-entries"></a>Entradas de ligação

As extensões do Visual C++ para ADO mapeiam os campos de um objeto [Recordset](recordset-object-ado.md) para as variáveis C/C++. A definição de um mapeamento entre um campo e uma variável é chamada *entrada de ligação*. As macros fornecem entradas de ligação para dados numéricos de tamanhos fixo e variável. As entradas de ligação e as variáveis C/C++ são declaradas em uma classe derivada da classe **CADORecordBinding** de extensões do Visual C++. A classe **CADORecordBinding** é definida internamente pelas macros de entrada de ligação.

O ADO mapeia internamente os parâmetros nessas macros para uma estrutura **DBBINDING** do OLE DB e cria um objeto **Accessor** do OLE DB para gerenciar o movimento e a conversão de dados entre campos e variáveis. O OLE DB define os dados em três partes: um *buffer* para repositório dos dados; um *status* que indica se um campo foi armazenado com êxito no buffer, ou como a variável deve ser restaurada para o campo; e o *comprimento* dos dados. (Para obter mais informações, consulte *OLE DB Programmer's Reference*, capítulo 6: Getting and Setting Data [em inglês].)

## <a name="header-file"></a>Arquivo de cabeçalho

Inclua o arquivo a seguir em seu aplicativo para usar as extensões do Visual C++ para ADO:

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Acoplando campos de Recordset

**Para acoplar campos de Recordset às variáveis C/C++**

1.  Crie uma classe derivada da classe **CADORecordBinding**.

2.  Especifique as entradas de ligação e as variáveis C/C++ correspondentes na classe derivada. Colchete as entradas de ligação entre **começar\_ADO\_VINCULAÇÃO** e **END\_ADO\_VINCULAÇÃO** macros. Não termine as macros com vírgula ou ponto-e-vírgula. Delimitadores apropriados são especificados automaticamente por cada macro. Especifique uma entrada de ligação para cada campo a ser mapeado para uma variável C/C++. Use um membro apropriado do **ADO\_def\_comprimento\_entrada**, **ADO\_numéricos\_entrada**, ou **ADO\_VARIÁVEL\_comprimento\_entrada** família de macros.

3.  No seu aplicativo, crie uma instância da classe derivada de **CADORecordBinding**. Obtenha a interface **IADORecordBinding** de **Recordset**. Em seguida, chame o método **BindToRecordset** para acoplar os campos **Recordset** às variáveis C/C++.

Consulte o [Exemplo de extensões do Visual C++](visual-c-extensions-example.md) para obter mais informações.

## <a name="interface-methods"></a>Métodos de interface

A interface **IADORecordBinding** possui três métodos: **BindToRecordset**, **AddNew** e **Update**. O único argumento de cada método é um ponteiro para uma instância da classe derivada de **CADORecordBinding**. Portanto, os métodos **AddNew** e **Update** não podem especificar nenhum parâmetro de seus homônimos de método ADO.

**Sintaxe**

O método **BindToRecordset** associa os campos **Recordset** às variáveis C/C++.

`BindToRecordset(CADORecordBinding *binding)` 

O método **AddNew** chama seu homônimo, o método ADO [AddNew](addnew-method-ado.md), para adicionar uma nova linha a **Recordset**.

`AddNew(CADORecordBinding *binding)` 

O método **Update** chama seu homônimo, o método ADO [Update](update-method-ado.md), para atualizar o **Recordset**.

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>Macros de entrada de ligação

As macros de entrada de ligação definem a associação de um campo **Recordset** e uma variável. Uma macro inicial e uma macro final delimitam o conjunto de entradas de ligação.

As famílias de macros são fornecidas para dados de comprimento fixo, como **adDate** ou **adBoolean**; dados numéricos, como **adTinyInt**, **adInteger** ou **adDouble**; e dados de comprimento variável, como **adChar**, **adVarChar** ou **adVarBinary**. Todos os tipos numéricos, exceto **adVarNumeric**, também são tipos de comprimento fixo. Cada família possui conjuntos de parâmetros diferentes, o que permite excluir as informações de ligação que não sejam de seu interesse.

Consulte os tipos de dados *OLE DB referência do programador,* apêndice a: para obter informações adicionais.

_**Início das entradas de ligação**_

**COMEÇAR\_ADO\_ASSOCIANDO**(*classe*)

_**Dados de comprimento fixo**_

**ADO\_def\_comprimento\_entrada**(*Ordinal, DataType, Buffer, Status, modificar*)  
**ADO\_def\_comprimento\_Entrada2**(*Ordinal, DataType, Buffer, modificar*)

_**Dados numéricos**_

**ADO\_numéricos\_entrada**(*Ordinal, DataType, Buffer, precisão, escala, Status, modificar*)  
**ADO\_numéricos\_Entrada2**(*Ordinal, DataType, Buffer, precisão, escala, modificar*)

_**Dados de comprimento variável**_

**ADO\_VARIÁVEL\_comprimento\_entrada**(*Ordinal, DataType, Buffer, tamanho, Status, comprimento, modificar*)  
**ADO\_VARIÁVEL\_comprimento\_Entrada2**(*Ordinal, DataType, Buffer, tamanho, Status, modificar*)  
**ADO\_VARIÁVEL\_comprimento\_Entrada3**(*Ordinal, DataType, Buffer, tamanho, comprimento, modificar*)  
**ADO\_VARIÁVEL\_comprimento\_Entrada4**(*Ordinal, DataType, Buffer, tamanho, modificar*)

_**Final das entradas de ligação**_

**END\_ADO\_ASSOCIANDO** ()

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parâmetro</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Classe</em></p></td>
<td><p>Classe na qual são definidas as entradas de ligação e as variáveis C/C++.</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>Número ordinal, contado a partir de um, do campo <strong>Recordset</strong> correspondente a sua variável C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>Tipo de dados ADO equivalente da variável C/C++ (consulte <a href="datatypeenum.md">DataTypeEnum</a> para obter uma lista de tipos de dados válidos). Se necessário, o valor do campo <strong>Recordset</strong> será convertido nesse tipo de dados.</p></td>
</tr>
<tr class="even">
<td><p><em>Buffer</em></p></td>
<td><p>Nome da variável C/C++ de repositório do campo <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Tamanho máximo, em bytes, de <em>Buffer</em>. Se <em>Buffer</em> contiver uma sequência de caracteres de comprimento variável, deixe espaço para um zero de terminação.</p></td>
</tr>
<tr class="even">
<td><p><em>Status</em></p></td>
<td><p>Nome de uma variável que indicará se o conteúdo de <em>Buffer</em> é válido e se a conversão do campo em <em>DataType</em> foi bem-sucedida.
 Os dois valores mais importantes dessa variável são <strong>adFldOK</strong>, indicando que a conversão foi bem-sucedida; e <strong>adFldNull</strong>, indicando que o valor do campo será um VARIANT de tipo VT_NULL, e não simplesmente vazio. Os valores possíveis para <em>Status</em> estão listados na tabela a seguir, &quot;valores de Status.&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modificar</em></p></td>
<td><p>Sinalizador booleano; se for TRUE, indicará que o ADO tem permissão para atualizar o campo <strong>Recordset</strong> correspondente com o valor contido em <em>Buffer</em>.
 Defina o parâmetro booleano <em>modify</em> como TRUE para permitir que o ADO atualize o campo acoplado e como FALSE se desejar examinar o campo, mas sem alterá-lo.</p></td>
</tr>
<tr class="even">
<td><p><em>Precisão</em></p></td>
<td><p>Número de dígitos que podem ser representados em uma variável numérica.</p></td>
</tr>
<tr class="odd">
<td><p><em>Escala</em></p></td>
<td><p>Número de casas decimais em uma variável numérica.</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p>Nome de uma variável de quatro bytes que conterá o comprimento real dos dados em <em>Buffer</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Valores de status

O valor da variável *Status* indica se um campo foi copiado com êxito a uma variável.

Ao configurar os dados, defina *Status* como **adFldNull** para indicar que o campo **Recordset** seja definido como nulo.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Um valor de campo não-nulo foi retornado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldBadAccessor</strong></p></td>
<td><p>1</p></td>
<td><p>A ligação era inválida.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>O valor não pôde ser convertido devido a razões diferentes de incompatibilidade de sinal ou estouro de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>3</p></td>
<td><p>Quando um campo é obtido, indica que um valor nulo foi retornado.
 Na configuração de um campo, indica que o campo deve ser definido como <strong>NULL</strong> quando ele não puder codificar o próprio <strong>NULL</strong> (por exemplo, uma matriz de caracteres ou um número inteiro).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>Os dados de comprimento variável ou os dígitos numéricos foram truncados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>O valor tem sinal e o tipo de dados variáveis não.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldDataOverFlow</strong></p></td>
<td><p>6</p></td>
<td><p>O valor é maior do que pôde ser armazenado no tipo de dados variáveis.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldCantCreate</strong></p></td>
<td><p>7</p></td>
<td><p>Tipo de coluna desconhecida e campo já aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>Não foi possível determinar o valor de campo — por exemplo, em um novo campo sem alocação sem nenhum valor padrão.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>Durante uma atualização, não houve permissão para gravar dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Durante uma atualização, o valor de campo violaria a integridade da coluna.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Durante uma atualização, o valor de campo violaria o esquema de coluna.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>Durante uma atualização, um parâmetro de status inválido foi retornado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Durante uma atualização, um valor padrão foi utilizado.</p></td>
</tr>
</tbody>
</table>
