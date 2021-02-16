---
title: Responder a eventos de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], respondendo a eventos,modelos de formulário compatíveis com o InfoPath 2003, respondendo a eventos de formulário
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Você pode escrever código para responder a vários eventos que podem ocorrer à medida que um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, crie manipuladores de eventos no designer do InfoPath.
ms.openlocfilehash: b7347f882df991e64bdf4e76c471b1220a84dc58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433490"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Responder a eventos de formulário usando o modelo de objeto do InfoPath 2003

Você pode escrever código para responder a vários eventos que podem ocorrer à medida que um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, crie manipuladores de eventos no designer do InfoPath.
  
Os manipuladores de eventos do InfoPath devem ser criados no designer do InfoPath porque, ao usar o modelo de objeto compatível com o InfoPath 2003, o InfoPath adiciona automaticamente a declaração correta e aplica um atributo ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) no arquivo de código de um formulário (FormCode.cs ou FormCode.vb) para identificar e agregar o manipulador de eventos. Depois de criar um manipulador de eventos, você não deve alterar sua declaração e atributo no arquivo de código do formulário. 
  
Para obter informações sobre como criar manipuladores de eventos do InfoPath, consulte Adicionar um manipulador de eventos usando o modelo de objeto do [InfoPath 2003.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
## <a name="overview-of-the-event-objects"></a>Visão geral dos objetos Event

O modelo de objeto compatível com InfoPath 2003 implementa nove objetos de evento que são expostos no namespace [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) A tabela a seguir lista cada um dos objetos de evento do InfoPath, os manipuladores de eventos aos que estão associados e uma descrição da funcionalidade que eles fornecem. 
  
|**Nome**|**Manipuladores de eventos**|**Descrição**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário, ao status de retorno e a outras propriedades que contêm informações sobre o nó XML durante uma alteração do DOM (Modelo de Objeto de Documento) XML. Também inclui um método para a criação de um erro.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário, ao status de retorno e ao nó XML de origem durante um clique de botão na área de formulário.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Retorna informações sobre o nó DOM (Modelo de Objeto de Documento) XML que é o contexto atual do documento XML subjacente do formulário.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário durante uma operação de mesclagem de formulário ou modo de exibição de opção.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário e ao status de retorno durante o carregamento ou envio de um formulário.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Retorna propriedades e métodos que podem ser usados durante um evento **OnMergeRequest** para interagir programaticamente com o documento XML subjacente de um formulário e para determinar propriedades de mesclagem, como o número de arquivos que estão sendo mesclados.  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Retorna um número de propriedades e métodos que podem ser usados durante uma operação de salvar do manipulador de eventos **OnSaveRequest** para interagir programaticamente com o documento XML subjacente de um formulário, determinar as propriedades de salvar e executar a operação de salvar.  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Usado para adicionar dados adicionais à assinatura digital.  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário, ao status de retorno e aos números de versão do documento e da solução durante a operação de atualização da versão.  <br/> |
   
## <a name="using-the-event-objects"></a>Usando os objetos Event

Quando você cria um manipulador de eventos, o InfoPath cria a declaração do manipulador de eventos no arquivo de código de formulário do projeto (FormCode.cs ou FormCode.vb). Na declaração do manipulador de eventos, o InfoPath usa **e** como o nome do parâmetro que é passado para o manipulador de eventos. Esse parâmetro contém o objeto de evento associado ao manipulador de eventos. 
  
Por exemplo, quando você cria um manipulador de eventos para o evento **OnLoad** no modo de design (clicando no evento **On Load** na guia Desenvolvedor), o InfoPath adiciona a declaração para o manipulador de eventos que recebe o objeto **DocReturnEvent** ao arquivo de código do formulário e abre o Editor de Código para que você possa adicionar seu código à seguinte declaração de manipulador de eventos.  
  
```cs
// The following function handler is created by Microsoft Office 
// InfoPath. Do not modify the type or number of arguments.
[InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
public void FormEvents_OnLoad(DocReturnEvent e)
{
   // Write your code here.
}
```

```vb
' The following function handler is created by Microsoft Office 
' InfoPath. Do not modify the type or number of arguments.
<InfoPathEventHandler(EventType:=InfoPathEventType.OnLoad)> _
Public Sub FormEvents_OnLoad(ByVal e As DocReturnEvent)
   ' Write your code here.
End Sub
```

Ao escrever código para um manipulador de eventos, você pode usar as propriedades e os métodos implementados pelo objeto de evento que é passado pelo **parâmetro e.** Por exemplo, no manipulador de eventos **OnBeforeChange** a seguir, a propriedade [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) do objeto de evento **DataDOMEvent** é usada para verificar o valor do campo que acabou de ser alterado. Se estiver em branco, a propriedade [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) do objeto de evento **DataDOMEvent** será usada para exibir um erro para o usuário em uma caixa de diálogo e a propriedade [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) será definida como **false,** indicando que as alterações feitas pelo usuário não devem ser aceitas.
  
```cs
[InfoPathEventHandler(MatchPath="/my:myFields/my:field1", 
    EventType=InfoPathEventType.OnBeforeChange)]
public void field1_OnBeforeChange(DataDOMEvent e)
{
   // Determine whether there is a new value.
   if ((string)e.NewValue == "")
   {
      // The value is blank, so display an error message and roll
      // back the changes.
      e.ReturnMessage = "You must supply a value for this field.";
      e.ReturnStatus = false;
      return;
   }
}
```

```vb
<InfoPathEventHandler(MatchPath:="/my:myFields/my:field1", _ EventType:=InfoPathEventType.OnBeforeChange)> _
Public Sub field1_OnBeforeChange(ByVal e As DataDOMEvent)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message and roll back
      ' the changes.
      e.ReturnMessage = "You must supply a value for this field."
      e.ReturnStatus = False
      Return
   End If
End Sub
```

> [!NOTE]
> Cada um dos objetos de evento do InfoPath no modelo de objeto compatível com o InfoPath 2003 implementa diferentes propriedades e métodos. Para obter mais informações sobre um objeto de evento específico, clique no objeto apropriado na tabela Objetos de Evento mostrada anteriormente. 
  

