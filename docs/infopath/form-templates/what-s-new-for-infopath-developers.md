---
title: O que há de novo para desenvolvedores do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- o que há de novo para desenvolvedores de [infopath 2007], [InfoPath 2007], o InfoPath 2007, o que há de novo de recursos, novos recursos [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath foi projetado para facilitar a criação de aplicativos sofisticados baseada em formulários, na plataforma do Microsoft SharePoint Server. Microsoft InfoPath 2013 junto com o InfoPath Forms Services e o Microsoft SharePoint Server 2013 possuem muitos recursos para desenvolvedores. InfoPath Forms Services, que está disponível no SharePoint Server 2013, permite que você implante um modelo de formulário do InfoPath em um SharePoint Server, para que usuários sem o cliente avançado do InfoPath podem abrir e preencher formulários do InfoPath em um navegador da Web.
ms.openlocfilehash: a11c6b4018e60a470197ecd7ffdf3b79a13658b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765715"
---
# <a name="whats-new-for-infopath-developers"></a>O que há de novo para desenvolvedores do InfoPath

InfoPath foi projetado para facilitar a criação de aplicativos sofisticados baseada em formulários, na plataforma do Microsoft SharePoint Server. Microsoft InfoPath 2013 junto com o InfoPath Forms Services e o Microsoft SharePoint Server 2013 possuem muitos recursos para desenvolvedores. InfoPath Forms Services, que está disponível no SharePoint Server 2013, permite que você implante um modelo de formulário do InfoPath em um SharePoint Server, para que usuários sem o cliente avançado do InfoPath podem abrir e preencher formulários do InfoPath em um navegador da Web.
  
Modelos de formulários criados usando o InfoPath 2013 continuam a oferecer suporte a lógica de negócios gravadas contra as classes e os membros do namespace **Microsoft.Office.InfoPath** , que funciona da mesma maneira para um formulário do InfoPath Filler e em um formulário aberto em uma Web aberto Navegador. Usando a lógica de negócios gravada esse modelo de objeto gerenciado e trabalhando com recursos do InfoPath Designer de verificação de design, você pode criar um modelo de formulário simples que poderá ser implantado em uma biblioteca de documentos devidamente configurado no SharePoint Server 2013, qual será executado no InfoPath filler e em um navegador da Web. 
  
## <a name="new-features-and-improvements"></a>Melhorias e novos recursos

As seções a seguir descrevem brevemente esses recursos e aperfeiçoamentos que são interessantes para desenvolvedores do InfoPath:
  
- Nova maneira de gravar e editar código
    
- Soluções em área restrita do SharePoint
    
- Publicar formulários com um clique
    
- Aprimorar a formulários de lista do SharePoint
    
- Formulários de host em páginas do Portal usando a web part de formulário do InfoPath
    
- Rica e formulários da Web
    
- Formulários de navegador compatível com padrões
    
- Fornecer aperfeiçoado das informações de segurança e de integridade com assinaturas digitais
    
- Novos controles
    
## <a name="new-way-to-write-and-edit-code"></a>Nova maneira de gravar e editar código

O Microsoft Visual Studio Tools for Applications IDE que foi integrado com o InfoPath 2010 foi removido do InfoPath 2013. Para escrever ou editar formulário código no InfoPath 2013 agora requer o Visual Studio 2012 com o complemento do [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. A experiência de programação não mudou radicalmente, mas agora você pode usar a experiência de desenvolvimento do Visual Studio completa ao escrever código gerenciado para formulários do InfoPath. 
  
As seções a seguir descrevem os recursos que foram adicionados pela primeira vez no InfoPath 2010 e o SharePoint Server 2010 e continuam a adicionar um valor para desenvolvedores usando o InfoPath 2013 e SharePoint Server 2013.
  
## <a name="sharepoint-server-sandboxed-solutions"></a>Soluções em área restrita do SharePoint Server

Com o InfoPath, é mais fácil do que nunca para implantar os formulários com código no SharePoint Server 2013. No Office InfoPath 2007, todos os formulários com código tinham a ser aprovado e carregados por um administrador de farm do SharePoint. Com suporte para soluções em área restrita no SharePoint Server 2013, os designers de formulário que possuem permissões de administração do conjunto de sites podem publicar agora a maioria dos formulários com código, diretamente aos seus sites do SharePoint. Uso de recurso excessivo de limites de uma configuração de cota de recurso no servidor. O administrador do conjunto de sites permanece no controle e faz com que as decisões de confiança sobre a solução. O administrador de farm pode ser participação ativa. Para obter mais informações sobre modelos de formulário InfoPath publicação como soluções em área restrita, consulte [Publicando formulários com código](publishing-forms-with-code.md).
  
## <a name="publish-forms-with-one-click"></a>Publicar formulários com um clique

InfoPath é projetado para tornar mais fácil do que nunca para publicar atualizações aos seus formulários.. Após a primeira vez que você publicar um modelo de formulário, em vez de clicar em várias caixas de diálogo, você pode concluir essa tarefa com um clique no botão novo **Publicar rápida** , que está disponível na barra de **Ferramentas de acesso rápido**e na nova Microsoft Office Backstage, que está disponível, clicando na guia **arquivo** . 
  
## <a name="enhance-sharepoint-list-forms"></a>Aprimorar a formulários de lista do SharePoint

Usando o InfoPath, agora você pode estender e aprimorar os formulários usados para criação, edição e exibição de itens em uma lista do SharePoint. Abrindo uma lista, clicando na guia **lista** , em **Ferramentas de lista**e, em seguida, clicando em **Personalizar formulário**, você pode automático gerar um formulário do InfoPath que se parece com o padrão, o formulário de lista do SharePoint-de-imediata. Em seguida, você pode personalizar e melhore a este formulário modificando o layout, criar exibições adicionais e adicionando regras e validação de dados no InfoPath. Quando tiver terminado de modificar seu formulário de lista aprimorada, você pode publicá-lo no SharePoint usando o novo um clique publicar o recurso no InfoPath.
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>Formulários de host em páginas do Portal usando a web part de formulário do InfoPath

No SharePoint Server 2013, é mais fácil do que nunca para hospedar seus formulários em páginas da Web usando a nova **web part de formulário do InfoPath**. No Microsoft Office SharePoint Server 2007, os usuários que desejam hospedar seus formulários do InfoPath em páginas da Web tem de escrever o código no Visual Studio. Agora, sem escrever uma única linha de código, você pode adicionar a **web part de formulário do InfoPath** a uma página de Web Parts e apontá-lo para seu formulário publicado. Você pode usar a **web part de formulário do InfoPath** para hospedar qualquer formulários de navegador do InfoPath que é publicado em uma biblioteca de formulário de lista ou do SharePoint. Também é possível conectá-la a outras Web Parts na página enviar ou receber dados. Para obter mais informações sobre como usar a **web part de formulário do InfoPath**, consulte [Trabalhando com a web part de formulário do InfoPath](http://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) no SDK do SharePoint 2010. 
  
## <a name="richer-web-forms"></a>Rica e formulários da Web

A diferença entre os formulários de navegador e cliente os recurso foi reduzida, criando um experiência de todos os usuários de preenchimento de formulário mais consistente. Controles e a funcionalidade que agora são suportadas nos formulários de navegador incluem o seguinte:
  
- Com marcadores, numerada e listas sem formatação
    
- Várias caixas de listagem de seleção
    
- Caixas de combinação
    
- Botões de imagem
    
- Recursos de hiperlink
    
- Seção e o grupo de opção 
    
- Controles de data e hora
    
- Escolha de pessoa/grupo
    
- Funcionalidade de filtragem
    
## <a name="standards-compliant-browser-forms"></a>Formulários de navegador compatível com padrões

Formulários de navegador do InfoPath agora são compatíveis com o conteúdo da Web acessibilidade diretrizes 2.0 (WCAG 2.0) AA, que permite que os designers de formulário Criar formulários que estão disponíveis para usuários com deficiências.
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>Fornecer aperfeiçoado das informações de segurança e de integridade com assinaturas digitais

InfoPath suporta CNG Cryptography Next Generation () assinado digitalmente o conteúdo. Para ajudar a garantir a integridade das informações que estão contidas em formulários, o cliente do InfoPath e o SharePoint Server 2013 fornecem os controles necessários para habilitar o único, co entrar e entrar no cenários para o formulário completo ou seções do formulário. Formulários podem ser assinados no Internet Explorer usando o controle de linha de assinatura do ActiveX. Formulários assinados podem ser exibidos em qualquer navegador compatíveis com o SharePoint Server 2013.
  
## <a name="new-controls"></a>Novos controles

InfoPath fornece um conjunto rico de controles que podem ser adicionados aos seus formulários. A lista a seguir descreve brevemente alguns dos novos controles:
  
- **Botão de imagem** — em vez de um retângulo cinza; Use qualquer imagem como um botão em seu formulário. 
    
- **Hiperlink** — permitem que os usuários insiram seus próprios hiperlinks ao preencher formulários. 
    
- **Seletor de pessoas/grupos** — permitem que os usuários verificar e nomes de contas e grupos de consulta ao preencher formulários. 
    
- **Seletor de entidade** — permitem que os usuários selecionem valores de listas externas em um servidor que está executando o SharePoint Server 2013 quando formulários. 
    
- **Linha de assinatura** — fornecer aos usuários uma linha ou da carimbo de imagem da assinatura, como um lacre inkan ou hanko, ao assinar digitalmente formulários. 
    
## <a name="see-also"></a>Confira também



[Desenvolvimento de modelos de formulário do InfoPath com código](developing-infopath-form-templates-with-code.md)
  
[Desenvolvimento de modelos de formulário usando o modelo de objeto do InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md)

