---
title: Propriedade MaxRecords (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d66a26cffb14220670643c5b6b5aafe94e8fcb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870083"
---
# <a name="maxrecords-property-ado"></a>Propriedade MaxRecords (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o número máximo de registros a serem retornados a um [Recordset](recordset-object-ado.md) a partir de uma consulta.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica o número máximo de registros a serem retornados. O padrão é zero (sem limite).

## <a name="remarks"></a>Comentários

Use a propriedade **MaxRecords** para limitar o número de registros que o provedor retorna da fonte de dados. A definição padrão dessa propriedade é zero, o que significa que o provedor retorna todos os registros solicitados.

A propriedade **MaxRecords** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando estiver aberto.

