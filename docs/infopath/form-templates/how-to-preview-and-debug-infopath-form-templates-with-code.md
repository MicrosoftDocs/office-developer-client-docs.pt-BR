---
title: Visualizar e depurar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Visualizando modelos de formulário [InfoPath 2007], modelos de formulário de depuração [InfoPath 2007], modelos de formulário [InfoPath 2007], visualização, depuração [InfoPath 2007], modelos de formulário de código gerenciado, modelos de formulário [InfoPath 2007], depuração, InfoPath 2007, depuração modelos de formulário, InfoPath 2007, visualizações de modelos de formulário
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: O Microsoft InfoPath com o Visual Studio 2012 permite a depuração executando o código de formulário no modo de visualização. Quando você inicia o código de formulário de depuração, seu projeto é compilado e o InfoPath exibe o formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ela é encontrada, o foco é movido para o editor de código. Quando você continua após um ponto de interrupção, o foco é movido de volta para a janela de visualização. A depuração pára quando você fecha a janela de visualização.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405237"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Visualizar e depurar modelos de formulário do InfoPath com código

O Microsoft InfoPath com o Visual Studio 2012 permite a depuração executando o código de formulário no modo de visualização. Quando você inicia o código de formulário de depuração, seu projeto é compilado e o InfoPath exibe o formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ela é encontrada, o foco é movido para o editor de código. Quando você continua após um ponto de interrupção, o foco é movido de volta para a janela de visualização. A depuração pára quando você fecha a janela de visualização.
  
Você também pode modificar as opções de formulário do modelo de formulário para visualizar e depurar usando uma função de usuário específica, um arquivo de dados de exemplo ou especificando o domínio no qual o formulário será publicado. 
  
> [!NOTE]
> Não é possível depurar modelos de formulário depois que eles são implantados no tempo de execução do Visual Studio 2012. Isso inclui modelos de formulário que são compatíveis apenas com o InfoPath, bem como aqueles que são compatíveis com o InfoPath e o navegador da Web usando o InfoPath Forms Services. No enTanto, é possível registrar valores em um campo a partir do código em tempo de execução para ajudar na depuração da lógica de negócios de um modelo de formulário. Para obter informações sobre como fazer isso, consulte [registrar valores em um campo para depuração](how-to-log-values-to-a-field-for-debugging.md). 
  
## <a name="debugging-in-preview-mode"></a>Depuração no modo de visualização

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>Para depurar um projeto do InfoPath no modo de visualização

1. Criar ou abrir um modelo de formulário de código gerenciado do InfoPath no Visual Studio 2012.
    
2. Defina um ou mais pontos de interrupção no seu código de formulário no editor de código clicando na barra cinza à esquerda da linha de código onde você deseja inserir um ponto de interrupção.
    
    Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.
    
3. No menu **depurar** , clique em **Iniciar Depuração**; ou pressione F5.
    
    O projeto será compilado e o formulário será exibido na janela de visualização.
    
4. Interagir com o formulário até que uma linha de código contendo um ponto de interrupção seja encontrada.
    
    O foco retorna para o editor de código.
    
5. No menu **depurar** , clique em **continuar**; ou pressione F5.
    
6. Ao concluir a depuração, feche a janela de visualização; ou no menu **depurar** , clique em **parar depuração**.
    
> [!NOTE]
> Para depurar um modelo de formulário de código gerenciado do InfoPath ao usar um membro de modelo de objeto que exija confiança total, você deve configurar o modelo de formulário conforme descrito nos [modelos de formulário Visualizar e depurar que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  
## <a name="using-a-sample-data-file"></a>Usando um arquivo de dados de exemplo

Por padrão, a depuração e a visualização usam o arquivo template. XML que é criado quando um modelo de formulário é criado. Você pode criar seu próprio arquivo de dados e especificar para usá-lo ao visualizar ou depurar usando um dos procedimentos a seguir. 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>Para especificar um arquivo de dados de exemplo a ser usado durante a depuração ou visualização no Visual Studio Tools for Applications

1. Para exibir o modelo. xml, abra o modelo de formulário no modo de design do InfoPath.
    
2. Clique na guia **arquivo** , clique em **salvar**, clique em **salvar modelo de formulário como**e, em seguida, clique em **arquivos de origem**.
    
3. Salve os arquivos de modelo de formulário em uma pasta e, em seguida, abra o arquivo template. xml em um editor de texto.
    
4. Crie e salve um arquivo com a mesma estrutura que template. XML com os dados de exemplo que você deseja usar.
    
5. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
6. Clique na categoria **Visualizar** da caixa de diálogo **Opções de formulário** e, em seguida, em dados de **exemplo** , especifique o arquivo de dados de exemplo que você criou na caixa local do **arquivo** . 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Especificando uma função de usuário a ser usada durante a depuração ou a visualização

Se o formulário com o qual você está trabalhando tiver funções de usuário definidas para ele, você poderá especificar uma função de usuário a ser usada durante a depuração ou visualização do formulário. Para obter informações sobre como definir funções de usuário, procure "função de usuário" na ajuda do InfoPath.
  
> [!NOTE]
> A opção para especificar uma função de usuário não estará disponível se a configuração de compatibilidade do modelo de formulário estiver definida como **formulário de navegador da Web**. Não há suporte para funções de usuário em modelos de formulário abertos no navegador a partir do InfoPath Forms Services. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>Para especificar uma função a ser usada durante a depuração ou a visualização

1. Se você estiver trabalhando no Visual Studio 2012, alterne para o designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na categoria **Visualizar** da caixa de diálogo **Opções de formulário** e, em seguida, especifique a função de usuário a ser usada na caixa de menu de **visualização como** . 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>Especificando um domínio a ser usado durante a depuração ou visualização

Você pode visualizar um formulário como se ele tenha sido publicado em um domínio específico. Essa configuração só será aplicada se o nível de segurança do modelo de formulário estiver explicitamente definido como **Domain**.
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>Para especificar um domínio a ser usado durante a depuração ou visualização

1. Se você estiver trabalhando no Visual Studio 2012, alterne para o designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na categoria **Visualizar** da caixa de diálogo **Opções de formulário** e, em seguida, especifique o domínio a ser usado durante a visualização e a depuração na caixa **domínio** . 
    
4. Clique na categoria **segurança e confiança** da caixa de diálogo **Opções de formulários** , desmarque a caixa de seleção **determinar automaticamente o nível de segurança** e clique em **domínio**.
    

