---
title: Método Update (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306234"
---
# <a name="update-method-ado"></a>Método Update (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Salva quaisquer alterações feitas na linha atual de um objeto [Recordset](recordset-object-ado.md) ou na coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxe

*recordset*. Campos *de atualização,* *valores*

*registro*. *Campos*. Atualizar

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Fields* |Opcional. Uma **Variant** que representa um único nome, ou uma matriz **Variant** que representa nomes ou posições ordinais do campo ou campos que deseja modificar.|
|*Values* |Opcional. Uma **Variant** que representa um único valor, ou uma matriz **Variant** que representa valores para o campo ou campos no novo registro.|

## <a name="remarks"></a>Comentários

### <a name="recordset"></a>Recordset

Utilize o método **Update** para salvar quaisquer alterações feitas no registro atual de um objeto **Recordset** desde a chamada ao método [AddNew](addnew-method-ado.md) ou desde a alteração de quaisquer valores de campo em um registro existente. O objeto **Recordset** deve suportar atualizações.

Para definir valores de campos, execute um dos seguintes procedimentos:

- Atribua valores à propriedade [Value](field-object-ado.md) de um objeto [Field](value-property-ado.md) e chame o método **Update**.

- Passe o nome de um campo e um valor como argumentos com a chamada a **Update**.

- Passe uma matriz de nomes de campo e uma matriz de valores com a chamada a **Update**.

Ao utilizar matrizes de campos e valores, deve haver um número igual de elementos em ambas as matrizes. Além disso, a ordem dos nomes de campo deve corresponder à ordem dos valores de campo. Se o número e a ordem dos campos e valores não corresponder, ocorrerá um erro.

Se o objeto **Recordset** suportar atualização em lote, você poderá armazenar localmente em cache diversas alterações em um ou mais registros até chamar o método [UpdateBatch](updatebatch-method-ado.md). Se estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método **Update** para salvar quaisquer alterações pendentes no registro atual antes de transmitir as alterações em lote ao provedor.

Se você mover do registro que está adicionando ou editando antes de chamar o método **Update**, o ADO chamará **Update** automaticamente para salvar as alterações. Você deve chamar o método [CancelUpdate](cancelupdate-method-ado.md) se deseja cancelar quaisquer alterações feitas no registro atual ou descartar um registro recém-adicionado.

O registro atual permanece atual depois da chamada ao método **Update**.

### <a name="record"></a>Registro

O método **Update** finaliza adições, exclusões e atualizações de campos na coleção [Fields](fields-collection-ado.md) de um objeto **Record**.

Por exemplo, campos excluídos com o método **Delete** são marcados para exclusão imediatamente, mas permanecem na coleção. O método **Update** deve ser chamado para realmente excluir esses campos da coleção do provedor.

