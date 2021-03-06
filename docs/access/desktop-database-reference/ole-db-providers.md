---
title: Provedores OLE DB (referência do banco de dados da área de trabalho do Access)
TOCTitle: OLE DB providers
ms:assetid: ef412198-eac5-bf86-73fd-574e67276408
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250215(v=office.15)
ms:contentKeyID: 48548576
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 649f1db283b772a0f6798fae0d56a3a80c59e21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288480"
---
# <a name="ole-db-providers"></a>Provedores OLE DB


**Aplica-se ao:** Access 2013, Office 2013

A Introdução do programador do ADO discute a relação entre o ADO e o restante da arquitetura do Microsoft Data Access. [](introduction-to-ado-programming.md) O OLE DB define um conjunto de interfaces COM para fornecer aos aplicativos acesso uniforme aos dados armazenados em diversas fontes de informação. Essa abordagem permite que uma fonte de dados compartilhe seus dados por meio de interfaces que suportam o número de funcionalidades DBMS apropriado para a fonte de dados. De acordo com o design, a arquitetura de alto desempenho do OLE DB é baseada no uso de um modelo de serviços flexível e baseado em componentes. Em vez de ter um número prescrito de camadas intermediárias entre o aplicativo e os dados, o OLE DB requer somente os componentes necessários para realizar uma tarefa específica.

Por exemplo, suponha que um usuário deseje realizar uma consulta. Considere as seguintes situações:

  - Os dados residem em um banco de dados relacional para o qual existe no momento um driver ODBC, mas não existe Provedor do OLE DB nativo. O aplicativo usa o ADO para falar com o Provedor do OLE DB para ODBC, que então carrega o driver de ODBC apropriado. O driver passa a instrução SQL para DBMS, que recupera os dados.

  - Os dados residem no Microsoft SQL Server para o qual existe um provedor do OLE DB nativo. O aplicativo usa o ADO para falar diretamente com o Provedor do OLE DB para Microsoft SQL Server. Não são necessários intermediários.

  - Os dados residem no Microsoft Exchange Server, para o qual existe um provedor do OLE DB, mas que não expõe um mecanismo para processar consultas SQL. O aplicativo usa o ADO para falar com o Provedor do OLE DB para Microsoft Exchange e pede auxílio a um componente do processador de consulta do OLE DB para lidar com o pedido de consulta.

  - Os dados residem no sistema de arquivos NTFS da Microsoft na forma de documentos. Os dados são acessados por um provedor do OLE DB no Serviço de indexação da Microsoft, que indexa o conteúdo e as propriedades dos documentos no sistema de arquivos para permitir pesquisas eficientes de conteúdo.

Em todos os exemplos anteriores, o aplicativo pode consultar os dados. As necessidades do usuário são correspondidas com um número mínimo de componentes. Em cada caso só utilizam-se componentes adicionais se necessário, e somente os componentes necessários são solicitados. Esse carregamento sob demanda de componentes reutilizáveis e compartilháveis contribui grandemente para um alto desempenho, quando OLE DB é usado.

Há duas categorias de provedores: os que fornecem dados e os que fornecem serviços. Um [provedor de dados](data-providers.md) é proprietário de seus próprios dados e os expõe em um formulário tabular para o aplicativo. Um [provedor de serviços](service-providers-and-components.md) encapsula um serviço produzindo e consumindo dados, aumentando os recursos nos aplicativos ADO. Um provedor de serviços também pode ser definido como um [componente de serviço](service-providers-and-components.md), que deve trabalhar juntamente com outros provedores ou componentes de serviços.

O ADO fornece uma interface consistente e de alto nível para os vários provedores OLE DB.

Esta seção inclui os seguintes tópicos:

- [Provedores de Dados](data-providers.md)

- [Provedores de serviços e componentes](service-providers-and-components.md)
