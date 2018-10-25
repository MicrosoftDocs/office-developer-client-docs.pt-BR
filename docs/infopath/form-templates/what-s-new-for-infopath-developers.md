---
title: Novidades para desenvolvedores do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- novidades [infopath 2007],recursos para desenvolvedores [InfoPath 2007],InfoPath 2007,novidades,novos recursos [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: O InfoPath foi projetado para facilitar a criação de aplicativos avançados baseados em formulários na plataforma do Microsoft SharePoint Server. O Microsoft InfoPath 2013 em conjunto com o Microsoft SharePoint Server 2013 e o InfoPath Forms Services têm muitos recursos para desenvolvedores. O InfoPath Forms Services, disponível no SharePoint Server 2013, permite implantar um modelo de formulário do InfoPath em um SharePoint Server para que usuários sem o cliente avançado do InfoPath possam abrir e preencher formulários do InfoPath em um navegador da Web.
ms.openlocfilehash: 5d469dfb99290054008271867f24d947a42efeee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385148"
---
# <a name="whats-new-for-infopath-developers"></a>Novidades para desenvolvedores do InfoPath

O InfoPath foi projetado para facilitar a criação de aplicativos avançados baseados em formulários na plataforma do Microsoft SharePoint Server. O Microsoft InfoPath 2013 em conjunto com o Microsoft SharePoint Server 2013 e o InfoPath Forms Services têm muitos recursos para desenvolvedores. O InfoPath Forms Services, disponível no SharePoint Server 2013, permite implantar um modelo de formulário do InfoPath em um SharePoint Server para que usuários sem o cliente avançado do InfoPath possam abrir e preencher formulários do InfoPath em um navegador da Web.
  
Os modelos de formulário criados com o InfoPath 2013 continuam a oferecer suporte à lógica de negócios escrita com base nas classes e nos membros do namespace **Microsoft.Office.InfoPath**, que funciona da mesma maneira para um formulário aberto no InfoPath Filler e em um formulário aberto em um navegador da Web. Usando a lógica de negócios escrita nesse modelo de objeto gerenciado e trabalhando com recursos de verificação de design no InfoPath Designer, você pode criar um único modelo de formulário que pode ser implantado em uma biblioteca de documentos devidamente configurada no SharePoint Server 2013, que será executada tanto no InfoPath Filler quanto em um navegador da Web. 
  
## <a name="new-features-and-improvements"></a>Novos recursos e aprimoramentos

As seções a seguir descrevem brevemente os recursos e aprimoramentos que podem interessar a desenvolvedores do InfoPath:
  
- Nova maneira de escrever e editar código
    
- Soluções de área restrita do SharePoint
    
- Publicar formulários com um único clique
    
- Aprimorar formulários de lista do SharePoint
    
- Hospedar formulários em páginas de portal usando a Web Part de formulário do InfoPath
    
- Formulários da Web mais avançados
    
- Formulários de navegador compatíveis com padrões
    
- Forneça segurança e integridade avançadas de informações com assinaturas digitais
    
- Novos controles
    
## <a name="new-way-to-write-and-edit-code"></a>Nova maneira de escrever e editar código

O IDE do Microsoft Visual Studio Tools for Applications que estava integrado ao InfoPath 2010 foi removido no InfoPath 2013. Para escrever ou editar código de formulário no InfoPath 2013, agora é necessário que o Visual Studio 2012 com o complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) esteja instalado. A experiência de programação propriamente dita não mudou muito, mas agora você pode usar toda a experiência de desenvolvimento do Visual Studio ao escrever código gerenciado em seus formulários do InfoPath. 
  
As seções a seguir descrevem os recursos que foram adicionados pela primeira vez no InfoPath 2010 e no SharePoint Server 2010 e que continuam a agregar valor para os desenvolvedores que usam o InfoPath 2013 e o SharePoint Server 2013.
  
## <a name="sharepoint-server-sandboxed-solutions"></a>Soluções de área restrita do SharePoint Server

Com o InfoPath, está mais fácil do que nunca implantar formulários com código no SharePoint Server 2013. No Office InfoPath 2007, todos os formulários com código precisavam ser aprovados e carregados por um administrador de farm do SharePoint. Com o suporte para soluções de área restrita no SharePoint Server 2013, os designers de formulários com permissões de administração de conjuntos de sites agora podem publicar a maioria dos formulários com código diretamente em seus sites do SharePoint. Uma configuração de cota de recursos no servidor limita o uso excessivo de recursos. O administrador do conjunto de sites permanece no controle e toma decisões de confiança sobre a solução. O administrador do farm pode ser dispensado. Para saber mais sobre como publicar modelos de formulário do InfoPath como soluções de área restrita, consulte [Publicação de formulários com código](publishing-forms-with-code.md).
  
## <a name="publish-forms-with-one-click"></a>Publicar formulários com um único clique

