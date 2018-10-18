---
title: Propriedade Update Resync -- Dinâmica (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4eea391e99202eeb075d73daa1034dff2042e49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604418"
---
# <a name="update-resync-property--dynamic-ado"></a>Propriedade Update Resync -- Dinâmica (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Especifica se o método [UpdateBatch](updatebatch-method-ado.md) é seguido por uma operação de método [Resync](resync-method-ado.md) implícita e, em caso positivo, o escopo dessa operação.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna uma ou mais do [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valores.

## <a name="remarks"></a>Comentários

Os valores de ADCPROP\_UPDATERESYNC\_ENUM pode ser combinado, exceto para adresyncall, que já representa a combinação do restante dos valores.

A constante **adResyncConflicts** armazena os valores de ressincronização como valores de base, mas não substitui as alterações pendentes.

**Update Resync** é uma propriedade dinâmica acrescentada à coleção [Properties](recordset-object-ado.md) do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for configurada como **adUseClient**.

