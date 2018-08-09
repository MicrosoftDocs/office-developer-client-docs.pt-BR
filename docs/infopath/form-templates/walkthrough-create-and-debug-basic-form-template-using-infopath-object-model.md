---
title: 'Passo a passo: Criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], passo a passo, modelos [InfoPath 2007], criando compatíveis com o InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, passo a passo de formulário
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Este tópico fornece um passo a passo de criação de um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto do InfoPath 2003 compatíveis fornecido pelo namespace SemiTrust.
ms.openlocfilehash: 3939cfcfdf2a8683fe614c5f49cc8b2719484ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765711"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Passo a passo: Criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath

Este tópico fornece um passo a passo de criação de um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto do InfoPath 2003 compatíveis fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="hello-world"></a>Hello World

O exemplo a seguir, você aprenderá como exibir uma caixa de diálogo alerta simples usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do modelo de objeto compatível com o InfoPath 2003. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Criar um novo modelo de formulário do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003

1. Crie um novo modelo de formulário que funciona com o modelo de objeto do InfoPath 2003 compatíveis, conforme descrito em [criar um formulário modelo usando o modelo de objeto do InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).
    
2. Nome do projeto de modelo de formulário HelloWorld e salvá-lo. 
    
   O sistema de projeto cria arquivos de projeto e de código e, depois, abre um modelo de formulário em branco no modo de design do InfoPath. Agora você está pronto para adicionar manipuladores de eventos.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Adicionar um botão com um manipulador de eventos OnClick

1. Na seção de **controles** na guia **página inicial** , clique no controle de **botão** para inseri-lo no modo de exibição. 
    
2. Com o botão direito no controle e, em seguida, clique em **Propriedades do botão**.
    
3. Altere o **rótulo** para o alerta.
    
4. Altere a **ID** para AlertID.
    
5. Clique em **Editar o código do formulário**.
    
   Um esqueleto de manipulador de evento para o evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) é criado e o foco é movido para o editor de código no Visual Studio 2012. Para obter mais informações sobre como trabalhar com manipuladores de eventos, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md). 
    
   Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão.
    
### <a name="add-form-code-to-the-event-handler"></a>Adicione o código de formulário para o manipulador de eventos

1. No manipulador de eventos **OnClick** , digite o código a seguir: 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Observe que é exibida uma lista de lista suspensa do Microsoft IntelliSense após digitar cada período em que a linha de código. O manipulador de eventos inteira deve se parecer com o seguinte:
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > Como alternativa para o uso do método de **alerta** , você pode usar o método **MessageBox. show** do namespace **System.Windows.Forms** para exibir uma caixa de mensagem. Para isso, você deve adicionar uma referência para o assembly System.Windows.Forms, adicionar `using System.Windows.Forms;` ou `Imports System.Windows.Forms` às diretivas no início do seu arquivo de código e digite uma linha de código como o seguinte:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Alternar para a janela do modo de design do InfoPath e, em seguida, clique no botão **Visualizar** na guia **página inicial** . 
    
3. Na janela de **visualização** , clique no botão de **alerta** . 
    
   Será exibida uma caixa de mensagem com o texto "Hello World!"
    
   O procedimento a seguir mostra como adicionar pontos de interrupção de depuração ao seu código de formulário.
    
### <a name="debug-form-code"></a>Depurar código de formulário

1. No editor de código, clique na barra cinza à esquerda da linha:
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.
    
2. No menu **Depurar**, clique em **Iniciar Depuração** (ou pressione F5). 
    
3. Na janela de **visualização** do InfoPath, clique no botão de **alerta** . 
    
   O editor de código recebe o foco e a linha de ponto de interrupção é realçada.
    
4. No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código. 
    
   O código de método de **alerta** é executado e "Olá mundo!" alerta é exibida na janela de **visualização** do InfoPath. 
    
## <a name="getting-the-current-users-name"></a>Obtendo o nome do usuário atual

Usando as classes do .NET Framework, você pode obter acesso à funcionalidade que não estava disponível facilmente no script. Neste exemplo, você vai aprender como usar as classes do .NET Framework para recuperar o nome do usuário atual.
  
### <a name="add-an-onload-event-handler"></a>Adicionar um manipulador de eventos OnLoad

1. Abra o projeto do InfoPath HelloWorld que você criou anteriormente.
    
2. Na guia **Exibir** , clique em **Mostrar campos**.
    
3. Com o botão direito no nó **myFields** e, em seguida, clique em **Adicionar**.
    
4. Em **nome**, tipo de **funcionário**, em seguida, clique em **Okey**.
    
5. Arraste o nó do **funcionário** para o modo de exibição. 
    
6. Na guia **desenvolvedor** , clique **Em evento OnLoad**.
    
   Isso irá criar um manipulador de eventos para o evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , e o foco é movido para o editor de código. O código no manipulador de eventos será chamado sempre que o formulário é carregado. O próximo procedimento mostra como adicionar o código de formulário que recupera o nome do usuário para o manipulador de eventos. 
    
### <a name="add-form-code"></a>Adicione o código de formulário

1. No manipulador de eventos **OnLoad** , digite o código a seguir: 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. Compilar e visualize o formulário.
    
   A caixa de texto de funcionário agora deve ser preenchida com seu nome de usuário. 
    
Para obter informações sobre como implantar um modelo de formulário de código gerenciado, consulte [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md). Para obter informações sobre o modelo de objeto do InfoPath e tarefas de programação comuns nos modelos de formulário de código gerenciado que funcionam com o modelo de objeto do InfoPath 2003 compatíveis, consulte [Compreendendo o modelo de objeto do InfoPath 2003](understanding-the-infopath-2003-object-model.md). 
  
## <a name="see-also"></a>Confira também

- [Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [InfoPath 2003 compatível com modelos de objeto](infopath-2003-compatible-object-models.md)
- [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

