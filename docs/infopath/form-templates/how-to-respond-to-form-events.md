---
title: Responder a eventos de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- ordem de eventos [InfoPath 207], eventos [InfoPath 2007], responder, eventos [InfoPath 2007], ordem, InfoPath 2007, responder a eventos, classes EventArgs [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Você pode escrever código para responder a vários eventos que podem ocorrer quando um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, você adiciona manipuladores de eventos ao trabalhar com um modelo de formulário no modo de design.
ms.openlocfilehash: 0db3209dfe005f2a87ad65f3fc89b1714ec7d95c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407680"
---
# <a name="respond-to-form-events"></a>Responder a eventos de formulário

Você pode escrever código para responder a vários eventos que podem ocorrer quando um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, você adiciona manipuladores de eventos ao trabalhar com um modelo de formulário no modo de design.
  
Manipuladores de eventos do InfoPath sempre devem ser criados no modo de design porque o InfoPath adiciona automaticamente a declaração correta para coletar o evento para o método **InternalStartup** e insere o esqueleto de código do manipulador de eventos em um arquivo de código do formulário ( FormCode.cs ou FormCode. vb). Após ter criado um manipulador de eventos, você não deve alterar sua declaração no arquivo de código do formulário. 
  
Para obter informações sobre como criar os manipuladores de eventos do InfoPath, consulte [Adicionar um manipulador de eventos](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Visão geral das classes de evento

O modelo do InfoPath fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) implementa três classes que implementam os 12 eventos que podem ser gerados e manipulados pela lógica de negócios do modelo de formulário. A tabela a seguir lista cada um dos objetos de evento do InfoPath, os eventos aos quais estão associados e uma descrição da funcionalidade que fornecem. 
  
|**Nome**|**Eventos**|**Descrição**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Tiver](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |A classe **ButtonEvent** implementa o evento **clicado** que é gerado quando um controle de **botão** é clicado em um formulário.  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Carregando](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Enviar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |A classe **FormEvents** implementa os eventos que são específicos de um modelo de formulário do InfoPath em si:  <br/> **ContextChanged** <br/> Ocorre após o nó de contexto ser alterado.  <br/> **Carregando** <br/> Ocorre quando o modelo de formulário foi carregado, mas antes de qualquer visualização ter sido inicializada.  <br/> **Merge** <br/> Ocorre quando o comando **mesclar formulários** é invocado a partir da interface do usuário ou o InfoPath `/aggregate` é iniciado com a opção de linha de comando.  <br/> **Save** <br/> Ocorre quando os comandos **Save** ou **Save** as são usados a partir da interface do usuário ou quando os métodos [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) e [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe XmlForm são usados. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> **Sign** <br/> Ocorre após um conjunto de dados assinados ter sido selecionado para entrar na caixa de diálogo **assinaturas digitais** .  <br/> **Enviar** <br/> Ocorre quando o comando **Enviar** é usado a partir da interface do usuário ou o método [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) da **** classe XmlForm é usado.  <br/> **VersionUpgrade** <br/> Ocorre quando o número da versão do formulário que está sendo aberto é mais antigo do que o número da versão do modelo de formulário no qual ele se baseia.  <br/> **ViewSwitched** <br/> Ocorre após um modo de exibição de um formulário ter sido alternado com êxito.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Mudanças](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Alteração](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Conclui](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Implementa os eventos gerados por alterações nos dados no documento XML subjacente de uma instância de formulário:  <br/> **Mudanças** <br/> Ocorre após as alterações no documento XML subjacente de um formulário terem sido aceitas e após o evento **Validating** ter ocorrido.  <br/> **Alteração** <br/> Ocorre após as alterações no documento XML subjacente de um formulário terem sido feitas, mas antes de as alterações terem sido aceitas.  <br/> **Conclui** <br/> Ocorre após as alterações no documento XML subjacente de um formulário terem sido aceitas, mas antes do evento **Changed** ter ocorrido.  <br/> A **** classe xmlevent também implementa a propriedade [RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) , que Obtém ou define se o evento **Changed** será gerado quando ocorrer uma operação de desfazer ou refazer.  <br/> |
   
> [!NOTE]
>  Os eventos **Changed** e **Changing** são acionados apenas uma vez quando uma alteração é feita em um campo não vazio no formulário, enquanto os eventos comparáveis no InfoPath 2003 e o modelo de objeto compatível com o InfoPath 2003 fornecidos pelo [ Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) e [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) fogo duas vezes em alterações em um campo não vazio: uma vez quando o valor antigo é excluído e novamente quando o novo valor é inserido. 
  
## <a name="overview-of-the-eventargs-classes"></a>Visão geral das classes EventArgs

Cada um dos 12 eventos tem um objeto **EventArgs** associado ao evento que é passado para o manipulador de eventos para o evento para fornecer informações de estado e outras funcionalidades que podem ser usadas no código do manipulador de eventos. A tabela a seguir lista os eventos do InfoPath com seus objetos **EventArgs** associados e uma breve descrição da funcionalidade fornecida pelas propriedades e métodos do objeto. Para obter detalhes sobre propriedades específicas e métodos do objeto, clique no nome do objeto **EventArgs** na tabela e, em seguida, clique no link Membros no tópico. 
  
|**Event**|**Classe EventsArgs**|**Descrição**|
|:-----|:-----|:-----|
|**Tiver** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Obtém a ID do controle.  <br/> Obter um objeto **XPathNavigator** posicionado no nó XML mais interno do documento XML subjacente do formulário que contém o controle de **botão** .  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Obtém o tipo de alteração de contexto que foi executada quando o evento ocorreu.  <br/> Obtém um valor que indica se o evento de alteração de contexto ocorreu em resposta para desfazer ou refazer uma operação.  <br/> Obtém uma referência a um **XPathNavigator** posicionado no nó de contexto que disparou o evento.  <br/> |
|**Carregando** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Especifica o modo de exibição no qual o formulário será aberto após o carregamento.  <br/> Obtém uma referência ao objeto **XmlFormCancelEventArgs** .  <br/> Obtém um **IDictionary** contendo qualquer parâmetro de entrada especificado usando `/InputParameters` a opção de linha de comando ou especificado usando parâmetros de consulta em uma URL para abrir o formulário.  <br/> |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Obtém uma referência ao objeto **XmlFormCancelEventArgs** .  <br/> Obtém a contagem do número de formulários que estão sendo mesclados em uma operação de mesclagem.  <br/> Obtém o índice baseado em zero do formulário que está sendo mesclado no momento.  <br/> Obtém ou define um valor que é usado com a propriedade **Cancel** para determinar se deve cancelar apenas o formulário atual ou toda a operação de mesclagem.  <br/> Obtém um objeto **XPathNavigator** posicionado no nó raiz do documento XML subjacente do formulário que está sendo mesclado no momento.  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Executa a operação de salvamento solicitada pelo usuário.  <br/> Obtém uma referência ao objeto **SaveCancelEventArgs** que pode ser usado para cancelar o evento.  <br/> Obtém o nome do arquivo a ser usado no manipulador de eventos para o evento.  <br/> Obtém se a operação de salvamento será executada como uma operação de "salvar" ou como uma operação "salvar como".  <br/> |
|**Sign** <br/> |[Signeventargs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Obtém ou define se a caixa de diálogo **assinaturas digitais** deve ser exibida.  <br/> Obtém o conjunto de dados assináveis que geraram o evento.  <br/> |
|**Enviar** <br/> |[Submiteventargs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Obtém uma referência ao objeto **XmlFormCancelEventArgs** para cancelar o evento.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Obtém uma referência ao objeto **XmlFormCancelEventArgs** para cancelar o evento.  <br/> Obtém o número da versão do documento de formulário que está sendo atualizado.  <br/> Obtém o número da versão do modelo de formulário associado ao formulário que está sendo atualizado.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |A classe **ViewSwitchedEventArgs** não fornece propriedades e métodos para o evento diferente daqueles herdados de **System. Object**.  <br/> |
|**Mudanças** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Obtém um objeto **XPathExpression** que contém uma expressão XPath que retorna o nó que está sendo alterado no momento.  <br/> Obtém o novo valor para o nó que está sendo alterado.  <br/> Obtém um objeto **XPathNavigator** apontando para o nó que é o pai do nó que está sendo excluído.  <br/> Obtém o valor original do nó que está sendo alterado.  <br/> Obtém uma [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) enumeração de xmloperation que indica o tipo de operação que ocorreu quando o nó foi alterado.  <br/> Obtém um objeto **XPathNavigator** apontando para o nó que está sendo alterado.  <br/> Obtém um valor que indica se o nó que está sendo alterado é parte de uma operação de desfazer ou refazer.  <br/> |
|**Alteração** <br/> |[XmlChangingeventargs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Obtém um objeto **XmlFormCancelEventArgs** associado ao evento.  <br/> Herda todas as funcionalidades listadas acima para o **** objeto xmleventargs.  <br/> |
|**Conclui** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Cria um objeto [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) que contém informações de erro personalizadas com os valores especificados e o adiciona ao objeto [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) do formulário.  <br/> Herda todas as funcionalidades listadas acima para o **** objeto xmleventargs.  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Usando objetos EventArgs

Quando você cria um manipulador de eventos, o InfoPath cria a declaração do manipulador de eventos no código de formulário do projeto. Na declaração do manipulador de eventos, o InfoPath usa **e** como o nome do parâmetro que é passado para o manipulador de eventos. Esse parâmetro contém o objeto **EventArgs** associado ao manipulador de eventos para fornecer informações de estado e outras funcionalidades quando o evento ocorrer. 
  
Por exemplo, quando você cria um manipulador de eventos para o evento **loading** no modo de design (clicando no menu de **eventos de carregamento** na guia **desenvolvedor** ), o InfoPath adiciona a declaração para o manipulador de eventos que recebe o [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) objeto para o arquivo de código do formulário e, em seguida, abre o editor de código para que você possa adicionar seu código à seguinte declaração de manipulador de eventos. 
  
```cs
public void FormEvents_Loading(object sender, LoadingEventArgs e)
{
   // Write your code here.
}
```

```vb
Public Sub FormEvents_Loading(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Write your code here.
End Sub
```

Ao escrever código para um manipulador de eventos, você pode usar as propriedades e os métodos implementados pelo objeto **EventArgs** que é passado pelo parâmetro **e** . Por exemplo, no seguinte manipulador de eventos em **alteração** , a propriedade [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) do [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) objeto xmlchangingeventargs (que é herdada da [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) classe xmleventargs) é usada para verificar o valor do campo que acabou de ser alterado. Se o usuário alterou o campo e o deixou em branco, a propriedade [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) da classe [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) é acessada usando a propriedade [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) do objeto xmlchangingeventargs para exibir um erro para o usuário e **** a propriedade **XmlFormCancelEventArgs. Cancel** é definida como **true**, para cancelar o evento e reverter as alterações feitas pelo usuário.
  
```cs
public void field1_Changing(object sender, LoadingEventArgs e)
{
   // Determine whether there is a new value.
   if (e.NewValue == "")
   {
      // The value is blank, so display an error message
      // and roll back the changes.
      e.CancelableArgs.Message = 
         "You must supply a value for this field.";
      e.CancelableArgs.Cancel = true;
      return;
   }
}
```

```vb
Public Sub field1_Changing(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message 
      ' and roll back the changes.
      e.CancelableArgs.Message = _
         "You must supply a value for this field."
      e.CancelableArgs.Cancel = True
      Return
   End If
End Sub
```


