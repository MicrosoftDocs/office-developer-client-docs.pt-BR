---
title: Coleção Errors (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715899"
---
# <a name="errors-collection-ado"></a>Coleção Errors (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Contém todos os objetos [Error](error-object-ado.md) criados em resposta à falha relacionada a um único provedor.

## <a name="remarks"></a>Comentários

Qualquer operação envolvendo os objetos ADO pode gerar um ou vários erros de provedor. À medida que cada erro ocorrer, um ou vários objetos **Error** poderão ser colocados na coleção **Errors** do objeto [Connection](connection-object-ado.md). Quando outra operação do ADO gerar um erro, a coleção **Errors** será limpa e o novo conjunto de objetos **Error** poderá ser colocado na coleção **Errors**.

Cada objeto **Error** representa um erro de provedor específico e não um erro do ADO. Os erros do ADO são apresentados no mecanismo de tratamento de exceções do tempo de execução. Por exemplo, no Microsoft Visual Basic, a ocorrência de um erro específico do ADO disparará um evento [onError](onerror-event-rds.md) e aparecerá no objeto **Err**.

As operações do ADO que não geram um erro não têm efeito sobre a coleção **Errors**. Use o método [Clear](clear-method-ado.md) para limpar manualmente a coleção **Errors**.

O conjunto de objetos **Error** na coleção **Errors** descreve todos os erros que ocorreram em resposta a uma única instrução. A enumeração dos erros específicos na coleção **Errors** permite rotinas de tratamento de erros para determinar de modo mais preciso a causa e a origem de um erro e executar as etapas apropriadas para recuperação.

Algumas propriedades e métodos retornam avisos que aparecem como objetos **Error** na coleção **Errors** mas não suspendem a execução de um programa. Antes de chamar os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md), o método [Open](open-method-ado-connection.md) em um objeto **Connection** ou definir a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset**, chame o método **Clear** na coleção **Errors**. Dessa forma, você pode ler a propriedade [Count](count-property-ado.md) da coleção **Errors** para verificar os avisos retornados.


> [!NOTE]
> [!OBSERVAçãO] Consulte o tópico do objeto **Error** para obter uma explicação mais detalhada sobre como uma operação do ADO simples pode gerar erros múltiplos.


