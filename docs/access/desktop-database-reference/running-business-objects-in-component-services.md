---
title: Execução de objetos Business em serviços de componente
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309200"
---
# <a name="running-business-objects-in-component-services"></a>Execução de objetos Business em serviços de componente

**Aplica-se ao:** Access 2013, Office 2013

Os objetos de negócios podem ser arquivos executáveis (.exe) ou bibliotecas de link dinâmico (.dll). A configuração que você usa para executar o objeto de negócios depende de o objeto ser um arquivo .dll ou .exe:

- Os objetos de negócios criados como arquivos .exe podem ser chamados através do DCOM. Se esses objetos de negócios forem utilizados através do IIS (Internet Information Services), eles estarão sujeitos ao preparativo adicional de dados, que retardará o desempenho do cliente.

- Os objetos de negócios criados como arquivos .dll podem ser utilizados através do IIS (e portanto do HTTP). Eles também podem ser utilizados sobre o DCOM apenas através dos Component Services (ou Microsoft Transaction Server, se você estiver usando o Windows NT). As DLLs do objeto de negócios precisarão estar registradas no computador servidor IIS para fornecer a você acessibilidade através do IIS. (Para obter as etapas sobre como configurar uma DLL a ser executada no DCOM, consulte a seção, "[Ativando um DLL para executar no DCOM](enabling-a-dll-to-run-on-dcom.md).")


> [!NOTE]
> Quando os objetos de negócios na camada intermediária são implementados como componentes de serviços **** de componente (usando getObjectContext, SetComplete e SetAbort), eles podem usar os serviços de componente (ou MTS, se você estiver usando o Windows NT) objetos de contexto para **** **** manter o estado entre várias chamadas do cliente. Esse cenário é possível com o DCOM, que geralmente é implementado entre os clientes e os servidores confiáveis (uma intranet). 
>
> Nesse caso, o objeto [RDS.DataSpace](dataspace-object-rds.md) e o método [CreateObject](createobject-method-rds.md) na parte do cliente são substituídos pelo objeto de contexto de transação e o método **CreateInstance** (fornecidos pela interface **ITransactionContext** ) implementados pelos Component Services.


## <a name="see-also"></a>Confira também

- [Executando objetos de negócios nos serviços de componente (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
