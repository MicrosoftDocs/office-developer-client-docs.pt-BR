---
title: Responder eventos de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], respondendo aos eventos, modelos de formulário compatíveis com o InfoPath 2003, respondendo aos eventos do formulário
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Você pode escrever código para responder a diversos eventos que podem ocorrer como um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, você pode criar manipuladores de eventos no InfoPath designer.
ms.openlocfilehash: dff7b4f1657b7d1450d8b345521a747c0594462b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765614"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Responder eventos de formulário usando o modelo de objeto do InfoPath 2003

Você pode escrever código para responder a diversos eventos que podem ocorrer como um usuário preenche um formulário. Para trabalhar com eventos no InfoPath, você pode criar manipuladores de eventos no InfoPath designer.
  
Manipuladores de eventos do InfoPath devem ser criados no InfoPath designer porque, quando usando o modelo de objeto do InfoPath 2003 compatíveis, InfoPath automaticamente adiciona a declaração correta e aplica um atributo ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) em um arquivo de código do formulário (FormCode.cs ou FormCode.vb) para identificar e PIA o manipulador de eventos. Depois de criar um manipulador de eventos, você não deve alterar sua declaração e o atributo no arquivo de código do formulário. 
  
Para obter informações sobre como criar os manipuladores de eventos do InfoPath, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="overview-of-the-event-objects"></a>Visão geral dos objetos de evento

O modelo de objeto compatível com o InfoPath 2003 implementa nove objetos de eventos que são expostos no namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . A tabela a seguir lista cada um dos objetos de evento do InfoPath, os manipuladores de eventos no que qual estão associadas e uma descrição da funcionalidade de que eles oferecem. 
  
|**Name**|**Manipuladores de eventos**|**Descrição**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário, o status de retorno e outras propriedades que contêm informações sobre o nó XML durante uma alteração de modelo de objeto de documento (DOM) XML. Também inclui um método para geração de um erro.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário, o status de retorno e o nó XML de origem durante o clique de um botão na área do formulário.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Retorna informações sobre o nó XML DOM Document Object Model () que é o contexto atual do documento XML de base do formulário.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário durante uma operação de mesclagem de exibição ou formulário de comutador.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário e o status de retorno durante o carregamento ou envio de um formulário.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Retorna propriedades e métodos que podem ser usados durante um evento **OnMergeRequest** com programaticamente interagem com o documento XML subjacente de um formulário e determinar propriedades de mesclagem, como o número de arquivos que estão sendo mesclados.  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Retorna um número de propriedades e métodos que podem ser usados durante uma operação Salvar operação do manipulador de eventos **OnSaveRequest** programaticamente interagir com o documento XML subjacente de um formulário, determine salvar propriedades e executar Salvar operação.  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Usado para adicionar dados adicionais às assinaturas digitais.  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Retorna uma referência ao documento XML subjacente de um formulário, o status de retorno e os números de versão do documento e da solução durante a operação de atualização de versão.  <br/> |
   
## <a name="using-the-event-objects"></a>Usando os objetos de evento

Quando você cria um manipulador de eventos, o InfoPath cria a declaração do manipulador de eventos no arquivo de código de formulário do projeto (FormCode.cs ou FormCode.vb). Na declaração do manipulador de eventos, o InfoPath usa **e** como o nome do parâmetro que é passado ao manipulador de eventos. Este parâmetro contém o objeto event que está associado com o manipulador de eventos. 
  
Por exemplo, quando você cria um manipulador de eventos para o evento **OnLoad** no modo de design (clicando **Em evento OnLoad** na guia **desenvolvedor** ), o InfoPath adiciona a declaração para o manipulador de eventos que recebe o objeto **DocReturnEvent** para o formulário de código arquivo e, em seguida, abre o Editor de código para que você possa adicionar seu código para a seguinte declaração do manipulador de eventos. 
  
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

Ao escrever código para um manipulador de eventos, você pode usar as propriedades e métodos implementados pelo objeto event que é passado por meio do parâmetro **f** . Por exemplo, no manipulador de eventos **OnBeforeChange** seguir, a propriedade [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) do objeto event **DataDOMEvent** é usada para verificar o valor do campo que acabou de ser alterado. Se ele estiver em branco, a propriedade [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) do objeto event **DataDOMEvent** é usada para exibir um erro para o usuário em uma caixa de diálogo e a propriedade [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) é definida como **false**, indicando que as alterações feitas pelo usuário devem não aceito.
  
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
> Cada um dos objetos de evento do InfoPath no modelo de objeto compatível com o InfoPath 2003 implementa métodos e propriedades diferentes. Para obter mais informações sobre um objeto de evento específico, clique no objeto apropriado na tabela de objetos de evento mostrado anteriormente. 
  

