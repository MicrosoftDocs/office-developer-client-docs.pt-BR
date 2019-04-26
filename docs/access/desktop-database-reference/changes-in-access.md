---
title: Alterações no Access (referência no banco de dados da área de trabalho do Access)
TOCTitle: Changes in Access
description: Access não inclui suporte para projetos de dados do Access (ADPs). Access introduz um novo tipo de aplicativo que permite que você crie um aplicativo baseado na web Access.
ms:assetid: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15)
ms:contentKeyID: 49106417
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: de2ff21598639b445f5ff84240b115704b484209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296497"
---
# <a name="changes-in-access"></a>Alterações no Access

**Se aplica ao:** Access 2013, Office 2013

Access não inclui suporte para projetos de dados do Access (ADPs). Access introduz um novo tipo de aplicativo que permite que você crie um aplicativo baseado na web Access. Ao usar esse tipo de aplicativo, você pode criar aplicativos baseados na web que usam o poder do SQL Server no local ou na nuvem.

Em um aplicativo do Access no SharePoint Server, quando você cria uma tabela, uma consulta ou um macro de dados no cliente Access no qual você está criando as tabelas, exibições ou disparadores em um banco de dados SQL Server, ao usar o cliente Access, você poderá abrir seu banco de dados para outros aplicativos que se conectam ao SQL Server. Isso permite que você compartilhe seus dados ou carregar dados de outros sistemas para seu aplicativo Access.

Com Office 365 e Access, você pode criar aplicativos que chegam seus usuários sem ter que se preocupar com os desafios de implantação, problemas de instalação de software ou compatibilidades de sistema operacional. Crie seu aplicativo em um único local e compartilhá-las pela web com o poder do SQL Azure e SQL Server.

[O SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), a versão de nuvem do SQL Server, não oferece suporte a recursos que dependem projetos de dados do Access (ADPs) para operar. Para suportar ADPs em SQL Azure, Access exigiria alterações significativas.

Por esse motivo, o Access não oferece suporte aos ADPs. ADPs têm sido uma ótima ferramenta para trabalhar com o SQL Server em um ambiente local, no entanto, muita coisa foi alterada desde que as ADPs foram introduzidas no Access 2000. Os usuários agora esperam que o banco de dados esteja disponível onde quer que estejam.

## <a name="adp-support-and-the-future"></a>Suporte à ADP e o futuro

ADPs continuam a funcionar em versões anteriores do Access. Você pode continuar a desenvolver aplicativos ADP e podemos continuará a dar suporte a versões anteriores do Access sob o standard [ciclo de vida de suporte](https://support.microsoft.com/lifecycle/search). Não atualizaremos versões mais antigas do Access para suportar novas versões dos SQL Server ou SQL Azure. Portanto, você poderá encontrar problemas se você usar SQL Server 2012 ou versões posteriores com sua ADP. ADPs continuará dar suporte a SQL 2008 R2 e versões anteriores.

No futuro, os desenvolvedores ADP podem considerar várias possibilidades diferentes:

- **Converter um aplicativo Access** - usando o Access, você pode importar suas tabelas para um novo aplicativo do Access e formulários para seu aplicativo são criados automaticamente para você. Você pode estender a funcionalidade dos formulários base que o Access cria para você e os usuários podem usar seu aplicativo na web. Embora algumas das funcionalidades que você usa em ADPs podem não estar disponíveis agora, esperam Microsoft para continuar a melhorias de foco do produto para esse tipo de aplicativo.

- **Converter em um banco de dados vinculado da área de trabalho ** – O Access continua oferecendo suporte à criação de bancos de dados da área de trabalho no formato de arquivo .accdb. Você pode converter seu aplicativo para o formato .accdb, incluindo todos os seus formulários e relatórios e deixar os dados no SQL Server. Você pode vincular ao banco de dados do SQL Server usando as tabelas vinculadas e o aplicativo continuará a operar os mesmos dados.

- **Criar um aplicativo híbrido** – se o aplicativo for grande e você não quiser converter tudo ao mesmo tempo, é possível importar seus dados em um aplicativo Access e um link para o banco de dados do SQL Server de uma .accdb. Isso permite migrar gradualmente, adicionar formulários e funcionalidades ao longo do tempo ao seu aplicativo do Access, mantendo o seu aplicativo de cliente, como um .accdb com as tabelas vinculadas ao banco de dados do SQL Server por trás do aplicativo do Access.

- **Atualizar para o .NET Framework** - Seu aplicativo pode ser complexo suficiente para considerar a mudança para uma plataforma de desenvolvimento profissional, como o .NET Framework. O SQL Server foi projetado para facilitar a utilização da infra-estrutura do banco de dados existente e estender a funcionalidade do seu aplicativo sem reescrever significativamente seu código.

## <a name="conclusion"></a>Conclusão

Access foi projetado para se conectar a bancos de dados com a nuvem com base em tecnologias SharePoint Server e SQL Server e facilmente trabalhar com Office 365. Access foi projetado para ajudá-lo a criar rapidamente e compartilhar aplicativos de negócios orientadas a dados que ajudam a executar o seu negócio.

## <a name="see-also"></a>Confira também

- [Novidades no Access 2013 para desenvolvedores](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)


