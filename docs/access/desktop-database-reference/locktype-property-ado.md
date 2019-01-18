---
title: Propriedade LockType (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712474"
---
# <a name="locktype-property-ado"></a>Propriedade LockType (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tipo de bloqueio colocado nos registros durante a edição.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [LockTypeEnum](locktypeenum.md). O valor padrão é **adLockReadOnly**.

## <a name="remarks"></a>Comentários

Defina a propriedade **LockType** antes de abrir um [Recordset](recordset-object-ado.md) para especificar qual tipo de bloqueio o provedor deve usar ao abri-lo. Leia a propriedade para retornar o tipo de bloqueio em uso em um objeto **Recordset** aberto.

Talvez os provedores não ofereçam suporte a todos os tipos de bloqueio. Se um provedor não puder oferecer suporte à definição de **LockType** solicitada, ele substituirá outro tipo de bloqueio. Para determinar a funcionalidade real do bloqueio disponível em um objeto **Recordset**, use o método [Supports](supports-method-ado.md) com **adUpdate** e **adUpdateBatch**.

A definição **adLockPessimistic** não terá suporte se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, não ocorrerá nenhum erro; o **LockType** com suporte mais próximo será usado em seu lugar.

A propriedade **LockType** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando estiver aberto.

**Uso de serviço de dados remotos** Quando usado em um objeto Recordset do lado do cliente, a propriedade **LockType** só pode ser definida como **adLockBatchOptimistic**.

