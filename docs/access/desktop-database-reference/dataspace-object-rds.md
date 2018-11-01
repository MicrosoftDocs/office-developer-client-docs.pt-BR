---
title: Objeto DataSpace (RDS)
TOCTitle: DataSpace Object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1715a1d1207955d47897fee8ba191117bcfaa244
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882914"
---
# <a name="dataspace-object-rds"></a>Objeto DataSpace (RDS)

**Aplica-se a**: Access 2013, o Office 2013

Cria proxies do cliente para personalizar os objetos corporativos localizados na camada intermediária.

## <a name="remarks"></a>Comentários

O RDS precisa de proxies do objeto, de modo que o componente do cliente possa comunicar os objetos corporativos localizados na camada intermediária. Os proxies facilitam a compactação, a descompactação e o transporte (a disposição) dos dados [Recordset](recordset-object-ado.md) do aplicativo por meio do processo ou dos limites da máquina.

O RDS usa o método **CreateObject** do objeto [RDS.DataSpace](createobject-method-rds.md) para criar os proxies do objeto corporativo. O proxy do objeto corporativo será criado dinamicamente assim que for criada uma instância da contraparte do objeto corporativo da camada intermediária. O RDS oferece suporte aos seguintes protocolos: HTTP, HTTPS (HTTP Secure Sockets), DCOM, e em processo (os componentes do cliente e o objeto corporativo residem no mesmo computador).

> [!NOTE]
> [!OBSERVAçãO] O RDS se comportará de uma maneira "sem estado" quando o objeto **RDS.DataSpace** usar os protocolos HTTP ou HTTPS, ou seja, qualquer informação interna sobre a solicitação do cliente será descartada depois que o servidor retornar a resposta.

Embora o objeto corporativo pareça existir durante a vida útil do proxy do objeto corporativo, na verdade, esse objeto existe somente até que uma resposta seja enviada para uma solicitação. Quando uma solicitação for emitida (ou seja, o método for chamado no objeto corporativo), o proxy abrirá uma nova conexão com o servidor e este criará uma nova instância do objeto corporativo. Depois que o objeto corporativo responder à solicitação, o servidor destruirá o objeto corporativo e fechará a conexão.

Esse comportamento significa que não é possível passar dados de uma solicitação para outra usando a propriedade ou a variável do objeto corporativo. Use algum outro mecanismo, como um arquivo ou um argumento de método, para permanecer com os dados no estado.

A ID de classe do objeto **RDS.DataSpace** é BD96C556-65A3-11D0-983A-00C04FC29E36.

