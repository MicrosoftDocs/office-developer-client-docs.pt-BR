---
title: Executando objetos de negócios em serviços de componente
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0eb70a615f49ff351ec31a826abc9775558218dd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862552"
---
# <a name="running-business-objects-in-component-services"></a>Executando objetos de negócios em serviços de componente


**Aplica-se a**: Access 2013 | Office 2013

Os objetos de negócios podem ser arquivos executáveis (.exe) ou bibliotecas de link dinâmico (.dll). A configuração que você usa para executar o objeto de negócios depende de o objeto ser um arquivo .dll ou .exe:

  - Os objetos de negócios criados como arquivos .exe podem ser chamados através do DCOM. Se esses objetos de negócios forem utilizados através do IIS (Internet Information Services), eles estarão sujeitos ao preparativo adicional de dados, que retardará o desempenho do cliente.

  - Os objetos de negócios criados como arquivos .dll podem ser utilizados através do IIS (e portanto do HTTP). Eles também podem ser utilizados sobre o DCOM apenas através dos Component Services (ou Microsoft Transaction Server, se você estiver usando o Windows NT). As DLLs do objeto de negócios precisarão estar registradas no computador servidor IIS para fornecer a você acessibilidade através do IIS. (Para obter as etapas sobre como configurar uma DLL a ser executada no DCOM, consulte a seção, "[Ativando um DLL para executar no DCOM](enabling-a-dll-to-run-on-dcom.md).")


> [!NOTE]
> Quando objetos corporativos na camada intermediária são implementados como componentes de serviços de componentes (usando **GetObjectContext**, **SetComplete**e **SetAbort**), eles podem usar os serviços de componentes (ou MTS, se você estiver usando o Windows NT) para os objetos de contexto manter seu estado entre várias chamadas do cliente. Esse cenário é possível com o DCOM, que geralmente é implementado entre os clientes e os servidores confiáveis (uma intranet). 
>
> Nesse caso, o objeto [RDS.DataSpace](dataspace-object-rds.md) e o método [CreateObject](createobject-method-rds.md) na parte do cliente são substituídos pelo objeto de contexto de transação e o método **CreateInstance** (fornecidos pela interface **ITransactionContext** ) implementados pelos Component Services.


## <a name="see-also"></a>Confira também

- [Executar objetos corporativos nos serviços de componentes (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)