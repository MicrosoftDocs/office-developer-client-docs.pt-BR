---
title: Introdução rápida ao Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Um desenvolvedor de aplicativos pode personalizar um site Project Online (SharePoint hospedado) usando aplicativos autônomos e/ou complementos do projeto. Uma ampla gama de aplicativos é possível que variam de endereçamento às necessidades das pessoas envolvidas em um projeto para funções de suporte PMO, como um destes procedimentos:'
ms.openlocfilehash: 25a38a7c7359020058983e271067a87da29f1b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594527"
---
# <a name="from-0-to-60-with-project-online"></a>Introdução rápida ao Project Online

Um desenvolvedor de aplicativos pode personalizar um site Project Online (SharePoint hospedado) usando aplicativos autônomos e/ou complementos do projeto. Uma ampla gama de aplicativos é possível que variam de endereçamento às necessidades das pessoas envolvidas em um projeto para funções de suporte PMO, como um destes procedimentos:
  
- Entrada de dados de cartão de ponto simplificada para trabalhadores
- Aprovação de cartão eficiente para supervisores
- Supervisão de autorizações (compras e status) necessário para um projeto
- Verificação de status/integridade dos projetos ativos
- Relatório de problemas
- Alterar o relatório de Status de gerenciamento
    
Project Online inclui suporte de API para acomodar os cenários a seguintes:
  
- Para um suplemento do Project (SharePoint) hospedado:
    
  - Código (JavaScript, HTML, CSS) que está hospedado no SharePoint Online
  - Ativos que são baixados para o navegador e executados no SharePoint Online.  
  - Lógica de negócios que esteja no JavaScript   
  - Acesse os dados são como em/armazenados no Project Online ou do SharePoint (mas não estão limitado a):  
  - Campos personalizados  
  - Listas
    
- Para um projeto (SharePoint) hospedado em provedor suplemento:
    
  - Código que existe em um site externo para o site do Project Online 
  - Um site externo, que pode ser (mas não está limitado a):  
  - Outro site do SharePoint  
  - Serviço/aplicativo Web baseado em qualquer plataforma  
  - O site externo contém a lógica de negócios  
  - O navegador é redirecionado do Project Online site externo com tokens de acesso ao Project Online  
  - O site externo pode fazer chamadas para o SharePoint e o Project Online
    
- Para um suplemento externo/autônomo:
    
  - Usuário executa um aplicativo no seu dispositivo
  - Aplicativo autentica e chama APIs do Project Online diretamente
    

|Tipo de aplicativo|Implementação da API|Ambiente de destino|Exemplos de aplicativos|
|:-----|:-----|:-----|:-----|
|Projeto hospedado  <br/> |JSOM (modelo de objeto do Java Script)  <br/> REST  <br/> |Browser  <br/> |Entrada de cartão de ponto  <br/> Aprovação de cartão de ponto  <br/> Status do projeto  <br/> Relatório de problemas  <br/> |
|Provedor de projeto hospedado  <br/> |Biblioteca do cliente CSOM  <br/> |Site do Windows Azure/App  <br/> Ambiente de não-Windows (LÂMPADA, etc.)  <br/> |Validador de quadro de horários externo  <br/> Importador de projeto  <br/> |
|Externa/autônomo  <br/> |REST  <br/> CSOM  <br/> |REST - qualquer plataforma  <br/> CSOM - todas as plataformas com suporte do .NET  <br/> |Entrada de cartão de ponto  <br/> Migração de projetos para um novo site  <br/> Alterar o Status de gerenciamento.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>O que leva para começar a desenvolver aplicativos para o Project Online?

Os itens comuns necessários para o desenvolvimento de aplicativos do Project Online são uma conta do Project Online e testam dados--projetos e informações relacionados ao projeto que incluem atribuições, tarefas, recursos e campos personalizados. Um ambiente de desenvolvimento necessário também, mas as especificações do ambiente de desenvolvimento dependem do tipo de aplicativo e a interface de API necessária para o aplicativo. As próximas seções descrevem as necessidades de desenvolvimento para as interfaces de API três.
  
A documentação de referência descreve o modelo de objeto que é comum para todas as interfaces de três, bem como um mapa de entidade que mostra as relações entre os componentes do modelo de objeto.
  
## <a name="project-hosted-add-in-development-environment"></a>Ambiente de desenvolvimento de suplemento do Project hospedado

Um suplemento hospedado é um suplemento que reside no servidor e é baixado para um navegador para execução de tempo de execução. Suplementos hospedados podem usar as interfaces JSOM ou REST e escritos em JavaScript. Project Online fornece referências à biblioteca JSOM para execução de tempo de execução. Desenvolvimento considerando está em uma plataforma Windows, o acompanhamento de recursos necessários:
  
