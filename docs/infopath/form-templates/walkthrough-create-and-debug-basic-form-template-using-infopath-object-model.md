---
title: 'Passo a passo: Criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], passo a passo, modelos de formulário [InfoPath 2007], criação de modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, passo a passo
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Este tópico fornece um passo a passo da criação de um modelo de formulário de código gerenciado básico do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414337"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Passo a passo: Criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath

Este tópico fornece um passo a passo da criação de um modelo de formulário de código gerenciado básico do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 
  
## <a name="hello-world"></a>Olá, Mundo

No exemplo a seguir, você aprenderá a exibir uma caixa de diálogo de alerta simples usando o método [Alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do modelo de objeto compatível com o InfoPath 2003. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Criar um novo modelo de formulário do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003

1. Crie um novo modelo de formulário que funcione com o modelo de objeto compatível com o InfoPath 2003, conforme descrito em [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).
    
2. Nome do projeto de modelo de formulário HelloWorld e salve-o. 
    
   O sistema de projeto cria arquivos de código e projeto e abre um modelo de formulário em branco no modo de design do InfoPath. Agora você está pronto para adicionar manipuladores de eventos.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Adicionar um botão com um manipulador de eventos OnClick

1. Na seção **Controles** da guia **Página** Início, clique no controle **Botão** para inseri-lo na exibição. 
    
2. Clique com o botão direito do mouse no controle e clique em **Propriedades do Botão.**
    
3. Altere **o Rótulo** para Alerta.
    
4. Altere **a ID** para AlertID.
    
5. Clique **em Editar Código do Formulário.**
    
   Um esqueleto do manipulador de eventos para [o evento OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) é criado e o foco é move para o editor de código no Visual Studio 2012. Para obter mais informações sobre como trabalhar com manipuladores de eventos, consulte Adicionar um manipulador de eventos usando o modelo de objeto do [InfoPath 2003.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md) 
    
   Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão.
    
### <a name="add-form-code-to-the-event-handler"></a>Adicionar código de formulário ao manipulador de eventos

1. No manipulador **de eventos OnClick,** digite o seguinte código: 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Observe que uma lista drop-down do Microsoft IntelliSense é exibida depois que você digita cada ponto na linha de código. Todo o manipulador de eventos deve ter a seguinte aparência:
    
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
   > Como alternativa ao uso do método **Alerta,** você pode usar o método **MessageBox.Show** do namespace **System.Windows.Forms** para exibir uma caixa de mensagem. Para fazer isso, você deve adicionar uma referência ao assembly System.Windows.Forms, adicionar ou às diretivas no início do arquivo de código e digitar uma linha de código como a  `using System.Windows.Forms;`  `Imports System.Windows.Forms` seguinte:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Alternar para a janela do modo de design do InfoPath e clique no botão **Visualizar** na **guia** Página Início. 
    
3. Na janela **Visualizar,** clique no **botão** Alerta. 
    
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
    
3. Na janela Visualização **do** InfoPath, clique no **botão** Alerta. 
    
   O editor de código recebe o foco e a linha de ponto de interrupção é realçada.
    
4. No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código. 
    
   O **código do** método Alerta é executado e o "Hello World!" é exibido na janela visualização **do** InfoPath. 
    
## <a name="getting-the-current-users-name"></a>Obtendo o nome do usuário atual

Usando as classes do .NET Framework, você pode obter acesso à funcionalidade que não estava facilmente disponível no script. Neste exemplo, você aprenderá a usar as classes do .NET Framework para recuperar o nome do usuário atual.
  
### <a name="add-an-onload-event-handler"></a>Adicionar um manipulador de eventos OnLoad

1. Abra o projeto HelloWorld do InfoPath criado anteriormente.
    
2. Na guia **Exibir,** clique em **Mostrar Campos.**
    
3. Clique com o botão direito do mouse **no nó myFields** e clique em **Adicionar**.
    
4. In **Name**, type **employee**, then click **OK**.
    
5. Arraste o **nó do** funcionário para a exibição. 
    
6. Na guia **Desenvolvedor,** clique **em Carregar Evento**.
    
   Isso criará um manipulador de eventos para [o evento OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) e o foco será movedo para o editor de código. O código nesse manipulador de eventos será chamado sempre que o formulário for carregado. O procedimento a seguir mostra como adicionar código de formulário que recupera o nome do usuário ao manipulador de eventos. 
    
### <a name="add-form-code"></a>Adicionar código de formulário

1. No manipulador **de eventos OnLoad,** digite o seguinte código: 
    
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

2. Compile e visualize o formulário.
    
   A caixa de texto do funcionário agora deve ser preenchida com seu nome de usuário. 
    
Para obter informações sobre como implantar um modelo de formulário de código gerenciado, consulte Implantar modelos de formulário do [InfoPath com código.](how-to-deploy-infopath-form-templates-with-code.md) Para obter informações sobre o modelo de objeto do InfoPath e tarefas comuns de programação em modelos de formulário de código gerenciado que funcionam com o modelo de objeto compatível com o InfoPath 2003, consulte Noções básicas sobre o Modelo de Objeto do [InfoPath 2003.](understanding-the-infopath-2003-object-model.md) 
  
## <a name="see-also"></a>Confira também

- [Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [Modelos de objeto compatíveis com o InfoPath 2003](infopath-2003-compatible-object-models.md)
- [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

