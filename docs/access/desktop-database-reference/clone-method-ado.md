---
title: Método Clone-ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296343"
---
# <a name="clone-method-ado"></a>Método Clone (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um objeto [Recordset](recordset-object-ado.md) duplicado a partir de um objeto **Recordset** existente. Opcionalmente, especifica que o clone seja somente leitura.

## <a name="syntax"></a>Sintaxe

**Definir** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)

## <a name="return-value"></a>Valor de retorno

Retorna uma referência do objeto **Recordset**.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*rstDuplicate* |Uma variável de objeto que identifica o objeto **Recordset** duplicado a ser criado.|
|*rstOriginal* |Uma variável de objeto que identifica o objeto **Recordset** a ser duplicado.|
|*LockType* |Opcional. Um valor [LockTypeEnum](locktypeenum.md) que especifica o tipo de bloqueio do **Recordset** original ou um **Recordset** somente leitura. Os valores válidos são **adLockUnspecified** ou **adLockReadOnly**.|

## <a name="remarks"></a>Comentários

Utilize o método **Clone** para criar diversos objetos **Recordset** duplicados, especialmente se deseja manter mais de um registro atual em um determinado conjunto de registros. A utilização do método **Clone** é mais eficiente do que a criação e abertura de um novo objeto **Recordset** com a mesma definição que o original.

A propriedade [Filter](filter-property-ado.md) do **Recordset** original, se existir, não será aplicada ao clone. Defina a propriedade **Filter** do novo **Recordset** para filtrar os resultados. A forma mais simples de copiar qualquer valor de **Filter** existente é atribuí-lo diretamente, como a seguir:

O registro atual de um clone recém-criado é definido para o primeiro registro.

As alterações efetuadas em um objeto **Recordset** são visíveis em todos os seus clones, independentemente do tipo do cursor. No entanto, depois de executar [Requery](requery-method-ado.md) no **Recordset** original, os clones não mais estarão sincronizados com o original.

Fechar o **Recordset** original não fecha suas cópias, assim como fechar uma cópia não fecha o original e nenhuma das demais cópias.

É possível clonar apenas um objeto **Recordset** que suporte indicadores. Os valores de indicadores são intercambiáveis; isto é, uma referência de indicador de um objeto **Recordset** se refere ao mesmo registro em qualquer um de seus clones.

Alguns eventos **Recordset** que são disparados também o serão em todos os clones do **Recordset**. No entanto, como o registro atual pode ser diferente entre os **Recordsets** clonados, os eventos podem não ser válidos para o clone.

Por exemplo, se você alterar o valor de um campo, ocorrerá um evento [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) no **Recordset** alterado e em todos os clones. O parâmetro *Fields* do evento **WillChangeField** de um **Recordset** clonado (em que a alteração não foi feita) irá simplesmente se referir aos campos do registro atual do clone, que pode ser um registro diferente do registro atual do **Recordset** original onde a alteração ocorreu.

A tabela a seguir fornece uma lista completa de todos os eventos de **Recordset** e indica se eles são válidos e disparados para quaisquer clones de recordset gerados utilizando-se o método **Clone**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Evento</p></th>
<th><p>Disparado nos clones?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>Não</p></td>
</tr>
</tbody>
</table>

