---
title: Propriedade ReadyState (RDS)
TOCTitle: ReadyState Property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 804a98a6fa7c93617a5b6e165a2a012969c66913
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464055"
---
# <a name="readystate-property-rds"></a>Propriedade ReadyState (RDS)


**Aplica-se a**: Access 2013 | Office 2013

Indica o progresso de um objeto [DataControl](datacontrol-object-rds.md) à medida que ele recupera dados em seu objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um dos seguintes valores.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcReadyStateLoaded</strong></p></td>
<td><p>A consulta atual ainda está sendo executada e nenhuma linha foi pesquisada. O <strong>Recordset</strong> do objeto <strong>DataControl</strong> não está disponível para uso.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Um conjunto inicial de linhas recuperado pela consulta atual foi armazenado no <strong>Recordset</strong> do objeto <strong>DataControl</strong> e está disponível para uso. As linhas restantes ainda estão sendo pesquisadas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Todas as linhas recuperadas pela consulta atual foram armazenadas no <strong>Recordset</strong> do objeto <strong>DataControl</strong> e estão disponíveis para uso.
 Este estado também é possível se uma operação for anulada devido a um erro ou se o objeto <strong>Recordset</strong> não for inicializado.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!OBSERVAçãO] Cada arquivo executável do lado do cliente que utilizar essas constantes deverá fornecer suas respectivas declarações. Você pode recortar e colar as declarações da constante que deseja do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</P>



## <a name="remarks"></a>Comentários

Utilize o evento [onReadyStateChange](onreadystatechange-event-rds.md) para monitorar as alterações da propriedade **ReadyState** durante uma operação de consulta assíncrona. Esse procedimento é mais eficiente do que verificar periodicamente o valor da propriedade.

Se ocorrer um erro durante uma operação assíncrona, a propriedade **ReadyState** será alterada para **adcReadyStateComplete**, a propriedade [State](state-property-ado.md) será alterada de **adStateExecuting** para **adStateClosed**e o **conjunto de registros** propriedade [Value](value-property-ado.md) do objeto permanecerá como *Nothing*.
