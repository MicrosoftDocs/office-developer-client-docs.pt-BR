---
title: 'Passo a passo: criar um modelo de formulário básico com código'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- modelos de formulário do [InfoPath 2007], criar código gerenciado, modelos de formulário de código gerenciado do [InfoPath 2007], criação, modelos de formulário [InfoPath 2007], passo a passo, InfoPath 2007, passo a passo
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: No Microsoft InfoPath, você pode escrever lógica de negócios no Visual Basic ou no C# abrindo um modelo de formulário no designer do InfoPath e então usando um dos comandos da interface do usuário para adicionar um manipulador de eventos, que abrirá o ambiente de desenvolvimento do Visual Studio 2012 para que seu código seja escrito.
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420644"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>Passo a passo: criar um modelo de formulário básico com código

No Microsoft InfoPath, você pode escrever lógica de negócios no Visual Basic ou no C# abrindo um modelo de formulário no designer do InfoPath e então usando um dos comandos da interface do usuário para adicionar um manipulador de eventos, que abrirá o ambiente de desenvolvimento do Visual Studio 2012 para que seu código seja escrito. Por padrão, projetos de modelo de formulário criados usando o Visual Studio 2012 funcionam no modelo de objeto de código gerenciado fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
Primeiro, este passo a passo mostra como criar um aplicativo Hello World simples usando C# ou Visual Basic no ambiente de desenvolvimento do Visual Studio 2012. O passo a passo conclui com um exemplo de código que mostra como usar a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar o nome do usuário atual e preencher um controle **Caixa de Texto** com esse valor. 
  
## <a name="prerequisites"></a>Pré-requisitos

Para concluir este passo a passo usando o ambiente de desenvolvimento do Visual Studio 2012, será necessário:
  
- Microsoft InfoPath com Visual Studio 2012 instalado.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Hello World no Visual Studio Tools for Applications

No passo a passo a seguir, você aprenderá a escrever código no ambiente de desenvolvimento do Visual Studio 2012 para exibir uma caixa de diálogo de alerta simples escrevendo um manipulador de eventos para o evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) da classe [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , associado ao controle **Botão**. 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Criar um novo projeto e especificar a linguagem de programação

1. Inicie o designer do InfoPath e então clique duas vezes no modelo de formulário **Em Branco (Editor do InfoPath)**. 
    
2. Para especificar qual linguagem de programação será usada, clique no **Botão do Office**, clique em **Opções de Formulário**, clique em **Programação** na lista **Categoria** e então selecione **Visual Basic** ou **C#** na lista suspensa **Linguagem do código do modelo de formulário**. 
    
   > [!NOTE]
   > As outras opções de linguagem de programação da lista **Linguagem do código do modelo de formulário** oferecem compatibilidade com versões anteriores do InfoPath. As opções **C# (Compatível com o InfoPath 2007)** e **Visual Basic (Compatível com o InfoPath 2007)** funcionarão com os procedimentos deste tópico. No entanto, para usar as opções **C# (Compatível com o InfoPath 2003)** e **Visual Basic (Compatível com o InfoPath 2003)**, consulte [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Agora você está pronto para adicionar um controle **Botão** e criar seu manipulador de eventos. 
    
### <a name="add-a-button-control-and-event-handler"></a>Adicionar um controle Botão e um manipulador de eventos

1. No grupo **Controles**, clique no controle **Botão** para adicioná-lo ao formulário. 
    
2. Clique duas vezes no controle **Botão**, digite Hello para a propriedade **Rótulo** na guia **Propriedades** da faixa de opções e então clique em **Código Personalizado**. Quando solicitado, salve o formulário e nomeie-o como HelloWorld.
    
   Isso abrirá o ambiente **Visual Studio Tools for Applications** com o cursor no manipulador de eventos para o evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) do controle **Botão**. 
    
   Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão. 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>Adicione código do "Hello World" ao manipulador de eventos e visualize o formulário

