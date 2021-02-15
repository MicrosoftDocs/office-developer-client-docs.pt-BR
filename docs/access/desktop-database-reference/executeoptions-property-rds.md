---
title: Propriedade ExecuteOptions (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf773090ccb37bf4cad4aff41499ad01f966479
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293249"
---
# <a name="executeoptions-property-rds"></a>Propriedade ExecuteOptions (RDS)


**Aplica-se ao:** Access 2013, Office 2013

Indica se a execução assíncrona está habilitada.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um dos valores a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcExecSync</strong></p></td>
<td><p>Executa a próxima atualização do <a href="recordset-object-ado.md">Recordset</a> de maneira síncrona.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcExecAsync</strong></p></td>
<td><p>Padrão. Executa a próxima atualização do <strong>Recordset</strong> de maneira assíncrona.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Cada arquivo executável do lado do cliente que usa essas constantes deve fornecer declarações para elas. Você pode recortar e colar as declarações de constantes desejadas do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.

## <a name="remarks"></a>Comentários

Se **ExecuteOptions** for definido como **adcExecAsync**, a próxima chamada do **Refresh** no **Recordset** do objeto [RDS.DataControl](datacontrol-object-rds.md) será executada de forma assíncrona.

Ocorrerá um erro se você tentar chamar [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) ou [Recordset](recordset-sourcerecordset-properties-rds.md) enquanto outra operação assíncrona que possa alterar o **Recordset** do objeto [RDS.DataControl](datacontrol-object-rds.md) estiver sendo executada.

Se ocorrer um erro durante uma operação assíncrona, o valor [ReadyState](readystate-property-rds.md) do objeto **RDS.DataControl** será alterado de **adcReadyStateLoaded** para **adcReadyStateComplete**, e o valor da propriedade **Recordset** permanecerá *Nothing*.

