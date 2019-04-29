---
title: Manipular erros
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- erros [InfoPath 2007], lidando, FormErrorCollection [InfoPath 2007], InfoPath 2007, tratamento de erros, FormError [InfoPath 2007], tratamento de erros [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Ao criar aplicativos personalizados, os desenvolvedores geralmente devem realizar o tratamento de erros que envolve a gravação do código de programação para verificar se há erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto do InfoPath fornecido pelo namespace Microsoft. Office. InfoPath oferece suporte ao tratamento de erros por meio do uso da classe FormError em associação com a classe FormErrorCollection.
ms.openlocfilehash: 30cf649188b7e4cbc35469d2a50540bb13ecb38d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410774"
---
# <a name="handle-errors"></a>Manipular erros

Ao criar aplicativos personalizados, os desenvolvedores geralmente devem realizar o tratamento de erros que envolve a gravação do código de programação para verificar se há erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto do InfoPath fornecido pelo namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) oferece suporte ao tratamento de erros por meio do uso da classe [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) em associação com a classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
  
No InfoPath, os erros podem ocorrer pelos seguintes motivos:
  
- Quando os dados inseridos em um formulário falham na validação de esquema XML.
    
- Quando uma restrição de validação personalizada falha.
    
- Quando um erro é gerado pelo método [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) do objeto de [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) evento xmlvalidation. 
    
- Quando um erro definido pelo usuário é criado usando o método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) da classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Visão geral da classe FormErrorCollection

A classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para gerenciar os objetos [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) que o conjunto contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) (+ 3 sobrecargas)  <br/> |Cria um objeto **FormError** e o adiciona à coleção.  <br/> |
|Método [delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) (+ 1 sobrecarga)  <br/> |Exclui o erro definido pelo usuário especificado da coleção.  <br/> |
|Método [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx)  <br/> |Exclui todos os objetos **FormError** contidos na coleção.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) GetErrors (sobrecarga + 1)  <br/> |Retorna todos os objetos **FormError** do nome ou tipo especificado da coleção.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)  <br/> |Obtém uma contagem do número de objetos **FormError** contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)  <br/> |Obtém uma referência a um objeto **FormError** com base no número de índice especificado.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Visão geral da classe FormError

A classe [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) fornece as seguintes propriedades, que os desenvolvedores de formulários podem usar para acessar informações sobre o erro que foi gerado. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx)  <br/> |Obtém ou define a mensagem de erro detalhada do objeto **FormError** .  <br/> |
|Propriedade [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx)  <br/> |Obtém ou define o código de erro do objeto **FormError** .  <br/> |
|Propriedade [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Obtém um objeto **XPathNavigator** posicionado no nó associado ao objeto **FormError** .  <br/> |
|Propriedade [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx)  <br/> |Obtém ou define a mensagem de erro curta do objeto **FormError** .  <br/> |
|Propriedade [FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx)  <br/> |Obtém o tipo do objeto **FormError** .  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Usando as classes FormErrorCollection e FormError

O objeto **FormErrorCollection** associado a um formulário é acessado através da propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) do objeto XmlForm. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) O objeto **FormErrorCollection** está associado ao documento XML subjacente de um formulário para que, quando ocorrer um erro, ele e quaisquer erros adicionais possam ser acessados e gerenciados no documento XML atual. O exemplo a seguir demonstra como um loop pode ser usado para verificar os erros que podem existir no documento XML subjacente de um formulário. Se houver erros, a função entrará em loop por meio de cada um deles e, usando a propriedade **Message** do objeto **FormError** , exibirá uma caixa de mensagem para o usuário. 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

A função precedente pode ser chamada de um dos manipuladores de eventos de validação de dados do formulário. Por exemplo, quando usado no manipulador de eventos para o evento [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) de um campo no formulário, a chamada para a função passa o argumento de nó XML usando a propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) do objeto de [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) evento xmleventargs da seguinte maneira. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Além de lidar com erros gerados pelo InfoPath, os desenvolvedores de formulários também podem gerar erros personalizados usando o método [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) do [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) objeto de evento xmlvalidation ou usando a [adição ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)método da classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . Para obter informações sobre como usar o [ReportError (XPathNavigator, Boolean, Cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) ou [Adicionar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) métodos, clique nos links para esses métodos no início deste tópico. 
  
## <a name="handling-managed-code-exceptions"></a>Tratamento de exceções de código gerenciado

Você pode usar a manipulação de exceção de try-catch para lidar com exceções geradas no modelo de formulário de código gerenciado, conforme mostrado no exemplo de código a seguir.
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

Se você não usar a manipulação de exceção de tentativa-catch no seu código de formulário, o InfoPath exibirá informações sobre exceções não tratadas na caixa de diálogo de erro do InfoPath durante a depuração e a visualização. Além disso, por padrão, as exceções não manipuladas não são exibidas na caixa de diálogo de erro do InfoPath em tempo de execução quando você implanta seu modelo de formulário de código gerenciado. Para exibir informações sobre exceções não tratadas no tempo de execução, use o procedimento a seguir.
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Habilitar notificações para exceções de código gerenciado não manipuladas no tempo de execução

1. Abra o designer do InfoPath e, em seguida, clique na guia **arquivo** . 
    
2. Clique em **Opções**e, em seguida, clique em **Opções do InfoPath** na categoria **geral** . 
    
3. Na guia **avançado** , marque a caixa de seleção **mostrar uma notificação para erros de código do Visual Basic e C#** . 
    