1. No esqueleto do manipulador de eventos, digite:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   O código do seu modelo de formulário deve ser semelhante ao seguinte:
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. Alterne para a janela do designer do InfoPath.
    
3. Clique no botão **Visualizar** na guia **Página Inicial**. 
    
4. Clique no botão Hello no formulário. 
    
   Será exibida uma caixa de mensagem com o texto "Hello World!"
    
   O procedimento a seguir mostra como adicionar pontos de interrupção de depuração ao seu código de formulário.
    
### <a name="debug-form-code"></a>Depurar código de formulário

1. Alterne novamente para a janela do Visual Studio 2012.
    
2. Clique na barra cinza à esquerda da linha:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.
    
3. No menu **Depurar**, clique em **Iniciar Depuração** (ou pressione F5). 
    
4. Na janela **Visualizar** do InfoPath, clique no botão Hello do formulário. 
    
5. O editor de códigos do Visual Studio 2012 receberá o foco e a linha do ponto de interrupção será realçada.
    
6. No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código. 
    
7. O código do manipulador de eventos é executado e a mensagem "Hello World!" é exibida. 
    
8. Clique em **OK** para retornar ao editor de código do Visual Studio 2012 e clique em **Interromper a Depuração** no menu **Depurar** (ou pressione Ctrl+Alt+Break). 
    
## <a name="getting-the-current-users-name"></a>Obtendo o nome do usuário atual

No exemplo a seguir, você aprenderá a usar a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar o nome do usuário atual e preencher o valor de um controle **Caixa de Texto** usando um manipulador de eventos para o evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
O preenchimento do controle **Caixa de Texto** é realizado com uma instância da classe [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para gravar o nome do usuário atual no nó XML ao qual o controle está associado. 
  
Primeiro, a propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é chamada para recuperar uma instância da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa o documento XML subjacente do formulário. O objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) então chama o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) que cria o objeto **XPathNavigator** e o posiciona no nó raiz da fonte de dados principal do formulário. 
  
O método [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) da classe **XPathNavigator** é chamado para selecionar o campo funcionário na fonte de dados do formulário. Por fim, o método [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) é chamado para definir o valor do campo com a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) . 
  
Confira mais informações sobre o trabalho com **System.Xml** em modelos de formulário de código gerenciado em [Trabalhar com as classes XPathNavigator e XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="add-a-loading-event-handler"></a>Adicionar um manipulador de eventos de Carregamento

1. Abra o modelo de formulário HelloWorld criado no passo a passo anterior no designer do InfoPath.
    
2. Na guia **Exibir**, selecione **Mostrar Campos**.
    
3. Clique com o botão direito do mouse na pasta **myFields** e então clique em **Adicionar**.
    
4. Em **Nome**, digite funcionário e clique em **OK**.
    
5. Arraste o campo funcionário para a exibição. 
    
6. Na guia **Desenvolvedor**, clique em **Evento Loading**.
    
   Isso criará um manipulador de eventos para o evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) e moverá o foco para esse manipulador de eventos no editor de códigos. 
    
7. No editor de códigos, digite o seguinte:
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. Alterne para a janela de design de formulários do InfoPath e então clique no botão **Visualizar** na guia **Página Inicial** para visualizar o formulário. 
    
   O campo funcionário deverá ser automaticamente preenchido com o seu nome de usuário. 
    
## <a name="next-steps"></a>Próximas etapas

- Confira mais informações sobre como trabalhar com manipuladores de eventos para outros controles e eventos em [Adicionar um Manipulador de Eventos](how-to-add-an-event-handler.md).
    
- Confira mais informações sobre como visualizar e depurar códigos em modelos de formulário em [Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md).
    
- Confira mais informações sobre como implantar um modelo de formulário de código gerenciado em [Implantar os modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).
    
- Para saber mais sobre o modelo de objeto e as tarefas comuns de programação do InfoPath em modelos de formulário de código gerenciado, consulte [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md).
    
## <a name="see-also"></a>Confira também

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

