---
title: Propriedade CursorLocation (ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463763"
---
# <a name="cursorlocation-property-ado"></a>Propriedade CursorLocation (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o local do serviço de cursor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que pode ser definido como um dos valores [CursorLocationEnum](cursorlocationenum.md).

## <a name="remarks"></a>Comentários

Essa propriedade permite que você escolha entre diversas bibliotecas de cursores acessíveis ao provedor. Geralmente, é possível escolher entre usar uma biblioteca de cursores do lado do cliente ou uma que esteja localizada no servidor.

A definição dessa propriedade afeta as conexões estabelecidas apenas depois que a propriedade tiver sido configurada. A alteração da propriedade **CursorLocation** não afeta as conexões existentes.

Os cursores retornados pelo método [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) herdam essa definição. Os objetos **Recordset** herdarão automaticamente essa definição de suas conexões associadas.

Essa propriedade é leitura/gravação em um [Connection](connection-object-ado.md) ou um [Recordset](recordset-object-ado.md) fechado e somente leitura em um **Recordset** aberto.

**Uso de serviço de dados remotos** Quando usado em um cliente **Recordset** ou um objeto de **Conexão** , a propriedade **CursorLocation** só pode ser definida como **adUseClient**.

