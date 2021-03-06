---
title: Objeto DataControl (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294516"
---
# <a name="datacontrol-object-rds"></a>Objeto DataControl (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Vincula um [Recordset](recordset-object-ado.md) de consulta de dados a um ou mais controles (por exemplo, uma caixa de texto, um controle de grade ou uma caixa de combinação) para exibir os dados do **Recordset** em uma página da Web.

## <a name="syntax"></a>Sintaxe

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>Comentários

A ID de classe do objeto **RDS.DataControl** é BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!OBSERVAçãO] Se você receber um erro informando que um objeto [RDS.DataSpace](dataspace-object-rds.md) ou **RDS.DataControl** não foi carregado, verifique se está usando a ID de classe correta. As IDs de classe desses objetos foram alteradas da versão 1.0 e 1.1.

Para um cenário básico, é necessário definir somente as propriedades **SQL**, **Connect** e **Server** do objeto **RDS.DataControl**, que chamará automaticamente o objeto corporativo padrão, [RDSServer.DataFactory](datafactory-object-rdsserver.md).

Todas as propriedades do **RDS.DataControl** são opcionais porque os objetos corporativos personalizados podem substituir sua funcionalidade.

> [!NOTE]
> [!OBSERVAçãO] Se você consultar vários resultados, somente o primeiro [Recordset](recordset-object-ado.md) será retornado. Se forem necessárias várias definições de resultados, atribua cada uma ao próprio **DataControl**. 
> 
> Um exemplo de uma consulta para vários resultados poderia ser o seguinte: `"Select * from Authors, Select * from Topics"` .

A adição de "DFMode=20;" à sua sequência de conexão durante o uso do objeto **RDS.DataControl** pode melhorar o desempenho do servidor na atualização de dados. Com essa definição, o objeto **RDSServer.DataFactory** do servidor usa um modo de recursos menos intensivo. No entanto, os seguintes recursos não estão disponíveis nesta configuração:

  - Uso de consultas parametrizadas.

  - Obtenção de informações de parâmetro ou de coluna antes da chamada do método **Execute**.

  - Definição de **Transacionar Atualizações** como **Verdadeira**.

  - Obtenção de status da linha.

  - Chamada do método [Resync](resync-method-ado.md).

  - Atualização (de forma explícita ou automática) por meio da propriedade [Update Resync](update-resync-property-dynamic-ado.md).

  - Definição das propriedades **Command** ou [Recordset](recordset-sourcerecordset-properties-rds.md).

  - Uso de **adCmdTableDirect**.

O objeto **RDS.DataControl** é executado no modo assíncronopor padrão. Se você solicitar a execução síncrona do aplicativo, defina o parâmetro [ExecuteOptions](executeoptions-property-rds.md) igual a **adcExecSync** e o parâmetro [FetchOptions](fetchoptions-property-rds.md) igual a **adcFetchUpFront**, como mostra o exemplo a seguir.

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

Use um objeto **RDS.DataControl** para vincular os resultados de uma única consulta a um ou vários controles visuais. Por exemplo, suponha que você codificou uma consulta solicitando dados do cliente, como Nome, Residência, Local de Nascimento, Idade e Status de Prioridade. Use um único objeto **RDS.DataControl** para exibir o Nome, a Idade e a Região do cliente em três caixas de texto separadas; o Status de Prioridade do Cliente em uma caixa de seleção e todos os dados em um controle de grade.

Use objetos **RDS.DataControl** diferentes para vincular resultados de várias consultas a controles visuais diferentes. Por exemplo, suponha que você está usando uma consulta para obter informações sobre um cliente e uma segunda consulta para obter informações da mercadoria comprada pelo cliente. Você deseja exibir resultados da primeira consulta em três caixas de texto e uma caixa de seleção e os resultados da segunda consulta em um controle de grade. Se você usar o objeto corporativo padrão (**RDSServer.DataFactory**), será necessário fazer o seguinte:

  - Adicione dois **RDS. Objetos DataControl** em sua página da Web.

  - Gravar duas consultas, uma para cada propriedade **SQL** de dois objetos **RDS.DataControl**. O primeiro objeto **RDS.DataControl** conterá uma consulta SQL solicitando informações do cliente; o segundo conterá uma consulta solicitando uma lista de mercadorias compradas pelo cliente.

  - Em cada uma das marcas OBJECT dos controles vinculados, especifique o valor DATAFLD para definir os valores dos dados que você deseja exibir em cada controle visual.

Não há restrição de contagem no número de **RDS. Objetos DataControl** que você pode incorporar por meio de marcas OBJECT em uma única página da Web.

Quando você define o **RDS. Objeto DataControl** em uma página da  Web, use valores de altura e largura diferentes de zero, como 1 (para evitar a inclusão de espaço extra). 

Os componentes do cliente RDS já foram incluídos como parte do Internet Explorer 4.0; por esse motivo, não é necessário incluir um parâmetro CODEBASE na marca de objeto **RDS.DataControl**.

Com o Internet Explorer 4.0 ou posterior, você pode se vincular aos dados usando controles HTML e controles ActiveX somente se eles são marcados como controles de modelo de apartment.

**Usuários do Microsoft Visual Basic** O **RDS. O DataControl** é usado somente em aplicativos baseados na Web. Não é necessário um aplicativo cliente do Visual Basic.

