---
title: Introdução rápida ao Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Um desenvolvedor de aplicativos pode personalizar um site do Project Online (SharePoint hospedado) usando aplicativos autônomos e/ou os complementos do Project. Uma grande variedade de aplicativos é possível, desde o endereçamento de necessidades das pessoas envolvidas em um projeto até funções de suporte PMO, como qualquer uma das seguintes opções:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344405"
---
# <a name="from-0-to-60-with-project-online"></a>Introdução rápida ao Project Online

Um desenvolvedor de aplicativos pode personalizar um site do Project Online (SharePoint hospedado) usando aplicativos autônomos e/ou os complementos do Project. Uma grande variedade de aplicativos é possível, desde o endereçamento de necessidades das pessoas envolvidas em um projeto até funções de suporte PMO, como qualquer uma das seguintes opções:
  
- Entrada simplificada de dados do cartão de ponto para funcionários
- Aprovação eficiente de cartão de ponto para supervisores
- Supervisão de permissões (compras e status) necessárias para um projeto
- Verificação de status/saúde de projetos ativos
- Relatório de problemas
- Relatório de Status de Gerenciamento de Alterações
    
O Project Online inclui suporte à API para acomodar os seguintes cenários:
  
- Para um complemento hospedado do Project (SharePoint:
    
  - Código (JavaScript, HTML, CSS) hospedado no SharePoint Online
  - Ativos baixados para o navegador e executados no SharePoint Online.  
  - Lógica de negócios que está em JavaScript   
  - Acessar dados armazenados no Project Online ou no SharePoint, como (mas não está limitado a):  
  - Campos personalizados  
  - Listas
    
- Para um complemento hospedado pelo provedor do Project (SharePoint:
    
  - Código que existe em um site externo ao site do Project Online 
  - Um site externo, que pode ser (mas não está limitado a):  
  - Outro site do SharePoint  
  - Web App/Serviço criado em qualquer plataforma  
  - O site externo contém lógica comercial  
  - O navegador é redirecionado do Project Online para o site externo com tokens de acesso para o Project Online  
  - O site externo pode fazer chamadas para o SharePoint e o Project Online
    
- Para um complemento externo/autônomo:
    
  - O usuário executa um aplicativo em seu dispositivo
  - O aplicativo autentica e chama as APIs do Project Online diretamente
    

|Tipo de aplicativo|Implementação da API|Ambiente de destino|Exemplos de aplicativo|
|:-----|:-----|:-----|:-----|
|Projeto hospedado  <br/> |JSOM (modelo de objeto do Java Script)  <br/> REST  <br/> |Navegador  <br/> |Entrada de cartão de ponto  <br/> Aprovação de cartão de ponto  <br/> Status do Projeto  <br/> Relatório de Problemas  <br/> |
|Provedor de Projetos Hospedado  <br/> |Biblioteca de cliente CSOM  <br/> |Site/Aplicativo do Azure  <br/> Ambiente não Windows (LAMP, etc.)  <br/> |Validador de quadro de horários externo  <br/> Importador de Projeto  <br/> |
|Externo/autônomo  <br/> |REST  <br/> CSOM  <br/> |REST - qualquer plataforma  <br/> CSOM - qualquer plataforma com suporte do .NET  <br/> |Entrada de cartão de ponto  <br/> Migração de projetos para um novo site  <br/> Alterar o Status de Gerenciamento.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>O que é preciso para começar a desenvolver aplicativos para o Project Online?

Os itens comuns necessários para o desenvolvimento de aplicativos do Project Online são uma conta do Project Online e dados de teste – projetos e informações relacionadas ao projeto que incluem atribuições, tarefas, recursos e campos personalizados. Um ambiente de desenvolvimento também é necessário, mas as especificidades do ambiente de desenvolvimento dependem do tipo de aplicativo e da interface de API necessária para o aplicativo. As próximas seções descrevem as necessidades de desenvolvimento para as três interfaces de API.
  
A documentação de referência descreve o modelo de objeto que é comum para todas as três interfaces, bem como um mapa de entidade que mostra relações entre os componentes do modelo de objeto.
  
## <a name="project-hosted-add-in-development-environment"></a>Ambiente de desenvolvimento de add-in hospedado pelo Project

Um complemento hospedado é um add-in que reside no servidor e é baixado para um navegador para execução no tempo de execução. Os complementos hospedados podem usar as interfaces JSOM ou REST e são escritos em JavaScript. O Project Online fornece referências à biblioteca JSOM para execução do tempo de execução. Supondo que o desenvolvimento está em uma plataforma Windows, os recursos necessários são:
  
- Visual Studio 2015 (preferencial) ou Visual Studio 2013
    
- Ferramentas de desenvolvimento do Office para Visual Studio
    
- Linguagem JavaScript
    
Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages um aplicativo de exemplo. 
  
Você pode baixar e executar o exemplo em algumas etapas simples:
  
1. Baixar e abrir o aplicativo de exemplo
    
2. Atualizar o SiteURL na janela Propriedades
    
   O Project Online examina o escopo do aplicativo do complemento e as permissões do usuário para controle do acesso às informações no host do Project Online. Se o acesso for explicitamente negado em uma ou ambas as configurações, o Project Online negará o acesso às informações. Caso contrário, o acesso será concedido.
    
3. [Habilita o sideload](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) em seu site.  
    
4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Ambiente de desenvolvimento de add-in hospedado pelo provedor do Project

Os complementos hospedados pelo provedor são aplicativos escritos e residindo em qualquer plataforma Web. Eles podem se conectar e executar operações de dados usando a API REST (ou CSOM para plataformas Microsoft). Qualquer idioma e ambiente que suporte a interface REST pode ser usado para desenvolvimento. 
  
Um exemplo do ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:
  
-  Visual Studio 2015 (preferencial) ou Visual Studio 2013 
    
- Microsoft Office Development Tools para Visual Studio (fornecido com edições Do Visual Studio 2015 Professional e Enterprise)
    
- .NET Framework 4.0 ou mais novo
    
- [Pacote CSOM do SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas CSOM) 
    
- Uma linguagem de programação, como C # 
    
Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations scripts de exemplo de trabalho. 
  
Você pode executar o exemplo em algumas etapas:
  
1. Baixar e abrir o aplicativo de exemplo
    
2. Atualizar o SiteURL na janela Propriedades
    
   O Project Online examina o escopo do aplicativo do complemento e as permissões do usuário para controle do acesso às informações no host do Project Online. Se o acesso for explicitamente negado em uma ou ambas as configurações, o Project Online negará o acesso às informações. Caso contrário, o acesso será concedido.
    
3. [Habilita o sideload](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) em seu site. 
    
4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="externalstandalone-application-development-environment"></a>Ambiente de desenvolvimento de aplicativos autônomo/externo

Um aplicativo autônomo pode chamar o Project Online usando o Modelo de Objeto do Lado do Cliente (CSOM) ou REST para se comunicar com o Project Online para criar, recuperar, atualizar e excluir informações residindo no servidor. Esse é um aplicativo cliente autônomo que depende do nível de acesso do usuário a ser executado. 
  
Um exemplo do ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:
  
- Visual Studio 2015 (preferencial) ou Visual Studio 2013 
    
- Microsoft Office Development Tools para Visual Studio (fornecido com edições Do Visual Studio 2015 Professional e Enterprise)
    
- .NET Framework 4.0 ou mais novo
    
- [Pacote CSOM do SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas CSOM) 
    
- Uma linguagem de programação, como C # 
    
Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields um aplicativo de exemplo. 
  
Você pode executar o exemplo em algumas etapas:
  
1. Baixar o aplicativo de exemplo
    
2. Faça algumas alterações para acessar seu site do Project Online: nome do site, conta de usuário e senha.
    
   Verifique se o usuário tem acesso a todos os projetos. O Project Online usa permissões de usuário para reger o acesso a informações no armazenamento de dados.
    
3. Adicione o assembly do SharePoint às referências usando o Console do Gerenciador de Pacotes Nuget, disponível no menu Ferramentas digitando o seguinte no console nuget: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="next-steps"></a>Próximas etapas

Cada aplicativo de exemplo tem um artigo para explicar os destaques de como trabalhar com a API individual do Project. Os artigos aparecem na lista a seguir, juntamente com alguns artigos que descrevem as relações de entidade, as informações sobre o sistema de consulta e o acesso a Campos Personalizados. 
  
- [Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do lado do cliente](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Desenvolver um complemento do Project Online usando o Modelo de Objeto do JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Acessar campos personalizados da empresa no Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Confira também

Confira a documentação e exemplos relacionados ao desenvolvimento de aplicativos usando o CSOM e Project Online no [Portal de Desenvolvimento do Project](https://developer.microsoft.com/en-us/project).
    

