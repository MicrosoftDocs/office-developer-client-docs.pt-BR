---
title: Lidar com erros
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- erros [infopath 2007], manipulação, FormErrorCollection [InfoPath 2007], o InfoPath 2007, tratamento de erros FormError [InfoPath 2007], [InfoPath 2007] de tratamento de erros
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Ao criar aplicativos personalizados, os desenvolvedores devem frequentemente executar tratamento de erros que envolve escrever códigos de programação para verificar erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto do InfoPath fornecido pelo Microsoft.Office.InfoPath namespace suporta a manipulação de erros devido ao uso a classe FormError em associação com a classe FormErrorCollection.
ms.openlocfilehash: 3bfad103c31d0b5364d1c75acfbb2f590f7658bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765624"
---
# <a name="handle-errors"></a>Lidar com erros

Ao criar aplicativos personalizados, os desenvolvedores devem frequentemente executar tratamento de erros que envolve escrever códigos de programação para verificar erros gerados pelo aplicativo ou para criar e gerar erros personalizados. O modelo de objeto do InfoPath fornecido pelo [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace suporta a manipulação de erros devido ao uso a classe [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) em associação com a classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
  
No InfoPath, os erros podem ocorrer pelos seguintes motivos:
  
- Quando os dados inseridos em um formulário não validação de esquema XML.
    
- Quando uma restrição de validação personalizada falha.
    
- Quando um erro é gerado pelo método do objeto event [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) . 
    
- Quando um erro definido pelo usuário é criado usando o método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) da classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Visão geral da classe FormErrorCollection

A classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para gerenciar os objetos [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) contido na coleção. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) (sobrecargas + 3)  <br/> |Cria um objeto **FormError** e o adiciona à coleção.  <br/> |
|Método [Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) (sobrecarga + 1)  <br/> |Exclui o erro de definidas pelo usuário especificado da coleção.  <br/> |
|Método [DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx)  <br/> |Exclui todos os objetos **FormError** contidos na coleção.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (sobrecarga + 1)  <br/> |Retorna todos os objetos **FormError** do tipo ou nome especificado da coleção.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)  <br/> |Obtém uma contagem do número de objetos **FormError** contido na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)  <br/> |Obtém uma referência a um objeto **FormError** com base no número de índice especificado.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Visão geral da classe FormError

A classe [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) fornece as seguintes propriedades, os desenvolvedores de formulário podem usar para acessar informações sobre o erro que foi gerado. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx)  <br/> |Obtém ou define a mensagem de erro detalhadas do objeto **FormError** .  <br/> |
|Propriedade [ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx)  <br/> |Obtém ou define o código de erro do objeto **FormError** .  <br/> |
|Propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Obtém um objeto **XPathNavigator** que está posicionado no nó associado ao objeto **FormError** .  <br/> |
|Propriedade [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx)  <br/> |Obtém ou define a mensagem de erro curta do objeto **FormError** .  <br/> |
|Propriedade [FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx)  <br/> |Obtém o tipo do objeto **FormError** .  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Usando as Classes de FormError e o FormErrorCollection

O objeto de **FormErrorCollection** associado a um formulário é acessado por meio da propriedade [erros](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) do objeto [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . O objeto **FormErrorCollection** é associado ao documento XML subjacente de um formulário, para que quando ocorre um erro, ele e quaisquer erros adicionais podem ser acessados e gerenciados dentro do documento XML atual. O exemplo a seguir demonstra como um loop pode ser usado para verificar os erros que podem existir no documento XML subjacente de um formulário. Se houver erros, a função faz um loop por cada um deles e, usando a propriedade de **mensagem** do objeto **FormError** , exibe uma caixa de mensagem para o usuário. 
  
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

A função anterior poderia ser chamada de um dos manipuladores de eventos de validação de dados do formulário. Por exemplo, quando usada no evento manipulador para o evento [alterado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) de um campo no formulário, a chamada para a função seria passar o argumento do nó XML usando a propriedade de [sites](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) do objeto event [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) da seguinte maneira. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Além de tratamento de erros gerados pelo InfoPath, os desenvolvedores de formulário também podem o gerar erros personalizados usando o método [ReportError (XPathNavigator, Boolean, cadeia de caracteres)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) do objeto event [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) , ou usando o [Adicionar ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)método da classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . Para obter informações sobre como usar os métodos [ReportError (XPathNavigator, booleano, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) ou [Adicionar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) , clique nos links para os métodos no início deste tópico. 
  
## <a name="handling-managed-code-exceptions"></a>Tratamento de exceções de código gerenciado

Você pode usar o tratamento de exceção de try-catch para manipular exceções geradas no modelo de formulário de código gerenciado, conforme mostrado no exemplo de código a seguir.
  
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

Se você não usar try-catch de tratamento de exceção no seu código de formulário, o InfoPath exibirá informações sobre exceções não tratadas na caixa de diálogo de erro do InfoPath durante a depuração e visualização. Além disso, por padrão, exceções não tratadas não são exibidas na caixa de diálogo de erro do InfoPath em tempo de execução quando você implanta o seu modelo de formulário de código gerenciado. Para exibir informações sobre exceções não tratadas em tempo de execução, use o procedimento a seguir.
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Ativar notificações para exceções não tratadas de código gerenciado em tempo de execução

1. Abra o InfoPath designer e, em seguida, clique na guia **arquivo** . 
    
2. Clique em **Opções**e clique em **Opções do InfoPath** em categoria **Geral** . 
    
3. Na guia **Avançado** , marque a caixa de seleção **Mostrar uma notificação para erros de código do Visual Basic e c#** . 
    

