---
title: Propriedade FetchOptions (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60eb05d87e7d31d283cdcf29c0f6240892fe29ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463378"
---
# <a name="fetchoptions-property-rds"></a>Propriedade FetchOptions (RDS)


**Aplica-se a**: Access 2013 | Office 2013

Indica o tipo de busca assíncrona.

## <a name="setting-and-return-values"></a>Configurações e valores de retorno

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
<td><p><strong>adcFetchUpFront</strong></p></td>
<td><p>Todos os registros do <a href="recordset-object-ado.md">Recordset</a> são encontrados antes que o controle seja retornado ao aplicativo. O <strong>Recordset</strong> completo deve ser encontrado para que o aplicativo possa utilizá-lo de algum modo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>O controle pode retornar ao aplicativo assim que o primeiro lote de registros for encontrado. Uma leitura subsequente do <strong>Recordset</strong> que tente acessar um registro não encontrado no primeiro lote será adiada até que o registro procurado seja realmente encontrado, quando o controle retornará ao aplicativo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>Padrão. O controle retorna imediatamente ao aplicativo enquanto os registros são encontrados em segundo plano. Se o aplicativo tentar ler um registro que ainda não foi encontrado, o registro mais próximo ao procurado será lido, e o controle retornará imediatamente, indicando que o fim atual do <strong>Recordset</strong> foi atingido. Por exemplo, uma chamada ao <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> moverá a posição atual do registro para o último registro que foi realmente encontrado, embora mais registros continuem preenchendo o <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!OBSERVAçãO] Cada arquivo executável do lado do cliente que utilizar essas constantes deverá fornecer suas respectivas declarações. Você pode recortar e colar as declarações da constante que deseja do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</P>



## <a name="remarks"></a>Comentários

Em um aplicativo Web, você geralmente usará **adcFetchAsync** (o valor padrão), pois ele proporciona um desempenho melhor. Em um aplicativo cliente compilado, você geralmente usará **adcFetchBackground**.

