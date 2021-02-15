---
title: Propriedade Recordset.BOF (DAO)
TOCTitle: BOF Property
ms:assetid: c50a0c5f-1b26-33ea-4cf2-311f9514a94a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823092(v=office.15)
ms:contentKeyID: 48547603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: babd2351775a9a3cf3128a55627be291a29ea025
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300585"
---
# <a name="recordsetbof-property-dao"></a>Propriedade Recordset.BOF (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna um valor que indica se a posição atual do registro será antes do primeiro registro em um objeto **Recordset**. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . BOF

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Você pode usar as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao se mover de registro em registro.

O local do ponteiro do registro atual determina os valores de retorno **BOF** e **EOF**.

Se a propriedade **BOF** ou **EOF** for **True**, não existirá um registro atual.

Se você abrir um objeto **Recordset** que não contenha registros, as propriedades **BOF** e **EOF** estarão definidas como **True** e a definição da propriedade **RecordCount** do objeto **Recordset** será 0. Quando você abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **False**. Essas propriedades permanecerão como **False** até que você se mova além do início ou do final do objeto **Recordset** por meio do método **MovePrevious** ou **MoveNext**, respectivamente. Quando você se mover além do início ou do final do **Recordset**, não existirá nenhum registro, incluindo o registro atual .

Se você excluir o último registro do objeto **Recordset**, as propriedades **BOF** e **EOF** permanecerão como **False** até você tentar o reposicionamento do registro atual.

Se você usar o método **MoveLast** em um objeto **Recordset** que contenha registros, o último registro se tornará o registro atual; mais tarde, se você usar o método **MoveNext**, o registro atual se tornará inválido e a propriedade **EOF** será definida como **True**. De modo inverso, se você usar o método **MoveFirst** em um objeto **Recordset** que contenha registros, o primeiro registro se tornará o registro atual; mais tarde, se você usar o método **MovePrevious**, não existirá nenhum registro atual e a propriedade **BOF** será definida como **True**.

De um modo geral, quando você trabalhar com todos os registros em um objeto **Recordset**, o código fará um loop pelos registros usando o método **MoveNext** até que a propriedade **EOF** seja definida como **True**.

Se você usar o método **MoveNext** enquanto a propriedade **EOF** estiver definida como **True** ou o método **MovePrevious** enquanto a propriedade **BOF** estiver definida como **True**, ocorrerá um erro.

Esta tabela mostra quais métodos Move são permitidos com diferentes combinações das propriedades **BOF** e **EOF**.

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
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Move &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Move &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF=True,</strong><br />
<strong>EOF=False</strong></p></td>
<td><p>Permitido</p></td>
<td><p>Erro</p></td>
<td><p>Erro</p></td>
<td><p>Permitido</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF=False,</strong><br />
<strong>EOF=True</strong></p></td>
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

Um método **OpenRecordset** chama internamente um método **MoveFirst**. Por esse motivo, o uso de um método **OpenRecordset** em um conjunto de registros vazio definirá as propriedades **BOF** e **EOF** como **True**. (Consulte a tabela a seguir para conhecer o comportamento de um método **MoveFirst** com falha.)

Todos os métodos Move localizados com sucesso em um registro definirão as propriedades **BOF** e **EOF** como **False**.

Em um espaço de trabalho do Microsoft Access, se você adicionar um registro a um **Recordset** vazio, **BOF** se tornará **False**, mas **EOF** permanecerá **True**, indicando que a posição atual está no final do **Recordset**.

Qualquer método **Delete**, mesmo que remova somente o registro restante de um **Recordset**, não alterará a definição da propriedade **BOF** ou **EOF**.

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
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p><strong>Verdadeiro</strong></p></td>
<td><p><strong>Verdadeiro</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Sem alteração</p></td>
<td><p>Sem alteração</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p><strong>Verdadeiro</strong></p></td>
<td><p>Sem alteração</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Sem alteração</p></td>
<td><p><strong>Verdadeiro</strong></p></td>
</tr>
</tbody>
</table>

