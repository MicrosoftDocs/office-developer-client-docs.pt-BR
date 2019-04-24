---
title: Componentes e provedores de serviços
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308698"
---
# <a name="service-providers-and-components"></a>Componentes e provedores de serviços


**Aplica-se ao:** Access 2013, Office 2013

Provedores e componentes de serviços são componentes que estendem a funcionalidade de provedores de dados implementando interfaces estendidas que não são suportadas originariamente pelo repositório de dados.

O Microsoft Data Access fornece uma *arquitetura de componente* que permite que componentes específicos e especializados implementem conjuntos discretos de funcionalidades de bancos de dados, ou "serviços", no topo de repositórios menos capazes. Portanto, em vez de forçar cada repositório de dados a fornecer sua própria implementação de funcionalidade estendida ou de forçar aplicativos genéricos a implementar funcionalidades de bancos de dados internamente, os componentes de serviços fornecem uma implementação comum que qualquer aplicativo pode usar quando acessar qualquer repositório de dados. O fato de algumas funcionalidades serem implementadas originariamente pelo repositório de dados e outras pelos componentes genéricos é transparente para o aplicativo.

Por exemplo, um mecanismo de cursor, como o Microsoft Cursor Service para OLE DB, é um componente de serviço que pode consumir dados de um repositório de dados sequencial e somente de encaminhamento para produzir dados roláveis. Outros provedores de serviços comumente usados pelo ADO incluem o Microsoft OLE DB Persistence Provider (para salvar dados em um arquivo), o Microsoft Data Shaping Service para OLE DB (para **Conjuntos de registros** hierárquicos) e o Microsoft OLE DB Remoting Provider (para chamar provedores de dados em um computador remoto)

Para obter mais informações sobre provedores de dados e serviços, consulte [Apêndice A: Provedores](appendix-a-providers.md).

