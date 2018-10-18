---
título: alterações no Access (referência de banco de dados da área de trabalho do Access) TOCTitle: alterações no Access <<<<<<< ms:assetid cabeça: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15) ms:contentKeyID: ms.date 49106417: 18/09/2015 === Descrição: acesso não inclui suporte para projetos de dados do Access (ADPs). Access introduz um novo tipo de aplicativo que permite que você crie um aplicativo baseado na web Access.
MS:AssetID: 8dfc5fc9-a6a7-4a91-8e97-c3874e9b880f ms:mtpsurl: https://msdn.microsoft.com/library/JJ618413(v=office.15) ms:contentKeyID: ms.date 49106417: 10/16/2018
>>>>>>> mtps_version mestre: v=office.15
---

# <a name="changes-in-access"></a>Alterações no acesso 2013

**Aplica-se a:** Access 2013 | Office 2013

<<<<<<< Cabeça acesso não inclui suporte para projetos de dados do Access (ADPs). Access introduz um novo tipo de aplicativo que permite que você crie um aplicativo baseado na web Access. Ao usar esse tipo de aplicativo, você pode criar aplicativos baseados na web que usam o poder do SQL Server no local ou na nuvem.

Access introduz um novo tipo de aplicativo que permite que você crie um aplicativo baseado na web Access. Ao usar esse tipo de aplicativo, você pode criar aplicativos baseados na web que usam o poder do SQL Server no local ou na nuvem.

Em um aplicativo de Access em SharePoint Server, quando você cria uma tabela, uma consulta ou uma macro de dados no cliente Access no qual você está criando as tabelas, exibições ou disparadores em um banco de dados SQL Server. Usando o cliente Access, você poderá abrir seu banco de dados para outros aplicativos que se conectam ao SQL Server. Isso permite que você compartilhe seus dados ou carregar dados de outros sistemas para seu aplicativo Access.

Com Office 365 e Access, você pode criar aplicativos que chegam seus usuários sem ter que se preocupar com os desafios de implantação, problemas de instalação de software ou compatibilidades de sistema operacional. Crie seu aplicativo em um único local e compartilhá-las pela web com o poder do SQL Azure e SQL Server.