- O Visual Studio (preferencial) de 2015 ou Visual Studio 2013
    
- Ferramentas de desenvolvimento do Office para Visual Studio
    
- Idioma do JavaScript
    
Visite https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages para um aplicativo de amostra. 
  
Você pode baixar e executar a amostra em algumas etapas simples:
  
1. Baixe e abra o aplicativo de amostra
    
2. Atualizar o SiteURL na janela Propriedades
    
   Project Online examina o escopo de aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project Online. Se o acesso negado explicitamente em uma ou ambas as configurações, Project Online nega acesso às informações. Caso contrário, o acesso é concedido.
    
3. Habilite [sideloading](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) em seu site.  
    
4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Ambiente de desenvolvimento hospedado em provedor suplemento do Project

Suplementos do provedor hospedado são aplicativos escritos e que residem em qualquer plataforma da web. Eles podem se conectar e executar operações de dados usando o REST (ou CSOM para plataformas de Microsoft) API. Qualquer idioma e um ambiente com suporte para a interface REST podem ser usados para desenvolvimento. 
  
Um exemplo do ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:
  
-  O Visual Studio (preferencial) de 2015 ou Visual Studio 2013 
    
- Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecidos com o Visual Studio 2015 Professional e Enterprise Edition)
    
- .NET framework 4.0 ou mais recente
    
- [Pacote de CSOM do SharePoint Online](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas do CSOM) 
    
- Uma linguagem de programação, como c# 
    
Visite https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations para trabalhar scripts de amostra. 
  
Você pode executar o exemplo em algumas etapas:
  
1. Baixe e abra o aplicativo de amostra
    
2. Atualizar o SiteURL na janela Propriedades
    
   Project Online examina o escopo de aplicativo do suplemento e as permissões de usuário para controlar o acesso às informações no host do Project Online. Se o acesso negado explicitamente em uma ou ambas as configurações, Project Online nega acesso às informações. Caso contrário, o acesso é concedido.
    
3. Habilite [sideloading](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) em seu site. 
    
4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="externalstandalone-application-development-environment"></a>Ambiente de desenvolvimento de aplicativo externo/autônomo

Um aplicativo autônomo pode chamar Project Online usando o modelo de objeto de lado do cliente (CSOM) ou o REST para se comunicar com o Project Online para criar, recuperar, atualizar e excluir informações residentes no servidor. Este é um aplicativo cliente autônomo que depende do nível de acesso de usuário para executar. 
  
Um exemplo do ambiente de desenvolvimento do Windows para esse tipo de aplicativo inclui os seguintes itens:
  
- O Visual Studio (preferencial) de 2015 ou Visual Studio 2013 
    
- Ferramentas de desenvolvimento do Microsoft Office para Visual Studio (fornecidos com o Visual Studio 2015 Professional e Enterprise Edition)
    
- .NET framework 4.0 ou mais recente
    
- [Pacote de CSOM do SharePoint Online](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (para chamadas do CSOM) 
    
- Uma linguagem de programação, como c# 
    
Visite https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields para um aplicativo de amostra. 
  
Você pode executar o exemplo em algumas etapas:
  
1. Baixar o aplicativo de amostra
    
2. Fazer algumas alterações de acessar o site do Project Online — o nome do site, a conta de usuário e senha.
    
   Certifique-se de que o usuário tem acesso a todos os projetos. Project Online usa as permissões de usuário para controlar o acesso às informações no repositório de dados.
    
3. Adicione o assembly do SharePoint as referências usando o Console do Gerenciador de pacotes do Nuget, disponível no menu Ferramentas, digitando o seguinte no console do Nuget: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Compile o projeto.
    
5. Execute o projeto.
    
## <a name="next-steps"></a>Próximas etapas

Cada aplicativo de amostra possui um artigo para explicar os destaques dos trabalhando com a API de projeto individuais. Os artigos aparecem na lista a seguir, juntamente com alguns artigos que descrevem as relações de entidade, informações sobre o sistema de consulta e acessar os campos personalizados. 
  
- [Desenvolvendo um aplicativo do Project Online usando o modelo de objeto do cliente](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Desenvolvendo um suplemento Project Online usando o modelo de objeto JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Acessar campos personalizados da empresa no Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Confira também

Para documentação e exemplos relacionados ao Project Online e desenvolvimento de aplicativos usando CSOM, consulte o [Portal de desenvolvimento do Project](https://developer.microsoft.com/en-us/project).
    

