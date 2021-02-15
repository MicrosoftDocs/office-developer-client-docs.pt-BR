---
title: Propriedade Status (Field do ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c5f9d73a1081bb27c88541ac99307165222ab65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306318"
---
# <a name="status-property-ado-field"></a>Propriedade Status (Field do ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o status de um objeto [Field](field-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor [FieldStatusEnum](fieldstatusenum.md). O valor padrão é **adFieldOK**.

## <a name="remarks"></a>Comentários

Essa propriedade sempre retorna **adFieldOK** para os campos de um objeto [Recordset](recordset-object-ado.md).

Adições e exclusões executadas nas coleções [Fields](fields-collection-ado.md) do objeto [Record](record-object-ado.md) são armazenadas em cache até que o método [Update](update-method-ado.md) seja chamado. A propriedade **Status** permite que você identifique quais campos foram adicionados ou excluídos com êxito.

Para melhorar o desempenho, as alterações de esquema são armazenadas em cache até que o método **Update** seja chamado e, em seguida, são efetuadas em uma atualização em lote otimista. Se o método **Update** não for chamado, o servidor não será atualizado. Se as atualizações falharem, um erro será retornado e a propriedade **Status** indicará os valores combinados da operação e o código de status do erro. Por exemplo, **adFieldPendingInsert** **OU** **adFieldPermissionDenied**. A propriedade **Status** de cada **Field** pode ser usada para determinar o motivo pelo qual o **Field** não foi adicionado, modificado ou excluído. **O status** só é exposto significativamente no **Registro.** **Coleção Fields** e não **o Recordset**. **Coleção Fields.**

Podem surgir dois problemas durante a adição, modificação ou exclusão de um **Field**. Se o usuário excluir um **Field**, ele será marcado para exclusão da coleção **Fields**. Se o **Update** subsequente retornar um erro porque o usuário tentou excluir um **Field** para o qual não tinha permissão, o **Field** terá o status de **adFieldPermissionDenied** **OU** **adFieldPendingDelete**. A chamada do método [CancelUpdate](cancelupdate-method-ado.md) restaura os valores originais e define **Status** como **adFieldOK**. Da mesma forma, o método **Update** pode retornar um erro porque um novo **Field** foi adicionado com um valor inválido. Neste caso, o novo **Field** estará na coleção **Fields** e terá o status **adFieldPendingInsert** e, talvez, **adFieldCantCreate**. Você pode inserir um valor válido para o novo **Field** e chamar **Update** novamente. Em vez disso, a chamada de **Resync** repete a consulta ao provedor.

