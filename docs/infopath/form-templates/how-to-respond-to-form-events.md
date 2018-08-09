---
title: Responder a eventos de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- ordem de eventos [infopath 207], [InfoPath 2007], de eventos respondendo, eventos [InfoPath 2007], pedidos, InfoPath 2007, reponding eventos, classes EventArgs [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Você pode escrever código para responder a diversos eventos que podem ocorrer como um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, você pode adicionar manipuladores de evento enquanto estiver trabalhando com um modelo de formulário no modo de design.
ms.openlocfilehash: 7968837fe0ed524104111bc3f2960860af51c75a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765647"
---
# <a name="respond-to-form-events"></a>Responder a eventos de formulário

Você pode escrever código para responder a diversos eventos que podem ocorrer como um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, você pode adicionar manipuladores de evento enquanto estiver trabalhando com um modelo de formulário no modo de design.
  
Manipuladores de eventos do InfoPath sempre devem ser criados no modo de design porque o InfoPath adiciona a declaração correta para baixar o evento para o método **InternalStartup** automaticamente e insere esqueleto do código do manipulador de eventos (de arquivo de código de um formulário FormCode.cs ou FormCode.vb). Depois de criar um manipulador de eventos, você não deve alterar sua declaração no arquivo de código do formulário. 
  
Para obter informações sobre como criar os manipuladores de eventos do InfoPath, consulte [Adicionar um manipulador de eventos](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Visão geral das Classes de evento

Modelo do InfoPath fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) implementa três classes que implementam os 12 eventos que podem ser gerados e manipulados pelo lógica de negócios do modelo de formulário. A tabela a seguir lista cada um dos objetos de evento do InfoPath, os eventos que eles estão associados e uma descrição da funcionalidade de que eles oferecem. 
  
|**Name**|**Eventos**|**Descrição**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |A classe **ButtonEvent** implementa o evento **Clicked** que é acionado quando um controle de **botão** é clicado em um formulário.  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Carregando](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sinal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Enviar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |A classe **FormEvents** implementa os eventos que são específicos para um modelo de formulário do InfoPath em si:  <br/> **ContextChanged** <br/> Ocorre após as alterações do nó de contexto.  <br/> **Carregando** <br/> Ocorre quando o modelo de formulário foi carregado, mas antes de todas as exibições foram inicializadas.  <br/> **Mesclar** <br/> Ocorre quando o comando **Mesclar Formulários** é invocado da interface do usuário ou InfoPath é iniciado com o `/aggregate` opção de linha de comando.  <br/> **Save** <br/> Ocorre quando os comandos **Salvar** ou **Salvar como** são usados da interface do usuário, ou quando são usados os métodos [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) e [Salvar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) .  <br/> **Sinal** <br/> Ocorre depois que um conjunto de dados assinados foi selecionado para assinar através da caixa de diálogo **Assinaturas digitais** .  <br/> **Enviar** <br/> Ocorre quando o comando **Enviar** é usado da interface do usuário, ou o método de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) da classe **XmlForm** é usado.  <br/> **VersionUpgrade** <br/> Ocorre quando o número de versão do formulário está sendo aberto é mais antigo do que o número da versão do modelo de formulário no qual ele se baseia.  <br/> **ViewSwitched** <br/> Ocorre após um modo de exibição de um formulário foi alternado com êxito.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Alterado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Alterando](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Validando](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Implementa os eventos gerados pelos alterações nos dados do documento XML subjacente de uma instância do formulário:  <br/> **Alterado** <br/> Ocorre após as alterações ao documento XML subjacente de um formulário terem sido aceitas e após o evento **Validando** ocorreu.  <br/> **Alterando** <br/> Ocorre depois que tiver sofrido alterações ao documento XML subjacente de um formulário, mas antes das alterações foram aceitas.  <br/> **Validando** <br/> Ocorre após as alterações ao documento XML subjacente de um formulário terem sido aceitas, mas antes do **alterado** o evento ocorreu.  <br/> A classe **XmlEvent** também implementa a propriedade [RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) , que obtém ou define se o evento **Changed** será gerado quando ocorre uma operação de desfazer ou refazer.  <br/> |
   
> [!NOTE]
>  Os eventos **alterado** e **alterando** acionada apenas uma vez quando é feita uma alteração em um campo não está em branco no formulário, enquanto os eventos comparáveis no InfoPath 2003 e o modelo de objeto compatível com o InfoPath 2003 fornecem pelo [ SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) incêndio namespace ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) e [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) duas vezes em alterações a um campo não está em branco: uma vez quando o valor antigo for excluído, e novamente quando o novo valor é inserido. 
  
## <a name="overview-of-the-eventargs-classes"></a>Visão geral das Classes EventArgs

Cada um dos 12 eventos ter um objeto **EventArgs** associado ao evento que são passados para o manipulador de eventos para o evento fornecer informações de estado e outras funcionalidades que podem ser usadas no evento código do manipulador. A tabela a seguir lista os eventos do InfoPath com seus objetos **EventArgs** associados e uma breve descrição da funcionalidade fornecida pelas propriedades e métodos do objeto. Para obter detalhes sobre as propriedades e métodos específicos do objeto, clique no nome do objeto **EventArgs** na tabela e, em seguida, clique no link membros no tópico. 
  
