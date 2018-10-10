---
title: Método Resync (ADO)
TOCTitle: Resync Method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fc91be8b78ed7362029849dfb22a78d758c886e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463767"
---
# <a name="resync-method-ado"></a>Método Resync (ADO)


**Aplica-se a**: Access 2013 | Office 2013



Atualiza os dados no objeto [Recordset](recordset-object-ado.md) atual, ou a coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a partir do banco de dados subjacente.

## <a name="syntax"></a>Sintaxe

*Conjunto de registros*. Resync*AffectRecords*, *ResyncValues*

*Registro*. *Campos*. Resync*ResyncValues*

## <a name="parameters"></a>Parâmetros

  - *AffectRecords*

  - Opcional. Um valor [AffectEnum](affectenum.md) que determina a quantidade de registros que serão afetados pelo método **Resync**. O valor padrão é **adAffectAll**. Esse valor não está disponível com o método **Resync** da coleção **Fields** de um objeto **Record**.

  - *ResyncValues*

  - Opcional. Um valor [ResyncEnum](resyncenum.md) que especifica se os valores subjacentes serão substituídos. O valor padrão é **adResyncAllValues**.

## <a name="remarks"></a>Comentários

**Objeto Recordset**

Use o método **Resync** para sincronizar novamente os registros do **Recordset** atual com o banco de dados subjacente. Esse procedimento será útil se você estiver usando um cursor estático ou somente de encaminhamento e desejar ver as alterações no banco de dados subjacente.

Se você definir a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**, **Resync** somente estará disponível para os objetos **Recordset** que não sejam somente leitura.

Diferente do método [Requery](requery-method-ado.md), o método **Resync** não reexecuta o comando subjacente do objeto **Recordset**. Os novos registros no banco de dados subjacente não estarão visíveis.

Se a tentativa de nova sincronização falhar devido a um conflito com os dados subjacentes (por exemplo, por causa da exclusão de um registro por outro usuário), o provedor retornará avisos à coleção [Errors](errors-collection-ado.md) e ocorrerá um erro em tempo de execução. Use a propriedade [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.

Se as propriedades dinâmicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e [Resync Command](resync-command-property-dynamic-ado.md) forem definidas e **Recordset** resultar da execução de uma operação JOIN em várias tabelas, o método **Resync** executará o comando fornecido na propriedade **Resync Command** somente na tabela nomeada na propriedade **Unique Table**.

**Coleção Fields**

Use o método **Resync** para sincronizar novamente os valores da coleção **Fields** de um objeto **Record** com a fonte de dados subjacente. A propriedade [Count](count-property-ado.md) não é afetada por esse método.

Se *ResyncValues* for definido como **adResyncAllValues** (o valor padrão), as propriedades de [OriginalValue](originalvalue-property-ado.md) de objetos [Field](field-object-ado.md) na coleção, [valor](value-property-ado.md)e [UnderlyingValue](underlyingvalue-property-ado.md)são sincronizadas. Se *ResyncValues* for definido como **adResyncUnderlyingValues**, apenas a propriedade **UnderlyingValue** é sincronizada.

O valor da propriedade **Status** para cada objeto **Field** no momento da chamada também afeta o comportamento de **Resync**. **Resync** não terá efeito para os objetos **Field** com valor **adFieldPendingUnknown** ou **adFieldPendingInsert** para **Status**. Para o valor **adFieldPendingChange** ou **adFieldPendingDelete** de **Status**, **Resync** sincronizará os valores de dados dos campos ainda existentes na fonte de dados.

**Resync** não modificará os valores de **Status** dos objetos **Field**, a menos que ocorra um erro no momento em que ele for chamado. Por exemplo, se o campo não existir mais, o provedor retornará um valor de **Status** apropriado para o objeto **Field**, por exemplo, **adFieldDoesNotExist**. Os valores de **Status** retornados poderão ser combinados logicamente dentro do valor da propriedade **Status ******.

