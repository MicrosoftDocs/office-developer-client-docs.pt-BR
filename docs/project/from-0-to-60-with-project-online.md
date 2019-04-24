---
title: Introdução rápida ao Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Um desenvolvedor de aplicativos pode personalizar um site do Project online (hospedado no SharePoint) usando aplicativos autônomos e/ou suplementos do Project. É possível que O alcance de vários aplicativos seja de acordo com as necessidades de endereçamento dos envolvidos em um projeto para as funções de suporte de PMO, como qualquer um dos seguintes:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344405"
---
# <a name="from-0-to-60-with-project-online"></a>Introdução rápida ao Project Online

Um desenvolvedor de aplicativos pode personalizar um site do Project online (hospedado no SharePoint) usando aplicativos autônomos e/ou suplementos do Project. É possível que O alcance de vários aplicativos seja de acordo com as necessidades de endereçamento dos envolvidos em um projeto para as funções de suporte de PMO, como qualquer um dos seguintes:
  
- Entrada de dados de cartão de timeSimplificada para trabalhadores
- Aprovação de cartão de visita eficiente para supervisores
- Supervisão de permissões (aquisição e status) necessárias para um projeto
- Verificação de status/integridade dos projetos ativos
- Relatório de problemas
- Relatório de status de gerenciamento de alterações
    
O Project online inclui suporte à API para acomodar os seguintes cenários:
  
- Para um suplemento hospedado do projeto (SharePoint):
    
  - Código (JavaScript, HTML, CSS) hospedado no SharePoint Online
  - Ativos que são baixados para o navegador e executados no SharePoint Online.  
  - Lógica de negócios que está em JavaScript   
  - Acessar dados que estão armazenados no Project online ou no SharePoint, como (mas não está limitado a):  
  - Custom fields (campos personalizados)  
  - Listas
    
- Para um suplemento hospedado pelo provedor do projeto (SharePoint):
    
  - Código existente em um site externo para o site do Project online 
  - Um site externo, que pode ser (mas não está limitado a):  
  - Outro site do SharePoint  
  - Aplicativo Web/serviço criado em qualquer plataforma  
  - O site externo contém lógica comercial  
  - O navegador é redirecionado do Project online para o site externo com tokens de acesso para o Project online  
  - O site externo pode fazer chamadas para o SharePoint e o Project online
    
- Para um suplemento externo/autônomo:
    
  - O usuário executa um aplicativo no dispositivo
  - O aplicativo autentica e chama as APIs do Project online diretamente
    

|Tipo de aplicativo|Implementação da API|Ambiente de destino|Exemplos de aplicativos|
|:-----|:-----|:-----|:-----|
|Projeto hospedado  <br/> |JSOM (modelo de objeto java script)  <br/> REST  <br/> |Navegador  <br/> |Entrada do cartão de um  <br/> Aprovação de cartão de visita  <br/> Status do projeto  <br/> Relatório de problemas  <br/> |
|Provedor de projeto hospedado  <br/> |Biblioteca de cliente do CSOM  <br/> |Site/aplicativo do Azure  <br/> Ambiente não Windows (lâmpada etc.)  <br/> |Validador de quadro de horários externo  <br/> Importador de projeto  <br/> |
|Externo/autônomo  <br/> |REST  <br/> CSOM  <br/> |RESTANTE-qualquer plataforma  <br/> CSOM-qualquer plataforma com suporte do .NET  <br/> |Entrada do cartão de um  <br/> Migração de projetos para um novo site  <br/> Status de gerenciamento de alterações.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>O que é necessário para começar a desenvolver aplicativos para o Project online?

Os itens comuns necessários para o desenvolvimento de aplicativos do Project online são uma conta do Project online e dados de teste, projetos e informações relacionadas ao projeto que incluem atribuições, tarefas, recursos e campos personalizados. Um ambiente de desenvolvimento também é necessário, mas as especificações do ambiente de desenvolvimento dependem do tipo de aplicativo e da interface de API necessárias para o aplicativo. As próximas seções descrevem as necessidades de desenvolvimento para as três interfaces de API.
  
A documentação de referência descreve o modelo de objeto que é comum para todas as três interfaces, bem como um mapa de entidade que mostra as relações entre os componentes do modelo de objeto.
  
## <a name="project-hosted-add-in-development-environment"></a>Ambiente de desenvolvimento de suplementos hospedados do Project

