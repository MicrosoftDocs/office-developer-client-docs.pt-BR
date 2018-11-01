---
title: Provedores e componentes de serviços
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d215c7c66c489e54d513941604b1c66c0e9094c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881206"
---
# <a name="service-providers-and-components"></a>Provedores e componentes de serviços


**Aplica-se a**: Access 2013, o Office 2013

Provedores e componentes de serviços são componentes que estendem a funcionalidade de provedores de dados implementando interfaces estendidas que não são suportadas originariamente pelo repositório de dados.

Microsoft Data Access fornece uma *arquitetura de componente* que permite que os componentes individuais, especializados implementar discretos define da funcionalidade de banco de dados ou "services", na parte superior de armazenamentos de menor capacidade. Portanto, em vez de forçar cada repositório de dados a fornecer sua própria implementação de funcionalidade estendida ou de forçar aplicativos genéricos a implementar funcionalidades de bancos de dados internamente, os componentes de serviços fornecem uma implementação comum que qualquer aplicativo pode usar quando acessar qualquer repositório de dados. O fato de algumas funcionalidades serem implementadas originariamente pelo repositório de dados e outras pelos componentes genéricos é transparente para o aplicativo.

Por exemplo, um mecanismo de cursor, como o Microsoft Cursor Service para OLE DB, é um componente de serviço que pode consumir dados de um repositório de dados sequencial e somente de encaminhamento para produzir dados roláveis. Outros provedores de serviços comumente usados pelo ADO incluem o Microsoft OLE DB Persistence Provider (para salvar dados em um arquivo), o Microsoft Data Shaping Service para OLE DB (para **Conjuntos de registros** hierárquicos) e o Microsoft OLE DB Remoting Provider (para chamar provedores de dados em um computador remoto)

Para obter mais informações sobre provedores de dados e serviços, consulte [Apêndice A: Provedores](appendix-a-providers.md).

