---
title: Método Update (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0a62618eef0a829db84de050aa07c2c645636e5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929430"
---
# <a name="update-method-ado"></a>Método Update (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Salva quaisquer alterações feitas na linha atual de um objeto [Recordset](recordset-object-ado.md) ou na coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. Atualizar*campos*, *valores*

*registro*. *Campos*. Atualização

## <a name="parameters"></a>Parâmetros

  - *Fields*

  - Opcional. Uma **Variant** que representa um único nome, ou uma matriz **Variant** que representa nomes ou posições ordinais do campo ou campos que deseja modificar.

  - *Values*

  - Opcional. Uma **Variant** que representa um único valor, ou uma matriz **Variant** que representa valores para o campo ou campos no novo registro.

## <a name="remarks"></a>Comentários

**Recordset**

Utilize o método **Update** para salvar quaisquer alterações feitas no registro atual de um objeto **Recordset** desde a chamada ao método [AddNew](addnew-method-ado.md) ou desde a alteração de quaisquer valores de campo em um registro existente. O objeto **Recordset** deve suportar atualizações.

Para definir valores de campos, execute um dos seguintes procedimentos:

  - Atribua valores à propriedade [Value](field-object-ado.md) de um objeto [Field](value-property-ado.md) e chame o método **Update**.

  - Passe o nome de um campo e um valor como argumentos com a chamada a **Update**.

  - Passe uma matriz de nomes de campo e uma matriz de valores com a chamada a **Update**.

Ao utilizar matrizes de campos e valores, deve haver um número igual de elementos em ambas as matrizes. Além disso, a ordem dos nomes de campo deve corresponder à ordem dos valores de campo. Se o número e a ordem dos campos e valores não corresponder, ocorrerá um erro.

Se o objeto **Recordset** suportar atualização em lote, você poderá armazenar localmente em cache diversas alterações em um ou mais registros até chamar o método [UpdateBatch](updatebatch-method-ado.md). Se estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método **Update** para salvar quaisquer alterações pendentes no registro atual antes de transmitir as alterações em lote ao provedor.

Se você mover do registro que está adicionando ou editando antes de chamar o método **Update**, o ADO chamará **Update** automaticamente para salvar as alterações. Você deve chamar o método [CancelUpdate](cancelupdate-method-ado.md) se deseja cancelar quaisquer alterações feitas no registro atual ou descartar um registro recém-adicionado.

O registro atual permanece atual depois da chamada ao método **Update**.

**Record**

O método **Update** finaliza adições, exclusões e atualizações de campos na coleção [Fields](fields-collection-ado.md) de um objeto **Record**.

Por exemplo, campos excluídos com o método **Delete** são marcados para exclusão imediatamente, mas permanecem na coleção. O método **Update** deve ser chamado para realmente excluir esses campos da coleção do provedor.

