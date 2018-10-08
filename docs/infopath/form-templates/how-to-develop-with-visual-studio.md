---
title: Desenvolvimento com o Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Você pode aprimorar a funcionalidade de formulários do InfoPath estendendo-as com código gerenciado desenvolvido no Visual Studio 2012. Em seguida, você pode publicar os formulários com o código para bibliotecas de formulários no SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401094"
---
# <a name="develop-with-visual-studio"></a>Desenvolvimento com o Visual Studio

Você pode aprimorar a funcionalidade de formulários do InfoPath estendendo-as com código gerenciado desenvolvido no Visual Studio 2012. Em seguida, você pode publicar os formulários com o código para bibliotecas de formulários no SharePoint Server 2013.
  
Você pode iniciar a programação e implantar os formulários do InfoPath com código gerenciado em três etapas de alto nível:
  
1. Instalar o Visual Studio 2012 com o complemento[Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807). 
    
2. Definir o idioma de programação, escrever e depurar código no editor de código do Visual Studio 2012.
    
3. Quando terminar de criar o formulário e desenvolver o código, o modelo de formulário poderá ser publicado para o SharePoint Server 2013.
    
Aqui estão alguns motivos para considerar a criação de formulários que são compatíveis com o SharePoint Server 2013:
  
- Formulários do SharePoint Server 2013 com o InfoPath Forms Services implantados podem ser preenchidos em um navegador. Isso permite aos usuários que não tenham o InfoPath instalado abrir e usar formulários do InfoPath.
    
- Criar apenas uma versão do formulário. Formulários que são compatíveis com o Microsoft SharePoint Server também são compatíveis com o InfoPath Filler, mas os formulários que são compatíveis somente com o InfoPath Filler não podem ser abertos no navegador.
    
Há duas maneiras para publicar seu formulário no SharePoint: solução de área restrita e implantação do administrador do SharePoint. Confira mais informações sobre cada método de publicação para obter sugestões sobre qual método é o mais adequado para seu cenário.Veja [formulários de publicação com o código](publishing-forms-with-code.md). Para exemplos de soluções de área restrita, consulte [soluções de área restrita exemplo](sample-sandboxed-solutions.md).
  
## <a name="developing-with-visual-studio"></a>Desenvolvendo com o Visual Studio

Com o Visual Studio 2012 e no Microsoft Visual Studio Tools for Applications 2012 aplicativos instalados, você está pronto para iniciar a desenvolver soluções de código de gerenciamento do InfoPath.
  
### <a name="choosing-a-programming-language"></a>Escolher uma linguagem de programação

InfoPath fornece opções para o programa em quatro versões do modelo de objeto do InfoPath em dois idiomas: Visual Basic e c#. As quatro versões do modelo de objeto proporcionam uma compatibilidade com o InfoPath 2013, o InfoPath, o Office InfoPath 2007 e o Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>Para especificar o modelo de programação de idioma e objetos

1. Com um projeto de modelo de formulário aberto no InfoPath designer, clique em **idioma** no **guia** do desenvolvedor. 
    
2. Na categoria **programação** das **opções de formulário** na caixa de diálogo, selecione o idioma que deseja para trabalhar com**a lista suspensa** no código de linguagem do modelo de formulário. Em seguida, selecione a versão do modelo de objeto da **versão de destino** na lista suspensa. A opção **versão de destino** compatível com o InfoPath 2013 não tem a versão do ano seguinte no**nome** Infopath. 
    
    > [!NOTE]
    > Nem todos os tipos de modelo de formulário suportam código. Por exemplo, na **lista do SharePoint** o tipo de modelo de formulário e as **partes de modelo** não suportam código do formulário. Ao criar um tipo de modelo de formulário que não suporte código, o guia**desenvolvedor** não estará disponível. Além disso, alguns tipos de modelos formulário suportam todas as quatro versões do modelo de objeto. Por exemplo, o modelo**formulário em branco (InfoPath Filler)** oferece suporte a todas as quatro versões do modelo de objeto (e cria um modelo de formulário compatíveis com o InfoPath Filler nessas versões), mas o **Formulário** modelo em branco suporta apenas o InfoPath 2013 e o InfoPath (e cria modelos de formulário compatíveis com o InfoPath Filler e navegador). 
  
    Você pode definir um padrão de linguagem de programação para que o designer de formulário do InfoPath sempre comece com a versão de idioma e o objeto de modelo de sua escolha.
    
### <a name="to-set-the-default-programming-language"></a>Para definir o padrão de linguagem de programação

1. Clique na guia **Arquivo** e, em seguida, em **Opções**.
    
2. Na **seção** geral** da caixa de diálogo** do InfoPath, clique em **mais opções**.
    
3. No guia **Design ** nas **opções** da caixa de diálogo, escolha a programação de idioma padrão na seção**programação padrões**. 
    
### <a name="writing-code"></a>Escrever códigos

Agora você pode começar desenvolver com o InfoPath 2013 e o Visual Studio 2012. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Para iniciar o Editor do Visual Studio Code

1. Abra um modelo de formulário no InfoPath designer.
    
2. Clique em **Editor de código** no **guia** desenvolvedor. 
    
> [!TIP]
> Você também pode iniciar o editor de código e adicionar automaticamente manipuladores de eventos para eventos de formulário e controle usando comandos na guia**desenvolvedor** menus de contexto e outros métodos de interface do usuário. Para saber mais, confira [adicionar um manipulador de eventos](how-to-add-an-event-handler.md)
  

