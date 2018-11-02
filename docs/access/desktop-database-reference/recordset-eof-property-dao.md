---
title: Propriedade Recordset.EOF (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6fc6c304f427d4ee98f6c7c653cfd4da76c8cf96
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931050"
---
# <a name="recordseteof-property-dao"></a>Propriedade Recordset.EOF (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica se a posição atual do registro é após o último registro em um objeto **Recordset**. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . EOF

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Você pode usar as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao se mover de registro em registro.

A localização do ponteiro do registro atual determina os valores de retorno de **BOF** e **EOF**.

Se a propriedade **BOF** ou **EOF** for **Verdadeiro**, não haverá registro atual.

Se você abrir um objeto **Recordset** sem registros, as propriedades **BOF** e **EOF** serão definidas como **Verdadeiro** e a configuração da propriedade **RecordCount** do objeto **Recordset** será 0. Quando você abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **Falso**; elas permanecerão **Falso** até você se mover para além do início ou do fim do objeto **Recordset** usando o método **MovePrevious** ou **MoveNext**, respectivamente. Quando você se move além do início ou do fim do **Recordset**, não há registro atual ou não há registro algum.

Se você excluir o último registro restante do objeto **Recordset**, as propriedades **BOF** e **EOF** poderão permanecer **Falso** até você tentar reposicionar o registro atual.

Se você usar o método **MoveLast** em um objeto **Recordset** com registros, o último registro se tornará o registro atual; se você então usar o método **MoveNext**, o registro atual se tornará inválido e a propriedade **EOF** será definida como **Verdadeiro**. De modo inverso, se você usar o método **MoveFirst** em um objeto **Recordset** com registros, o primeiro registro se tornará o registro atual; se você então usar o método **MovePrevious**, não haverá registro atual e a propriedade **BOF** será definida como **Verdadeiro**.

Normalmente, quando você trabalhar com todos os registros em um objeto **Recordset**, seu código fará um loop pelos registros usando o método **MoveNext** até a propriedade **EOF** ser definida como **Verdadeiro**.

Se você usar o método **MoveNext** enquanto a propriedade **EOF** estiver definida como **Verdadeiro** ou o método **MovePrevious** enquanto a propriedade **BOF** estiver definida como **Verdadeiro**, ocorrerá um erro.

Esta tabela mostra quais métodos Move são permitidos com combinações diferentes das propriedades **BOF** e **EOF**.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>Métodos MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Mover &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Mover &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = verdadeiro,</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Erro</p></td>
<td><p>Erro</p></td>
<td><p>Permitido</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False,</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
<td><p>Erro</p></td>
<td><p>Erro</p></td>
</tr>
<tr class="odd">
<td><p>Ambas <strong>Verdadeiras</strong></p></td>
<td><p>Erro</p></td>
<td><p>Erro</p></td>
<td><p>Erro</p></td>
<td><p>Erro</p></td>
</tr>
<tr class="even">
<td><p>Ambas <strong>Falsas</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
<td><p>Permitido</p></td>
</tr>
</tbody>
</table>


Permitir um método Move significa que o método localizará com êxito um registro. Ele simplesmente indica que uma tentativa de executar o método Move especificado é permitida e não gerará um erro. O estado das propriedades **BOF** e **EOF** pode ser alterado como resultado da tentativa de Move.

Um método **OpenRecordset** invoca internamente um método **MoveFirst**. Portanto, usar um método **OpenRecordset** em um conjunto de registros vazio define as propriedades **BOF** e **EOF** como **Verdadeiras** (consulte a tabela a seguir par obter o comportamento de um método **MoveFirst** com falha).

Todos os métodos Move que localizam com êxito um registro definirão **BOF** e **EOF** como **Falso**.

Em um espaço de trabalho do Microsoft Access, se você adicionar um registro a um **Recordset** vazio, **BOF** se tornará **Falso**, mas **EOF** permanecerá **Verdadeiro**, indicando a posição atual no final do **Recordset**.

Qualquer método **Delete**, mesmo se remover somente o registro restante de um **Recordset**, não alterará a configuração da propriedade **BOF** ou **EOF**.

A tabela a seguir mostra como os métodos Move que não localizam um registro afetam as configurações das propriedades **BOF** e **EOF**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Métodos MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p><strong>Verdadeiro</strong></p></td>
<td><p><strong>Verdadeiro</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Nenhuma alteração</p></td>
<td><p>Nenhuma alteração</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>mova</strong> &lt; 0</p></td>
<td><p><strong>Verdadeiro</strong></p></td>
<td><p>Nenhuma alteração</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>mova</strong> &gt; 0</p></td>
<td><p>Nenhuma alteração</p></td>
<td><p><strong>Verdadeiro</strong></p></td>
</tr>
</tbody>
</table>

