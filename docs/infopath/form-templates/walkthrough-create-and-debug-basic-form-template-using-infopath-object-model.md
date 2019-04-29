---
title: 'Passo a passo: criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- modelos de formulário [InfoPath 2007], passo a passo, modelos de formulário [InfoPath 2007], criação de modelos de formulário compatíveis com o InfoPath 2003, o InfoPath 2003
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Este tópico fornece um passo a passo para criar um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace Microsoft. Office. Interop. InfoPath. SemiTrust.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414337"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Passo a passo: criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath

Este tópico fornece um passo a passo para criar um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="hello-world"></a>Hello World

No exemplo a seguir, você aprenderá como exibir uma caixa de diálogo alerta simples usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do modelo de objeto compatível com o InfoPath 2003. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Criar um novo modelo de formulário do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003

1. Crie um novo modelo de formulário que funcione com o modelo de objeto compatível com o InfoPath 2003, conforme descrito em [criar um modelo de formulário usando o modelo de objeto do infopath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).
    
2. Nomeie o projeto de modelo de formulário HelloWorld e salve-o. 
    
   O sistema do projeto cria arquivos de código e de projeto e, em seguida, abre um modelo de formulário em branco no modo de design do InfoPath. Agora você está pronto para adicionar manipuladores de eventos.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Adicionar um botão com um manipulador de eventos OnClick

1. Na seção **controles** da guia **página inicial** , clique no controle **botão** para inseri-lo no modo de exibição. 
    
2. Clique com o botão direito do mouse no controle e clique em **Propriedades do botão**.
    
3. Altere o **rótulo** para alerta.
    
4. Altere a **ID** para Alertid.
    
5. Clique em **Editar código de formulário**.
    
   Um esqueleto de manipulador de eventos [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) para o evento onclick é criado e o foco é movido para o editor de código no Visual Studio 2012. Para obter mais informações sobre como trabalhar com manipuladores de eventos, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md). 
    
   Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão.
    
### <a name="add-form-code-to-the-event-handler"></a>Adicionar código de formulário ao manipulador de eventos

1. No manipulador **** de eventos OnClick, digite o seguinte código: 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Observe que uma lista suspensa do Microsoft IntelliSense é exibida após você digitar cada período na linha de código. O manipulador de eventos inteiro deve se parecer com o seguinte:
    
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
   > Como alternativa ao uso do método **Alert** , você pode usar o método **MessageBox. show** do namespace **System. Windows. Forms** para exibir uma caixa de mensagem. Para fazer isso, você deve adicionar uma referência ao assembly System. Windows. Forms, adicionar `using System.Windows.Forms;` ou `Imports System.Windows.Forms` às diretivas no início do seu arquivo de código e, em seguida, digitar uma linha de código como a seguinte:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Alterne para a janela modo de design do InfoPath e, em seguida, clique no botão **Visualizar** na guia **página inicial** . 
    
3. Na janela de **Visualização** , clique no botão **alerta** . 
    
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
    
3. Na janela de **Visualização** do InfoPath, clique no botão **alerta** . 
    
   O editor de código recebe o foco e a linha do ponto de interrupção é realçada.
    
4. No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código. 
    
   O código do método **Alert** é executado e o "Hello World!" o alerta é exibido na janela de **Visualização** do InfoPath. 
    
## <a name="getting-the-current-users-name"></a>Obtendo o nome do usuário atual

Usando as classes do .NET Framework, você pode obter acesso a funcionalidades que não estavam disponíveis no script. Neste exemplo, você aprenderá como usar as classes do .NET Framework para recuperar o nome do usuário atual.
  
### <a name="add-an-onload-event-handler"></a>Adicionar um manipulador de eventos OnLoad

1. Abra o projeto do InfoPath HelloWorld que você criou anteriormente.
    
2. Na guia **Exibir** , clique em **Mostrar campos**.
    
3. Clique com o botão **** direito do mouse no nó myFields e clique em **Adicionar**.
    
4. Em **nome**, digite **funcionário**e clique em **OK**.
    
5. Arraste o nó **Employee** para o modo de exibição. 
    
6. Na guia **desenvolvedor** , clique **em carregar evento**.
    
   Isso criará um manipulador de eventos para o evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) e o foco será movido para o editor de código. O código neste manipulador de eventos será chamado cada vez que o formulário for carregado. O procedimento a seguir mostra como adicionar o código de formulário que recupera o nome do usuário para o manipulador de eventos. 
    
### <a name="add-form-code"></a>Adicionar código de formulário

1. No manipulador de eventos **OnLoad** , digite o seguinte código: 
    
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

2. Compilar e visualizar o formulário.
    
   A caixa de texto do funcionário agora deve ser preenchida com seu nome de usuário. 
    
Para obter informações sobre como implantar um modelo de formulário de código gerenciado, consulte [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md). Para obter informações sobre o modelo de objeto do InfoPath e tarefas comuns de programação em modelos de formulário de código gerenciado que funcionam com o modelo de objeto compatível com o InfoPath 2003, consulte underStanding [The infopath 2003 Object Model](understanding-the-infopath-2003-object-model.md). 
  
## <a name="see-also"></a>Confira também

- [Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [Modelos de objeto compatíveis com o InfoPath 2003](infopath-2003-compatible-object-models.md)
- [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

