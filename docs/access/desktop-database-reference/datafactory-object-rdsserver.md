---
title: Objeto DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702177"
---
# <a name="datafactory-object-rdsserver"></a>Objeto DataFactory (RDSServer)


**Aplica-se a**: Access 2013, o Office 2013

Este objeto corporativo padrão do servidor implementa os métodos que fornecem acesso de leitura/gravação aos dados das fontes de dados especificadas para os aplicativos do cliente.

## <a name="remarks"></a>Comentários

O objeto **RDSServer.DataFactory** foi criado como um objeto Automation do servidor que recebe solicitações do cliente. Em uma implementação de Internet, ele reside em um servidor web e é instanciado pelo componente ADISAPI. O objeto **RDSServer.DataFactory** fornece acesso de leitura e gravação às fontes de dados especificadas, mas não contém nenhuma validação ou regras comerciais lógicas.

Se você usar um método disponível em ambos os objetos **RDSServer.DataFactory** e [RDS.DataControl](datacontrol-object-rds.md), o RDS usará a versão **RDS.DataControl** por padrão. O padrão adotará um cenário de programação básico, no qual o **RDSServer.DataFactory** servirá como um objeto corporativo genérico do servidor.

Se desejar que seu aplicativo web para lidar com tarefas específicas processamento do lado do servidor, você pode substituir o **Rdsserver** com um objeto corporativo personalizado.

Crie os objetos corporativos do servidor que chamam os métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) e [CreateRecordset](createrecordset-method-rds.md). Isso será útil, caso você queira adicionar funcionalidade aos objetos corporativos, mas tire proveito das tecnologias RDS existentes.

A ID de classe do objeto **RDSServer.DataFactory** é 9381D8F5-0288-11D0-9501-00AA00B911A5.

