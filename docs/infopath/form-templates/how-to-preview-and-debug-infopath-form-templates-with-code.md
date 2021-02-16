---
title: Visualizar e depurar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- visualização de modelos de formulário [infopath 2007], modelos de formulário de depuração [InfoPath 2007], modelos de formulário [InfoPath 2007], visualização,depuração [InfoPath 2007], modelos de formulário de código gerenciado, modelos de formulário [InfoPath 2007], depuração,InfoPath 2007, modelos de formulário de depuração,InfoPath 2007, visualização de modelos de formulário
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: O Microsoft InfoPath com Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização. Quando você inicia a depuração de código de formulário, seu projeto é compilado e o InfoPath exibe seu formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ele é encontrada, o foco se move para o editor de código. Quando você continua após um ponto de interrupção, o foco volta para a janela de visualização. A depuração para quando você fecha a janela de visualização.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405237"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Visualizar e depurar modelos de formulário do InfoPath com código

O Microsoft InfoPath com Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização. Quando você inicia a depuração de código de formulário, seu projeto é compilado e o InfoPath exibe seu formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ele é encontrada, o foco se move para o editor de código. Quando você continua após um ponto de interrupção, o foco volta para a janela de visualização. A depuração para quando você fecha a janela de visualização.
  
Você também pode modificar as opções de formulário do modelo de formulário para visualizar e depurar usando uma função de usuário específica, um arquivo de dados de exemplo ou especificando o domínio no qual o formulário será publicado. 
  
> [!NOTE]
> Não é possível depurar modelos de formulário depois que eles são implantados em tempo de executar do Visual Studio 2012. Isso inclui modelos de formulário que são compatíveis apenas com o InfoPath, bem como aqueles compatíveis com o InfoPath e o navegador da Web usando o InfoPath Forms Services. No entanto, é possível registrar valores em um campo do código em tempo de executar para ajudar na depuração da lógica de negócios de um modelo de formulário. Para obter informações sobre como fazer isso, consulte [Valores de log para um campo para depuração.](how-to-log-values-to-a-field-for-debugging.md) 
  
## <a name="debugging-in-preview-mode"></a>Depuração no modo de visualização

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>Para depurar um projeto do InfoPath no Modo de Visualização

1. Criar ou abrir um modelo de formulário de código gerenciado do InfoPath no Visual Studio 2012.
    
2. De definir um ou mais pontos de interrupção em seu código de formulário no editor de código clicando na barra cinza à esquerda da linha de código onde você deseja inserir um ponto de interrupção.
    
    Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.
    
3. No menu **Depurar,** clique **em Iniciar Depuração**; ou pressione F5.
    
    O projeto será compilado e o formulário será exibido na janela de visualização.
    
4. Interagir com o formulário até que uma linha de código contendo um ponto de interrupção seja encontrada.
    
    O foco retorna ao editor de código.
    
5. No menu **Depurar,** clique em **Continuar**; ou pressione F5.
    
6. Quando terminar a depuração, feche a janela de visualização; ou no menu **Depurar,** clique em **Parar Depuração.**
    
> [!NOTE]
> Para depurar um modelo de formulário de código gerenciado do InfoPath ao usar um membro do modelo de objeto que exija confiança total, você deve configurar seu modelo de formulário conforme descrito em Visualizar e Depurar Modelos de Formulário que Exigem Confiança [Total.](how-to-preview-and-debug-form-templates-that-require-full-trust.md) 
  
## <a name="using-a-sample-data-file"></a>Usando um arquivo de dados de exemplo

Por padrão, a depuração e a visualização usam template.xml arquivo criado quando um modelo de formulário é criado. Você pode criar seu próprio arquivo de dados e especificar usá-lo ao visualizar ou depurar usando um dos procedimentos a seguir. 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>Para especificar um arquivo de dados de exemplo a ser usado durante a depuração ou visualização no Visual Studio Tools for Applications

1. Para exibir template.xml, abra o modelo de formulário no modo de design do InfoPath.
    
2. Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click Source **Files**.
    
3. Salve os arquivos de modelo de formulário em uma pasta e abra o arquivo template.xml em um editor de texto.
    
4. Crie e salve um arquivo com a mesma estrutura template.xml com os dados de exemplo que você deseja usar.
    
5. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
6. Clique na categoria **Visualização** da caixa **de** diálogo Opções de Formulário e, em Exemplo de Dados, especifique o arquivo de dados de exemplo que você criou na caixa **Local do** arquivo.  
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Especificando uma função de usuário a ser usada durante a depuração ou visualização

Se o formulário com o qual você está trabalhando tiver funções de usuário definidas para ele, você poderá especificar uma função de usuário a ser usada durante a depuração ou visualização do formulário. Para obter informações sobre como definir funções de usuário, pesquise a ajuda do InfoPath para "função de usuário".
  
> [!NOTE]
> A opção para especificar uma função de usuário não estará disponível se a configuração de compatibilidade do seu modelo de formulário estiver definida como Formulário **do Navegador da Web.** As funções de usuário não são suportadas em modelos de formulário abertos no navegador do InfoPath Forms Services. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>Para especificar uma função a ser usada durante a depuração ou visualização

1. Se você estiver trabalhando no Visual Studio 2012, alternar para o designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na **categoria Visualização** da caixa **de** diálogo Opções de  Formulário e especifique a função de usuário a ser usada na caixa Desv. 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>Especificando um domínio a ser usado durante a depuração ou visualização

Você pode visualizar um formulário como se ele tivesse sido publicado em um domínio específico. Essa configuração só se aplicará se o nível de segurança do modelo de formulário estiver explicitamente definido como **Domínio.**
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>Para especificar um domínio a ser usado durante a depuração ou visualização

1. Se você estiver trabalhando no Visual Studio 2012, alternar para o designer do InfoPath.
    
2. Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**. 
    
3. Clique na **categoria Visualização** **da** caixa de diálogo Opções de Formulário e especifique o domínio a ser usado durante a visualização e a depuração na caixa **Domínio.** 
    
4. Clique na categoria Segurança  **e** Confiança da caixa  de diálogo Opções de Formulários, des marque a caixa de seleção Determinar automaticamente o nível de segurança e clique em **Domínio.**
    

