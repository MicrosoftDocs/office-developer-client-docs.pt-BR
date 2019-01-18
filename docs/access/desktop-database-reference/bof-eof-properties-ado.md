---
title: Propriedades BOF, EOF (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726124"
---
# <a name="bof-eof-properties-ado"></a>Propriedades BOF, EOF (ADO)


**Aplica-se a**: Access 2013, o Office 2013

**BOF**  Indica que a posição do registro atual é antes do primeiro registro em um objeto [Recordset](recordset-object-ado.md).

**EOF**  Indica que a posição do registro atual é após o último registro em um objeto **Recordset**.

## <a name="return-value"></a>Valor de retorno

As propriedades **BOF** e **EOF** retornam valores **booleanos**.

## <a name="remarks"></a>Comentários

Use as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao passar de um registro para outro.

A propriedade **BOF** retorna **Verdadeiro** (-1) se a posição do registro atual for antes do primeiro registro e **Falso** (0) se a posição for no primeiro registro ou após ele.

A propriedade **EOF** retorna **Verdadeiro** se a posição do registro atual for após o último registro e **Falso** se a posição do registro atual for no último registro ou antes dele.

Se tanto a propriedade **BOF** como a **EOF** forem **Verdadeiras**, não existe registro atual.

Se você abrir um objeto **Recordset** sem nenhum registro, as propriedades **BOF** e **EOF** são configuradas como **Verdadeiro** (consulte a propriedade [RecordCount](recordcount-property-ado.md) para obter mais informações sobre esse estado de um **Recordset**). Quando você abre um objeto **Recordset** contendo ao menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** são **Falsas**.

Se você excluir o último registro restante do objeto **Recordset**, as propriedades **BOF** e **EOF** poderão permanecer **Falsas** até que você tente reposicionar o registro atual.

Esta tabela mostra quais métodos **Move** são permitidos com diferentes combinações das propriedades **BOF** e **EOF**.

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


A permissão para um método **Move** não garante que o método localizará com sucesso um registro; ela apenas significa que a chamada para o método **Move** especificado não resultará em erro.

A tabela a seguir mostra o que acontece às configurações de propriedade de **BOF** e **EOF** quando você chama diversos métodos **Move** mas não consegue localizar com sucesso um registro.

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
<td><p>Defina como <strong>True</strong></p></td>
<td><p>Defina como <strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Nenhuma alteração</p></td>
<td><p>Nenhuma alteração</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>mova</strong> &lt; 0</p></td>
<td><p>Configurada como <strong>Verdadeiro</strong></p></td>
<td><p>Nenhuma alteração</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>mova</strong> &gt; 0</p></td>
<td><p>Nenhuma alteração</p></td>
<td><p>Configurada como <strong>Verdadeiro</strong></p></td>
</tr>
</tbody>
</table>

