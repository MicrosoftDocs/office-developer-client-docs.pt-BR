---
title: Propriedade Status (Recordset do ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 396188dcd959b229f7f7a58ccafb76b00508aa49
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944231"
---
# <a name="status-property-ado-recordset"></a>Propriedade Status (Recordset do ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o status do registro atual com relação às atualizações em lote ou outras operações em massa.

## <a name="return-value"></a>Valor de retorno

Retorna a soma de um ou mais valores [RecordStatusEnum](recordstatusenum.md).

## <a name="remarks"></a>Comentários

Utilize a propriedade **Status** para verificar quais alterações estão pendentes para registros modificados durante a atualização em lote. Você também pode utilizar a propriedade **Status** para exibir o status dos registros que falharam durante as operações em massa; por exemplo, quando você chama os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md) ou define a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset** para uma matriz de indicadores. Com esta propriedade, você pode identificar como um registro específico falhou e solucionar o problema de forma adequada.