O InfoPath foi projetado para facilitar ainda mais o processo de publicação de atualizações nos seus formulários. Após publicar um modelo de formulário pela primeira vez, ao invés de clicar em várias caixas de diálogo, você pode concluir essa tarefa com um único clique no novo botão **Publicação Rápida**, disponível na **Barra de Ferramentas de Acesso Rápido** e no novo Microsoft Office Backstage, disponível na guia **Arquivo**. 
  
## <a name="enhance-sharepoint-list-forms"></a>Aprimorar formulários de lista do SharePoint

Usando o InfoPath, agora você pode estender e aprimorar os formulários usados para criar, editar e exibir itens em uma lista do SharePoint. Ao abrir uma lista clicando na guia **Lista** em **Ferramentas de Lista** e, em seguida, clicando em **Personalizar Formulário**, você pode gerar automaticamente um formulário do InfoPath que se parece com o formulário de lista padrão do SharePoint, que está pronto para uso. Em seguida, é possível personalizar e aprimorar esse formulário modificando o layout, criando exibições adicionais e adicionando regras e validação de dados no InfoPath. Quando terminar de modificar o formulário de lista aprimorado, você pode publicá-lo no SharePoint usando o novo recurso de publicação com um clique no InfoPath.
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>Hospedar formulários em páginas de portal usando a Web Part de formulário do InfoPath

No SharePoint Server 2013, está mais fácil do que nunca hospedar seus formulários em páginas da Web usando a nova **Web Part de Formulário do InfoPath**. No Microsoft Office SharePoint Server 2007, os usuários que desejam hospedar seus formulários do InfoPath em páginas da Web precisam escrever código no Visual Studio. Agora, sem escrever uma única linha de código, você pode adicionar a **Web Part de Formulário do InfoPath** a uma página de Web Parts e fazer com que ela aponte para o formulário publicado. Você pode usar a **Web Part de Formulário do InfoPath** para hospedar qualquer formulário de navegador do InfoPath que esteja publicado em um lista ou biblioteca de formulários do SharePoint. Você também pode conectá-la a outras Web Parts na página para enviar ou receber dados. Para saber mais sobre como usar a **Web Part de Formulário do InfoPath**, consulte [Trabalhar com a Web Part de Formulário do InfoPath](https://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) no SDK do SharePoint 2010. 
  
## <a name="richer-web-forms"></a>Formulários da Web mais avançados

A falta de recursos entre formulários de cliente e de navegador foi reduzida, criando uma experiência de preenchimento de formulários mais consistente para todos os usuários. Os controles e as funcionalidades agora disponíveis em formulários de navegador incluem:
  
- Listas com marcadores, numeradas e simples
    
- Caixas de listagem de seleção múltipla
    
- Caixas de combinação
    
- Botões de imagem
    
- Recursos de hiperlink
    
- Grupo e seção de escolha 
    
- Controles de data e hora
    
- Seletores de pessoas/grupos
    
- Funcionalidade de filtragem
    
## <a name="standards-compliant-browser-forms"></a>Formulários de navegador compatíveis com padrões

Os formulários de navegador do InfoPath agora estão em conformidade com o padrão WCAG 2.0 (Web Content Accessibility Guidelines 2.0) AA, que permite aos designers de formulários criar formulários disponíveis para usuários com deficiências.
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>Forneça segurança e integridade avançadas de informações com assinaturas digitais

O InfoPath oferece suporte para conteúdo assinado digitalmente pela CNG (Cryptography Next Generation). Para ajudá-lo a garantir a integridade das informações contidas nos seus formulários, o cliente do InfoPath e o SharePoint Server 2013 fornecem os controles necessários para permitir cenários de assinatura única, coassinatura e contra-assinatura para todo o formulário ou seções dele. Os formulários podem ser assinados no Internet Explorer usando o controle de linha de assinatura do ActiveX. Os formulários assinados podem ser exibidos em qualquer navegador compatível com o SharePoint Server 2013.
  
## <a name="new-controls"></a>Novos controles

O InfoPath fornece um conjunto mais avançado de controles que podem ser adicionados aos seus formulários. A lista a seguir descreve brevemente alguns dos novos controles:
  
- **Botão de imagem**: ao invés de um retângulo cinza, é possível usar qualquer imagem como um botão no seu formulário. 
    
- **Hiperlink**: deixe que os usuários insiram seus próprios hiperlinks ao preencherem formulários. 
    
- **Seletor de pessoas/grupos**: deixe que os usuários verifiquem e consultem nomes de contas e grupos ao preencherem formulários. 
    
- **Seletor de entidades**: deixe que os usuários selecionem valores de listas externas em um servidor que esteja executando o SharePoint Server 2013. 
    
- **Linha de assinatura**: forneça aos usuários uma linha de assinatura ou imagem de carimbo, como um selo inkan ou hanko, ao assinar formulários digitalmente. 
    
## <a name="see-also"></a>Confira também



[Desenvolver modelos de formulário do InfoPath com código](developing-infopath-form-templates-with-code.md)
  
[Desenvolver modelos de formulário usando o modelo de objeto do InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md)