Um suplemento hospedado é um suplemento que reside no servidor e é baixado para um navegador para execução em tempo de execução. Os suplementos hospedados podem usar as interfaces JSOM ou REST e são escritos em JavaScript. O Project online fornece referências à biblioteca JSOM para execução em tempo de execução. Supondo que o desenvolvimento esteja em uma plataforma do Windows, os recursos necessários são os seguintes:
  
- Visual Studio 2015 (preferencial) ou Visual Studio 2013
    
- Ferramentas de desenvolvimento do Office para Visual Studio
    
- Linguagem JavaScript
    
Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para obter um exemplo de aplicativo. 
  
Você pode baixar e executar o exemplo em algumas etapas simples:
  
1. Baixe e abra o aplicativo de exemplo
    
2. Atualizar o SiteURL na janela de propriedades
    
   O Project online examina o escopo do aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project online. Se o acesso for explicitamente negado em uma ou ambas as configurações, o Project online negará o acesso às informações. Caso contrário, o acesso é concedido.
    
3. Habilite o [Sideload](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) no site.  
    
4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Ambiente de desenvolvimento de suplementos hospedados pelo provedor de projeto

Os suplementos hospedados pelo provedor são aplicativos escritos e residentes em qualquer plataforma Web. Eles podem conectar e realizar operações de dados usando a API REST (ou CSOM para plataformas Microsoft). Todos os idiomas e ambientes que dão suporte à interface REST podem ser usados para desenvolvimento. 
  
Um exemplo de ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:
  
-  Visual Studio 2015 (preferencial) ou Visual Studio 2013 
    
- Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecido com o Visual Studio 2015 Professional e Enterprise Editions)
    
- .NET Framework 4,0 ou mais recente
    
- [Pacote SHAREPOINTONLINE CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas CSOM) 
    
- Uma linguagem de programação, como C# 
    
Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations exemplos de scripts de amostra. 
  
Você pode executar o exemplo em algumas etapas:
  
1. Baixe e abra o aplicativo de exemplo
    
2. Atualizar o SiteURL na janela de propriedades
    
   O Project online examina o escopo do aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project online. Se o acesso for explicitamente negado em uma ou ambas as configurações, o Project online negará o acesso às informações. Caso contrário, o acesso é concedido.
    
3. Habilite o [Sideload](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) no site. 
    
4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="externalstandalone-application-development-environment"></a>Ambiente de desenvolvimento de aplicativos externos/autônomos

Um aplicativo autônomo pode chamar o Project online usando o modelo de objeto do lado do cliente (CSOM) ou o REST para se comunicar com o Project online para criar, recuperar, atualizar e excluir informações residentes no servidor. Este é um aplicativo cliente autônomo que depende do nível de acesso do usuário a ser executado. 
  
Um exemplo de ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:
  
- Visual Studio 2015 (preferencial) ou Visual Studio 2013 
    
- Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecido com o Visual Studio 2015 Professional e Enterprise Editions)
    
- .NET Framework 4,0 ou mais recente
    
- [Pacote SHAREPOINTONLINE CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas CSOM) 
    
- Uma linguagem de programação, como C# 
    
Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para obter um exemplo de aplicativo. 
  
Você pode executar o exemplo em algumas etapas:
  
1. Baixar o aplicativo de exemplo
    
2. Faça algumas alterações para acessar seu site do Project online, o nome do site, a conta do usuário e a senha.
    
   Verifique se o usuário tem acesso a todos os projetos. O Project online usa permissões de usuário para controlar o acesso a informações no repositório de dados.
    
3. Adicione o assembly do SharePoint às referências usando o console do Gerenciador de pacotes do NuGet, disponível no menu ferramentas, digitando o seguinte no console do NuGet: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="next-steps"></a>Próximas etapas

Cada aplicativo de exemplo tem um artigo para explicar os destaques do trabalho com a API de projeto individual. Os artigos aparecem na lista a seguir, juntamente com alguns artigos que descrevem as relações de entidade, as informações no sistema de consulta e o acesso a campos personalizados. 
  
- [Desenvolver um aplicativo do Project online usando o modelo de objeto do lado do cliente](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Desenvolver um suplemento do Project online usando o modelo de objeto do JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Acessar campos personalizados da empresa no Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Confira também

Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/en-us/project).
    

