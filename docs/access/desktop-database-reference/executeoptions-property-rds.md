---
title: Propriedade ExecuteOptions (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 641e7942f5336f230d396db7e06b9d0601645cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462434"
---
# <a name="executeoptions-property-rds"></a>Propriedade ExecuteOptions (RDS)


**Aplica-se a**: Access 2013 | Office 2013

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
> <P>[!OBSERVAçãO] Cada arquivo executável do lado do cliente que usa essas constantes deve fornecer declarações para elas. Você pode recortar e colar as declarações de constantes desejadas do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</P>



## <a name="remarks"></a>Comentários

Se **ExecuteOptions** for definido como **adcExecAsync**, a próxima chamada do **Refresh** no [Recordset](datacontrol-object-rds.md) do objeto **RDS.DataControl** será executada de forma assíncrona.

Ocorrerá um erro se você tentar chamar [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) ou [Recordset](recordset-sourcerecordset-properties-rds.md) enquanto outra operação assíncrona que possa alterar o [Recordset](datacontrol-object-rds.md) do objeto **RDS.DataControl** estiver sendo executada.

Se ocorrer um erro durante uma operação assíncrona, o valor [ReadyState](readystate-property-rds.md) do objeto **RDS.DataControl** será alterado de **adcReadyStateLoaded** para **adcReadyStateComplete**, e o valor da propriedade **Recordset** permanecerá *Nothing*.
