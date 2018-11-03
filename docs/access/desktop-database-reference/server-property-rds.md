---
title: Propriedade Server (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492602d7150f3080df329d30a38e3af51755cf0f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949497"
---
# <a name="server-property-rds"></a>Propriedade Server (RDS)

**Aplica-se a**: Access 2013, o Office 2013

Indica o nome do IIS (Serviços de Informações da Internet) e o protocolo de comunicação.

Você pode definir a propriedade **Server** no tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.

## <a name="syntax"></a>Sintaxe

|Protocolo|Sintaxe no tempo de design|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|Em processo|`<PARAM NAME="Server" VALUE="">`|


|Protocolo|Sintaxe em tempo de execução|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|Em processo|`DataControl.Server=""`|


## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*awebsrvr* ou *computername* |Um valor **String** que contém um caminho de Internet ou intranet, ou nome do computador, se o servidor estiver em um computador remoto; ou, uma cadeia de caracteres em branco, se o servidor estiver no computador local.|
|*porta* |Opcional. Uma porta que é utilizada para conexão com um servidor IIS. O número da porta é definido no Internet Explorer (no menu **Exibir**, clique em **Opções** e selecione a guia **Conexões** ) ou no IIS.|
|*DataControl* |Uma variável de objeto que representa um objeto **RDS.DataControl**.|

## <a name="remarks"></a>Comentários

O servidor é o local onde a solicitação de **RDS.DataControl** (isto é, uma consulta ou atualização) é processada. Por padrão, todas as solicitações são processadas pelo objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), pelo componente [ MSDFMAP.Handler ](datafactory-customization.md) e pelo arquivo [MSDFMAP.INI](understanding-the-customization-file.md) no servidor especificado. 

Lembre-se de reconciliar as definições nos arquivos **MSDFMAP.INI** antigos e novos, quando alterar os servidores. Incompatibilidades poderão fazer com que solicitações bem-sucedidas em um servidor, falhem em outro servidor. Se a propriedade Server estiver definida como "", esses objetos serão utilizados na máquina local.

