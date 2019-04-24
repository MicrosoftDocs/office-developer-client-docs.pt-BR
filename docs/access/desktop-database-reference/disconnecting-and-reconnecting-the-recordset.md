---
title: Desconexão e reconexão do conjunto de registros
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c028a7d867a105f35b4848ecbe95339f5fcd4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293858"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Desconexão e reconexão do conjunto de registros


**Aplica-se ao:** Access 2013, Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Desconectando e reconectando o Recordset

Um dos recursos mais eficientes encontrados no ADO é a capacidade de abrir um **Recordset** no cliente a partir de uma fonte de dados e, em seguida, *desconectar* o **Recordset** dessa fonte. Uma vez desconectado o **Recordset**, a conexão com a fonte de dados poderá ser fechada, liberando assim os recursos no servidor usado para mantê-lo. Você pode continuar a exibir e editar os dados no **Recordset** enquanto ele estiver desconectado e reconectar-se posteriormente à fonte de dados para enviar suas atualizações no modo em lotes.

Para desconectar um **Recordset**, abra-o com o local de cursor **adUseClient** e defina a propriedade **ActiveConnection** como *Nothing*. (os usuários de C++ devem definir **ActiveConnection** como NULL para se desconectar.)

Usaremos um **Recordset** desconectado posteriormente neste capítulo quando abordarmos a persistência do **Recordset** para lidar com um cenário em que é necessário haver dados em um **Recordset** disponíveis para um aplicativo enquanto o computador cliente não está conectado a uma rede.

