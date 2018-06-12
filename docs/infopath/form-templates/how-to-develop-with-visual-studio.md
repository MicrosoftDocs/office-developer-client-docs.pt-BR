---
title: Desenvolver com o Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Você pode aprimorar a funcionalidade dos formulários do InfoPath bastante estendendo-as com código gerenciado desenvolvido no Visual Studio 2012. Em seguida, você pode publicar seus formulários com código bibliotecas de formulários no SharePoint Server 2013.
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765625"
---
# <a name="develop-with-visual-studio"></a>Desenvolver com o Visual Studio

Você pode aprimorar a funcionalidade dos formulários do InfoPath bastante estendendo-as com código gerenciado desenvolvido no Visual Studio 2012. Em seguida, você pode publicar seus formulários com código bibliotecas de formulários no SharePoint Server 2013.
  
Você pode iniciar a programação e a implantação de formulários do InfoPath com código gerenciado em três etapas de alto nível:
  
1. Instale o Visual Studio 2012 com o complemento do [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) . 
    
2. Definir sua linguagem de programação e, em seguida, escrever e depurar código no editor de código do Visual Studio 2012.
    
3. Quando você concluir a criação do formulário e desenvolvimento de seu código, o modelo de formulário pode ser publicado para o SharePoint Server 2013.
    
Aqui estão algumas razões para considerar a criação de formulários que são compatíveis com o SharePoint Server 2013:
  
- Formulários implantados para o SharePoint Server 2013 com o InfoPath Forms Services podem ser preenchidos em um navegador. Isso permite que os usuários que não têm instalado para abrir e usar os formulários do InfoPath.
    
- Projetar apenas uma versão do formulário. Formulários que são compatíveis com o Microsoft SharePoint Server também são compatíveis com o InfoPath Filler, mas os formulários que são compatíveis apenas com o InfoPath Filler não podem ser abertos no navegador.
    
Existem duas maneiras de publicar o formulário para o SharePoint: SharePoint soluções em área restrita e soluções implantados pelo administrador. Para obter mais informações sobre cada método de publicação e sugestões sobre qual método é melhor para seu cenário, consulte [Publicando formulários com código](publishing-forms-with-code.md). Por exemplo, soluções para soluções em área restrita, consulte [Exemplos de soluções em área restrita](sample-sandboxed-solutions.md).
  
## <a name="developing-with-visual-studio"></a>Desenvolvendo com o Visual Studio

Com o Visual Studio 2012 e o Microsoft Visual Studio Tools para o complemento aplicativos 2012 instalado, você estará pronto para começar a desenvolver soluções de código gerenciado do InfoPath.
  
### <a name="choosing-a-programming-language"></a>Escolher um idioma de programação

InfoPath fornece as opções para programar usando quatro versões do modelo de objeto do InfoPath em dois idiomas: Visual Basic e c#. As quatro versões do modelo de objeto fornecem compatibilidade com o InfoPath 2013, InfoPath, Office InfoPath 2007 e Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>Para especificar o modelo de objeto e da linguagem de programação

1. Com um projeto de modelo de formulário aberto no InfoPath designer, clique em **idioma** , na guia **desenvolvedor** . 
    
2. Na categoria **programação** da caixa de diálogo **Opções de formulário** , selecione o idioma que você deseja trabalhar com na lista suspensa **linguagem de código do modelo de formulário** . Em seguida, selecione a versão do modelo de objeto da lista suspensa de **versão de destino** . A opção de **versão de destino** é compatível com o InfoPath 2013 não tem um versão ano depois do nome do **InfoPath** . 
    
    > [!NOTE]
    > Nem todos os tipos de modelo de formulário suportam de código. Por exemplo, o tipo de modelo de formulário de **Lista do SharePoint** e **Partes do modelo** não suportam o código de formulário. Ao criar um tipo de modelo de formulário que não oferece suporte a código, a guia **desenvolvedor** não estará disponível. Além disso, somente alguns tipos de modelo de formulário suportam a todas as quatro versões do modelo de objeto. Por exemplo, o tipo de modelo de **Formulário em branco (InfoPath Filler)** oferece suporte a todas as quatro versões do modelo de objeto (e cria um modelo de formulário que são compatíveis apenas com o InfoPath Filler nessas versões), mas o modelo de **Formulário em branco** suporta apenas InfoPath 2013 e InfoPath (e cria os modelos de formulário compatíveis com o InfoPath Filler e o navegador). 
  
    Você pode definir um padrão de linguagem de programação para que o designer de formulários do InfoPath sempre iniciará com a versão de modelo de objeto e de idioma de sua escolha.
    
### <a name="to-set-the-default-programming-language"></a>Para definir o padrão de linguagem de programação

1. Clique na guia **arquivo** e, em seguida, clique em **Opções**.
    
2. Na seção **Geral** da caixa de diálogo **Opções do InfoPath** , clique em **Mais opções**.
    
3. Na guia **Design** da caixa de diálogo **Opções** , selecione a linguagem na seção **Padrões de programação** de programação padrão. 
    
### <a name="writing-code"></a>Escrevendo códigos

Agora, você pode começar a desenvolver com InfoPath 2013 e o Visual Studio 2012. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Para iniciar o Editor de código do Visual Studio

1. Abra um modelo de formulário no designer do InfoPath.
    
2. Na guia **desenvolvedor** , clique em **Editor de código** . 
    
> [!TIP]
> Também pode iniciar o editor de código e adicionar automaticamente os manipuladores de eventos para o formulário e controlar eventos usando os comandos na guia **desenvolvedor** , menus de contexto e outros métodos de interface do usuário. Para obter mais informações, consulte [Adicionar um manipulador de eventos](how-to-add-an-event-handler.md)
  