|**Event**|**Classe de EventsArgs**|**Descrição**|
|:-----|:-----|:-----|
|**Clicado** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Obtém a ID de controle.  <br/> Obtenha um objeto **XPathNavigator** posicionado no nó XML mais interno do documento XML subjacente do formulário que contém o controle de **botão** .  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Obtém o tipo de alteração de contexto que foi executada quando o evento ocorreu.  <br/> Obtém um valor indicando se o evento de alteração de contexto ocorreu em resposta às desfazer ou refazer uma operação.  <br/> Obtém uma referência a um **XPathNavigator** posicionadas no nó de contexto que gerou o evento.  <br/> |
|**Carregando** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Especifica o modo de exibição abrir o formulário após o carregamento.  <br/> Obtém uma referência ao objeto **XmlFormCancelEventArgs** .  <br/> Obtém um **IDictionary** que contenham uma entrada parâmetros especificados usando o `/InputParameters` opção de linha de comando ou especificado com parâmetros em uma URL de consulta para abrir o formulário.  <br/> |
|**Mesclar** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Obtém uma referência ao objeto **XmlFormCancelEventArgs** .  <br/> Obtém a contagem do número de formulários que estão sendo mesclados em uma operação de mesclagem.  <br/> Obtém o índice baseado em zero do formulário que está sendo mesclado.  <br/> Obtém ou define um valor que é usado com a propriedade **Cancel** para determinar se deseja cancelar apenas o formulário atual ou a operação mesclada inteira.  <br/> Obtém um objeto **XPathNavigator** posicionado no nó raiz do documento XML subjacente do formulário que está sendo mesclado.  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Executa o salvamento operação solicitada pelo usuário.  <br/> Obtém uma referência ao objeto **SaveCancelEventArgs** que pode ser usado para cancelar o evento.  <br/> Obtém o nome do arquivo a ser usado no manipulador de eventos para o evento.  <br/> Obtém se salvar operação será executada como uma operação de "Salvar" ou como uma operação de "Salvar como".  <br/> |
|**Sinal** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Obtém ou define se deseja exibir a caixa de diálogo **Assinaturas digitais** .  <br/> Obtém o conjunto de dados assinados que gerou o evento.  <br/> |
|**Enviar** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Obtém uma referência ao objeto **XmlFormCancelEventArgs** para cancelar o evento.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Obtém uma referência ao objeto **XmlFormCancelEventArgs** para cancelar o evento.  <br/> Obtém o número de versão do documento do formulário que estão sendo atualizado.  <br/> Obtém o número de versão do modelo de formulário associado ao formulário que estão sendo atualizado.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |A classe **ViewSwitchedEventArgs** não oferece quaisquer propriedades e métodos para o evento além daquelas herdadas de **Object**.  <br/> |
|**Alterado** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Obtém um objeto **XPathExpression** que contém uma expressão XPath que retorna o nó que está sendo alterado no momento.  <br/> Obtém o novo valor para o nó que está sendo alterado.  <br/> Obtém um objeto **XPathNavigator** apontando para o nó que é o pai do nó que está sendo excluído.  <br/> Obtém o valor original do nó que está sendo alterado.  <br/> Obtém uma enumeração [XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) que indica o tipo de operação que ocorreram quando o nó foi alterado.  <br/> Obtém um objeto **XPathNavigator** apontando para o nó que está sendo alterado.  <br/> Obtém um valor que indica se o nó que está sendo alterado faz parte de uma operação de desfazer ou refazer.  <br/> |
|**Alterando** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Obtém um objeto **XmlFormCancelEventArgs** associado ao evento.  <br/> Herda todas as funcionalidades listadas acima para o objeto **XmlEventArgs** .  <br/> |
|**Validando** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Cria um objeto [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) que contém informações de erro personalizada com os valores especificados e o adiciona ao objeto [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) do formulário.  <br/> Herda todas as funcionalidades listadas acima para o objeto **XmlEventArgs** .  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Usando os objetos EventArgs

Quando você cria um manipulador de eventos, o InfoPath cria a declaração do manipulador de eventos no código de formulário do projeto. Na declaração do manipulador de eventos, o InfoPath usa **e** como o nome do parâmetro que é passado ao manipulador de eventos. Este parâmetro contém o objeto **EventArgs** associado com o manipulador de eventos para fornecer informações de estado e outras funcionalidades quando o evento ocorre. 
  
Por exemplo, quando você cria um manipulador de eventos para o evento **Carregando** no modo de design (clicando em **Evento de carregamento** de menu na guia **desenvolvedor** ), o InfoPath adiciona a declaração para o manipulador de eventos que recebe o [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) objeto para o arquivo de código do formulário e, depois, abre o editor de código para que você possa adicionar seu código para a seguinte declaração do manipulador de eventos. 
  
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

Ao escrever código para um manipulador de eventos, você pode usar as propriedades e métodos implementados pelo objeto **EventArgs** que é passado por meio do parâmetro **f** . Por exemplo, no manipulador de eventos **Changing** seguir, a propriedade [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) do objeto [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) (que é herdada da classe [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) ) é usada para verificar o valor do campo que acabou de ser alterado. Se o usuário alterou o campo e deixado em branco, a propriedade de [mensagem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) da classe [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) for acessada usando a propriedade [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) do objeto **XmlChangingEventArgs** para exibir um erro para o usuário, e a propriedade **XmlFormCancelEventArgs.Cancel** é definida como **true**, para cancelar o evento e reverta as alterações feito ao usuário.
  
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


