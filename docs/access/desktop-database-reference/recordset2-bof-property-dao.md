---
title: Propriedade Recordset2.BOF (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f68d14d4da0c1bd416deff5077588108281c4f87
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462496"
---
# <a name="recordset2bof-property-dao"></a>Propriedade Recordset2.BOF (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna um valor que indica se a posição do registro atual é antes do primeiro registro em um objeto **Recordset**. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . BOF

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Você pode usar as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao se mover de registro em registro.

A localização do ponteiro do registro atual determina os valores de retorno de **BOF** e **EOF**.

Se a propriedade **BOF** ou **EOF** for **True**, não existirá um registro atual.

Se você abrir um objeto **Recordset** que não contenha registros, as propriedades **BOF** e **EOF** estarão definidas como **True** e a propriedade **RecordCount** do objeto **Recordset** estará definida como 0. Quando você abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **False**; essas propriedades permanecerão como **False** até que você se mova além do início ou do final do objeto **Recordset** por meio do método **MovePrevious** ou **MoveNext**, respectivamente. Quando você se mover além do início ou do final do conjunto de registros, não existirá nenhum registro incluindo o registro atual .

Se você excluir o último registro do objeto **Recordset**, as propriedades **BOF** e **EOF** permanecerão como **False** até você tentar o reposicionamento do registro atual.

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

Todos os métodos Move localizados com sucesso em um registro definirão as propriedades **BOF** e **EOF** como **False**.

Em umespaço de trabalho do Microsoft Access, se você adicionar um registro a um conjunto de registros vazio, **BOF** se tornará **False**, mas **EOF** permanecerá **True**, indicando que a posição atual é o final do conjunto de registros.

Qualquer método **Delete**, mesmo que remova somente o registro restante de um conjunto de registros, não alterará a definição da propriedade **BOF** ou **EOF**.

A tabela a seguir mostra como os métodos Move que não localizam um registro afetam as definições das propriedades **BOF** e **EOF**.

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

