---
title: Propriedade CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295217"
---
# <a name="cursorlocation-property-ado"></a>Propriedade CursorLocation (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o local do serviço de cursor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que pode ser definido como um dos valores [CursorLocationEnum](cursorlocationenum.md).

## <a name="remarks"></a>Comentários

Essa propriedade permite que você escolha entre diversas bibliotecas de cursores acessíveis ao provedor. Geralmente, é possível escolher entre usar uma biblioteca de cursores do lado do cliente ou uma que esteja localizada no servidor.

A definição dessa propriedade afeta as conexões estabelecidas apenas depois que a propriedade tiver sido configurada. A alteração da propriedade **CursorLocation** não afeta as conexões existentes.

Os cursores retornados pelo método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) herdam essa definição. Os objetos **Recordset** herdarão automaticamente essa definição de suas conexões associadas.

Essa propriedade é leitura/gravação em um [Connection](connection-object-ado.md) ou um [Recordset](recordset-object-ado.md) fechado e somente leitura em um **Recordset** aberto.

**Uso do Remote Data Service** Quando usado em um objeto **Recordset** ou **Connection** do lado do cliente, a propriedade **CursorLocation** só pode ser definida como **adUseClient**.

