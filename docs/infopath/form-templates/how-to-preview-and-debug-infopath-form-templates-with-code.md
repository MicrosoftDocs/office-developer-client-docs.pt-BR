---
title: Visualizar e depurar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [InfoPath 2007], modelos de formulário [InfoPath 2007], visualização, depuração [InfoPath 2007], modelos de formulário de código gerenciado, modelos de formulário [InfoPath 2007], depuração, InfoPath 2007, depuração de depuração de visualização modelos de formulário [infopath 2007] modelos de formulário, o InfoPath 2007, visualização de modelos de formulário
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath com o Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização. Quando você inicia a depuração de código de formulário, o projeto seja compilado e InfoPath exibe seu formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ele for encontrado, o foco é movido para o editor de código. Quando você passar um ponto de interrupção, o foco volta para a janela de visualização. Depuração paradas quando você fecha a janela de visualização.
ms.openlocfilehash: c33a7740d5f5dba1f8443f020007a2942bc0fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765609"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Visualizar e depurar modelos de formulário do InfoPath com código

Microsoft InfoPath com o Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização. Quando você inicia a depuração de código de formulário, o projeto seja compilado e InfoPath exibe seu formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ele for encontrado, o foco é movido para o editor de código. Quando você passar um ponto de interrupção, o foco volta para a janela de visualização. Depuração paradas quando você fecha a janela de visualização.
  
Você também pode modificar as opções de formato do modelo de formulário para visualizar e depurar usando uma função de usuário específico, um arquivo de dados de amostra, ou especificando-se o domínio ao qual o formulário será publicado. 
  
> [!NOTE]
> Não é possível depurar modelos de formulário depois que elas estejam implantadas em tempo de execução do Visual Studio 2012. Isso inclui os modelos de formulário que são compatíveis com o InfoPath, bem como aquelas que são compatíveis com o InfoPath e o navegador da Web usando o InfoPath Forms Services. No entanto, é possível fazer logon valores de um campo de código em tempo de execução para ajudá-lo com lógica de negócios de um modelo de formulário de depuração. Para obter informações sobre como fazer isso, consulte [Valores de Log para um campo para depuração](how-to-log-values-to-a-field-for-debugging.md). 
  
## <a name="debugging-in-preview-mode"></a>No modo de visualização de depuração

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>Depurar um projeto do InfoPath no modo de visualização

1. Criar ou abrir um modelo de formulário de código gerenciado do InfoPath no Visual Studio 2012.
    
2. Defina um ou mais pontos de interrupção em seu código de formulário no editor de código clicando na barra cinza à esquerda da linha de código onde deseja inserir um ponto de interrupção.
    
    Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.
    
3. No menu **Depurar** , clique em **Iniciar depuração**; ou pressione F5.
    
    O projeto será compilado e o formulário é exibido na janela de visualização.
    
4. Interagir com o formulário até encontrar uma linha de código que contém um ponto de interrupção.
    
    O foco retorna para o editor de código.
    
5. No menu **Depurar** , clique em **continuar**; ou pressione F5.
    
6. Quando tiver terminado de depuração, feche a janela de visualização; ou, no menu **Depurar** , clique em **Parar Depuração**.
    
> [!NOTE]
> Para depurar um modelo de formulário de código gerenciado do InfoPath ao usar um membro de modelo de objeto que requer confiança total, você deve configurar seu modelo de formulário, conforme descrito em [Visualizar e modelos de formulário de depuração que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  
## <a name="using-a-sample-data-file"></a>Usando um arquivo de dados de amostra

Por padrão, a depuração e visualização usa o arquivo de Template. XML que é criado quando um modelo de formulário é criado. Você pode criar seu próprio arquivo de dados e especificar para usá-la ao visualizar ou depuração usando um dos procedimentos a seguir. 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>Para especificar um arquivo de dados de amostra para usar durante a depuração ou pré-visualizar no Visual Studio Tools for Applications

1. Para exibir Template. XML, abra o modelo de formulário no modo de design do InfoPath.
    
2. Clique na guia **arquivo** , clique em **Salvar**, **Salvar o modelo de formulário como**e clique em **Arquivos de origem**.
    
3. Salvar arquivos de modelo de formulário para uma pasta e abra o arquivo Template. XML em um editor de texto.
    
4. Criar e salvar um arquivo com a mesma estrutura Template. XML com os dados de amostra que você deseja usar.
    
5. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
6. Clique na categoria de **visualização** da caixa de diálogo **Opções de formulário** e, em seguida, em **dados de amostra** , especifique o arquivo de dados de amostra que você criou na caixa **local do arquivo** . 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Especificando uma função de usuário para uso durante a depuração ou pré-visualizar

Se o formulário que você estiver trabalhando com tem funções de usuário definidas para ele, você poderá especificar uma função de usuário a ser usado durante a depuração ou visualizando o formulário. Para obter informações sobre como definir as funções de usuário, consulte a Ajuda do InfoPath para "função do usuário".
  
> [!NOTE]
> A opção para especificar uma função de usuário não estará disponível se a configuração de compatibilidade para o seu modelo de formulário está definida como **Formulário de navegador da Web**. Funções de usuário não são suportadas nos modelos de formulário abertos no navegador do InfoPath Forms Services. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>Para especificar uma função usar durante a depuração ou pré-visualizar

1. Se você estiver trabalhando no Visual Studio 2012, alterne para o InfoPath designer.
    
2. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
3. Clique na categoria de **visualização** da caixa de diálogo **Opções de formulário** e especifique a função de usuário para usar na caixa de lista suspensa **Preview como** . 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>A especificação de um domínio para uso durante a depuração ou pré-visualizar

Você pode visualizar um formulário como se ele foi publicado para um domínio específico. Essa configuração se aplicará somente se o nível de segurança do modelo de formulário é definido explicitamente como **domínio**.
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>Para especificar um domínio a ser usado durante a depuração ou pré-visualizar

1. Se você estiver trabalhando no Visual Studio 2012, alterne para o InfoPath designer.
    
2. Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
3. Clique na categoria de **visualização** da caixa de diálogo **Opções de formulário** e, em seguida, especifique o domínio a ser usado durante a visualização e depuração na caixa **domínio** . 
    
4. Clique na categoria de **segurança e confiança** da caixa de diálogo **Opções de formulários** , desmarque a caixa de seleção **determinar automaticamente o nível de segurança** e, em seguida, clique em **domínio**.
    