[O SQL Azure](https://msdn.microsoft.com/library/azure/ee336279.aspx), a versão de nuvem do SQL Server, não oferece suporte a recursos que dependem projetos de dados do Access (ADPs) para operar. Para suportar ADPs em SQL Azure, Access exigiria alterações significativas.

Por esses motivos, Access não suporta ADPs. ADPs têm sido uma ótima ferramenta para trabalhar com SQL Server em um ambiente no local, no entanto, grande parte foi alterado desde a ADPs foram introduzidos no Access 2000. Agora, os usuários esperam seu banco de dados esteja disponível, onde quer que estejam.

## <a name="adp-support-and-the-future"></a>Suporte de ADP e para o futuro

ADPs continuam a funcionar em versões anteriores do Access. Você pode continuar a desenvolver aplicativos ADP e podemos continuará a dar suporte a versões anteriores do Access sob o standard [ciclo de vida de suporte](https://support.microsoft.com/gp/lifeselect). Não atualizaremos versões mais antigas do Access para suportar novas versões dos SQL Server ou SQL Azure. Portanto, você poderá encontrar problemas se você usar SQL Server 2012 ou versões posteriores com sua ADP. ADPs continuará dar suporte a SQL 2008 R2 e versões anteriores.

No futuro, os desenvolvedores ADP podem considerar várias possibilidades diferentes:

- **Converter um aplicativo do Access** – usando o Access, você pode importar suas tabelas em um novo aplicativo do Access e formulários para seu aplicativo são criados automaticamente para você. Você pode estender a funcionalidade dos formulários base Access cria para você e os usuários podem usar seu aplicativo na web. Embora algumas das funcionalidades que você usa em ADPs podem não estar disponíveis agora, esperam Microsoft para continuar a melhorias de foco do produto para esse tipo de aplicativo.

- **Converter um banco de dados da área de trabalho vinculado** – acesso continua a oferecer suporte à criação de bancos de dados da área de trabalho no formato de arquivo. accdb. Você pode converter seu aplicativo para o formato. accdb, incluindo todos os seus formulários existentes e relatórios e deixar os dados no SQL Server. Você pode vincular a banco de dados do SQL Server usando as tabelas vinculadas e seu aplicativo continuará a operar contra os mesmos dados.

- **Criar um aplicativo híbrido** – se seu aplicativo for grande e você não deseja converter tudo ao mesmo tempo, você pode importar os dados em um aplicativo do Access e o link para o banco de dados do SQL Server de um. accdb. Isso permite que você migra gradualmente, adicionando formulários e funcionalidade ao longo do tempo para seu aplicativo do Access, mantendo o seu aplicativo cliente como um. accdb com tabelas vinculadas ao banco de dados do SQL Server por trás do aplicativo do Access.

- **Atualizar para o .NET Framework** – seu aplicativo pode ser complexo suficiente que considerar a mudança para uma plataforma de desenvolvimento profissional, como o .NET Framework. SQL Server foi projetado para facilitar para utilizar sua infra-estrutura existente do banco de dados você já tenha criado e estende a funcionalidade do seu aplicativo sem reescrever significativamente seu código.
=== Acesso não inclui suporte para projetos de dados do Access (ADPs). Access introduz um novo tipo de aplicativo que permite que você crie um aplicativo baseado na web Access. Ao usar esse tipo de aplicativo, você pode criar aplicativos baseados na web que usam o poder do SQL Server no local ou na nuvem.

Em um aplicativo do Access no SharePoint Server, quando você cria uma tabela, uma consulta ou uma macro de dados no cliente do Access no qual você está criando tabelas, exibições ou disparadores em um banco de dados do SQL Server, usando o cliente do Access, você pode abrir o banco de dados para outros aplicativos que conn ect ao SQL Server. Isso permite que você compartilhe seus dados ou carregar dados de outros sistemas para seu aplicativo Access.

Com Office 365 e Access, você pode criar aplicativos que chegam seus usuários sem ter que se preocupar com os desafios de implantação, problemas de instalação de software ou compatibilidades de sistema operacional. Crie seu aplicativo em um único local e compartilhá-las pela web com o poder do SQL Azure e SQL Server.

[O SQL Azure](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview), a versão de nuvem do SQL Server, não oferece suporte a recursos que dependem projetos de dados do Access (ADPs) para operar. Para suportar ADPs em SQL Azure, Access exigiria alterações significativas.

Por esses motivos, Access não suporta ADPs. ADPs foram uma excelente ferramenta para trabalhar com o SQL Server em um ambiente local. No entanto, grande parte mudou desde que ADPs introduzidas no Access 2000. Agora, os usuários esperam seu banco de dados esteja disponível, onde quer que estejam.

## <a name="adp-support-and-the-future"></a>Suporte de ADP e para o futuro

ADPs continuam a funcionar em versões anteriores do Access. Você pode continuar a desenvolver aplicativos ADP e podemos continuará a dar suporte a versões anteriores do Access sob o standard [ciclo de vida de suporte](https://support.microsoft.com/lifecycle/search). Não atualizaremos versões mais antigas do Access para suportar novas versões dos SQL Server ou SQL Azure. Portanto, você poderá encontrar problemas se você usar SQL Server 2012 ou versões posteriores com sua ADP. ADPs continuará dar suporte a SQL 2008 R2 e versões anteriores.

No futuro, os desenvolvedores ADP podem considerar várias possibilidades diferentes:

- **Converter um aplicativo do Access** – usando o Access, você pode importar suas tabelas em um novo aplicativo do Access e formulários para seu aplicativo são criados automaticamente para você. Você pode estender a funcionalidade dos formulários base que o Access criará para você e os usuários podem usar seu aplicativo na web. Embora algumas das funcionalidades que você usa em ADPs podem não estar disponíveis agora, esperam Microsoft para continuar a melhorias de foco do produto para esse tipo de aplicativo.

- **Converter um banco de dados da área de trabalho vinculado** – acesso continua a oferecer suporte à criação de bancos de dados da área de trabalho no formato de arquivo. accdb. Você pode converter seu aplicativo para o formato. accdb, incluindo todos os seus formulários existentes e relatórios e deixar os dados no SQL Server. Você pode vincular ao banco de dados do SQL Server por meio de tabelas vinculadas e seu aplicativo continuará a operar contra os mesmos dados.

- **Criar um aplicativo híbrido** – se seu aplicativo for grande e você não deseja converter tudo ao mesmo tempo, você pode importar os dados em um aplicativo do Access e o link para o banco de dados do SQL Server de um. accdb. Isso permite que você migra gradualmente, adicionando formulários e funcionalidade ao longo do tempo para seu aplicativo do Access, enquanto mantém o seu aplicativo cliente como um. accdb com tabelas vinculadas ao banco de dados do SQL Server por trás do aplicativo do Access.

- **Atualizar para o .NET Framework** – seu aplicativo pode ser complexo o suficiente para considerar a mudança para uma plataforma de desenvolvimento profissional, como o .NET Framework. SQL Server foi projetado para facilitar a usar sua infraestrutura existente do banco de dados e estender a funcionalidade do seu aplicativo sem reescrever significativamente seu código.
>>>>>>> mestre

## <a name="conclusion"></a>Conclusion

Access foi projetado para se conectar a bancos de dados com a nuvem com base em tecnologias SharePoint Server e SQL Server e facilmente trabalhar com Office 365. Access foi projetado para ajudá-lo a criar rapidamente e compartilhar aplicativos de negócios orientadas a dados que ajudam a executar o seu negócio.

## <a name="see-also"></a>Confira também

<<<<<<< Cabeça
- [Novo no Access para desenvolvedores](https://msdn.microsoft.com/library/jj250134\(v=office.15\))
- [Ciclo de vida de suporte da Microsoft](https://support.microsoft.com/lifecycle/)
- [O banco de dados do Microsoft Azure SQL](https://msdn.microsoft.com/library/azure/ee336279.aspx)
=======
- [Novo no Access 2013 para desenvolvedores](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/new-in-access-for-developers)

>>>>>>> mestre

